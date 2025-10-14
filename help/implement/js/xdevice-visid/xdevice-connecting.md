---
description: De identificatie van bezoekers tussen apparaten helpt u bezoekers over veelvoudige apparaten aan te sluiten.
keywords: Analyseimplementatie
subtopic: Visitors
title: Gebruikers op verschillende apparaten verbinden
feature: Implementation Basics
exl-id: dfe278db-01de-4bba-b07a-66d52de1dbe2
role: Developer
source-git-commit: e242276f931e9939081b948a9d9ef8a087e16461
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 0%

---

# Gebruikers op verschillende apparaten verbinden

>[!IMPORTANT]
>
>Deze methode voor het identificeren van bezoekers op verschillende apparaten wordt niet langer aanbevolen. Zie [&#x200B; Analytics van het Apparaat &#x200B;](/help/components/cda/overview.md) in de de gebruikersgids van Componenten.

De identificatie van bezoekers tussen apparaten helpt u bezoekers over veelvoudige apparaten aan te sluiten. De identificatie van bezoekers tussen apparaten gebruikt de `visitorID` variabele om een gebruiker over apparaten te associëren. De variabele `visitorID` heeft de hoogste prioriteit bij het identificeren van unieke bezoekers.

Wanneer u een treffer verzendt met een aangepaste bezoeker-id, controleert Adobe of er bezoekersprofielen zijn die een overeenkomende bezoeker-id hebben. Als er al een bezoekersprofiel in het systeem aanwezig is, wordt dat profiel vanaf dat punt gebruikt en wordt het vorige bezoekersprofiel niet meer gebruikt.

Het instellen van de variabele `visitorID` wordt doorgaans ingesteld na verificatie of nadat een bezoeker een andere handeling uitvoert waarmee u deze onafhankelijk van het gebruikte apparaat kunt identificeren. Effectieve id&#39;s bevatten een hash van hun gebruikersnaam, e-mailadres of een interne id die geen persoonlijk identificeerbare informatie bevat.

Nadat de klant zich vanaf elk apparaat heeft aangemeld, zijn deze allemaal gekoppeld aan hetzelfde gebruikersprofiel. Als de bezoeker zich later afmeldt op een apparaat, blijven ze tot hetzelfde bezoekersprofiel behoren omdat Adobe herkent dat het browsercookie op elk apparaat tot hetzelfde bezoekersprofiel behoort. Adobe raadt u aan de variabele `visitorID` zo mogelijk te gebruiken als het browsercookie wordt verwijderd.

## Beperkingen

Het gebruik van uw eigen aangepaste bezoeker-id&#39;s geeft u meer controle over de manier waarop bezoekers worden geïdentificeerd, maar de beperkingen ervan zijn van toepassing.

* **deduplicatie van de bezoeker is niet retroactief**: Als een bezoeker tot uw plaats voor het eerst toegang heeft, dan voor authentiek verklaart, worden twee unieke bezoekers geteld. Één unieke bezoeker telt automatisch voor generische identiteitskaart van de Analyse, en een andere tellingen voor identiteitskaart van de douanebezoeker wanneer zij login. Dit dupliceren van unieke bezoekers wordt altijd getoond wanneer een bezoeker een nieuw apparaat gebruikt of zijn cookies wist.
* **Onverenigbaarheid met de Dienst van identiteitskaart van Experience Cloud**: Sinds de introductie van de identificatie van de dwars-apparatenbezoeker, heeft Adobe krachtigere en betrouwbaardere manieren vrijgegeven om bezoekers over apparaten te volgen. Deze nieuwe identificatiemethoden zijn niet compatibel met de overschrijving van de aangepaste bezoeker-id. Als u van plan bent om de Dienst van identiteitskaart of de Analytics van het Apparaat (CDA) te gebruiken, adviseert Adobe sterk tegen het gebruiken van de `visitorID` variabele.
