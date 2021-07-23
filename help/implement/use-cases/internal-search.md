---
title: Interne zoektermen vastleggen
description: Gebruik een aangepaste variabele om interne zoektermen vast te leggen.
source-git-commit: 3986084eaab81842b6ea0dbabc7bdb78e39f887a
workflow-type: tm+mt
source-wordcount: '362'
ht-degree: 0%

---


# Interne zoektermen vastleggen

Interne zoekrapportage is een integraal onderdeel van veel organisaties en is geen kant-en-klare dimensie met Adobe Analytics. Maar met minimale implementatieinspanningen kan de interne rapportage op de zoekterm eenvoudig worden vastgelegd.

## Vereisten

[Een ontwikkelimplementatie valideren en publiceren naar productie](../launch/validate-publish-prod.md): Deze pagina veronderstelt dat u een basiswerkende implementatie hebt, en een Adobe Analytics beeldverzoeken in debugger van de Adobe ziet.

## Een eVar maken voor intern zoeken

Volg [Conversievariabelen admin](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) om een nieuwe eVar te creëren gewijd aan intern onderzoek. Geef de eVar een gemakkelijk herkenbare naam (zoals &quot;Interne onderzoekstermijn&quot;), en registreer de nieuwe eVar in het [document van het het ontwerpontwerp van de Oplossing](../prepare/solution-design.md) van uw organisatie.

## Intern zoekwoord bepalen

De meeste interne zoekopdrachten gebruiken querytekenreeksen om trefwoordgegevens tussen pagina&#39;s door te geven. Gebruik de interne zoekopdracht van uw site en noteer de URL op de pagina met zoekresultaten:

`https://example.com/search.html?q=kittens`

Als de interne zoekopdracht van uw site geen URL gebruikt, zoekt u naar de zoekterm op andere locaties, zoals een gegevenslaag of cookie. Werk met uw team van de plaatsontwikkeling als u niet zeker bent waar te om interne onderzoekstermijn te vinden.

## Wijs de parameter van het vraagkoord aan een gegevenselement toe

Volg [Gegevenslaagobjecten toewijzen aan gegevenselementen](../launch/layer-to-elements.md). Selecteer **[!UICONTROL Data Element Type]** in plaats van **[!UICONTROL JavaScript Variable]** bij het selecteren van **[!UICONTROL Query string parameter]**. Plaats de gewenste parameter van het vraagkoord (typisch `q`) in het tekstgebied.

## Het gegevenselement toewijzen aan de eVar

Volg [Gegevenselementen toewijzen aan analytische variabelen](../launch/elements-to-variable.md). Zorg ervoor dat u de zelfde eVar selecteert die u in de montages van de Reeks van het Rapport creeerde.

## Implementatie van tags starten

Volg [Implementeer een analytische implementatie in een ontwikkelomgeving](../launch/deploy-dev.md). Nadat u hebt bevestigd dat het programma in uw ontwikkelomgeving werkt, kunt u [een ontwikkelimplementatie valideren en publiceren naar productie](../launch/validate-publish-prod.md).

## Rapporteren in werkruimte

Geef uw implementatie wat tijd om gegevens te verzamelen, dan kunt u beginnen de dimensie in Analysis Workspace te gebruiken.

1. Meld u aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) met uw Adobe-id-referenties.
2. Als u niet automatisch het programma wordt geopend aan Adobe Analytics, klik het 9-rasterpictogram in het hoogste recht, en selecteer **[!UICONTROL Analytics]**.
3. Klik op het tabblad **[!UICONTROL Workspace]** en maak een nieuw project.
4. Zoek de naam van de eVar die u onder Dimension hebt gemaakt en sleep deze naar het canvas van de werkruimte.
