---
title: Einde van de levensduur voor volledige gegevensbronnen
description: Meer informatie over de aankondiging aan het einde van de levensduur voor volledige gegevensverwerkingsbronnen.
exl-id: 7dd6d518-156f-4bf5-86cb-04d0acc8ff0c
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# Einde van de levensduur voor volledige gegevensbronnen

Volledige gegevensbronnen voor verwerking hebben organisaties er historisch toe gebracht gegevens op raakniveau naar Adobe Analytics te verzenden. Deze gegevens werden op dezelfde manier verwerkt als gegevens die via traditionele gegevensverzamelingsmethoden, zoals AppMeasurement, werden verzameld. In 2020 heeft Adobe de [Opsommings-API voor gegevens](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/), die dezelfde functies uitvoert als volledige gegevensbronnen voor verwerking, maar met extra functies. Deze pagina bevat informatie over extra functionaliteit die wordt geboden door de API voor het invoegen van gegevens in bulk en schetst verschillen in bestandsindelingen.

Op 25 maart 2021 heeft Adobe verhinderd dat er nieuwe volledige verbindingen voor gegevensbronnen voor verwerking werden gecreëerd. Op 31 januari 2022 zijn alle volledige verwerkingsdatadiensten gedeactiveerd.

## Belangrijkste verschillen tussen volledige gegevensbronnen voor verwerking en de API voor het invoegen van gegevens in bulk

* Met het invoegen van bulkgegevens kunt u meerdere bestanden verzenden voor parallelle verwerking. Bezoekersgroepen zorgen voor continuïteit van de bezoeker en toewijzing van eVar.
* De toevoeging van bulkgegevens heeft de mogelijkheden van de gegevensbevestiging en fout behandeling, die sommige administratieve werk verwijderen van het voorleggen van klapgegevens.
* Het opnemen van bulkgegevens ondersteunt meerdere ID-identificatiemethoden voor bezoekers.
* De toevoeging van bulkgegevens heeft een aantal aanvullende vereiste velden: een kolom met de identificatie van de bezoeker, een `pageName` (of koppelingsequivalent), `reportSuiteID`, `timestamp`, en `userAgent`.
* Voor continuïteit en attributie van bezoekers moeten rijen in bestanden in chronologische volgorde worden gesorteerd wanneer gegevens in een bulk worden ingevoegd. Zie [Bezoekersgroepen](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/visitor-groups/) voor meer informatie over de volgorde van bezoekersactiviteiten in verschillende bestanden.
* Voor het invoegen van bulkgegevens moeten bestanden .csv gecomprimeerd zijn in .gzip-indeling.
* BDIA gebruikt `timestamp` in plaats van `date`.

## Variabele vergelijking tussen BDIA en volledige verwerkingsgegevensbronnen

De volgende variabelen werden geïntroduceerd in Bulk gegevens toevoegend, eerder niet beschikbaar in volledige verwerkingsgegevensbronnen:

* **`aamlh`**: Adobe Audience Manager-locatiehint.
* **`contextData.key`**: [Contextgegevensvariabelen](/help/implement/vars/page-vars/contextdata.md).
* **`customerID`**: Experience Cloud ID service variables. Inclusief `id`, `authState` en `isMCSeed`.
* **`hints`**: [Clienttip](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html) variabelen. Inclusief `bitness`, `brands`, `mobile`, `model`, `platform`, `platformversion`, en `wow64`.
* **`ipaddress`**: IP van de bezoeker adres.
* **`language`**: De [Taal](/help/components/dimensions/language.md) dimensie.
* **`list1`** - **`list3`**: [Lijstvariabelen](/help/implement/vars/page-vars/list.md).
* **`marketingCloudVisitorID`**: De Experience Cloud-id van de bezoeker.
* **`tnta`**: Doelgegevensuitkering gebruikt in [Analyses voor doel](https://experienceleague.adobe.com/docs/target/using/integrate/a4t/a4t.html) integratie.
* **`trackingServer`**: De [`trackingServer`](/help/implement/vars/config-vars/trackingserver.md) variabele.
* **`transactionID`**: De [`transactionID`](/help/implement/vars/page-vars/transactionid.md) variabele.
* **`userAgent`**: De userAgent-tekenreeks van het apparaat.

De volgende variabelen worden niet ondersteund door Bulk-gegevensinvoeging:

* **`charSet`**: De [`charSet`](/help/implement/vars/config-vars/charset.md) variabele. Bulkgegevensinvoeging ondersteunt alleen UTF-8.
* **`timezone`**: De tijdzone van de bezoeker wordt in uren verschoven van GMT.
* **`clickAction`**, **`clickActionType`**, **`clickContext`**, **`clickContextType`**, **`clickSourceID`**, **`clickTag`**: Variabelen die worden gebruikt in gegevensverzameling voor Activity Mappen.
