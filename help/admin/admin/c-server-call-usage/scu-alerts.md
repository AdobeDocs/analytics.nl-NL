---
description: Voeg of beheer server alle gebruiksalarm toe. Wanneer u opstelling een alarm, het op alle rapportsuites in alle login bedrijven van een het facturerings bedrijf van toepassing is.
title: Gebruikswaarschuwingen voor serveroproep
feature: Server Call Usage
exl-id: 35926566-c570-4ed2-9bbc-0906518bcf64
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%

---

# Gebruikswaarschuwingen voor serveroproep

Wanneer u opstelling een alarm, het op alle rapportsuites in alle login bedrijven van een het facturerings bedrijf van toepassing is.

## Overzicht

Een nieuwe waarschuwingscategorie genaamd **[!UICONTROL Server Calls Usage Alert]** maakt deel uit van de bestaande [Waarschuwingsbeheer](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html) gebruikersinterface.

Het is vooraf gevuld met **1 standaardwaarschuwing** dat binnen om het even welk login bedrijf verschijnt dat toegang tot de eigenschap van het Gebruik van de Vraag van de Server heeft. Dit alarm brengt een bericht teweeg dat aan alle beheerders van het login bedrijf wordt gericht als één van de volgende criteria wordt voldaan:

* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;100% voor om het even welk server-vraagtype is u gerechtigd aan, OF
* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;90% voor om het even welk server-vraagtype is u gerechtigd aan, OF
* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;75% voor om het even welk server-vraagtype is u gerechtigd aan, EN de &quot;bestede periode van het Gebruik&quot;is onder of evenaart&quot;75% van de periode van het Gebruik.

![](/help/admin/admin/c-server-call-usage/assets/alerts.png)

U kunt tot het gebruiksalarm van de servervraag op twee manieren toegang hebben:

* Klikken **[!UICONTROL Manage Alerts]** in de rechterbovenhoek op het tabblad Huidig gebruik of het tabblad Gebruik van de rapportsuite, of
* Navigeren naar **[!UICONTROL Components]** > **[!UICONTROL Alerts]** in Adobe Analytics.

## Waarschuwingen voor serveroproepgebruik maken {#section_2A2882C6D48D47C1944D52FB7C766BEC}

Als u aanvullende waarschuwingen wilt maken,

1. Klik op **[!UICONTROL + Add]** en selecteer **[!UICONTROL Server Call Usage Alert]**.

   ![](/help/admin/admin/c-server-call-usage/assets/server_call_alert.png)

1. Definieer de waarschuwing.

   ![](/help/admin/admin/c-server-call-usage/assets/sc_alert.png)

   * **Titel**: Geef een beschrijvende naam op. U kunt de waarschuwing niet opslaan zonder een naam.
   * **Tijdgranulatie**: Verwijst naar hoe vaak de alarm zal worden gecontroleerd. *We steunen op dit moment slechts wekengranulariteit.* Dit betekent dat de waarschuwing wekelijks wordt gecontroleerd en zal terugkijken naar de gegevens van de huidige gebruiksperiode.
   * **Ontvangers**: Geef iedereen in de organisatie op die een e-mailbericht moet ontvangen wanneer de waarschuwing de opgegeven drempelwaarde activeert.
   * **Vervaldatum**: De vervaldatum is standaard één jaar vanaf de aanmaakdatum van de waarschuwing.
   * **Een waarschuwing verzenden wanneer**:

      * Een van deze metrieke trigger voegt het type serveraanroep/s als metrisch toe en geeft de waarschuwingsdrempel op door de modifier en de drempel te selecteren:
         * boven of gelijk aan
         * lager is dan of gelijk is
      * Met Opgeven geeft u de drempel en voorwaarde op (boven of gelijk aan of onder of gelijk aan) voor de verbruiksperiode die wordt besteed.

1. Klik op **[!UICONTROL Save]**.

## Gebruikswaarschuwingen voor serveraanroepen beheren {#section_8FF98170763C4B5CBEC6DD43F893177A}

![](/help/admin/admin/c-server-call-usage/assets/alert_mgmt.png)

Waarschuwingen beheren:

1. Schakel het selectievakje naast een of meer waarschuwingen in. De acties van het waakzame beheer tonen bij de bovenkant.
1. Voer een of meer van de volgende handelingen uit:

   | Handeling | Definitie |
   |--- |--- |
   | + Toevoegen | Toegang krijgen tot [Alert Builder](/help/admin/admin/c-server-call-usage/scu-alerts.md) door te klikken  [!UICONTROL + Add]. |
   | Tag | Label waarschuwingen om deze voor gebruiksgemak in te delen. |
   | Verwijderen | U kunt alle waarschuwingen verwijderen, behalve standaardwaarschuwingen. |
   | Naam wijzigen | U kunt de naam van alle waarschuwingen wijzigen, behalve standaardwaarschuwingen. |
   | Goedkeuren | Waarschuwingen goedkeuren om ze &quot;officieel&quot; te maken. |
   | In-/uitschakelen | U kunt alle waarschuwingen in- of uitschakelen, ook de standaardwaarschuwingen. |
   | Vernieuwen | Wanneer een of meer waarschuwingen zijn geselecteerd, kunnen deze worden vernieuwd. De vervaldatums worden verlengd tot één jaar vanaf de dag [!UICONTROL Renew] is aangeklikt, ongeacht de oorspronkelijke vervaldatum. |
   | Exporteren naar CSV | Zie [Gebruiksrapport downloaden](/help/admin/admin/c-server-call-usage/report-suite-usage.md) |
