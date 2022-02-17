---
description: In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.
title: Workflow van de Builder voor classificatieregels
feature: Classifications
exl-id: cdb20dcc-0635-4d5e-9c54-f102d17a0a3d
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# Workflow van de Builder voor classificatieregels

In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.

Hier volgt een video-overzicht van de Classification Rule Builder:

>[!VIDEO](https://video.tv.adobe.com/v/25884/?quality=12)

## Belangrijke kennisgeving voordat je aan de slag gaat

Houd dit in gedachten voordat u classificatieregels gaat gebruiken:

* Subclassificaties worden niet ondersteund met Classification Rule Builder (CRB).
* Ons huidige classificatiesysteem kan slechts 10 miljoen rijen tegelijk exporteren.
* Wanneer CRB om uitvoer verzoekt, trekt het zowel geclassificeerde ALS niet-geclassificeerde waarden, met niet-gerubriceerde waarden door aan het eind van de uitvoer. Dit betekent dat je in de loop der tijd 10 miljoen geclassificeerde waarden zou kunnen opvullen - zonder ooit de ongeclassificeerde waarden te krijgen.
* Omdat de architectuur op een manier wordt opgezet die CRB van &quot;n&quot;aantal servers zou kunnen trekken, kan dit tot inconsistenties leiden wat betreft welke servers worden opgepikt en in welke orde. Daarom is het heel moeilijk om niet-geclassificeerde waarden te krijgen.

Dit is het **tijdelijke** voor diegenen die meer dan 10 miljoen geclassificeerde waarden voor een dimensie hebben: U moet niet-geclassificeerde waarden exporteren via FTP, in 10 miljoen batches en ze handmatig classificeren.

## Aan de slag met classificatieregels {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Hier volgen de stappen op hoog niveau die u onderneemt om classificatieregels toe te passen:

| Stap | Waar uitgevoerd | Beschrijving |
|--- |--- |--- |
| Stap 1 (Vereiste): [Uw classificatieschema instellen](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html). | [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Edit Settings] > &lt;traffic classifications=&quot;&quot; or=&quot;&quot; conversion=&quot;&quot; classifications=&quot;&quot;> | Kies een variabele en definieer de classificaties die u voor die variabele wilt gebruiken. <br>Variabelen moeten ten minste één indelingskolom hebben voordat ze in regels kunnen worden gebruikt.<br>Zodra classificaties worden toegelaten, kunt u de importeur en de regelbouwer gebruiken om specifieke waarden te classificeren. |
| Stap 2: [Een regelset maken](/help/components/classifications/crb/classification-rule-set.md). | [!UICONTROL Admin] >  [!UICONTROL Classification Rule Builder] > [!UICONTROL Add Rule Set] | Een regelset is een groep classificatieregels voor een specifieke variabele. |
| Stap 3: Configureer rapportsuites en -variabelen. | [!UICONTROL Classification Rule Builder] >  &lt;your rule=&quot;&quot; set=&quot;&quot;> | Pas de regel toe die wordt ingesteld om reeksen en variabelen te rapporteren. |
| Stap 4: [Classificatieregels toevoegen aan de set](/help/components/classifications/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] >  &lt;your rule=&quot;&quot; set=&quot;&quot;> | Pas een voorwaarde aan een classificatie aan, en dan specificerend de actie voor de regel te nemen.  Wees vertrouwd met de informatie in  [Hoe regels worden verwerkt](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Stap 5: [Een set classificatieregel testen](/help/components/classifications/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | U zult regels voor bevestiging willen testen door hen op de wijze van het Ontwerp uit te geven. In de conceptmodus kunnen regels niet worden uitgevoerd.<br>Deze stap is belangrijk bij het gebruik [reguliere expressies](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Stap 6: [Geldige regels activeren](/help/components/classifications/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Zodra de regels geldig zijn, activeer de regelreeks.  Indien nodig kunt u bestaande toetsen overschrijven. Zie [Hoe regels worden verwerkt](/help/components/classifications/crb/classification-quickstart-rules.md). |
| Stap 7 (optioneel): [Ongewenste regels verwijderen](/help/components/classifications/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Verwijder ongewenste regels uit een set.<br>Opmerking: Als u regels verwijdert, worden geüploade gerubriceerde gegevens niet verwijderd.  Zie  [Classificatiegegevens verwijderen](/help/components/classifications/importer/t-delete-classification-data.md) als u gerubriceerde gegevens moet verwijderen. |

>[!NOTE]
>
>Groepen met machtigingen om het indelingsimportgereedschap te gebruiken, kunnen classificatieregels gebruiken. Zie [Hoe regels worden verwerkt](/help/components/classifications/crb/classification-quickstart-rules.md) voor belangrijke verwerkingsinformatie.

**Aanvullende resources**

**Blog**: Zie het blog Digital Marketing voor meer informatie over deze functie: [Op regels gebaseerde classificaties](https://theblog.adobe.com/rule-based-classifications-part-1-making-classifications-easier/).

**Video**: De weergave van [Overzicht van classificaties](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/classifications/overview-of-classifications.html) video.
