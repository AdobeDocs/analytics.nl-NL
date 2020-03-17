---
description: Hier volgen enkele gebruikelijke valkuilen bij gebruik van Report Builder met Power BI.
title: Probleemoplossing voor Power BI-integratie
uuid: c1e7e164-4bc6-4513-9332-92c53be021cc
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Probleemoplossing voor Power BI-integratie

Hier volgen enkele gebruikelijke valkuilen bij gebruik van Report Builder met Power BI.

## Stap 1. Publiceren naar Power BI mislukt {#section_5B87DC1C302C4FD8AB9E4DD6B162DC9B}

Geplande werkboeken waarvoor publicatie van Power BI vereist is, zijn afhankelijk van Power BI-services om aan de slag te kunnen gaan. Twee belangrijke redenen voor het niet publiceren zijn:

* Power BI-services zijn mogelijk uitgeschakeld.
* De gebruiker die het werkboek opende heeft niet meer geldige de rekeningsgeloofsbrieven van Microsoft.

Elke geplande taak van de Bouwer van het Rapport krijgt drie pogingen per geplande looppas:

* Na de eerste mislukte poging ontvangt u het volgende bericht: &quot;&quot;We konden dit geplande werkboek niet publiceren naar Microsoft Power BI. We proberen het binnenkort opnieuw.&quot;
* Na de tweede mislukte poging krijg je geen bericht meer.
* Na de derde mislukte poging ontvangt u het volgende bericht: &quot;We konden dit werkboek niet publiceren naar Power BI.&quot;

## Stap 2. Gebroken visualisaties in Power BI {#section_FFFE200D06F843B2AF093710FD678166}

Hier zijn de hoogste redenen waarom u met gebroken visualisaties na het publiceren van de verzoeken van de Bouwer van het Rapport aan Power BI kon eindigen:

* U hebt een verzoek bewerkt in Report Builder, zoals het wijzigen van metriek of afmetingen, en vervolgens opnieuw gepubliceerd naar Power BI. Door aanvragen te bewerken kunnen uw visualisaties worden verbroken.
* U hebt een aanvraag verwijderd die in een visualisatie is gebruikt.

