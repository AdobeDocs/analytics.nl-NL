---
title: Advertentieplatform
description: Zie de configuratie voor het geven van toestemming voor advertenties voor derden en providers.
feature: Dimensions
exl-id: bf63112d-7d20-4e35-9a59-5be21135ae51
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---

# Advertentieplatform

De &quot;Ad Platform Toestemming&quot; [ dimensie ](overview.md) toont of de toestemming wordt verzameld om gegevens naar derde reclameproviders, zoals Google, Meta, en anderen te verzenden.

Deze dimensie wordt momenteel alleen voor Google gebruikt. Op grond van de Europese privacywetgeving, de Digital Markets Act (DMA), eist Google dat gegevens die naar hun servers worden verzonden en in Europa worden verzameld, aangeven of toestemming wordt verzameld. Sommige klanten van Analytics verzenden gebeurtenisgegevens via Adobe Advertising als conversiegebeurtenissen naar Google.

In de toekomst kan deze dimensie worden gebruikt ter ondersteuning van de codering van aanvullende toestemmingsinformatie voor andere derde reclamebureaus.

## Deze dimensie vullen met gegevens

Deze afmeting verzamelt gegevens van de volgende [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md)

* `contextData.['adConsent']`

U vult de variabele van contextgegevens met relevante waarden voor de de toestemmingsgebieden van Google

* `ad_user_data` (eerste teken) en
* `ad_personalization` (tweede teken).

Zie [ Toestemming in de Verwijzing van API van Google Ads ](https://developers.google.com/google-ads/api/reference/rpc/v15/Consent) voor meer informatie.

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

* De Eigen van gegevens: De gegevens van de advertentie toestemmingen zijn beschikbaar gebruikend de `dataprivacydmaconsent` [ kolom ](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md).
* Data Warehouse rapporteert: de gegevens over de toestemming voor advertentie zijn beschikbaar met behulp van de **[!UICONTROL Ad Platform Consent]** -dimensie.

Uw organisatie bepaalt de logica om deze variabele van contextgegevens uit te voeren. De waarde blijft niet behouden na de treffer waarop deze is ingesteld, dus u moet de variabele met de contextgegevens op elke pagina instellen.

Wanneer u via Adobe Advertising advertentiegegevens stuurt naar Google voor conversiedoeleinden, raadpleegt u het Adobe Advertising-team voor hulp bij de integratie.

Voor meer informatie zie, [ Privacy die ](/help/admin/tools/manage-rs/edit-settings/privacy-reporting.md) meldt.
