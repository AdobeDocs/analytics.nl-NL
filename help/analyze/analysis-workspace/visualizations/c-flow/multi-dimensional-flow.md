---
description: Begrijp hoe een interdimensionale stroom u gebruikerspaden over diverse afmetingen laat onderzoeken.
title: Inter-dimensionale stromen
uuid: 51d08531-1c56-46c7-b505-bd8d5e6aa6c1
feature: Visualizations
role: User, Admin
exl-id: f84917a4-2c07-48fb-9af3-d96c537da65c
source-git-commit: 978bd8642011dd2c8e43564c90303f194689a64e
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Interdimensionale stromen

Met een interdimensionale stroom kunt u gebruikerspaden in verschillende dimensies bekijken.

>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ inter-dimensionele stromen ](https://video.tv.adobe.com/v/24041?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]

In dit artikel wordt getoond hoe u deze workflow kunt gebruiken voor twee gebruiksgevallen: interacties en gebeurtenissen voor mobiele apps en hoe campagnes webbezoeken aansturen.

## Interacties en gebeurtenissen voor mobiele apps

De [!UICONTROL Screen Name] -dimensie wordt gebruikt in deze voorbeeldstroom om te zien hoe gebruikers de verschillende schermen (scènes) in de app gebruiken. Het bovenste scherm dat wordt geretourneerd, is **[!UICONTROL luma: content: ios: en: home]** , de startpagina van de app:

![ de stroom die van A het Toegevoegde Punt toont.](assets/flowapp.png)

Als u de interactie tussen schermen en gebeurtenistypen (zoals toevoegen aan winkelwagentje, aankopen en andere) in deze app wilt verkennen, sleept u de **[!UICONTROL Event Types]** -dimensie en zet u deze neer:

* Boven op elke beschikbare stap in de flow, om die dimensie te vervangen:

  ![ de stroom van A die de afmeting van de Pagina toont sleept aan de veelvoudige gebieden.](assets/flowapp-replace.png)

* Buiten de huidige stroomvisualisatie om de dimensie toe te voegen:

  ![ de stroom van A die de afmeting van de Pagina toont aan het witte die ruimte aan het eind wordt gesleept.](assets/flowapp-add.png)

De stroomvisualisatie hieronder toont het resultaat van het toevoegen van de **[!UICONTROL Event Types]** dimensie. De visualisatie biedt inzicht in de manier waarop gebruikers van mobiele apps verschillende schermen in de app doorlopen voordat ze producten aan een winkelwagentje toevoegen, de toepassing sluiten, een aanbieding krijgen en nog veel meer.

![ A fLow die de de afmetingsresultaten van de Pagina bij de bovenkant van de lijst tonen.](assets/flowapp-result.png)

## Hoe campagnes webbezoeken sturen

U wilt analyseren welke campagnes bezoeken aan de website aansturen. U maakt een stroomvisualisatie met de **[!UICONTROL Campaign Name]** als dimensie

![ de dimensie van de het Webcampagne van de stroom ](assets/flowweb.png)

U vervangt de laatste **[!UICONTROL Campaign Name]** -dimensie door de **[!UICONTROL Formatted Page Name]** -dimensie en voegt nog een **[!UICONTROL Formatted Page Name]** -dimensie toe aan het einde van de flowvisualisatie.

![ de naam van de het Webcampagne van de stroom en Web-pagina dimensie ](assets/flowweb-replace.png)

U kunt de muisaanwijzer boven een willekeurige stroom houden om meer details weer te geven. Welke campagnes bijvoorbeeld hebben geleid tot een afhandeling van winkelwagentjes.

![ de naam van de het Webcampagne van de stroom en Web-pagina dimensie hover ](assets/flowweb-hover.png)
