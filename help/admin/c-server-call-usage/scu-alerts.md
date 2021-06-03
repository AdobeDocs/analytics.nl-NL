---
description: Voeg of beheer server alle gebruiksalarm toe. Wanneer u opstelling een alarm, het op alle rapportsuites in alle login bedrijven van een het facturerings bedrijf van toepassing is.
title: Gebruikswaarschuwingen voor serveroproep
uuid: 701fd542-5b24-42df-97a0-08e10929fa48
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 2%

---


# Gebruikswaarschuwingen voor serveroproep

Wanneer u opstelling een alarm, het op alle rapportsuites in alle login bedrijven van een het facturerings bedrijf van toepassing is.

## Overzicht

Een nieuwe waarschuwingscategorie met de naam **[!UICONTROL Server Calls Usage Alert]** maakt deel uit van de bestaande [Waarschuwingsbeheer](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/virtual-analyst/intelligent-alerts/intellligent-alerts.html)-gebruikersinterface.

Het is vooraf bevolkt met **1 standaardalarm** die binnen om het even welk login bedrijf verschijnt die toegang tot de eigenschap van het Gebruik van de Vraag van de Server heeft. Dit alarm brengt een bericht teweeg dat aan alle beheerders van het login bedrijf wordt gericht als één van de volgende criteria wordt voldaan:

* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;100% voor om het even welk server-vraagtype is u gerechtigd aan, OF
* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;90% voor om het even welk server-vraagtype is u gerechtigd aan, OF
* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;75% voor om het even welk server-vraagtype is u gerechtigd aan, EN de &quot;bestede periode van het Gebruik&quot;is onder of evenaart&quot;75% van de periode van het Gebruik.

![](assets/alerts.png)

U kunt tot het gebruiksalarm van de servervraag op twee manieren toegang hebben:

* Klik op **[!UICONTROL Manage Alerts]** in de rechterbovenhoek op het tabblad Huidig gebruik of het tabblad Gebruik van de rapportsuite, of
* Navigeer naar **[!UICONTROL Components]** > **[!UICONTROL Alerts]** in Adobe Analytics.

## Waarschuwingen voor serveroproepgebruik maken {#section_2A2882C6D48D47C1944D52FB7C766BEC}

Als u aanvullende waarschuwingen wilt maken,

1. Klik op **[!UICONTROL + Add]** en selecteer **[!UICONTROL Server Call Usage Alert]**.

   ![](assets/server_call_alert.png)

1. Definieer de waarschuwing.

   ![](assets/sc_alert.png)

   * **Titel**: Geef een beschrijvende naam op. U kunt de waarschuwing niet opslaan zonder een naam.
   * **Tijdgranulariteit**: Verwijst naar hoe vaak de alarm zal worden gecontroleerd. *We steunen op dit moment slechts wekengranulariteit.* Dit betekent dat de waarschuwing wekelijks wordt gecontroleerd en zal terugkijken naar de gegevens van de huidige gebruiksperiode.
   * **Ontvangers**: Geef iedereen in de organisatie op die een e-mailbericht moet ontvangen wanneer de waarschuwing de opgegeven drempelwaarde activeert.
   * **Vervaldatum**: De vervaldatum is standaard één jaar vanaf de aanmaakdatum van de waarschuwing.
   * **Een waarschuwing verzenden wanneer**:

      * Een van deze maateenheden activeert
Voeg het type van servervraag/s als metrisch toe en specificeer de waakzame drempel door de bepaling en de drempel te selecteren:
         * boven of gelijk aan
         * lager is dan of gelijk is
      * Met
Geef de drempel en voorwaarde voor de verbruiksperiode op (boven of gelijk aan of onder of gelijk aan).

1. Klik op **[!UICONTROL Save]**.

## Gebruikswaarschuwingen voor serveraanroepen beheren {#section_8FF98170763C4B5CBEC6DD43F893177A}

![](assets/alert_mgmt.png)

Waarschuwingen beheren:

1. Schakel het selectievakje naast een of meer waarschuwingen in. De acties van het waakzame beheer tonen bij de bovenkant.
1. Voer een of meer van de volgende handelingen uit:

   | Handeling | Definitie |
   |--- |--- |
   | + Toevoegen | Open [Alert Builder](/help/admin/c-server-call-usage/scu-alerts.md) door op [!UICONTROL + Add] te klikken. |
   | Tag | Label waarschuwingen om deze voor gebruiksgemak in te delen. |
   | Verwijderen | U kunt alle waarschuwingen verwijderen, behalve standaardwaarschuwingen. |
   | Naam wijzigen | U kunt de naam van alle waarschuwingen wijzigen, behalve standaardwaarschuwingen. |
   | Goedkeuren | Waarschuwingen goedkeuren om ze &quot;officieel&quot; te maken. |
   | In-/uitschakelen | U kunt alle waarschuwingen in- of uitschakelen, ook de standaardwaarschuwingen. |
   | Vernieuwen | Wanneer een of meer waarschuwingen zijn geselecteerd, kunnen deze worden vernieuwd. Hiermee worden de vervaldatums van de clips uitgebreid tot één jaar vanaf de dag waarop [!UICONTROL Renew] is aangeklikt, ongeacht de oorspronkelijke vervaldatum. |
   | Exporteren naar CSV | Zie [Rapport van het Gebruik van de download](/help/admin/c-server-call-usage/report-suite-usage.md) |

