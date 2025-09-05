---
title: Interface voor verwerkingsregels
description: Navigeer de interface om verwerkingsregels te maken, bewerken of verwijderen.
feature: Processing Rules
role: Admin
exl-id: 897d2bb6-cc10-43b1-b436-20985d24d998
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 0%

---

# Interface voor verwerkingsregels

Met de interface voor verwerkingsregels kunt u verwerkingsregels maken, bewerken of verwijderen.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Processing rules]**

>[!WARNING]
>
>De verwerkingsregels beïnvloeden direct gegevensinzameling, en kunnen gegevensverlies veroorzaken als verkeerd gebruikt. Test altijd de verwerkingsregels in een ontwikkelrapport voordat u ze in een productierapportsuite inschakelt om problemen met de gegevenskwaliteit te verhelpen.

## Overkoepelende structuur

Deze interface bevat twee hoofdcomponenten:

* **[!UICONTROL Processing order]**: Regels worden precies in de door u opgegeven volgorde uitgevoerd, vanaf regel 1. Elke hit loopt door elke regel. Er zijn geen vroege omstandigheden. Zorg ervoor dat de voorwaarden van elke verwerkingsregel elke hit aanpassen die naar de rapportsuite wordt verzonden.
* **[!UICONTROL Rule sets]**: De definities van elk van uw verwerkingsregels.

U kunt tot 150 verwerkingsregels en tot 30 voorwaarden per verwerkingsregel hebben. Er is geen redelijke limiet voor het aantal acties per verwerkingsregel.

## Structuur voor regelset

Elke verwerkingsregel bevat de volgende secties:

* **Titel van de Regel**: Het etiket van de regel. Het beïnvloedt geen verwerkingsregellogica, maar is waardevol om te helpen spoor van wat de regel doet.
* **Voorwaarde**: Getoond als tekst, &quot;[!UICONTROL If any/all of the following are true]&quot;. Als u geen voorwaarde omvat, loopt de regel altijd op elke slag.
* **Actie**: Als geen voorwaarde bestaat, wordt de tekst getoond zoals, &quot;[!UICONTROL Always execute]&quot;. Als een voorwaarde bestaat, wordt de tekst getoond zoals, &quot;[!UICONTROL Then do the following]&quot;. Als de bovenstaande voorwaarde `true` oplevert, wordt elke in deze sectie vermelde handeling mogelijk uitgevoerd. Naast de voorwaarde van een regel, kunt u _ook_ voorwaarden aan individuele acties verbinden. De volgende acties zijn beschikbaar:
   * **[!UICONTROL Overwrite value of]** - Hiermee overschrijft u de gewenste variabele met een andere variabele, een statische waarde of een samengevoegde waarde.
   * **[!UICONTROL Delete value of]**: verwijdert de gewenste variabele waarde voor die hit.
   * **[!UICONTROL Set event]** : activeert de gewenste gebeurtenis. Meestal zou u gebeurtenissen instellen op de aangepaste waarde `1` . Het is ook toegestaan gebeurtenissen in te stellen op andere waarden dan `1` of ze zelfs in te stellen op waarden die zijn ingesteld in contextgegevensvariabelen.
* **anders actie**: Als een voorwaarde bestaat, verschijnt deze sectie als, &quot;[!UICONTROL Otherwise do the following]&quot;. Als de bovenstaande voorwaarde `false` oplevert, wordt elke in deze sectie vermelde handeling mogelijk uitgevoerd. Deze sectie volgt de zelfde regelacties zoals hierboven, met inbegrip van de capaciteit om waarden te beschrijven, waarden te schrappen, en gebeurtenissen te plaatsen.
* **Reden**: Verslag die om de regel en verzocht het afhangt. Het beïnvloedt geen verwerkingsregellogica, maar is waardevol om te helpen volgen waarom de regel bestaat.

Zie [ Dimensies en metriek beschikbaar aan verwerkingsregels ](pr-variables.md) voor een uitvoerige lijst van variabelen die u in deze interface kunt gebruiken.

* Elke variabele die &quot;Read&quot; toestaat, kan in een voorwaarde worden gebruikt.
* Elke variabele die &quot;Write&quot; toestaat, kan in een handeling worden gebruikt.
