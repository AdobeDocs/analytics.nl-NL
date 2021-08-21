---
title: Overzicht van plug-ins
description: Plak code op uw site om nieuwe functionaliteit te introduceren.
exl-id: faae7963-078d-40ad-ba09-71efa0b90df1
source-git-commit: ab078c5da7e0e38ab9f0f941b407cad0b42dd4d1
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 1%

---

# Overzicht van plug-ins

Plug-ins zijn codefragmenten die verschillende geavanceerde functies uitvoeren om uw analytische implementatie te helpen. Deze plug-ins breiden de mogelijkheden van uw JavaScript-bestand uit, zodat u meer functionaliteit krijgt die niet beschikbaar is bij een eenvoudige implementatie. Adobe biedt een aantal andere plug-ins als onderdeel van geavanceerde oplossingen.

>[!IMPORTANT]
>
>Plug-ins worden geleverd door Adobe Consulting als hoffelijkheid om u te helpen meer waarde uit Adobe Analytics te krijgen. De klantenservice van Adobe biedt geen ondersteuning voor deze plug-ins, waaronder installatie of probleemoplossing. Neem contact op met de accountmanager van uw organisatie als u hulp nodig hebt met een plug-in. Zij kunnen een vergadering voor hulp met een consultant organiseren.

Adobe biedt verschillende manieren om een bepaalde plug-in te installeren:

1. De extensie &#39;Common Analytics Plugins&#39; gebruiken met tags in Adobe Experience Platform
2. Plug-incode plakken met de aangepaste code-editor
3. Plak de insteekcode in het `AppMeasurement.js`-bestand

Elke organisatie heeft verschillende implementatiebehoeften, zodat u kunt besluiten hoe u hen in uw implementatie wilt omvatten. Zorg ervoor dat u aan de volgende criteria voldoet wanneer u de code op uw site opneemt:

1. Instantieer eerst het object Analytics tracking (met [`s_gi`](../functions/s-gi.md)).
   * Uw tag-ingeschakelde site instantieert automatisch het volgende object wanneer Adobe Analytics wordt geladen.
   * Implementaties met `AppMeasurement.js` initialiseren doorgaans het volgende object boven aan het JavaScript-bestand.
2. Neem tweede plug-incode op.
   * De extensie &#39;Algemene insteekmodules voor analyse&#39; heeft een actieconfiguratie waarmee u insteekmodules kunt initialiseren.
   * Als u de extensie niet wilt gebruiken, kunt u insteekcode in de aangepaste code-editor plakken tijdens het configureren van de extensie Analytics.
   * Als uw implementatie geen labels gebruikt in Adobe Experience Platform, kunt u insteekcode in `AppMeasurement.js` plakken nadat u het volgende object hebt geïnstantieerd.
3. Roep de plug-in derde.
   * In alle implementaties, zowel binnen als buiten een site waarvoor tags zijn ingeschakeld, wordt JavaScript gebruikt om insteekmodules aan te roepen. Roep de plug-in aan de hand van de indeling die op de pagina van die plug-in wordt beschreven.
4. Valideer uw implementatie en publiceer.

Veel organisaties roepen insteekmodules aan met behulp van de functie [`doPlugins`](../functions/doplugins.md). Hoewel deze functie niet vereist is, beschouwt Adobe het als een goede praktijk om te gebruiken. AppMeasurement roept deze functie vlak voordat een afbeeldingsverzoek wordt gecompileerd en verzonden. Dit is ideaal omdat verschillende plug-ins afhankelijk zijn van andere analytische variabelen.
