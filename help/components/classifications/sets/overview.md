---
title: Overzicht van classificatiesets
description: Classificatiesets gebruiken om classificatiegegevens te beheren.
exl-id: a139b298-1188-42ce-b52f-c71e0ff7c4e3
feature: Classifications
source-git-commit: 66be48d0f41061d259cc53fb835ebd155294a710
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Overzicht van classificatiesets

Classificatiesets bieden één interface voor het beheer van classificaties en regels. Deze workflow combineert het concept van het maken van classificaties in de instellingen van de rapportsuite met het concept &#39;Classification importer&#39; om een intuïtievere interface te bieden voor het maken en beheren van classificatiegegevens.

**[!UICONTROL Components]** > **[!UICONTROL Classification sets]**

U moet een productbeheerder zijn of behoren tot een productprofiel dat het machtigingsitem bevat [!UICONTROL Report Suite Tools] > [!UICONTROL Classifications] om dit menu-item weer te geven. Merk op dat terwijl vorige classificatiebeheerinterfaces onder zijn [!UICONTROL Admin] menu&#39;s, classificatiesets vallen onder de [!UICONTROL Components] -menu.

## Verbeteringen

De backend architectuur die met de reeksen van de Classificatie wordt vrijgegeven bevat verscheidene opmerkelijke verbeteringen:

* Lagere verwerkingstijd (72 uur → 24 uur)
* Een vernieuwde interface voor het beheren van classificaties
* De optie om classificatiegegevens in Adobe Experience Platform in de toekomst via de [Adobe Analytics-bronconnector voor classificatiegegevens](https://experienceleague.adobe.com/nl/docs/experience-platform/sources/connectors/adobe-applications/classifications)

De backend architectuur die met de reeksen van de Classificatie wordt vrijgegeven bevat verscheidene opmerkelijke veranderingen:

* Wanneer u de browser of de automatische importbewerking gebruikt, &#39;[!UICONTROL Overwrite on conflict]&#39; is altijd ingeschakeld.
* Wanneer u de browser of de automatische importfunctie gebruikt, wordt de optie om direct na het importeren te exporteren niet meer ondersteund. De uitvoer moet afzonderlijk worden geïnitieerd.
* De API Analytics 2.0 `GetDimensions` het eindpunt keert nu koordherkenningstekens voor classificaties in plaats van numerieke herkenningstekens terug. Numerieke id&#39;s kunnen nog steeds worden gebruikt, maar Adobe raadt u aan waar mogelijk de nieuwe tekenreeks-id&#39;s te gebruiken. Numerieke id&#39;s kunnen worden opgehaald met de `?expansion=hidden` querytekenreeksparameter.

>[!IMPORTANT]
>
>De prestaties van classificatiesets zijn voornamelijk afhankelijk van het aantal unieke sleutelwaarden die gegevens bevatten. Adobe raadt aan voorzichtig te zijn bij het omgaan met variabelen die een groot aantal unieke waarden bevatten. Deze voorzichtigheid is vooral van toepassing wanneer het combineren van variabelen van veelvoudige rapportreeksen en dimensies in één enkele classificatieset.

Indelingssets bestaan uit drie hoofdgebieden:

* [**[!UICONTROL Classification sets manager]**](manage/set-manager.md): Classificatiesets maken, bewerken en verwijderen.
* [**[!UICONTROL Classification set jobs manager]**](job-manager.md): De status van indelingssettaken weergeven en exportbestanden downloaden.
* [**[!UICONTROL Classification set consolidations]**](consolidations/manage.md): Combineer meerdere classificatiesets tot één classificatieset.
