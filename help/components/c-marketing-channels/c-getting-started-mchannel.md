---
title: Aan de slag met marketingkanalen
description: Leer over het werkschema van de Kanalen van de Marketing, de automatische opstelling, en hoe te om de montages van de reeks van het malplaatjerapport op veelvoudige rapportreeksen toe te passen.
feature: Marketing Channels
exl-id: 35938bf9-89ab-434f-9dc2-7a65251412ef
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%

---

# Aan de slag met marketingkanalen

>[!NOTE]
>
>Om doeltreffendheid van de Kanalen van de Marketing voor Attributie en Customer Journey Analytics te maximaliseren, hebben wij sommige [ herzien beste praktijken ](/help/components/c-marketing-channels/mchannel-best-practices.md) gepubliceerd.
>
>De beheerders van Analytics kunnen marketing kanalen voor hun organisaties beheren zoals die in [ worden beschreven leiden de Kanalen van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md).

Marketingkanalen worden doorgaans gebruikt om insight te laten weten hoe bezoekers op uw site aankomen. U kunt uw Regels van de Verwerking van het Kanaal van de Marketing aanpassen die op welke kanalen worden gebaseerd u wilt volgen, en hoe u hen wilt volgen.

De kanalen van de marketing draaien rond Eerste en laatste aanraakmetriek, die componenten van standaardomzettingsmetriek zijn.

## Workflow voor marketingkanalen

![](assets/step1_icon.png) Bepaal elk kanaal op uw bedrijfsvereisten wordt gebaseerd die.

Het bepalen van de kanalen u gebruikt is één van de belangrijkste componenten van de Kanalen van de Marketing. Het bepalen van de kanalen kan samenwerking tussen verscheidene individuen in uw organisatie vereisen. Hier volgen enkele vragen:

* Gebruikt u een betaalde zoekopdracht?
* Gebruikt u e-mailcampagnes? Gebruikt u meerdere e-mailcampagnes die u afzonderlijk wilt bijhouden?
* Hebt u filialen die rechtstreeks naar uw site gaan? Zijn er filialen die u individueel wilt volgen?
* Zijn er externe campagnes die het nuttig zouden vinden om afzonderlijk te volgen?
* Wilt u alle sociale netwerksites samenvoegen, of wilt u er een hebben die u afzonderlijk wilt bijhouden?
* Zijn er andere kanalen die omzetting zouden kunnen beïnvloeden die u wilt volgen?

Een lijst van geadviseerde kanalen kan in [ Veelgestelde Vragen en Voorbeelden ](/help/components/c-marketing-channels/c-faq.md) worden gevonden. Maak een lijst met kanalen die u wilt gebruiken, zodat u ze gemakkelijker kunt in- en definiëren wanneer u kanalen maakt.

![](assets/step2_icon.png) Voeg marketingkanalen toe op de pagina [!UICONTROL Marketing Channel Manager] .

Nadat u hebt gedefinieerd welke kanalen u wilt bijhouden, schakelt u deze in **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** in.

Zie [ Kanalen en Regels ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md) voor belangrijke voorwaarde en conceptuele informatie.

Zie [ marketing kanalen ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md) voor de procedure toevoegen.

>[!NOTE]
>
>Als de Marketing Kanalen niet eerder zijn gevormd, [ automatische opstellings ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) vertoningen. Deze opstelling verstrekt verscheidene pre-gevormde kanalen die u kunt aanpassen. Adobe raadt u aan deze regels als sjabloon te gebruiken. Nochtans, als u reeds stevige kanaaldefinities hebt, kunt u de automatische opstelling overslaan.

![](assets/step3_icon.png) Configureer of verfijn de regels van elk kanaal op de [!UICONTROL Marketing Channel Processing Rules] -pagina.

Nadat u kanalen op de [!UICONTROL Marketing Channel Manager] pagina creeert, vormt u de regels zodat de kanalen gegevens kunnen terugwinnen en melden.

Zie [ de Verwerkingsregels van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md).

Als de kanalen in de automatische opstelling werden gecreeerd, worden de regels in die kanalen bepaald. U kunt deze naar wens aanpassen.

## Automatische installatie voor marketingkanalen {#run-auto-setup}

Het rapport van het Kanaal van de Marketing komt met een éénmalige opstellingspagina om u te krijgen begonnen. Het verstrekt verscheidene marketing kanalen die u voor het volgen kunt gebruiken. U kunt deze instelling overslaan als u het maken van kanalen en regels comfortabel vindt. Adobe raadt u echter aan de wizard toe te staan om de kanalen voor u te maken. De automatische opstelling laat u zien hoe de regels worden geconstrueerd, of geeft hen voor uw eigen doeleinden uit. U kunt de vooraf gedefinieerde kanalen op elk gewenst moment uitschakelen of verwijderen.

Hoe te om de automatische opstelling van de Kanalen van de Marketing in werking te stellen.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer in [!UICONTROL Report Suite Manager] een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.

   ![Stap Resultaat](assets/wizard.png)

   >[!NOTE]
   >
   >De pagina [!UICONTROL Marketing Channels: Auto Setup] wordt automatisch weergegeven wanneer u kanaalconfiguratietoepassingen opent in Admin Tools. (Zie [ de Manager van het Kanaal van de Marketing ](/help/admin/tools/manage-rs/edit-settings/marketing-channels/c-channels.md).) Deze pagina toont niet als uw rapportreeks één of meerdere marketing kanalen bevat. U hebt geen toegang meer tot deze pagina, tenzij u een andere rapportsuite selecteert die geen marketingkanalen bevat.

1. Controleer of de kanalen zijn geselecteerd die u wilt maken.

   Als deze optie is geselecteerd, zijn **[!UICONTROL Email]** , **[!UICONTROL Display]** en **[!UICONTROL Affiliate]** verplichte velden.

1. Klik op **[!UICONTROL Save]**.

## Pas de montages van de de reeksreeks van het malplaatjerapport op veelvoudige rapportreeksen toe

Hoe te om een hoofdrapportreeks als malplaatje te gebruiken voor het testen van uw configuratie van het marketingkanaal. Om tijd te besparen, kunt u dit malplaatje op één of meerdere reeksen van het productierapport in een massaupdate toepassen. U voert deze taak voor kanalen en regelreeksen afzonderlijk uit.

>[!NOTE]
>
>Pas kanalen van een malplaatje toe alvorens u regelreeksen toepast. Uw kanalen moeten voor alle rapportsuites het zelfde zijn wanneer het uitvoeren van deze procedure.

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Voor de **[!UICONTROL Report Suite Manager]** pagina, selecteer de reeks van het malplaatjerapport, evenals één of meerdere reeksen van het doelrapport.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Manager]**.
1. Selecteer op de pagina **[!UICONTROL Select Master Report Suites]** een sjabloonrapportsuite.
1. Klik op **[!UICONTROL Save All]**.
1. Pas regels van een malplaatje op veelvoudige rapportreeksen toe:
   1. Ga terug naar de pagina [!UICONTROL Report Suite Manager] .
   1. Selecteer de reeks van het malplaatjerapport, evenals één of meerdere reeksen van het doelrapport.
   1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Marketing Channels]** > **[!UICONTROL Marketing Channel Processing Rules]**.
   1. Klik op **[!UICONTROL Save]**. Als de knop Opslaan in deze stap is uitgeschakeld, schakelt u deze in door een van de regels uit te vouwen.
