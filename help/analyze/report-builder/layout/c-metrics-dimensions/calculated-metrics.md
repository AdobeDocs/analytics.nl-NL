---
description: 'Report Builder 5.2 steunt Adobe Analytics Verenigde Berekende Metriek. Naast andere innovaties hebben alle berekende standaarden nu een globale id: ze zijn niet meer beperkt tot één rapportsuite.'
title: Berekende cijfers
feature: Report Builder
role: User, Admin
exl-id: 462086eb-675f-443c-b3a6-b4fa390254da
source-git-commit: a979fc8787fa96f8fa8317996ac66341a6f54354
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 11%

---

# Berekende cijfers

Report Builder 5.2 ondersteunt Adobe Analytics verenigde berekende meetgegevens. Naast andere innovaties hebben alle berekende standaarden nu een globale id: ze zijn niet meer beperkt tot één rapportsuite.

>[!NOTE]
>
>De bestaande werkboeken zouden aan verzoeken met erfenis metrische IDs kunnen richten. Wanneer u Report Builder 5.2 gebruikt, zullen deze erfenis metrische IDs in nieuwe globale identiteitskaart worden omgezet. Als u dit werkboek met een gebruiker van Report Builder v5.1 of vroeger deelt, zal die gebruiker niet de berekende metriek kunnen zien.

Als u meer wilt weten over het maken en beheren van berekende metriek met de nieuwe Berekende Metrische Builder en Manager, raadpleegt u de [Berekende cijfers](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/cm-overview.html) Hulplijn.

In Stap 2 van de Tovenaar van het Verzoek, kunt u berekende metriek filtreren en toepassen.

## Berekende maateenheden filteren {#section_376E986D3E684999A7CDB08E53854159}

**Filter** berekende metriek door op het pictogram van de Filter te klikken:  ![Screenshot van de filteropties die de velden Toepassing, Gebruiker en Project weergeven.](/help/admin/admin/assets/filter.png)

Het dialoogvenster Geavanceerde filters wordt gevuld met zowel standaard als berekende meetwaarden.

Beschikbare filters zijn:

![Screenshot met de opties voor Geavanceerde filters die in de volgende tabel worden beschreven.](assets/advanced_filters.png)

| Filternaam | Beschrijving |
|---|---|
| Tags | Hiermee kunt u filteren op berekende metriek met specifieke tags. Merk op dat de filters van de Markering de exploitant EN gebruiken. Als u twee labels controleert, ziet u in het rechterdeelvenster de maateenheden die zijn getagd **beide** -tags. |
| Rapportsuites | Als u de optie Alleen *naam rapportsuite*&quot; in de Berekende Metrische Bouwer in [!DNL Adobe Analytics]en geeft u vervolgens het geavanceerde filter weer in [!DNL Report Builder], zal het Geavanceerde filter de berekende metriek voor de geselecteerde rapportreeks slechts tonen. |
| Eigenaars | Hiermee kunt u metingen filteren op eigenaar. Merk op dat eigenaarfilters de operator OR gebruiken. Als u twee eigenaars controleert, toont de juiste ruit metriek die door wordt bezeten **ofwel** eigenaar. |
| Overige filters > Goedgekeurd | Toont alle officieel goedgekeurde metriek. |
| Overige filters > Favorieten | Hiermee worden alle metrische gegevens weergegeven die u als Favorieten hebt gemarkeerd. |
| Overige filters > Mine | Toont alle metriek die u bezit. |
| Overige filters > Met mij gedeeld | Toont alle metriek die anderen met u deelden. |

## Berekende waarden toepassen {#section_DF5CF349460A45FDA4B6E6BB8B52F18E}

Klik op **[!UICONTROL Apply]** om deze op uw verzoek toe te passen. De geselecteerde metrische(n) worden nu toegevoegd aan de rapportlay-out.

![Screenshot die de Stap 2 van de Tovenaar van het Verzoek toont - de Totalen van de Plaats richtend aan het Geavanceerde venster van Filters en toegepaste rapportmetriek.](assets/filtering_for_metric.png)
