---
description: In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.
title: Workflow van de opbouwfunctie voor classificatieregels
feature: Classifications
exl-id: cdb20dcc-0635-4d5e-9c54-f102d17a0a3d
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# Overzicht van de builder van de classificatieregel (verouderd)

{{classification-rulebuilder-deprecation}}

In plaats van elke keer dat uw volgcodes veranderen classificaties te onderhouden en te uploaden, kunt u automatische, op regels gebaseerde classificaties maken en deze op meerdere rapportsuites toepassen. Regels worden regelmatig verwerkt, afhankelijk van uw volume van aan classificatie gerelateerd verkeer.

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de regelbouwer van de Classificatie ](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/components/classifications/using-the-classification-rule-builder){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

## Belangrijke kennisgeving voordat je aan de slag gaat

Houd rekening met de volgende punten wanneer u classificatieregels gebruikt:

* U kunt maximaal 10 miljoen rijen tegelijk exporteren.
* Wanneer CRB om uitvoer verzoekt, trekt het zowel geclassificeerde ALS niet-geclassificeerde waarden, met niet-gerubriceerde waarden door aan het eind van de uitvoer. Dit betekent dat je in de loop der tijd 10 miljoen geclassificeerde waarden zou kunnen opvullen - zonder ooit de ongeclassificeerde waarden te krijgen.
* Omdat de architectuur op een manier wordt opgezet die CRB van &quot;n&quot;aantal servers zou kunnen trekken, kan dit tot inconsistenties leiden wat betreft welke servers worden opgepikt en in welke orde. Daarom is het heel moeilijk om niet-geclassificeerde waarden te krijgen.

Dit is de **alternerende actie** voor degenen die meer dan 10 miljoen geclassificeerde waarden voor een dimensie hebben: U zult ongeclassificeerde waarden via FTP, in 10 miljoen partijen moeten uitvoeren, en manueel hen classificeren.

## Aan de slag met classificatieregels {#section_3FF666EF9D5B4E37A23B3FB400CDA2E6}

**[!UICONTROL Admin]** > **[!UICONTROL Classification Rule Builder]**

Hier volgen de stappen op hoog niveau die u onderneemt om classificatieregels toe te passen:

| Stap | Waar uitgevoerd | Beschrijving |
|--- |--- |--- |
| Stap 1 (Vereiste): Opstelling uw classificatieschema. | [!UICONTROL Admin] > [!UICONTROL Report Suites] > [!UICONTROL Edit Settings] > [!UICONTROL Traffic Classifications] of [!UICONTROL Conversion Classifications] | Kies een variabele en definieer de classificaties die u voor die variabele wilt gebruiken. <br> de Variabelen moeten minstens één gecreeerde classificatiekolom hebben alvorens zij voor gebruik in regels beschikbaar zijn.<br> Zodra classificaties worden toegelaten, kunt u de importer en de regelbouwer gebruiken om specifieke waarden te classificeren. |
| Stap 2: [ creeer een regelreeks ](classification-rule-set.md). | [!UICONTROL Admin] > [!UICONTROL Classification Rule Builder] > [!UICONTROL Add Rule Set] | Een regelset is een groep classificatieregels voor een specifieke variabele. |
| Stap 3: Vorm rapportreeksen en variabelen. | [!UICONTROL Classification Rule Builder] > &lt;uw regelset> | Pas de regel toe die wordt ingesteld om reeksen en variabelen te rapporteren. |
| Stap 4: [ voeg classificatieregels aan de reeks ](classification-quickstart-rules.md) toe. | [!UICONTROL Classification Rule Builder] > &lt;uw regelset> | Pas een voorwaarde aan een classificatie aan, en dan specificerend de actie voor de regel te nemen.  Ben vertrouwd met de informatie in [ hoe de Regels ](classification-quickstart-rules.md) worden verwerkt. |
| Stap 5: [ test een Reeks van de Regel van de Classificatie ](classification-quickstart-rules.md) | [!DNL Testing Page] | U zult regels voor bevestiging willen testen door hen op de wijze van het Ontwerp uit te geven. In de conceptmodus kunnen regels niet worden uitgevoerd.<br> Deze stap is belangrijk wanneer het gebruiken van [ regelmatige uitdrukkingen ](classification-quickstart-rules.md). |
| Stap 6: [ activeer geldige regels ](classification-rule-definitions.md). | [!DNL Rules Page] | Zodra de regels geldig zijn, activeer de regelreeks.  Indien nodig kunt u bestaande toetsen overschrijven. Zie [ hoe de regels ](classification-quickstart-rules.md) worden verwerkt. |
| Stap 7 (Facultatief): [ schrap ongewenste regels ](classification-rule-definitions.md). | [!DNL Rules Page] | Verwijder ongewenste regels uit een set.<br> Nota: Het schrappen van regels schrapt geen geuploade gerubriceerde gegevens. Zie [ classificatiegegevens van de Schrapping ](/help/components/classifications/importer/t-delete-classification-data.md) als u gerubriceerde gegevens moet schrappen. |

>[!NOTE]
>
>Groepen met machtigingen om het indelingsimportgereedschap te gebruiken, kunnen classificatieregels gebruiken. Zie [ hoe de Regels ](classification-quickstart-rules.md) voor belangrijke verwerkingsinformatie worden verwerkt.

**Extra Middelen**

**Blog**: Voor extra informatie over deze eigenschap, zie het Digitale Marketing Blog: [ Op regel-gebaseerde Classificaties ](https://theblog.adobe.com/rule-based-classifications-part-1-making-classifications-easier/).

**Video**: Bekijk de [ video van het Overzicht van Classificaties ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/components/classifications/overview-of-classifications.html).

