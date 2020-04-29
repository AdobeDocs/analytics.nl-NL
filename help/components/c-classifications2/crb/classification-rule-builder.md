---
description: In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.
subtopic: Classifications
title: Workflow van de opbouwfunctie voor classificatieregels
topic: Admin tools
uuid: edb1f07e-fa86-4055-8f4b-cce2d370edbb
translation-type: tm+mt
source-git-commit: 8d6685d241443798be46c19d70d8150d222ab9e8

---


# Workflow van de opbouwfunctie voor classificatieregels

In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.

## Belangrijke kennisgeving voordat je aan de slag gaat

Houd dit in gedachten voordat u classificatieregels gaat gebruiken:

* Subclassificaties worden niet ondersteund met Classification Rule Builder (CRB).
* Ons huidige classificatiesysteem kan slechts 10 miljoen rijen tegelijk exporteren.
* Wanneer CRB om uitvoer verzoekt, trekt het zowel geclassificeerde ALS niet-geclassificeerde waarden, met niet-gerubriceerde waarden door aan het eind van de uitvoer. Dit betekent dat je in de loop der tijd 10 miljoen geclassificeerde waarden zou kunnen opvullen - zonder ooit de ongeclassificeerde waarden te krijgen.
* Omdat de architectuur op een manier wordt opgezet die CRB van &quot;n&quot;aantal servers zou kunnen trekken, kan dit tot inconsistenties leiden wat betreft welke servers worden opgepikt en in welke orde. Daarom is het heel moeilijk om niet-geclassificeerde waarden te krijgen.

Dit is de **oplossing** voor diegenen die meer dan 10 miljoen geclassificeerde waarden voor een dimensie hebben: U moet niet-geclassificeerde waarden exporteren via FTP, in 10 miljoen batches en ze handmatig classificeren.

## Aan de slag met classificatieregels {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Hier volgen de stappen op hoog niveau die u onderneemt om classificatieregels toe te passen:

| Stap | Waar uitgevoerd | Beschrijving |
|--- |--- |--- |
| Stap 1 (Vereiste): [Stel het classificatieschema](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html)in. | [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Edit Settings] > &lt;Traffic Classifications or Conversion Classifications> | Kies een variabele en definieer de classificaties die u voor die variabele wilt gebruiken. <br>Variabelen moeten ten minste één indelingskolom hebben voordat ze in regels kunnen worden gebruikt.<br>Zodra classificaties worden toegelaten, kunt u de importeur en de regelbouwer gebruiken om specifieke waarden te classificeren. |
| Stap 2: [Maak een regelset](/help/components/c-classifications2/crb/classification-rule-set.md). | [!UICONTROL Admin] >  [!UICONTROL Classification Rule Builder] > [!UICONTROL Add Rule Set] | Een regelset is een groep classificatieregels voor een specifieke variabele. |
| Stap 3: Configureer rapportsuites en -variabelen. | [!UICONTROL Classification Rule Builder] > &lt;uw regelset> | Pas de regel toe die wordt ingesteld om reeksen en variabelen te rapporteren. |
| Stap 4: Classificatieregels [toevoegen aan de set](/help/components/c-classifications2/crb/classification-quickstart-rules.md). | [!UICONTROL Classification Rule Builder] > &lt;uw regelset> | Pas een voorwaarde aan een classificatie aan, en dan specificerend de actie voor de regel te nemen.  Ben vertrouwd met de informatie in [hoe de Regels worden verwerkt](/help/components/c-classifications2/crb/classification-quickstart-rules.md). |
| Stap 5: Een classificatieregel [testen](/help/components/c-classifications2/crb/classification-quickstart-rules.md) | [!DNL Testing Page] | U zult regels voor bevestiging willen testen door hen op de wijze van het Ontwerp uit te geven. In de conceptmodus kunnen regels niet worden uitgevoerd.<br>Deze stap is belangrijk bij het gebruik van [reguliere expressies](/help/components/c-classifications2/crb/classification-quickstart-rules.md). |
| Stap 6: [Activeer geldige regels](/help/components/c-classifications2/crb/classification-rule-definitions.md). | [!DNL Rules Page] | Zodra de regels geldig zijn, activeer de regelreeks.  Indien nodig kunt u bestaande toetsen overschrijven. Zie [Hoe regels worden verwerkt](/help/components/c-classifications2/crb/classification-quickstart-rules.md). |
| Stap 7 (optioneel): Ongewenste regels [](/help/components/c-classifications2/crb/classification-rule-definitions.md)verwijderen. | [!DNL Rules Page] | Verwijder ongewenste regels uit een set.<br>Opmerking:  Als u regels verwijdert, worden geüploade gerubriceerde gegevens niet verwijderd.  Zie Classificatiegegevens [](/help/components/c-classifications2/c-classifications-importer/t-delete-classification-data.md) verwijderen als u geclassificeerde gegevens moet verwijderen. |

>[!NOTE]
>
>Groepen met machtigingen om het indelingsimportgereedschap te gebruiken, kunnen classificatieregels gebruiken. Zie [hoe de Regels voor belangrijke verwerkingsinformatie worden verwerkt](/help/components/c-classifications2/crb/classification-quickstart-rules.md) .

**Aanvullende bronnen**

**Blog**: Zie het blog Digital Marketing voor meer informatie over deze functie: Op [regels gebaseerde classificaties](https://blogs.adobe.com/digitalmarketing/analytics/rule-based-classifications-part-1-making-classifications-easier/?utm_source=feedburner&amp;utm_medium=feed&amp;utm_campaign=Feed%3A+AdobeDigitalMarketing+%28Adobe+Digital+Marketing+Blog%29).

**Video**: Bezoek [YouTube](https://www.youtube.com/watch?v=6laI5SBXY-I) om de [!UICONTROL Classifications Overview] video te bekijken.
