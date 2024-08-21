---
description: Voeg of beheer server alle gebruiksalarm toe. Wanneer u opstelling een alarm, het op alle rapportsuites in alle login bedrijven van een het facturerings bedrijf van toepassing is.
title: Gebruikswaarschuwingen voor serveroproep
feature: Server Call Usage
exl-id: 35926566-c570-4ed2-9bbc-0906518bcf64
role: Admin
source-git-commit: 373a1ecffafdcefe3c7b60954f14c2f3a5ca386d
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 1%

---

# Gebruikswaarschuwingen voor serveroproepen

Wanneer u opstelling een alarm, het op alle rapportsuites in alle login bedrijven van een het facturerings bedrijf van toepassing is.

De Alarm van het Gebruik van de Vraag van de server maakt deel uit van het [ Alarm ](/help/components/c-alerts/alert-manager.md) gebruikersinterface.

Het is pre-bevolkt met **1 standaardalarm** dat binnen om het even welk login bedrijf verschijnt dat toegang tot de eigenschap van het Gebruik van de Vraag van de Server heeft. Dit alarm brengt een bericht teweeg dat aan alle beheerders van het login bedrijf wordt gericht als één van de volgende criteria wordt voldaan:

* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;100% voor om het even welk server-vraagtype is u gerechtigd aan, OF
* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;90% voor om het even welk server-vraagtype is u gerechtigd aan, OF
* &quot;Om het even welk&quot;gebruik van de servervraag dat &quot;boven of gelijk aan&quot;75% voor om het even welk server-vraagtype is u gerechtigd aan, EN de &quot;bestede periode van het Gebruik&quot;is onder of evenaart&quot;75% van de periode van het Gebruik.

![](/help/admin/admin/c-server-call-usage/assets/alerts.png)

U kunt tot het gebruiksalarm van de servervraag op twee manieren toegang hebben:

* Klik op **[!UICONTROL Manage Alerts]** in de rechterbovenhoek op het tabblad Huidig gebruik of het tabblad Gebruik van de rapportsuite, of
* Navigeer naar **[!UICONTROL Components]** > **[!UICONTROL Alerts]** in Adobe Analytics.

## Gebruikswaarschuwingen voor serveroproepen maken {#create}

Als u aanvullende waarschuwingen wilt maken,

1. Klik op **[!UICONTROL + Add]** en selecteer **[!UICONTROL Server Call Usage Alert]** .

   ![](/help/admin/admin/c-server-call-usage/assets/server_call_alert.png)

1. Definieer de waarschuwing.

   ![](/help/admin/admin/c-server-call-usage/assets/sc_alert.png)

   * **Titel**: Specificeer een beschrijvende naam. U kunt de waarschuwing niet opslaan zonder een naam.
   * **Korreligheid van de Tijd**: Verwijs naar hoe vaak het alarm zal worden gecontroleerd. *wij steunen slechts Wekelijkse granulariteit op dit ogenblik.* Dit betekent dat de waarschuwing wekelijks wordt gecontroleerd en zal terugkijken naar de gegevens van de huidige gebruiksperiode.
   * **Ontvangers**: Specificeer iedereen op de organisatie die een e-mail zou moeten krijgen wanneer het alarm de gespecificeerde drempel teweegbrengt.
   * **Datum van de Vervalsing**: Door gebrek, is de vervaldatum één jaar van de waakzame aanmaakdatum.
   * **verzend een alarm wanneer**:

      * Een van deze statistieken-trigger
Voeg het type van servervraag/s als metrisch toe en specificeer de waakzame drempel door de bepaling en de drempel te selecteren:
         * is boven of gelijk aan
         * is lager of gelijk aan
      * Met
Geef de drempel en voorwaarde voor de verbruiksperiode op (boven of gelijk aan of onder of gelijk aan).

1. Klik op **[!UICONTROL Save]**.

## Gebruikswaarschuwingen voor serveraanroepen beheren {#manage}

![](/help/admin/admin/c-server-call-usage/assets/alert_mgmt.png)

Waarschuwingen beheren:

1. Schakel het selectievakje naast een of meer waarschuwingen in. De acties van het waakzame beheer tonen bij de bovenkant.
1. Voer een of meer van de volgende handelingen uit:

   | Handeling | Definitie |
   |--- |--- |
   | + Toevoegen | Heb toegang tot [ Waakzame Bouwer ](/help/admin/admin/c-server-call-usage/scu-alerts.md) door [!UICONTROL + Add] te klikken. |
   | Tag | Label waarschuwingen om deze voor gebruiksgemak in te delen. |
   | Verwijderen | U kunt alle waarschuwingen verwijderen, behalve standaardwaarschuwingen. |
   | Naam wijzigen | U kunt de naam van alle waarschuwingen wijzigen, behalve van standaardwaarschuwingen. |
   | Goedkeuren | Waarschuwingen goedkeuren om ze &quot;officieel&quot; te maken. |
   | In-/uitschakelen | U kunt alle waarschuwingen in- of uitschakelen, ook de standaardwaarschuwingen. |
   | Vernieuwen | Wanneer een of meer waarschuwingen zijn geselecteerd, kunnen deze worden vernieuwd. Hierdoor worden de vervaldatums verlengd tot 1 jaar vanaf de dag waarop op [!UICONTROL Renew] is geklikt, ongeacht de oorspronkelijke vervaldatum. |
   | Exporteren naar CSV | Zie [ Rapport van het Gebruik van de Download ](/help/admin/admin/c-server-call-usage/report-suite-usage.md) |

   {style="table-layout:auto"}
