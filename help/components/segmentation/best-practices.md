---
title: Beste werkwijzen voor segmentering
description: Maak optimale segmenten die gegevens efficiënt retourneren.
feature: Segmentation
exl-id: 4115a804-5063-430a-b9d3-2b64b26ca4d8
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Beste werkwijzen voor segmentering

De complexe segmenten zijn vaak noodzakelijk om gewenste gegevens te verkrijgen. Als complexe segmenten inefficiënt zijn en in een grote rapportsuite worden gebruikt, duurt het aanzienlijk langer om rapporten uit te voeren. Houd rekening met de volgende bronnen wanneer u een segment maakt of bewerkt om de complexiteit te minimaliseren.

## Gebruik de operator &#39;Bevat&#39; alleen als laatste redmiddel

De operator &#39;Bevat&#39; is een van de meest verwerkingsintensieve onderdelen die worden gesegmenteerd, omdat de gehele inhoud van elke waarde moet worden geanalyseerd. U kunt ook andere operatoren gebruiken, zoals &#39;Begint met&#39; of &#39;Eindigt met&#39;, als de gewenste waarden zich aan het begin of einde van een tekenreeks bevinden.

Als &quot;bevat&quot;exploitant in een segment een groot aantal resultaten terugkeert, typisch tijden uit het rapport. Als u bijvoorbeeld een segment hebt gemaakt waarin `Referrer equals "."`, doorzoekt het segment de inhoud van elke waarde. Gebruik in plaats hiervan de operator &#39;Exists&#39;.

## Classificaties gebruiken voor items met groepsdimensies

Als u vele segmentvoorwaarden hebt, kunnen zij segmentprestaties snel degraderen. Bijvoorbeeld: `Page equals X or Page equals Y or Page equals Z` worden herhaald met honderden verschillende waarden. In plaats van deze honderden voorwaarden te schrijven, classificeer alle gewenste waarden in een segment, dan gebruik de geclassificeerde waarde in een segment.

1. Maak een classificatie voor de variabele waarmee u werkt.
2. Download het classificatiesjabloon en open het in het gewenste spreadsheet of de gewenste teksteditor.
3. Geef elk dimensie-item dat u in uw segment wilt opnemen dezelfde waarde.
4. De indelingimporter gebruiken om de spreadsheet weer in Adobe Analytics te importeren
5. Wanneer de classificatie klaar is met verwerken, maakt u een segment met de geclassificeerde waarde.

Deze methode verhoogt drastisch prestaties en verstrekt een gemakkelijke manier om segmentvoorwaarden te wijzigen. In plaats van het segment met verschillende waarden te bewerken, kunt u dimensie-items toevoegen aan of verwijderen uit de classificatie.
