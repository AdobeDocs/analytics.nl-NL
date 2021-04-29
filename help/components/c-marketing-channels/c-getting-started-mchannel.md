---
title: Aan de slag met marketingkanalen
description: Leer over het werkschema van de Kanalen van de Marketing, de automatische opstelling, en hoe te om de montages van de reeks van het malplaatjerapport op veelvoudige rapportreeksen toe te passen.
translation-type: tm+mt
source-git-commit: 7202a49dda7c3ef4f4b535476d3cf637b9e9f7f6
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 2%

---


# Aan de slag met marketingkanalen

>[!NOTE]
>
>Om de doeltreffendheid van de Kanalen van de Marketing voor Attribution IQ en Customer Journey Analytics te maximaliseren, hebben wij sommige [herziene beste praktijken](/help/components/c-marketing-channels/mchannel-best-practices.md) gepubliceerd.

Marketingkanalen worden doorgaans gebruikt om inzicht te verschaffen in de manier waarop bezoekers op uw site aankomen. U kunt uw Regels van de Verwerking van het Kanaal van de Marketing aanpassen die op welke kanalen worden gebaseerd u wilt volgen, en hoe u hen wilt volgen.

De kanalen van de marketing draaien rond Eerste en laatste aanraakmetriek, die componenten van standaardomzettingsmetriek zijn.

## Workflow voor marketingkanalen

![](assets/step1_icon.png) Bepaal elk kanaal dat op uw bedrijfsvereisten wordt gebaseerd.

Het bepalen van de kanalen u gebruikt is één van de belangrijkste componenten van de Kanalen van de Marketing. Het bepalen van de kanalen kan samenwerking tussen verscheidene individuen in uw organisatie vereisen. Hier volgen enkele vragen:

* Gebruikt u een betaalde zoekopdracht?
* Gebruikt u e-mailcampagnes? Gebruikt u meerdere e-mailcampagnes die u afzonderlijk wilt bijhouden?
* Hebt u filialen die rechtstreeks naar uw site gaan? Zijn er filialen die u individueel wilt volgen?
* Zijn er externe campagnes die het nuttig zouden vinden om afzonderlijk te volgen?
* Wilt u alle sociale netwerksites samenvoegen, of wilt u er een hebben die u afzonderlijk wilt bijhouden?
* Zijn er andere kanalen die omzetting zouden kunnen beïnvloeden die u wilt volgen?

Een lijst van geadviseerde kanalen kan in [Veelgestelde Vragen en Voorbeelden ](/help/components/c-marketing-channels/c-faq.md) worden gevonden. Maak een lijst met de kanalen die u wilt gebruiken, zodat u de kanalen eenvoudiger kunt inschakelen en definiëren wanneer u kanalen maakt.

![](assets/step2_icon.png) Voeg marketingkanalen toe op de  [!UICONTROL Marketing Channel Manager] pagina.

Nadat u hebt gedefinieerd welke kanalen u wilt bijhouden, schakelt u deze in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** in.

Zie [Kanalen en Regels](/help/components/c-marketing-channels/c-channels.md) voor belangrijke eerste vereiste en conceptuele informatie.

Zie [Markeringskanalen toevoegen](/help/components/c-marketing-channels/c-channels.md) voor de procedure.

>[!NOTE]
>
>Als de Kanalen van de Marketing niet eerder zijn gevormd, [automatische opstelling](/help/components/c-marketing-channels/c-getting-started-mchannel.md) vertoningen. Deze opstelling verstrekt verscheidene pre-gevormde kanalen die u kunt aanpassen. Adobe raadt u aan deze regels als sjabloon te gebruiken. Nochtans, als u reeds stevige kanaaldefinities hebt, kunt u de automatische opstelling overslaan.

![](assets/step3_icon.png) Configureer of verfijn de regels van elk kanaal op de  [!UICONTROL Marketing Channel Processing Rules] pagina.

Nadat u kanalen op de [!UICONTROL Marketing Channel Manager] pagina creeert, vormt u de regels zodat de kanalen gegevens kunnen terugwinnen en melden.

Zie [Regels voor kanaalverwerking voor marketing](/help/components/c-marketing-channels/c-rules.md).

Als de kanalen in de automatische opstelling werden gecreeerd, worden de regels in die kanalen bepaald. U kunt deze naar wens aanpassen.

## Automatische installatie voor marketingkanalen {#run-auto-setup}

Het rapport van het Kanaal van de Marketing komt met een éénmalige opstellingspagina om u te krijgen begonnen. Het verstrekt verscheidene marketing kanalen die u voor het volgen kunt gebruiken. U kunt deze instelling overslaan als u het maken van kanalen en regels comfortabel vindt. Adobe raadt u echter aan de wizard toe te staan om de kanalen voor u te maken. De automatische opstelling laat u zien hoe de regels worden geconstrueerd, of geeft hen voor uw eigen doeleinden uit. U kunt de vooraf gedefinieerde kanalen op elk gewenst moment uitschakelen of verwijderen.

Hoe te om de automatische opstelling van de Kanalen van de Marketing in werking te stellen.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite op [!UICONTROL Report Suite Manager].
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   ![Stap Resultaat](assets/wizard.png)

   >[!NOTE]
   >
   >De pagina [!UICONTROL Marketing Channels: Auto Setup] wordt automatisch weergegeven wanneer u kanaalconfiguratietoepassingen opent in Admin Tools. (Zie [Marketing Channel Manager](/help/components/c-marketing-channels/c-channels.md).) Deze pagina wordt niet weergegeven als uw rapportsuite een of meer marketingkanalen bevat. U kunt deze pagina niet opnieuw openen tenzij u een andere rapportsuite selecteert die geen marketingkanalen bevat.

1. Controleer of de kanalen zijn geselecteerd die u wilt maken.

   Als deze optie is geselecteerd, zijn **[!UICONTROL Email]**, **[!UICONTROL Display]** en **[!UICONTROL Affiliate]** vereiste velden.

1. Klik op **[!UICONTROL Save]**.

## Pas de montages van de de reeksreeks van het malplaatjerapport op veelvoudige rapportreeksen toe

Hoe te om een master rapportreeks als malplaatje te gebruiken voor het testen van uw configuratie van het marketing kanaal. Om tijd te besparen, kunt u dit malplaatje op één of meerdere reeksen van het productierapport in een massaupdate toepassen. U voert deze taak voor kanalen en regelreeksen afzonderlijk uit.

>[!NOTE]
>
>Pas kanalen van een malplaatje toe alvorens u regelreeksen toepast. Uw kanalen moeten voor alle rapportsuites het zelfde zijn wanneer het uitvoeren van deze procedure.

1. Zorg ervoor dat het Rapport van het Kanaal van de Marketing voor geselecteerde rapportreeksen wordt toegelaten. Deze stap wordt uitgevoerd door uw accountmanager.
1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Voor de **[!UICONTROL Report Suite Manager]** pagina, selecteer de reeks van het malplaatjerapport, evenals één of meerdere reeksen van het doelrapport.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.
1. Selecteer op de pagina **[!UICONTROL Select Master Report Suites]** een sjabloonrapportsuite.
1. Klik op **[!UICONTROL Save All]**.
1. Pas regels van een malplaatje op veelvoudige rapportreeksen toe:
   1. Ga terug naar de pagina [!UICONTROL Report Suite Manager].
   1. Selecteer de reeks van het malplaatjerapport, evenals één of meerdere reeksen van het doelrapport.
   1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.
   1. Klik op **[!UICONTROL Save]**. Als de knop Opslaan in deze stap is uitgeschakeld, schakelt u deze in door een van de regels uit te vouwen.

