---
description: Data Warehouse biedt een functie waarmee u een lijst met bezoekers-id's kunt ophalen. Deze id's zijn geen cookie-id's, maar id's die u vastlegt in een van uw conversievariabelen. Hoewel er andere manieren zijn om bij deze informatie te krijgen, is het volgende voorbeeld een kortere weg aan het produceren van een verzoek van het Pakhuis van Gegevens.
title: Hoofdletters gebruiken - Bezoeker-id's uitnemen
topic: Admin tools
uuid: ed228334-619c-43d7-b781-a18af73b00bb
translation-type: tm+mt
source-git-commit: ''

---


# Hoofdletters gebruiken - Bezoeker-id&#39;s uitnemen

Data Warehouse biedt een functie waarmee u een lijst met bezoekers-id&#39;s kunt ophalen. Deze id&#39;s zijn geen cookie-id&#39;s, maar id&#39;s die u vastlegt in een van uw conversievariabelen. Hoewel er andere manieren zijn om bij deze informatie te krijgen, is het volgende voorbeeld een kortere weg aan het produceren van een verzoek van het Pakhuis van Gegevens.

Bijvoorbeeld, veronderstel dat uw zaken marketing e-mail naar klanten en vooruitzichten verzendt. Elk van deze e-mailontvangers heeft een unieke id in uw e-mailsysteem (zoals *`EMAIL Contact ID`*). U stelt uw e-mails zo in dat wanneer contactpersonen een e-mail ontvangen en op een van de koppelingen klikken, de bezoeker op uw website aankomt met een campagne-id en een unieke E-MAIL-contactpersoon. Uw e-mailkoppeling kan bijvoorbeeld het volgende oplossen:

```js
https://www.test.com/?cid=springmailblast&mid=1363660158
```

Door deze in te stellen in conversievariabelen (eVars) kunt u zien hoe elke e-mail is uitgevoerd (via de campagne-id) en hoe vaak elke e-mailontvanger de site heeft bezocht (via de E-MAILcontact-id).

Stel dat u deze id&#39;s vastlegt. De meeste marketeers willen hun websitegedrag segmenteren en dan zien of kunnen zij aan hen opnieuw in de handel brengen die aan bepaalde criteria voldoen. U kunt bijvoorbeeld een e-mailbericht voor het opnieuw in de handel brengen verzenden naar alle e-mailontvangers die vanuit de e-mail naar uw site zijn gekomen en een websiteformulier hebben bekeken (of voltooid). Hiervoor zoekt u een manier om de e-MAILcontact-id&#39;s te identificeren van de personen die het specifieke formulier invullen.

Dit kunt u doen door een Subrelatierapport voor conversie te gebruiken om de eVar-waarde van de Formulier-id op te delen door de eVar E-MAIL-contactpersoon. Nochtans, is een pre-gebouwde eigenschap beschikbaar om dit te doen gebruikend het Pakhuis van Gegevens. Met deze functie kunt u zien welke eVar uw unieke gebruikers-id&#39;s opslaat (in dit geval E-MAIL-contact-id) en kunt u deze id&#39;s gemakkelijk extraheren met behulp van data-entrepot. Door deze eigenschap te gebruiken, kunt u een verzoek van het gegevenspakhuis automatisch tot stand brengen dat Unieke Bezoeker IDs trekt waarvoor u geinteresseerd bent.
