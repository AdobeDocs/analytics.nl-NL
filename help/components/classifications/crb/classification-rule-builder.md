---
description: In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.
subtopic: Classifications
title: Workflow van de Builder voor classificatieregels
feature: Admin Tools
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
exl-id: cdb20dcc-0635-4d5e-9c54-f102d17a0a3d
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 2%

---

# Workflow van de Builder voor classificatieregels

In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.

## Belangrijke kennisgeving voordat je aan de slag gaat

Houd dit in gedachten voordat u classificatieregels gaat gebruiken:

* Subclassificaties worden niet ondersteund met Classification Rule Builder (CRB).
* Ons huidige classificatiesysteem kan slechts 10 miljoen rijen tegelijk exporteren.
* Wanneer CRB om uitvoer verzoekt, trekt het zowel geclassificeerde ALS niet-geclassificeerde waarden, met niet-gerubriceerde waarden door aan het eind van de uitvoer. Dit betekent dat je in de loop der tijd 10 miljoen geclassificeerde waarden zou kunnen opvullen - zonder ooit de ongeclassificeerde waarden te krijgen.
* Omdat de architectuur op een manier wordt opgezet die CRB van &quot;n&quot;aantal servers zou kunnen trekken, kan dit tot inconsistenties leiden wat betreft welke servers worden opgepikt en in welke orde. Daarom is het heel moeilijk om niet-geclassificeerde waarden te krijgen.

Dit is de **tijdelijke oplossing** voor diegenen die meer dan 10 miljoen geclassificeerde waarden voor een dimensie hebben: U moet niet-geclassificeerde waarden exporteren via FTP, in 10 miljoen batches en ze handmatig classificeren.

## Aan de slag met classificatieregels {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Hier volgen de stappen op hoog niveau die u onderneemt om classificatieregels toe te passen:

| Stap | Waar uitgevoerd | Beschrijving |
|--- |--- |--- |
| Stap 1 (Vereiste): [Stel uw classificatieschema](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) in. | [!UICONTROL Admin] >  [!UICONTROL Report Suites] >  [!UICONTROL Edit Settings] >  &lt;traffic Classifications=&quot;&quot; or=&quot;&quot; Conversion=&quot;&quot; Classifications=&quot;&quot;> | Kies een variabele en definieer de classificaties die u voor die variabele wilt gebruiken. <br>Variabelen moeten ten minste één indelingskolom hebben voordat ze in regels kunnen worden gebruikt.<br>Zodra classificaties worden toegelaten, kunt u de importeur en de regelbouwer gebruiken om specifieke waarden te classificeren. |
| Stap 2: [Maak een regelset](/help/components/classifications/crb/classification-rule-set.md). | [!UICONTROL Admin] >  [!UICONTROL Classification Rule Builder] > [!UICONTROL Add Rule Set] | Een regelset is een groep classificatieregels voor een specifieke variabele. |
| Stap 3: Configureer rapportsuites en -variabelen. | [!UICONTROL Classification Rule Builder] >   &lt;your rule=&quot;&quot; set=&quot;&quot;> | Pas de regel toe die wordt ingesteld om reeksen en variabelen te rapporteren. |
| Stap 4: [Classificatieregels toevoegen aan de set](/help/components/classifications/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] >   &lt;your rule=&quot;&quot; set=&quot;&quot;> | Pas een voorwaarde aan een classificatie aan, en dan specificerend de actie voor de regel te nemen.  Ben vertrouwd met de informatie in [Hoe de Regels worden verwerkt](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Stap 5: [Een classificatieregel testen](/help/components/classifications/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | U zult regels voor bevestiging willen testen door hen op de wijze van het Ontwerp uit te geven. In de conceptmodus kunnen regels niet worden uitgevoerd.<br>Deze stap is belangrijk bij het gebruik van  [reguliere expressies](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Stap 6: [Voer geldige regels in](/help/components/classifications/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Zodra de regels geldig zijn, activeer de regelreeks.  Indien nodig kunt u bestaande toetsen overschrijven. Zie [Hoe worden de regels verwerkt](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Stap 7 (optioneel): [Ongewenste regels verwijderen](/help/components/classifications/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Verwijder ongewenste regels uit een set.<br>Opmerking: Als u regels verwijdert, worden geüploade gerubriceerde gegevens niet verwijderd.  Zie [Classificatiegegevens verwijderen](/help/components/classifications/importer/t-delete-classification-data.md) als u geclassificeerde gegevens moet verwijderen. |

>[!NOTE]
>
>Groepen met machtigingen om het indelingsimportgereedschap te gebruiken, kunnen classificatieregels gebruiken. Zie [Hoe worden de Regels verwerkt](/help/components/classifications/crb/classification-quickstart-rules.md) voor belangrijke verwerkingsinformatie.

**Aanvullende resources**

**Blog**: Zie het blog Digital Marketing voor meer informatie over deze functie:  [Op regels gebaseerde classificaties](https://theblog.adobe.com/rule-based-classifications-part-1-making-classifications-easier/).

**Video**: Bekijk de video  [Classificaties ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/classifications/overview-of-classifications.html) Oververzien.
