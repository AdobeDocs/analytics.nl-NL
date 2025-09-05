---
description: Leer hoe totalen in vrije-vormlijsten in Analysis Workspace worden berekend.
title: Totalen
feature: Freeform Tables
role: User, Admin
exl-id: 883c3e44-4139-46a1-a261-e11841312465
source-git-commit: 665319bdfc4c1599292c2e7aea45622d77a291a7
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 1%

---

# Totalen {#workspace-totals}

>[!CONTEXTUALHELP]
>id="workspace_freeformtable_grandtotal"
>title="Eindtotaal"
>abstract="Groot totaal wordt niet ondersteund voor tabellen of uitsplitsingen met statische rijen."

In Freeform-tabellen wordt op elk uitsplitsingsniveau een totale rij weergegeven met twee totalen:

![ vrije lijst die van de Vrije Vorm het grote totaal en het lijsttotaal benadrukt.](assets/total-row.png)

* **[!UICONTROL Table total]** ➊ - Dit totaal is doorgaans gelijk aan of een subset van de [!UICONTROL Grand total] . Het totaal bevat alle tabelfilters die in de vrije-vormtabel zijn toegepast, inclusief de optie [!UICONTROL Include None] .
* **[!UICONTROL Grand total]** (**[!UICONTROL out of]** *aantal*) ➋ - Dit totaal vertegenwoordigt alle gebeurtenissen die zijn verzameld. Wanneer een filter op paneelniveau of binnen de vrije vormlijst wordt toegepast, past dit totaal aan om op alle gebeurtenissen te wijzen die aan de filtercriteria voldoen.




## Totalen weergeven

Onder ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Column settings]**, zijn er opties aan **[!UICONTROL Show totals]** en **[!UICONTROL Show grand total]**. Als deze instellingen niet zijn ingeschakeld, worden de totalen uit de tabel verwijderd. Dit is mogelijk het geval als totalen onzinnig zijn.


In een vrije vormlijst die [ statische rijen ](/help/analyze/analysis-workspace/visualizations/freeform-table/column-row-settings/manual-vs-dynamic-rows.md) bevat, gedragen de totalen zich verschillend. En wordt gecontroleerd gebruikend ![ Plaatsend ](/help/assets/icons/Setting.svg) **[!UICONTROL Row Settings]**.

| Optie | Beschrijving |
|---|---|
| **[!UICONTROL Show sum of current rows as the total]** | Een som van de rijen in de tabel aan de clientzijde weergeven. Dit totaal **** dedupliceert metriek zoals zittingen of personen niet. |
| **[!UICONTROL Show grand total]** | Een som aan de serverzijde weergeven. Dit totaal dedupliceert metriek zoals sessies of personen. |

Zie [ Dynamische versus statische afmetingspunten in vrije vormlijsten ](column-row-settings/manual-vs-dynamic-rows.md).


## Veelgestelde vragen

| Vragen | Antwoord |
|---|---|
| Welk *totaal* zijn de grijze kolompercentages die op worden gebaseerd? | Dit *totaal* hangt van **[!UICONTROL Percentages]** het plaatsen selectie onder **[!UICONTROL Row Settings]** af:<ul><li>Percentage berekenen op kolom - Dit is de standaardinstelling. De percentages zijn gebaseerd op het totaal van de Lijst.</li><li>Percentage berekenen op rij - Percentages worden gebaseerd op het Eindtotaal.</li></ul> |
| Hoe beïnvloedt de instelling van **[!UICONTROL Include Unspecified (None)]** de totalen? | Als omvat niet gespecificeerd (niets) het plaatsen wordt ongecontroleerd, zal Geen/Niet gespecificeerde rij worden verwijderd uit de lijst, het Totaal van de Lijst, en zal door aan om het even welke berekende metriek gaan die [ &quot;Totaal&quot;metrische types ](/help/components/calculated-metrics/workflow/c-build-metrics/m-metric-type-alloc.md) gebruiken. |
| Wanneer de filters van de douanetabel op een vrije vormlijst worden toegepast, doe al mijn berekende metriek en voorwaardelijke het formatteren rekening voor de filter? | Momenteel niet. **[!UICONTROL Include Ubnspeficied (None)]** is een account, maar aangepaste tabelfilters hebben geen invloed op het volgende:<ul><li>Het maximale/minimale bereik van de kolom dat bij voorwaardelijke opmaak wordt gebruikt, loopt over alle gegevens.</li><li>Berekende waarden die gebruikmaken van **[!UICONTROL Grand total]** -metrische typen.</li><li>Berekende metriek met functies die over rijen in een vrije vormlijst berekenen: Kolomsom, Kolommaximum, Kolom min, Aantal, Gemiddelde, Mediaan, Percentage, Kwartaal, Aantal rijen, Standaardafwijking, Variantie, Cumulatief, Cumulatief Gemiddelde, Regressievarianten, T-Score, T-Test, Z-Score en Z-Test.</li></ul> |
| Wat weerspiegelt het metrische type **[!UICONTROL Grand total]** in Berekende metriek? | **[!UICONTROL Grand total]** blijft naar **[!UICONTROL Grand total]** verwijzen en geeft geen filters weer die op een tabel of de **[!UICONTROL Table total]** zijn toegepast. |
| Welk totaal wordt getoond wanneer de gegevens of van een vrije vormlijst worden gekopieerd en worden gekleefd of via CSV worden gedownload? | De totale rij geeft alleen **[!UICONTROL Table total]** weer en neemt de instelling voor de kolom **[!UICONTROL Show totals]** in acht. |
