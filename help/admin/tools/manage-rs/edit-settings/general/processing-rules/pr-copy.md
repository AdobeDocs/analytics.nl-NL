---
title: Verwerkingsregels kopiëren
description: Leer hoe u verwerkingsregels van de ene rapportsuite naar de andere kopieert.
feature: Processing Rules
role: Admin
exl-id: bb34ecac-0512-4cff-9ef0-72db2dcabc03
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# De verwerkingsregels van het exemplaar tussen rapportreeksen

Het kopiëren van verwerkingsregels bespaart u manueel het ontspannen van de zelfde logica in veelvoudige rapportreeksen. U kunt de exemplaareigenschap gebruiken om de functionaliteit van verwerkingsregels over vele rapportreeksen gemakkelijk te delen, of geteste functionaliteit van een reeks van het ontwikkelingsrapport aan een reeks van het productierapport te kopiëren.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Processing rules]** > **[!UICONTROL Copy processing rules]**

Deze interface biedt twee opties:

* **vervangt alle verwerkingsregels**: Deze optie schrapt alle verwerkingsregels van de reeks van het bestemmingsrapport, dan voegt alle verwerkingsregels aan de reeks van het bestemmingsrapport in de zelfde orde toe. U kunt geen beperkt aantal verwerkingsregels selecteren die u wilt vervangen.
* **voegt specifieke verwerkingsregels** toe: Deze optie staat u toe om één of meerdere verwerkingsregels te selecteren. De toegevoegde regels worden toegevoegd aan het eind van de lijst van verwerkingsregels in elke reeks van het bestemmingsrapport. Overweeg de orde en de regels van de verwerkingsregel die reeds wanneer het toevoegen van regels aan elke reeks van het bestemmingsrapport bestaan.

Wanneer u verwerkingsregels selecteert om te kopiëren reeksen toe te voegen of te melden, kunt u `Ctrl`/`Cmd` + `Click` gebruiken om meerdere verwerkingsregels of rapportsuites te selecteren. Nadat u de gewenste rapportsuites hebt geselecteerd waarnaar u wilt kopiëren, selecteert u **[!UICONTROL Copy]** en bevestigt u het modale venster dat wordt weergegeven.

>[!WARNING]
>
>De verwerkingsregels beïnvloeden direct gegevensinzameling, en kunnen gegevensverlies veroorzaken als verkeerd gebruikt. Test altijd verwerkingsregels in een ontwikkelrapport voordat u ze kopieert naar een productierapportsuite om problemen met de gegevenskwaliteit te verhelpen.
