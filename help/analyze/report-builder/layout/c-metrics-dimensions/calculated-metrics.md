---
description: 'Report Builder 5.2 biedt ondersteuning voor Adobe Analytics Unified Calculated Metrics. Naast andere innovaties hebben alle berekende standaarden nu een globale id: ze zijn niet meer beperkt tot één rapportsuite.'
title: Berekende standaarden
uuid: c9814894-cda6-40ff-8ec4-3ab2c1908ebc
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 15%

---


# Berekende standaarden

Report Builder 5.2 biedt ondersteuning voor Adobe Analytics Unified Calculated Metrics. Naast andere innovaties hebben alle berekende standaarden nu een globale id: ze zijn niet meer beperkt tot één rapportsuite.

>[!NOTE]
>
>De bestaande werkboeken zouden aan verzoeken met erfenis metrische IDs kunnen richten. Wanneer u Bouwer 5.2 van het Rapport gebruikt, zullen deze erfenis metrische IDs in nieuwe globale identiteitskaart worden omgezet. Als u dit werkboek met een gebruiker van de Bouwer van het Rapport v5.1 of vroeger deelt, zal die gebruiker niet de berekende metriek kunnen zien.

Meer over om berekende metriek met de nieuwe Berekende Metrische Bouwer en Manager tot stand te brengen en te beheren, verwijs naar de [Berekende Gids van Metriek](https://docs.adobe.com/content/help/nl-NL/analytics/components/calculated-metrics/cm-overview.html) .

In Stap 2 van de Tovenaar van het Verzoek, kunt u berekende metriek filtreren en toepassen.

## Berekende cijfers filteren {#section_376E986D3E684999A7CDB08E53854159}

**U kunt berekende maateenheden filteren** door op het pictogram Filter te klikken:  ![](assets/segment_filter.png)

. Het dialoogvenster Geavanceerde filters wordt gevuld met zowel standaard als berekende meetwaarden.

Beschikbare filters zijn:

![](assets/advanced_filters.png)

| Filternaam | Beschrijving |
|---|---|
| Tags | Hiermee kunt u filteren op berekende metriek met specifieke tags. Merk op dat de filters van de Markering de exploitant EN gebruiken. Als u twee labels controleert, ziet u in het rechterdeelvenster metrische gegevens die zijn gecodeerd met **beide** tags. |
| Rapportsuites | Als u het filter &quot;Alleen naam *van* rapportsuite&quot;toepast in de Berekende metrische bouwer in [!DNL Reports & Analytics], en vervolgens het Geavanceerde filter in weergeeft [!DNL Report Builder], geeft het filter Geavanceerd de berekende meetgegevens alleen weer voor de geselecteerde rapportsuite. |
| Eigenaars | Hiermee kunt u metingen filteren op eigenaar. Merk op dat eigenaarfilters de operator OR gebruiken. Als u twee eigenaars controleert, toont de juiste ruit metriek die door **één van beide** eigenaars worden bezeten. |
| Overige filters > Goedgekeurd | Toont alle officieel goedgekeurde metriek. |
| Overige filters > Favorieten | Hiermee worden alle metrische gegevens weergegeven die u als Favorieten hebt gemarkeerd. |
| Overige filters > Mine | Toont alle metriek die u bezit. |
| Overige filters > Met mij gedeeld | Toont alle metriek die anderen met u deelden. |

## Berekende waarden toepassen {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

Nadat u de filters hebt geselecteerd, klikt u **[!UICONTROL Apply]** om deze op uw verzoek toe te passen. De geselecteerde metrische(n) worden nu toegevoegd aan de rapportlay-out.

![](assets/filtering_for_metric.png)

