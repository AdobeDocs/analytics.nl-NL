---
description: De rijinstellingen variëren afhankelijk van de component die u naar de tabel hebt gesleept.
title: Rij-instellingen
uuid: f30c31d5-1fd4-4b93-94c3-ca441099fe2e
feature: Vrije-vormtabellen
role: User, Admin
exl-id: 9057e930-b4c6-439e-b82a-8ab9828de91d
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '392'
ht-degree: 2%

---

# Rij-instellingen

De rijinstellingen variëren afhankelijk van de component die u naar de tabel hebt gesleept. Als u de tabelrijinstellingen wilt openen, klikt u op het pictogram Instellingen naast een dimensie, segment, metrisch, tijdsperiode of een verdeling binnen elk van deze instellingen:

![](assets/row-settings.png)

| Instelling | Beschrijving |
|--- |--- |
| Datums uitlijnen | Dit is een instelling op tabelniveau waarmee de datums van elke kolom worden uitgelijnd op alle datums die op dezelfde rij beginnen. Uitlijnen op datum wordt standaard ingeschakeld wanneer een tijddimensie wordt gebruikt in de rijen van de tabel en verschillende datumbereiken worden toegepast in de kolommen. In een dagelijkse tabel waarin oktober en september op de kolommen worden toegepast, begint de linkerkolom bijvoorbeeld met 1 oktober en begint de rechterkolom met 1 september. |
| Uitsplitsing naar positie | Deze instelling is standaard uitgeschakeld en de onderverdelingen zijn gekoppeld aan statische rijitems. Bijvoorbeeld, laten wij zeggen u de hoogste 3 pagina afmetingspunten (Homepage, Resultaten van het Onderzoek, Afhandeling) door het Kanaal van de Marketing. Dan verlaat u het project en keert twee weken later terug. Nadat u het project opnieuw hebt geopend, zijn de bovenste drie pagina&#39;s gewijzigd. In plaats daarvan zijn Homepage, Zoekresultaten en Afhandeling de bovenste 4-6 pagina&#39;s. Standaard worden uw uitsplitsingen naar marketingkanaal nog steeds weergegeven onder Homepage, Zoekresultaten en Afhandeling, ook al staan deze nu in de rijen 4-6. <br> Daarentegen worden de  **bovenste drie posten altijd uitgesplitst naar** positie, ongeacht wat ze zijn. Als u terugverwijst naar ons voorbeeld, worden de uitsplitsingen van het marketingkanaal gekoppeld aan de bovenste drie pagina&#39;s van de tabel, niet aan Homepage, Zoekresultaten en Afhandeling, die nu in de rijen 4-6 staan. |
| Percentage | **Hiermee berekent u percentages op basis van de standaardinstelling** ; de in een kolom zichtbare percentages worden berekend op basis van het totale aantal kolommen. <br>**Bereken percentages door de tabel Freeform te** rowforeren om de celpercentages over de rij te berekenen in plaats van de celpercentages omlaag in de kolom, met Eindtotaal als noemer. Dit is vooral handig voor het trenderen van percentages. Deze instelling is standaard ingeschakeld wanneer u het pictogram Visualiseren gebruikt. |
| Kolomtotalen | Deze instellingen zijn alleen beschikbaar voor [statische rijen](manual-vs-dynamic-rows.md). <br> **Als som van de huidige rijen** wordt een som van de rijen in de tabel aan de clientzijde weergegeven. Dit betekent dat het totaal  ** niet-gedupliceerde cijfers zoals bezoeken of bezoekers bevat.  <br> **Toon het grote** totaliteit toont een server-zijsom wat betekent het totaal zal duplo metriek. |
