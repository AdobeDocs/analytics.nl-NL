---
title: Overzicht van classificatiesets
description: Classificatiesets gebruiken om classificatiegegevens te beheren.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# Overzicht van classificatiesets

Classificatiesets bieden één interface voor het beheer van classificaties en regels. Deze workflow combineert het concept van het maken van classificaties in Report Suite Settings met het concept Classification Importer om een intuïtievere interface te bieden voor het maken en beheren van classificatiegegevens.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]**

>[!NOTE]
>
>Deze functie is beschikbaar voor alle klanten in de architectuur van de Classificatieset. Neem contact op met de klantenservice van Adobe of uw Adobe-accountteam voor meer informatie.

De backend architectuur die met de Reeksen van de Classificatie wordt vrijgegeven bevat verscheidene opmerkelijke verbeteringen:

* Aanzienlijk kortere verwerkingstijd (72 uur → 24 uur)
* De mogelijkheid om de interface voor classificatiesets te gebruiken
* De optie om classificatiegegevens in Adobe Experience Platform in de toekomst via de [Adobe Analytics-bronconnector voor classificatiegegevens](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/classifications.html)

De backend architectuur die met de Reeksen van de Classificatie wordt vrijgegeven bevat verscheidene opmerkelijke veranderingen:

* Wanneer u de browser of FTP-import gebruikt, &#39;[!UICONTROL Overwrite on conflict]&#39; is altijd ingeschakeld.
* Wanneer u de browser of FTP-importmodule gebruikt, wordt de optie om direct na het importeren te exporteren niet meer ondersteund. De uitvoer moet afzonderlijk worden geïnitieerd.
* De API Analytics 2.0 `GetDimensions` het eindpunt keert nu koordherkenningstekens voor classificaties in plaats van numerieke herkenningstekens terug. Numerieke id&#39;s kunnen nog steeds worden gebruikt, maar Adobe raadt u aan waar mogelijk de nieuwe tekenreeks-id&#39;s te gebruiken. Numerieke id&#39;s kunnen worden opgehaald met de `?expansion=hidden` querytekenreeksparameter.


Classificatiesets bestaan uit twee hoofdgebieden:

* [**[!UICONTROL Classification Sets Manager]**](set-manager.md): Classificatiesets maken, bewerken en verwijderen.
* [**[!UICONTROL Classification Set Jobs Manager]**](job-manager.md): Bekijk de status van de Indelingsset Taken en download exportbestanden.
