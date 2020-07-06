---
title: Overzicht van plug-ins
description: Plak code op uw site om nieuwe functionaliteit te introduceren.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 1%

---


# Overzicht van plug-ins

Plug-ins zijn codefragmenten die verschillende geavanceerde functies uitvoeren om uw Analytics-implementatie te ondersteunen. Deze plug-ins breiden de mogelijkheden van uw JavaScript-bestand uit, zodat u meer functionaliteit krijgt die niet beschikbaar is bij een eenvoudige implementatie. Adobe biedt een aantal andere plug-ins als onderdeel van geavanceerde oplossingen.

>[!IMPORTANT]
>
>Plug-ins worden door Adobe Consulting aangeboden als een hoffelijkheid om u te helpen meer waarde te krijgen in Adobe Analytics. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-ins, zoals de installatie of het oplossen van problemen. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met een plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Adobe biedt verschillende manieren om een bepaalde plug-in te installeren:

1. De extensie &#39;Algemene Analytics-plug-ins&#39; gebruiken met Adobe Experience Platform Launch
2. Code van insteekmodule plakken met de aangepaste code-editor van Launch
3. De insteekcode in het `AppMeasurement.js` bestand plakken

Elke organisatie heeft verschillende implementatiebehoeften, zodat u kunt besluiten hoe u hen in uw implementatie wilt omvatten. Zorg ervoor dat u aan de volgende criteria voldoet wanneer u de code op uw site opneemt:

1. Instantieer eerst het volgende object van Analytics (met [`s_gi`](../functions/s-gi.md)).
   * Start instantieert automatisch het volgende object wanneer Adobe Analytics wordt geladen.
   * Implementaties die gebruikmaken van `AppMeasurement.js` initialiseren doorgaans het volgende object boven aan het JavaScript-bestand.
2. Neem tweede plug-incode op.
   * De extensie &#39;Algemene Analytics-plug-ins&#39; heeft een actieconfiguratie waarmee u plug-ins kunt initialiseren.
   * Als u de insteekmodule niet wilt gebruiken, kunt u insteekcode in de aangepaste code-editor plakken wanneer u de Analytics-extensie configureert.
   * Als uw implementatie geen Launch gebruikt, kunt u insteekcode in `AppMeasurement.js` overal kleven nadat u het volgende voorwerp concretiseert.
3. Roep de plug-in derde.
   * Alle implementaties, zowel binnen als buiten Launch, gebruiken JavaScript om insteekmodules aan te roepen. Roep de plug-in aan de hand van de indeling die op de pagina van die plug-in wordt beschreven.
4. Valideer uw implementatie en publiceer.

Vele organisaties roepen stop-ins gebruikend de [`doPlugins`](../functions/doplugins.md) functie. Hoewel deze functie niet vereist is, beschouwt Adobe deze als een aanbevolen werkwijze. AppMeasurement roept deze functie vlak voordat een afbeeldingsverzoek wordt gecompileerd en verzonden. Dit is ideaal omdat verschillende plug-ins afhankelijk zijn van andere Analytics-variabelen.
