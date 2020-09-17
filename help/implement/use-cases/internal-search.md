---
title: Interne zoektermen vastleggen
description: Gebruik een aangepaste variabele om interne zoektermen vast te leggen.
translation-type: tm+mt
source-git-commit: a94b8e090b9a3c75a57fd396cac8486bba2e5d79
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---


# Interne zoektermen vastleggen

Interne zoekrapportage is een integraal onderdeel van veel organisaties en is geen kant-en-klare dimensie met Adobe Analytics. Maar met minimale implementatieinspanningen kan de interne rapportage op de zoekterm eenvoudig worden vastgelegd.

## Vereisten

[Een ontwikkelimplementatie valideren en publiceren naar productie](../launch/validate-publish-prod.md): Deze pagina veronderstelt dat u een basiswerkende implementatie hebt, en een Adobe Analytics beeldverzoeken in debugger van de Adobe ziet.

## Een eVar maken voor intern zoeken

Volg de beheerder van [conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) om een nieuwe eVar te maken voor intern zoeken. Geef de eVar een gemakkelijk herkenbare naam (zoals &quot;Interne onderzoekstermijn&quot;), en registreer de nieuwe eVar in het het ontwerpdocument [van de](../prepare/solution-design.md)Oplossing van uw organisatie.

## Intern zoekwoord bepalen

De meeste interne zoekopdrachten gebruiken querytekenreeksen om trefwoordgegevens tussen pagina&#39;s door te geven. Gebruik de interne zoekopdracht van uw site en noteer de URL op de pagina met zoekresultaten:

`https://example.com/search.html?q=kittens`

Als de interne zoekopdracht van uw site geen URL gebruikt, zoekt u naar de zoekterm op andere locaties, zoals een gegevenslaag of cookie. Werk met uw team van de plaatsontwikkeling als u niet zeker bent waar te om interne onderzoekstermijn te vinden.

## Wijs de parameter van het vraagkoord aan een gegevenselement toe

Follow [Map data layer objects to data elements](../launch/layer-to-elements.md). Selecteer bij het selecteren van de **[!UICONTROL Data Element Type]** optie **[!UICONTROL Query string parameter]** in plaats van **[!UICONTROL JavaScript Variable]**. Plaats de gewenste parameter van het vraagkoord (typisch `q`) in het tekstgebied.

## Het gegevenselement toewijzen aan de eVar

Follow [Map Launch data elements to Analytics variables](../launch/elements-to-variable.md). Zorg ervoor dat u de zelfde eVar selecteert die u in de montages van de Reeks van het Rapport creeerde.

## Implementatieproces starten

Volg [Implementeer een analytische implementatie in een ontwikkelomgeving](../launch/deploy-dev.md). Nadat u hebt bevestigd dat het programma in uw ontwikkelomgeving werkt, kunt u een ontwikkelimplementatie [valideren en publiceren naar productie](../launch/validate-publish-prod.md).

## Rapporteren in werkruimte

Geef uw implementatie wat tijd om gegevens te verzamelen, dan kunt u beginnen de dimensie in Analysis Workspace te gebruiken.

1. Log in to [experiencecloud.adobe.com](https://experiencecloud.adobe.com) using your AdobeID credentials.
2. Als u niet automatisch bij Adobe Analytics wordt aangemeld, klikt u op het pictogram met het 9-raster rechtsboven en selecteert u **[!UICONTROL Analytics]**.
3. Klik op het **[!UICONTROL Workspace]** tabblad en maak een nieuw project.
4. Zoek de naam van de eVar die u onder Dimension hebt gemaakt en sleep deze naar het canvas van de werkruimte.
