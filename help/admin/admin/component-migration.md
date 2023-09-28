---
description: Verklaart hoe te om componenten en projecten van Adobe Analytics aan Customer Journey Analytics te migreren.
title: Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics
feature: Admin Tools
source-git-commit: 73cbfbbad4d8e7bb3107ee08861a6342aba85e84
workflow-type: tm+mt
source-wordcount: '1133'
ht-degree: 4%

---

# Componenten en projecten migreren van Adobe Analytics naar Customer Journey Analytics

Adobe Analytics-beheerders kunnen Adobe Analytics-componenten en -projecten migreren naar Customer Journey Analytics.

Het migratieproces omvat:

* Adobe Analytics-projecten opnieuw maken in Customer Journey Analytics.

* Overeenkomende afmetingen en maatstaven van Adobe Analytics melden reeksen aan afmetingen en metriek in de mening van de gegevens van de Customer Journey Analytics.

  Sommige dimensies en metriek komen automatisch overeen; andere moet u handmatig afstemmen als onderdeel van het migratieproces.

## Een migratie voorbereiden

### Vereisten

Voordat uw projecten en de bijbehorende dimensies en metriek gereed zijn voor migratie, moet u eerst het volgende doen:

* Gebruik de bronschakelaar van de Analyse om de gegevens van de het rapportreeks van Adobe Analytics in Customer Journey Analytics te bekijken. Om dat te doen, moet u:

   * [Rapportagesuites instellen voor opname in Adobe Experience Platform en Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/compare-aa-cja/cja-aa-comparison/aa-data-in-cja.html?lang=en#set-up-report-suites-for-ingestion-into-the-adobe-experience-platform-and-customer-journey-analytics)

   * [Gegevens opnemen en gebruiken](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-data-ingestion/ingest-use-guides/analytics.html)

* Zorg ervoor dat gebruikers in de Customer Journey Analytics zijn ingericht voor de gegevensweergaven waar de gegevens overeenkomen.

  Zie voor meer informatie [De toestemmingen van de Customer Journey Analytics in de Admin Console](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html?lang=en#customer-journey-analytics-permissions-in-admin-console) in [Toegangsbeheer Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-admin/cja-access-control.html).

  Het tabblad Machtigingen maakt deel uit van elk productprofiel in Admin Console. U kunt gebruikers toevoegen aan specifieke productprofielen. Vervolgens wijst u rechten toe aan specifieke gegevensweergaven en geeft u op welke machtigingen de gebruikers in een productprofiel hebben.

* Maak een migratieplan, zoals beschreven in de onderstaande sectie; [Een migratieplan maken als organisatie](#create-a-migration-plan-as-an-organization).

### Begrijpen wat er in een migratie is opgenomen

In de volgende tabel wordt aangegeven welke elementen van een project en component zijn opgenomen in een migratie:


|  | Projecten | Dimensionen en cijfers |
|---------|----------|---------|
| **Datumbereiken** | Ja | N.v.t. |
| **Segmenten** | Ja | N.v.t. |
| **Snelle segmenten** | Ja | N.v.t. |
| **Deelvensters** | Ja | N.v.t. |
| **Visualisaties** | Ja | N.v.t. |
| **Eigenaar** | (Gedefinieerd door gebruiker die de migratie uitvoert) | ? |
| **Curation** | Nee | N.v.t. |
| **Delen (projectrollen)** | Nee | Nee |
| **Annotaties** | Nee | N.v.t. |
| **Mapstructuur** | Nee | N.v.t. |
| **Beschrijvingen** | Ja | ? |
| **Tags** | ? | ? |
| **Planningen** | ? | N.v.t. |
| **Attributie (op afmetingen)** | N.v.t. | ? |
| **Anomaliedetectie** | ? | N.v.t. |
| **Contributieanalyse** | ? | N.v.t. |
| **Waarschuwingen** | ? | N.v.t. |

{style="table-layout:auto"}

### Een migratieplan maken als organisatie

Omdat om het even welke componenten die voor een bepaalde projectmigratie worden aangepast op om het even welke toekomstige projectmigraties voor de volledige organisatie van toepassing zijn, is het belangrijk dat uw organisatie alle projectmigraties vooraf plant.

U zou als organisatie moeten beslissen welke afmetingen en metriek zullen worden aangepast wat met wat wordt aangepast, om individuele beheerders te vermijden die besluiten in een silo op het tijdstip van de migratie van een project nemen.

## Adobe Analytics-projecten migreren naar Customer Journey Analytics

>[!IMPORTANT]
>
>Voordat u projecten migreert naar Customer Journey Analytics, zoals wordt beschreven in deze sectie, moet u meer weten over migrerende projecten in het deelvenster [De migratie plannen](#plan-the-migration) hierboven.
>
>Alle dimensies of metriek die u aanpast, zijn permanent, zowel voor dit project als voor alle toekomstige projecten die door uw volledige organisatie worden gemigreerd. De overeenkomsten die u aanbrengt, kunnen niet worden gewijzigd.



1. Selecteer in Adobe Analytics de optie [!UICONTROL **Beheerder**] tab, dan selecteren [!UICONTROL **Alle beheerders**].

1. Onder [!UICONTROL **Gegevensconfiguratie en -verzameling**], selecteert u [!UICONTROL **Componentmigratie**].

1. (Voorwaardelijk) Om het project snel te vinden dat u wilt migreren, kunt u:

   * Filter de lijst met projecten door het pictogram Filter te selecteren.

     U kunt filteren op de volgende criteria:

      * Status

      * Tags

      * Rapportsuite

      * Eigenaars

      * Overige filters

   * Gebruik het zoekveld om te zoeken naar het project dat u wilt migreren.

1. Plaats de muis boven het project dat u wilt migreren en selecteer vervolgens de knop **Migreren** pictogram ![Project migreren](assets/migrate.svg).

   of

   Selecteer het project dat u wilt migreren en selecteer vervolgens [!UICONTROL **Migreren naar Customer Journey Analytics**].

   U kunt slechts één project tegelijk selecteren voor migratie.

   De [!UICONTROL **Project_name migreren naar Customer Journey Analytics**] wordt weergegeven.

   <!-- add screenshot -->

1. In de [!UICONTROL **Projecteigenaar**] veld, typt u de naam van de gebruiker die u als eigenaar van het project in de Customer Journey Analytics wilt instellen en selecteert u vervolgens de naam van de gebruiker in het keuzemenu.

   De eigenaar die u specificeert heeft volledige beheersrechten aan het project.

1. In de [!UICONTROL **Het schema van de gelijke voor rapportreeksen**] , selecteert u een rapportsuite.

1. In de [!UICONTROL **Gegevens, weergave**] drop-down menu, selecteer de de gegevensmening van de Customer Journey Analytics waar u het project en de componenten wilt worden gemigreerd.

1. Selecteren [!UICONTROL **Schema afstemmen**].

1. In de [!UICONTROL **Schema afstemmen**] sectie, breid de [!UICONTROL **Dimensionen**] en [!UICONTROL **Metrisch**] secties.

   Sommige dimensies en metriek in Adobe Analytics worden automatisch aangepast aan een dimensie of metrisch in Customer Journey Analytics. Andere moeten handmatig worden aangepast.

   **Automatisch overeenkomende afmetingen en maatstaven**

   Sommige dimensies en metriek in Adobe Analytics worden automatisch aangepast aan een dimensie of metrisch in Customer Journey Analytics. U kunt geen overeenkomstige besluiten voor deze dimensies en metriek nemen.

   Bijvoorbeeld de **Bezoeken** De metrische waarde in Adobe Analytics komt automatisch overeen met de **Sessies** metrisch in Customer Journey Analytics.

   U kunt om het even welke afmeting of metrisch selecteren om hun bijbehorende IDs te bekijken.

   <!-- update screenshot after I can see the Status column -->

   ![Projectmigratieschema](assets/project-migration-schema.png)

   **Afmetingen en maatstaven handmatig afstemmen**

   Andere dimensies en maatstaven in Adobe Analytics kunnen niet automatisch worden aangepast aan een dimensie of metrisch in Customer Journey Analytics.

   Wanneer een afmeting of metrisch niet automatisch kan worden aangepast, verschijnt een oranje teller naast [!UICONTROL **Dimensionen**] of [!UICONTROL **Metrisch**] sectiekoptekst, die het aantal afmetingen of metriek aangeeft dat handmatig moet worden aangepast. In de tabel verschijnt een waarschuwingspictogram ![waarschuwingspictogram](assets/schema-warning.png) wordt weergegeven naast elke dimensie of metrische waarde die handmatig moet worden aangepast.

   <!-- update screenshot after I can see the Status column -->

   ![Handmatige overeenkomst voor migratieschema](assets/schema-manual-map.png)

1. Als u de afmetingen en metriek handmatig wilt afstemmen, selecteert u een dimensie of metrische waarde die een waarschuwingspictogram bevat ![waarschuwingspictogram](assets/schema-warning.png)en vervolgens in de [!UICONTROL **Metrisch overeenkomende Customer Journey Analytics**] (of de [!UICONTROL **Dimensie Customer Journey Analytics afstemmen**] (als u een afmeting aanpast), selecteer de afmeting of metrisch in Customer Journey Analytics die u met de afmeting of metrisch wilt aanpassen u selecteerde.

   ![maatstaven en maatstaven](assets/schema-manual-map-drop-down.png)

   Herhaal dit proces voor elke afmeting of metrisch die het waarschuwingspictogram bevat.

   Nadat alle dimensies en metriek in de het rapportreeks van Adobe Analytics aan een afmeting of metrisch in de de gegevensmening van de Customer Journey Analytics worden aangepast, een groen vinkje ![vinkje](assets/report-suite-check.png) wordt weergegeven naast de naam van de rapportsuite in het dialoogvenster [!UICONTROL **Het schema van de gelijke voor rapportreeksen**] sectie.

1. (Voorwaardelijk) als het project u migreert meer dan één rapportreeks bevat, selecteer een andere rapportreeks in het [!UICONTROL **Het schema van de gelijke voor rapportreeksen**] en herhaal vervolgens stap 6 tot en met stap 10. <!-- double-check that the step numbers are still correct -->

1. Selecteren [!UICONTROL **Migreren**].

   >[!WARNING]
   >
   >   Er verschijnt een waarschuwingsbericht op het scherm nadat u [!UICONTROL **Migreren**]. Voordat u doorgaat, moet u begrijpen dat alle dimensies of maatstaven die u aanpast permanent zijn, zowel voor dit project als voor alle toekomstige projecten die door uw gehele organisatie worden gemigreerd. Als u doorgaat, kunnen de overeenkomsten die u aanbrengt niet worden gewijzigd.
