---
description: Activity Map houdt verbindingen met een robuuster algoritme bij dat
title: Robuuste link tracking
uuid: a72b1652-2e69-41c7-8cf2-d39e9c705302
feature: Activity Map
role: User, Admin
exl-id: 1f077234-ff88-46ce-a931-2d21d68042b0
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 2%

---

# Robuuste link tracking

Activity Map houdt verbindingen met een robuuster algoritme bij dat:

* Bevat het bijhouden van paginagebieden om te voorkomen dat dezelfde koppeling op verschillende apparaten wordt verward, omdat de koppeling op verschillende posities op de pagina wordt weergegeven.
* Verzekert verbindingsuniciteit, die betekent dat de verschillende verbindingen niet voor één wegens kwesties met LinkID of over verschillende browser kunnen worden verward maakt.

Ga voor meer informatie over het bijhouden van koppelingen in de Activity Map naar [hier](/help/analyze/activity-map/activitymap-link-tracking/activitymap-link-tracking-methodology.md).

## Hoe Activity Map link tracking PII-gegevens kan verzamelen {#section_AEE57510D17B4C21A7D49D32D21D67B9}

>[!CAUTION]
>
>Door het bijhouden van Activity Mappen in te schakelen, verzamelt u mogelijk PII-gegevens (Persoonlijk identificeerbare gegevens). Deze gegevens kunnen op zichzelf of met andere informatie worden gebruikt om één persoon te identificeren, contact op te nemen of te vinden, of om een persoon in context te identificeren.

Hier zijn enkele bekende gevallen waarin PII-gegevens kunnen worden verzameld met behulp van Activity Map bijhouden:

* `Mailto` koppelingen. Een mailto-koppeling is een type HTML-koppeling waarmee de standaardmailclient op de computer wordt geactiveerd voor het verzenden van een e-mail.
* `User ID` koppelingen die worden weergegeven in de kop- of voettekst van een website nadat de gebruiker zich heeft aangemeld.
* Voor financiële instellingen kan het rekeningnummer als link worden weergegeven. Als u erop klikt, wordt de tekst van de koppeling verzameld.
* Op websites voor gezondheidszorg kunnen ook PII-gegevens als koppelingen worden weergegeven. Als u op deze koppelingen klikt, wordt de tekst van de koppeling verzameld en worden er dus PII-gegevens verzameld.
