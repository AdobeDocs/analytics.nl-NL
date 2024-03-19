---
title: Advertentie
description: Zie de configuratie voor het geven van toestemming voor advertenties voor derden en providers.
feature: Dimensions
source-git-commit: b5aba8a42f524ef3367a779e6fb1a731de680750
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 0%

---

# Advertentie

De &#39;AD-instemming&#39; [dimensie](overview.md) geeft aan of toestemming is verzameld voor het verzenden van gegevens naar andere reclamebureaus, zoals Google, Meta en anderen.

Deze dimensie wordt momenteel alleen voor Google gebruikt. Op grond van de Europese privacywetgeving, de Digital Markets Act (DMA), eist Google dat gegevens die naar hun servers worden verzonden en in Europa worden verzameld, aangeven of toestemming wordt verzameld. Sommige klanten van Analytics verzenden gebeurtenisgegevens via Adobe Advertising als omzettingsgebeurtenissen naar Google.

In de toekomst kan deze dimensie worden gebruikt ter ondersteuning van het coderen van aanvullende toestemmingsinformatie voor andere externe reclamebureaus.

## Deze dimensie vullen met gegevens

Deze dimensie verzamelt gegevens van het volgende [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md)

* `contextData.['adConsent']`

U vult de variabele van contextgegevens met relevante waarden voor de de toestemmingsgebieden van Google

* `ad_user_data` (eerste teken) en
* `ad_personalization` (tweede teken).

Zie [Toestemming in de API-naslaggids voor Google Ads](https://developers.google.com/google-ads/api/reference/rpc/v15/Consent) voor meer informatie .

De mogelijke waarden voor elk van deze velden kunnen zijn:

| Waarde | ad_user_data | ad_personalisatie |
|:-:|---|---|
| `Y` | Toestemming verlenen aan Google voor gegevens van gebruikers van advertenties. | Toestemming verlenen aan Google voor ad personalization. |
| `N` | Afkeuring van Google weigeren voor gegevens van gebruikers. | Twintig toestemming voor Google voor ad personalization. |
| `U` | Niet opgegeven. | Niet opgegeven. |

In het onderstaande voorbeeld wordt toestemming verleend aan Google voor gegevens van gebruikers van advertenties, maar niet voor personalisatie:

```
contextData.['adConsent'] = "YN..."
```

Tekens na het eerste en tweede teken worden momenteel genegeerd.

## De gegevens gebruiken

U kunt de verzamelde gegevens en toestemmingsgegevens gebruiken:

* Gegevensfeeds: de gegevens over de toestemming voor de advertentie zijn beschikbaar via de `dataprivacydmaconsent` [kolom](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).
* Rapporten van Data Warehouse: de gegevens over de toestemming voor de advertentie zijn beschikbaar via de **[!UICONTROL Ad Platform Consent]** dimensie.


Uw organisatie bepaalt de logica om deze variabele van contextgegevens uit te voeren. De waarde blijft niet behouden na de treffer waarop deze is ingesteld, dus u moet de variabele met de contextgegevens op elke pagina instellen.

Wanneer u reclamegegevens van Adobe Analytics via Adobe Advertising als conversiegebeurtenissen naar Google verzendt, raadpleegt u het team van de Adobe Advertising voor hulp bij de integratie.

Zie voor meer informatie [Privacy-rapportage](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md).
