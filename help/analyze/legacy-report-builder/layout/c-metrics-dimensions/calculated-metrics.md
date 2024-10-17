---
description: 'Report Builder 5.2 steunt Adobe Analytics Verenigde Berekende Metriek. Naast andere innovaties hebben alle berekende standaarden nu een globale id: ze zijn niet meer beperkt tot één rapportsuite.'
title: Berekende cijfers
feature: Report Builder
role: User, Admin
exl-id: 462086eb-675f-443c-b3a6-b4fa390254da
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 6%

---

# Berekende cijfers

{{legacy-arb}}

Report Builder 5.2 en hoger biedt ondersteuning voor berekende Adobe Analytics-meetwaarden. Alle berekende metriek hebben nu een globale identiteitskaart - zij zijn niet meer beperkt tot één rapportreeks.

>[!NOTE]
>
>De bestaande werkboeken zouden aan verzoeken met erfenis metrische IDs kunnen richten. Wanneer u Report Builder 5.2 gebruikt, zullen deze erfenis metrische IDs in nieuwe globale identiteitskaart worden omgezet. Als u dit werkboek met een gebruiker van Report Builder v5.1 of vroeger deelt, zal die gebruiker niet de berekende metriek kunnen zien.

Om meer over te weten te komen hoe te om berekende metriek met de nieuwe Berekende Metrische Bouwer en Manager tot stand te brengen en te beheren, verwijs naar de [ Berekende Gids van Metriek ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/cm-overview.html).

In Stap 2 van de Tovenaar van het Verzoek, kunt u berekende metriek filtreren en toepassen.

## Berekende maateenheden filteren {#section_376E986D3E684999A7CDB08E53854159}

**berekende metriek van de Filter** door op het pictogram van de Filter te klikken: ![ Schermafbeelding van de opties die van de Filter de Toepassing, Gebruiker, de gebieden van het Project tonen.](/help/admin/admin/assets/filter.png)

Het dialoogvenster Geavanceerde filters wordt gevuld met zowel standaard als berekende meetwaarden.

Beschikbare filters zijn:

![ Schermafbeelding die de Geavanceerde die opties toont van Filters in de volgende lijst worden beschreven.](assets/advanced_filters.png)

| Filternaam | Beschrijving |
|---|---|
| Tags | Hiermee kunt u filteren op berekende metriek met specifieke tags. Merk op dat de filters van de Markering de exploitant EN gebruiken. Als u twee markeringen controleert, toont de juiste ruit metriek die met **allebei** markeringen zijn geëtiketteerd. |
| Rapportsuites | Als u de &quot;slechts *&quot;filter van de 0} rapportsuite in de Berekende Metrische Bouwer in [!DNL Adobe Analytics] toepast, en dan de Geavanceerde Filter in [!DNL Report Builder] toont, zal de Geavanceerde filter de berekende metriek voor de geselecteerde slechts rapportreeks tonen.* |
| Eigenaars | Hiermee kunt u metingen filteren op eigenaar. Merk op dat eigenaarfilters de operator OR gebruiken. Als u twee eigenaars controleert, toont de juiste ruit metriek die door **of** eigenaar worden bezeten. |
| Overige filters > Goedgekeurd | Toont alle officieel goedgekeurde metriek. |
| Overige filters > Favorieten | Hiermee worden alle metrische gegevens weergegeven die u als Favorieten hebt gemarkeerd. |
| Overige filters > Mine | Toont alle metriek die u bezit. |
| Overige filters > Met mij gedeeld | Toont alle metriek die anderen met u deelden. |

## Berekende waarden toepassen {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

Nadat u de filters hebt geselecteerd, klikt u op **[!UICONTROL Apply]** om deze op uw verzoek toe te passen. De geselecteerde metrische(n) worden nu toegevoegd aan de rapportlay-out.

![ Schermafbeelding die de Stap 2 van de Tovenaar van het Verzoek toont - de Totalen van de Plaats die aan het Geavanceerde venster van Filters richten en rapportmetriek toepasten.](assets/filtering_for_metric.png)
