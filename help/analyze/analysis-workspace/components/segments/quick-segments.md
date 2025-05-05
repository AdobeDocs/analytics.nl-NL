---
description: Gebruik snelle segmenten in Analysis Workspace.
title: Snelle segmenten
feature: Segmentation
role: User, Admin
exl-id: 680e7772-10d3-4448-b5bf-def3bc3429d2
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '1101'
ht-degree: 0%

---

# Snelle segmenten

De snelle segmenten staan u toe om gegevens binnen een bepaald project gemakkelijk te onderzoeken, zonder de behoefte om een meer complex component-lijst segment in de [ segmentbouwer ](/help/components/segmentation/segmentation-workflow/seg-build.md) tot stand te brengen.

Houd rekening met het volgende wanneer u snelle segmenten maakt:

* De snelle segmenten zijn slechts op het project van toepassing waar zij werden gecreeerd. Ze zijn niet beschikbaar in andere projecten en kunnen niet worden gedeeld met andere gebruikers.
* Er zijn maximaal drie regels toegestaan.
* Geneste containers of opeenvolgende regels worden niet ondersteund.


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Snelle segmenten ](https://video.tv.adobe.com/v/341466?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Een snel segment maken

Elke gebruiker in Anlysis Workspace kan een snel segment maken.

Een snel segment maken:

1. Kies een van de volgende methoden om het snelsegment te maken:

   * **Ad hoc (belemmering-en-daling):** Van het linkerspoor, sleep een component aan de sectie van de segmentdaling in de paneelkopbal.

     ![ laat vallen een segment in de dalingsstreek ](assets/segment-dropzone.png)

     U kunt het segment uitgeven zoals die in [ wordt beschreven geeft snelle segmenten ](#edit-quick-segments) uit.

     >[!NOTE]
     >
     > Houd rekening met het volgende wanneer u een snel segment ad hoc maakt (slepen en neerzetten):
     > * De volgende componenttypen worden niet ondersteund: berekende metriek en dimensies, evenals metriek waaruit u geen segmenten kunt bouwen.
     > * Voor volledige afmetingen en gebeurtenissen maakt Analysis Workspace &#39;bestaande&#39; raaksegmenten. Voorbeelden: `Hit where eVar1 exists` of `Hit where event1 exists` .
     > * Als &quot;niet gespecificeerd&quot;of &quot;niets&quot;in de sectie van de segmentdaling wordt gelaten vallen, wordt het automatisch omgezet in een &quot;bestaat niet&quot;segment zodat het correct in segmenten wordt behandeld.


   * **Gebruikend het segmentpictogram:** in een lijst Freeform, selecteer het **pictogram van het Segment** in de paneelkopbal.

     ![ de filter van het Segment ](assets/quick-seg1.png)

1. Pas een van de volgende instellingen aan:

   | Instelling | Beschrijving |
   | --- | --- |
   | [!UICONTROL Name] | De standaardnaam van een segment is een combinatie van de regelnamen in het segment. U kunt de naam van het segment wijzigen in een vriendelijkere naam. |
   | [!UICONTROL Include/exclude] | U kunt of componenten in uw segmentdefinitie omvatten of uitsluiten, maar niet allebei. |
   | [!UICONTROL Hit/Visit/Visitor] container | De snelle segmenten omvatten één [ segmentcontainer ](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=nl-NL#section_AF2A28BE92474DB386AE85743C71B2D6) slechts die u een afmeting/metrische/datumwaaier in (of het van) het segment uitsluiten laat omvatten. [!UICONTROL Visitor] bevat overkoepelende gegevens die specifiek zijn voor de bezoeker in verschillende bezoeken en paginaweergaven. Met een [!UICONTROL Visit] -container kunt u regels instellen om de gegevens van de bezoeker op basis van bezoeken af te splitsen. Met een [!UICONTROL Hit] -container kunt u bezoekersinformatie afsplitsen op basis van afzonderlijke paginaweergaven. De standaardcontainer is [!UICONTROL Hit] . |
   | [!UICONTROL Components] (Dimension/metrisch/datumbereik) | Definieer maximaal 3 regels door componenten (afmetingen, metriek, datumbereiken of afmetingswaarden) toe te voegen. Er zijn drie manieren om de juiste component te vinden:<ul><li>Begin typend en de snelle segmentbouwer vindt automatisch de aangewezen component.</li><li>Gebruik de vervolgkeuzelijst om de component te zoeken.</li><li>Sleep componenten vanuit de linkerspoorstaaf.</li></ul> |
   | [!UICONTROL Operator] | Gebruik het vervolgkeuzemenu om standaardoperatoren en [!UICONTROL Distinct Count] -operatoren te zoeken. Zie [ exploitanten van het Segment ](/help/components/segmentation/seg-reference/seg-operators.md). |
   | plusteken (+) | Een andere regel toevoegen |
   | EN/OF kwalificatietekens | U kunt &quot;EN&quot;of &quot;OF&quot;bepalende eigenschappen aan de regels toevoegen, maar u kunt &quot;EN&quot;en &quot;OF&quot;in één enkele segmentdefinitie niet mengen. |
   | [!UICONTROL Apply] | Pas dit segment toe op het deelvenster. Als het segment geen gegevens bevat, wordt u gevraagd of u wilt doorgaan. |
   | [!UICONTROL Open builder] | Opent de Segment Builder. Nadat u sparen of het segment in de Bouwer van het Segment toepast, wordt het niet meer beschouwd als een &quot;snel segment&quot;. Het wordt deel van de component-lijst segmentbibliotheek. <p>Om de component beschikbaar te maken over al uw projecten en in het linkerspoor, selecteer de optie [!UICONTROL **maak dit segment beschikbaar aan al uw projecten en voeg het aan uw componentenlijst**] toe.</p><p>Voor meer informatie, zie de sectie [ sparen een snel segment als component-lijst segment ](#save-a-quick-segment-as-a-component-list-segment) in dit artikel.</p><p>**Nota:** slechts kunnen de gebruikers met de toestemming van de Aanmaak van het Segment in [ Adobe Admin Console ](/help/admin/admin-console/permissions/analytics-tools.md) de Bouwer van het Segment openen.</p> |
   | [!UICONTROL Cancel] | Annuleer dit snelle segment (pas het niet toe). |
   | [!UICONTROL Date range] | De validator gebruikt het datumbereik van het deelvenster voor het opzoeken van de gegevens. Maar elk datumbereik dat in een snel segment wordt toegepast, overschrijft het datumbereik van het deelvenster boven in het deelvenster. |
   | Voorvertoning (rechtsboven) | Hiermee kunt u zien of u een geldig segment hebt en hoe breed het segment is. Geeft de uitsplitsing aan van de gegevensset die u kunt verwachten wanneer u dit segment toepast. U zou een bericht kunnen krijgen dat erop wijst dat dit segment geen gegevens heeft. In dit geval kunt u doorgaan of de segmentdefinitie wijzigen. |

1. Selecteer [!UICONTROL **toepassen**] om uw veranderingen te bewaren.

## Snel segmenten bewerken

1. Beweeg over het snelle segment en selecteer **uitgeven** pictogram.

   ![ geef ad hoc filter ](assets/filter-adhoc-edit.png) uit

1. Bewerk de segmentdefinitie en/of de segmentnaam.

1. Selecteer [!UICONTROL **toepassen**].

## Snel segmenten opslaan als een segment met een lijst met componenten

>[!IMPORTANT]
>
> Houd rekening met het volgende wanneer u een snel segment opslaat:
> 
> * Om een snel segment te bewaren, hebt u de toestemming van de Aanmaak van het Segment in [ Adobe Admin Console ](/help/admin/admin-console/permissions/analytics-tools.md) nodig.
> 
> * Nadat u sparen of het segment toepast, kan het niet meer in de snelle segmentbouwer worden uitgegeven. In plaats daarvan moet u de gewone Segment Builder gebruiken.

U kunt snelle segmenten opslaan als een lijst met componenten. De voordelen van component-lijst segmenten omvatten:

* Beschikbaarheid voor al uw Workspace-projecten
* Ondersteuning voor meer complexe segmenten en opeenvolgende segmenten

U kunt segmenten opslaan vanuit de functie Snel segment maken of vanuit [!UICONTROL Filter Builder] .

### Opslaan in de functie Snel segment maken {#save2}

1. Nadat u het snelle segment hebt toegepast, houdt u de muisaanwijzer boven het segment en selecteert u het pictogram Info (&quot;i&quot;).
1. Selecteer **[!UICONTROL Make available to all projects and add to your component list]** .
1. (Optioneel) Wijzig de naam van het segment.
1. Selecteer **[!UICONTROL Save]** .

   Het segment wordt nu weergegeven in de lijst met componenten in de linkertrack. Let er ook op dat de zijbalk van het segment verandert van lichtblauw in donkerder blauw, wat aangeeft dat het segment niet langer kan worden bewerkt of geopend in de snelle segmentbuilder.

### Opslaan in de Segment Builder {#save3}

1. Nadat u het snelle segment hebt toegepast, houdt u de muisaanwijzer boven het segment en selecteert u het pictogram Info (&quot;i&quot;).
1. Selecteren **[!UICONTROL Save segment]**
1. (Facultatief) noem het segment anders, dan uitgezocht [!UICONTROL **ben**] van toepassing.

   Ga terug naar Workspace en merk op dat de zijbalk van het segment verandert van lichtblauw in donkerder blauw om aan te geven dat deze niet langer kan worden bewerkt of geopend in de functie Snel segment maken. En door het op te slaan, wordt het onderdeel van de componentenlijst.

Nadat u het segment toepast, kunt u verkiezen om het aan uw lijst van de segmentcomponent toe te voegen en het ter beschikking te stellen van al uw projecten.

1. Houd de cursor boven het opgeslagen segment en selecteer het potloodpictogram.

1. Selecteer [!UICONTROL **Open bouwer**].

1. Bij de bovenkant van de Bouwer van het Segment, zie de [!UICONTROL **project-slechts segment**] dialoog:

   ![ project-slechts segmentdialoog ](assets/project-only-segment-dialog.png)

1. Selecteren naast **[!UICONTROL Make available to all your projects and add to your component list.]**

1. Selecteer **[!UICONTROL Save]** .

   Het segment verschijnt nu in uw lijst van de segmentcomponent voor al uw projecten.
U kunt het segment [&#128279;](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html?lang=nl-NL#concept_4A9726927E7C44AFA260E2BB2721AFC6) met andere mensen in uw organisatie ook  delen.

## Voorbeeld van snel segment

In het volgende voorbeeld van een segment worden afmetingen en metriek gecombineerd:

![](assets/quick-seg2.png)

## Bekend probleem

1. Maak een snel segment met 2 items en **[!UICONTROL Save]** dit segment als Test1.
1. Klik op **[!UICONTROL Save as]** en sla dit snelle segment op als Test2.
1. Bewerk het snelle segment Test2 en sla het opnieuw op als Test2.
Bericht dat het Test1 snelle segment door Test2 wordt gewijzigd.
