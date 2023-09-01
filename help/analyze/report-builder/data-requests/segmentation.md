---
description: Adobe Analytics-segmenten toevoegen, bewerken, toepassen en filteren in Report Builder.
title: Segmenten beheren (Report Builder)
feature: Report Builder
role: User, Admin
exl-id: c4ad89e0-91c9-47e1-a226-69d82fdb8918
source-git-commit: d218d07ec16e981d7e148092b91fbbd5711e840f
workflow-type: tm+mt
source-wordcount: '986'
ht-degree: 0%

---

# Segmenten beheren

Adobe Analytics-segmenten toevoegen, bewerken, toepassen en filteren in Report Builder.

De Report Builder kenmerkt een segmentatiepaneel in Stap 1 van de Tovenaar van het Verzoek die u tot segmenten laat leiden en leidt.

![Schermafbeelding met de segmentopties voor het toevoegen, bewerken of wissen van segmenten en het markeren van de pictogrammen Besturing, Filter en Vernieuwen.](assets/seg_dialog.png)

## Segmenten toevoegen of bewerken {#section_B2BC136F9A53498D90C7C2ECC5DB892B}

>[!NOTE]
>
>Om segmenten toe te voegen of uit te geven, lanceert de de segmentinterface van de Report Builder de het segmentbouwer van de Analyse in een venster van Microsoft Internet Explorer. Uw Report Builder-sessie blijft actief. Andere browsers dan Internet Explorer worden niet ondersteund voor deze bewerking.

1. In het segmentpaneel van Stap 1 van de Tovenaar van het Verzoek, klik **[!UICONTROL Add]**.
1. Een venster van Internet Explorer lanceert dat de interface van de Bouwer van het Segment van de Analyse opent. Raadpleeg voor informatie over het maken van segmenten [Segmentatie van analyse](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html).
1. Nadat u het segment hebt bepaald en bewaard, ga terug naar de Tovenaar van het Verzoek.
1. Klik het Refresh pictogram om de segmentlijst te verfrissen.

>[!IMPORTANT]
>
>Deze lijst wordt in het cachegeheugen opgeslagen en het nieuwe segment wordt alleen weergegeven als u een vernieuwingsbewerking uitvoert.

## In-context-segmenten maken {#section_6DD2C663B2854469AA1075438F907678}

U kunt specifieke combinaties rapportdimensies hebben die u in een segment zou willen veranderen. U kunt deze segmenten maken via de interface Report Builder. Selecteer bijvoorbeeld een paar pagina&#39;s in een paginaaanvraaguitvoer en maak een segment op basis van deze waarden.

1. Selecteer de punten van de rapportoutput u in een segment wilt veranderen.
1. Klik met de rechtermuisknop om te selecteren **[!UICONTROL Create In-Context Segment in]** en geeft u de rechtercontainer op (de container van Hits, de container van Visitor, de container van de bezoeker).

   ![Screenshot met Maken in-Context Segment in geselecteerde en beschikbare containeropties.](assets/seg_in_context.png)

   Zie voor meer informatie over containers de [Segmenteringsgids](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-home.html).

1. De gebruikersinterface van Segment Builder wordt nu in Internet Explorer gestart. De UI van de Bouwer van het Segment zal met de container en de filter worden geïnitialiseerd u specificeerde.
1. Nadat u een naam en een beschrijving aan het segment hebt toegevoegd, sparen het.
1. Ga terug naar Report Builder en klik het Refresh pictogram om de lijst van segmenten te verfrissen.
1. U bent nu klaar om dit segment toe te passen.

## Segmenten zoeken en toepassen {#section_CACA269B48E94CFD91C2D5A15E9C77B7}

Om het even welke segmenten die in Rapporten &amp; Analytics, Report Builder, of Data Warehouse werden gecreeerd verschijnen in deze segmentlijst. Klik op het pictogram Vernieuwen om de lijst te vernieuwen ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg).

U kunt één of veelvoudige segmenten op om het even welk bepaald verzoek toepassen. Dit omvat opeenvolgende segmenten.

1. Ga naar de **[!UICONTROL Segment]** vervolgkeuzelijst en klik op de kleine pijl-omlaag in het dialoogvenster **[!UICONTROL Choose Segment]** om alle segmenten weer te geven.

1. Controleer welk segment of welke segmenten u wilt toepassen.

   ![Schermafbeelding met geselecteerde segmenten.](assets/seg_list.png)

>[!NOTE]
>
>Of u nu Admin of niet-Admin bent, in Report Builder kunt u alleen die segmenten zien die u bezit en die welke met u zijn gedeeld. (In de gebruikersinterface Marketing Reports &amp; Analytics kan de Admin alle segmenten in de organisatie zien.)

## Segmenten filteren {#section_376E986D3E684999A7CDB08E53854159}

**Filter** segmenten door op het pictogram Filter te klikken:  ![Filterpictogram](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg)

Beschikbare filters zijn:

| Filternaam | Beschrijving |
|---|---|
| Tags | Hiermee kunt u filteren op segmenten met specifieke tags. Merk op dat de filters van de Markering de exploitant EN gebruiken. Als u twee labels controleert, ziet u in het rechterdeelvenster segmenten die zijn gecodeerd **beide** -tags. |
| Eigenaars | Hiermee kunt u segmenten filteren op eigenaar. Merk op dat eigenaarfilters de operator OR gebruiken. Als u twee eigenaars controleert, toont de juiste ruit segmenten die door worden bezeten **ofwel** eigenaar. |
| Overige filters > Alleen *naam rapportsuite* | Als u de optie Alleen *naam rapportsuite*&quot;, filter in de Bouwer van het Segment in [!DNL marketing reports & analytics]en geeft u vervolgens het geavanceerde filter weer in [!DNL Report Builder], zal de Geavanceerde filter het segment voor de geselecteerde rapportreeks slechts tonen. |
| Overige filters > Mine | Toont alle segmenten die u bezit. |
| Overige filters > Met mij gedeeld | Toont alle segmenten die anderen met u deelden. |
| Overige filters > Favorieten | Hiermee worden alle segmenten weergegeven die u als Favorieten hebt gemarkeerd. |
| Overige filters > Goedgekeurd | Toont alle officieel goedgekeurde segmenten. |

## Voeg een segmentcontrole aan een werkboek toe {#section_E3E5149A8464441FA5445A98DBD520AC}

Het toevoegen van een segmentcontrole laat u segmenten van binnen een werkboek in plaats van het moeten in de Tovenaar van het Verzoek gaan.

1. Klik op het pictogram Besturing ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Filter_18_N.svg) naast de segment drop-down.

1. Controleer alle segmenten die u in de segmentcontrole wilt verschijnen, of controleer **[!UICONTROL Select All]**.

   ![Screenshot van het dialoogvenster Instellingen besturingselement met alle geselecteerde instellingen.](assets/seg_control.png)

1. Let op de optie **[!UICONTROL Automatically refresh linked requests upon item selection]**.

   * Als deze optie is ingeschakeld, worden alle aanvragen die gebruikmaken van dit besturingselement vernieuwd.
   * Als niet gecontroleerd, worden de bijbehorende verzoekparameters bijgewerkt, maar de verzoeken worden niet verfrist.

1. Specificeer de hogere linkercelplaats van de segmentcontrole.

1. Klikken **[!UICONTROL OK]** en de segmentcontrole verschijnt in de gespecificeerde plaats.

   ![Schermopname met het vervolgkeuzeveld Segment kiezen.](assets/seg_control2.png)

## Lijst met segmenten vernieuwen {#section_22E4A86789444B4A998532396B476EFB}

Als u een nieuw segment toevoegt of een bestaand segment bewerkt, klikt u op het pictogram Vernieuwen ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Refresh_18_N.svg) om de caching lijst van segmenten te verfrissen.

## Segmenten in verschillende verzoeken beheren {#section_C3D63FCBE1A94369A319243313B03C93}

Voorafgaand aan v5.4, laat de Report Builder gebruikers segmenten op veelvoudige verzoeken veranderen. Dit proces heeft echter altijd de bestaande segmenten vervangen. De gebruikers die één nieuw segment aan elk verzoek wilden toevoegen konden dit niet doen, aangezien het toevoegen van het segment de vorige reeks segmenten zou verwijderen die reeds aan elk verzoek wordt toegewezen.

Met Report Builder 5.4 kunt u alle segmenten binnen meerdere aanvragen toevoegen, verwijderen, vervangen en vervangen:

1. Selecteer veelvoudige verzoeken in een werkboek.
1. Klik met de rechtermuisknop en selecteer **[!UICONTROL Edit Requests]** > **[!UICONTROL By Segment]**.

   ![Screenshot met de opties Verzoeken bewerken en Op segment geselecteerd.](assets/edit_by_segment.png)

1. Selecteer in het dialoogvenster Groep bewerken een van de vier opties:

   | Optie | Beschrijving |
   |---|---|
   | Segment toevoegen | Hiermee kunt u een of meer segmenten kiezen die u wilt toevoegen aan de lijst met huidige segmenten. |
   | Segment(en) vervangen | Hiermee kunt u kiezen welk segment of welke segmenten door een of meer segmenten worden vervangen. |
   | Alle segmenten vervangen door | Hiermee kunt u een of meer segmenten kiezen om het huidige segment of de huidige segmenten te vervangen. |
   | Segment(en) verwijderen | Hiermee kunt u segmenten uit de aanvragen verwijderen. |
