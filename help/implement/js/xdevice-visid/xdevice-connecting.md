---
description: De identificatie van bezoekers tussen apparaten helpt u bezoekers over veelvoudige apparaten aan te sluiten. De identificatie van bezoekers tussen apparaten gebruikt de variabele van bezoekersidentiteitskaart, s.bezoekerID, om een gebruiker over apparaten te associëren.
keywords: Analyseimplementatie
subtopic: Visitors
title: Gebruikers op verschillende apparaten verbinden
topic-fix: Developer and implementation
uuid: 6243957b-5cc1-49ef-aa94-5b5ec4eac313
exl-id: dfe278db-01de-4bba-b07a-66d52de1dbe2
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 0%

---

# Gebruikers op verschillende apparaten verbinden

>[!IMPORTANT]
>
>Deze methode voor het identificeren van bezoekers op verschillende apparaten wordt niet langer aanbevolen. Zie [Apparaatanalyse](/help/components/cda/overview.md) in de gebruikershandleiding voor componenten.

De identificatie van bezoekers tussen apparaten helpt u bezoekers over veelvoudige apparaten aan te sluiten. De identificatie van bezoekers tussen apparaten gebruikt de `visitorID` variabele om een gebruiker over apparaten te associëren. De variabele `visitorID` krijgt de hoogste prioriteit bij het identificeren van unieke bezoekers.

Wanneer u een treffer verzendt met een aangepaste bezoeker-id, controleert Adobe op alle bezoekersprofielen die een overeenkomende bezoeker-id hebben. Als er al een bezoekersprofiel in het systeem aanwezig is, wordt dat profiel vanaf dat punt gebruikt en wordt het vorige bezoekersprofiel niet meer gebruikt.

Het plaatsen van `visitorID` variabele wordt typisch geplaatst na authentificatie, of nadat een bezoeker één of andere andere actie uitvoert die u toestaat om hen onafhankelijk van het apparaat uniek te identificeren dat wordt gebruikt. Effectieve id&#39;s bevatten een hash van hun gebruikersnaam, e-mailadres of een interne id die geen persoonlijk identificeerbare informatie bevat.

Nadat de klant zich vanaf elk apparaat heeft aangemeld, zijn deze allemaal gekoppeld aan hetzelfde gebruikersprofiel. Als de bezoeker zich later afmeldt op een apparaat, blijven ze tot hetzelfde bezoekersprofiel behoren, omdat Adobe inziet dat het browsercookie op elk apparaat tot hetzelfde bezoekersprofiel behoort. Adobe raadt u aan de variabele `visitorID` te gebruiken als het browsercookie wordt verwijderd.

## Beperkingen

Het gebruik van uw eigen aangepaste bezoeker-id&#39;s geeft u meer controle over de manier waarop bezoekers worden geïdentificeerd, maar de beperkingen ervan zijn van toepassing.

* **Deduplicatie van bezoeker is niet retroactief**: Als een bezoeker voor het eerst toegang krijgt tot uw site en vervolgens wordt geverifieerd, worden twee unieke bezoekers geteld. Één unieke bezoeker telt automatisch voor generische identiteitskaart van de Analyse, en een andere tellingen voor identiteitskaart van de douanebezoeker wanneer zij login. Dit dupliceren van unieke bezoekers wordt altijd getoond wanneer een bezoeker een nieuw apparaat gebruikt of zijn cookies wist.
* **Incompatibiliteit met de Experience Cloud ID-service**: Sinds de introductie van de identificatie van bezoekers op verschillende apparaten heeft Adobe krachtigere en betrouwbaardere manieren beschikbaar gemaakt om bezoekers op verschillende apparaten te volgen. Deze nieuwe identificatiemethoden zijn niet compatibel met de overschrijving van de aangepaste bezoeker-id. Als u van plan bent om de Dienst van identiteitskaart, de Analytics van het Apparaat (CDA), of co-op van het Apparaat te gebruiken, adviseert Adobe sterk tegen het gebruiken van `visitorID` variabele.
