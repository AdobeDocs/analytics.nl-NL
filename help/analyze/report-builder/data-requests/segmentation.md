---
description: Adobe Analytics-segmenten toevoegen, bewerken, toepassen en filteren in Report Builder.
title: Segmenten beheren
uuid: 4e4edc39-ed93-498f-913d-7b231b10e7a0
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 3%

---


# Segmenten beheren

Adobe Analytics-segmenten toevoegen, bewerken, toepassen en filteren in Report Builder.

Report Builder heeft een segmentatiepaneel in Stap 1 van de wizard Verzoek waarmee u segmenten kunt maken en beheren.

![](assets/seg_dialog.png)

## Segmenten {#section_B2BC136F9A53498D90C7C2ECC5DB892B} toevoegen of bewerken

>[!NOTE]
>
>Om segmenten toe te voegen of uit te geven, lanceert de het segmentinterface van Report Builder de het segmentbouwer van Analytics in een venster van Microsoft Internet Explorer. Uw rapportbuildersessie blijft actief. Andere browsers dan Internet Explorer worden niet ondersteund voor deze bewerking.

1. In het segmentpaneel van Stap 1 van de Tovenaar van het Verzoek, klik **[!UICONTROL Add]**.
1. Een venster van Internet Explorer lanceert dat de interface van de Bouwer van het Segment van de Analyse opent. Voor informatie over hoe te om segmenten te bouwen, verwijs naar [segmentatie van Analytics](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html).
1. Nadat u het segment hebt bepaald en bewaard, ga terug naar de Tovenaar van het Verzoek.
1. Klik op het pictogram Vernieuwen om de segmentlijst te vernieuwen.

>[!IMPORTANT]
>
>Deze lijst wordt in het cachegeheugen opgeslagen en het nieuwe segment wordt alleen weergegeven als u een vernieuwingsbewerking uitvoert.

## In-context-segmenten maken {#section_6DD2C663B2854469AA1075438F907678}

U kunt specifieke combinaties rapportafmetingen hebben die u in een segment zou willen veranderen. U kunt deze segmenten van de interface van Report Builder tot stand brengen. Selecteer bijvoorbeeld een paar pagina&#39;s in een paginaaanvraaguitvoer en maak een segment op basis van deze waarden.

1. Selecteer de punten van de rapportoutput u in een segment wilt veranderen.
1. Klik met de rechtermuisknop om **[!UICONTROL Create In-Context Segment in]** te selecteren en geef de rechtercontainer op (Container bezoekt, Container bezoeker, Container bezoeker).

   ![](assets/seg_in_context.png)

   Zie [Segmentatiegids](https://docs.adobe.com/content/help/en/analytics/components/segmentation/seg-home.html) voor meer informatie over containers.

1. De gebruikersinterface van Segment Builder wordt nu in Internet Explorer gestart. De UI van de Bouwer van het Segment zal met de container en de filter worden geïnitialiseerd u specificeerde.
1. Nadat u een naam en een beschrijving aan het segment hebt toegevoegd, sparen het.
1. Ga terug naar rapportbuilder en klik het Refresh pictogram om de lijst van segmenten te verfrissen.
1. U bent nu klaar om dit segment toe te passen.

## Segmenten zoeken en toepassen {#section_CACA269B48E94CFD91C2D5A15E9C77B7}

Om het even welke segmenten die in Rapporten &amp; Analytics, Report Builder, of Data Warehouse werden gecreeerd verschijnen in deze segmentlijst. Klik op het pictogram Vernieuwen ( ![](assets/refresh_icon.png)) om de lijst te vernieuwen.

U kunt één of veelvoudige segmenten op om het even welk bepaald verzoek toepassen. Dit omvat opeenvolgende segmenten.

1. Ga naar **[!UICONTROL Segment]** drop-down lijst en klik kleine benedenpijl in **[!UICONTROL Choose Segment]** doos om alle segmenten te tonen.

   ![](assets/seg_list.png)

1. Controleer welk segment of welke segmenten u wilt toepassen.

>[!NOTE]
>
>Of u nu Admin of niet-Admin bent, in Report Builder kunt u alleen die segmenten zien die u bezit en die welke met u zijn gedeeld. (In de gebruikersinterface Marketing Reports &amp; Analytics kan de Admin alle segmenten in de organisatie zien.)

## Segmenten filteren {#section_376E986D3E684999A7CDB08E53854159}

**Filtersegmenten** door op het pictogram Filter te klikken:   ![](assets/segment_filter.png)

Beschikbare filters zijn:

| Filternaam | Beschrijving |
|---|---|
| Tags | Hiermee kunt u filteren op segmenten met specifieke tags. Merk op dat de filters van de Markering de exploitant EN gebruiken. Als u twee markeringen controleert, toont de juiste ruit segmenten die met **allebei** markeringen zijn geëtiketteerd. |
| Eigenaars | Hiermee kunt u segmenten filteren op eigenaar. Merk op dat eigenaarfilters de operator OR gebruiken. Als u twee eigenaars controleert, toont de juiste ruit segmenten die door **of** eigenaar worden bezeten. |
| Overige filters > Alleen *naam van rapportsuite* | Als u &quot;slechts *rapportreeksnaam*&quot;filter in de Bouwer van het Segment in [!DNL marketing reports & analytics] toepast, en dan het Geavanceerde Filter in [!DNL report builder] toont, zal de Geavanceerde filter het segment voor de geselecteerde rapportreeks slechts tonen. |
| Overige filters > Mine | Toont alle segmenten die u bezit. |
| Overige filters > Met mij gedeeld | Hiermee geeft u alle segmenten weer die anderen met u hebben gedeeld. |
| Overige filters > Favorieten | Hiermee worden alle segmenten weergegeven die u als Favorieten hebt gemarkeerd. |
| Overige filters > Goedgekeurd | Hiermee geeft u alle officieel goedgekeurde segmenten weer. |

## Voeg een segmentcontrole aan een werkboek {#section_E3E5149A8464441FA5445A98DBD520AC} toe

Het toevoegen van een segmentcontrole laat u segmenten van binnen een werkboek in plaats van het moeten in de Tovenaar van het Verzoek gaan.

1. Klik het pictogram van de Controle ( ![](assets/control_icon.png)) naast de segment drop-down.

   ![](assets/seg_control.png)

1. Controleer alle segmenten die u in de segmentcontrole wilt verschijnen, of controleer **[!UICONTROL Select All]**.
1. Let op de optie **[!UICONTROL Automatically refresh linked requests upon item selection]**.

   * Als deze optie is ingeschakeld, worden alle aanvragen die gebruikmaken van dit besturingselement vernieuwd.
   * Als niet gecontroleerd, worden de bijbehorende verzoekparameters bijgewerkt, maar de verzoeken worden niet verfrist.

1. Specificeer de hogere linkercelplaats van de segmentcontrole.
1. Klik **[!UICONTROL OK]** en de segmentcontrole verschijnt in de gespecificeerde plaats.

   ![](assets/seg_control2.png)

## De lijst met segmenten {#section_22E4A86789444B4A998532396B476EFB} vernieuwen

Wanneer u een nieuw segment toevoegt of een bestaand segment bewerkt, moet u op het pictogram Vernieuwen ( ![](assets/refresh_icon.png)) klikken om de lijst met segmenten in de cache te vernieuwen.

## Segmenten beheren in verzoeken {#section_C3D63FCBE1A94369A319243313B03C93}

Voorafgaand aan v5.4, laat Report Builder gebruikers segmenten op veelvoudige verzoeken veranderen. Dit proces heeft echter altijd de bestaande segmenten vervangen. De gebruikers die één nieuw segment aan elk verzoek wilden toevoegen konden dit niet doen, aangezien het toevoegen van het segment de vorige reeks segmenten zou verwijderen die reeds aan elk verzoek wordt toegewezen.

Met Report Builder 5.4 kunt u alle segmenten binnen meerdere aanvragen toevoegen, verwijderen, vervangen en vervangen:

1. Selecteer veelvoudige verzoeken in een werkboek.
1. Klik met de rechtermuisknop en selecteer **[!UICONTROL Edit Requests]** > **[!UICONTROL By Segment]**.

   ![](assets/edit_by_segment.png)

1. Selecteer in het dialoogvenster Groep bewerken een van de vier opties:

   | Optie | Beschrijving |
   |---|---|
   | Segment toevoegen | Hiermee kunt u een of meer segmenten kiezen die u wilt toevoegen aan de lijst met huidige segmenten. |
   | Segment(en) vervangen | Hiermee kunt u kiezen welk segment of welke segmenten door een of meer segmenten worden vervangen. |
   | Alle segmenten vervangen door | Hiermee kunt u een of meer segmenten kiezen om het huidige segment of de huidige segmenten te vervangen. |
   | Segment(en) verwijderen | Hiermee kunt u segmenten uit de aanvragen verwijderen. |

