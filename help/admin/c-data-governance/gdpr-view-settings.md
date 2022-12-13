---
description: Het dialoogvenster Data Governance in Admin Tools biedt een overzicht van welke rapportsuites zijn geconfigureerd voor data-governance, of ze zijn toegewezen aan een Experience Cloud-organisatie, en of er een dataretentiebeleid voor deze rapportsuite bestaat.
title: Data Governance-instellingen voor een rapportsuite weergeven/beheren
feature: Data Governance
exl-id: 87b0be42-1098-4e72-8eb8-0c1bb56791f8
source-git-commit: 196e7672026a284591c0dba2336cb11fc3661c72
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 75%

---

# Data Governance-instellingen voor een rapportsuite weergeven/beheren

Het dialoogvenster Data Governance in Admin Tools biedt een overzicht van welke rapportsuites zijn geconfigureerd voor data-governance, of ze zijn toegewezen aan een Experience Cloud-organisatie, en of er een dataretentiebeleid voor deze rapportsuite bestaat.

1. Meld u aan bij Adobe Experience Cloud.
1. Ga naar  **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Governance]**.

>[!NOTE]
>
>Als dit menu-item niet zichtbaar is, moet u deze toevoegen aan een [productprofiel in Admin Console](https://experienceleague.adobe.com/docs/analytics/admin/admin-console/permissions/product-profile.html) met machtigingen voor deze functionaliteit.

1. Bekijk alle rapportsuites die deel van uw login bedrijf uitmaken:

   ![](assets/privacy_setup_an.png)

| Instelling | Beschrijving |
| --- | --- |
| **[!UICONTROL Report Suites]** | De eerste rij vermeldt de friendly name van de rapportsuite. De tweede rij bevat de interne naam van de rapportsuite. Als u labels voor een rapportsuite mag instellen, is de eerste rij een klikbare koppeling die u naar de labelpagina brengt. |
| **[!UICONTROL Organization Mapping]** | <ul><li>Toegewezen: Deze rapportsuite is al toegewezen aan dezelfde Experience Cloud-organisatie als het aanmeldingsbedrijf voor Analytics waarbij u bent aangemeld. Alleen rapportsuites met deze instelling kunnen worden gelabeld.</li><li>Toegewezen aan een andere organisatie: Deze rapportsuite is al aan een andere Experience Cloud-organisatie toegewezen.</li></ul> |
| **[!UICONTROL Data Retention Policy]** | Voor de Analytics Data Privacy-implementatie hebt u een dataretentiebeleid nodig. Met deze instelling wordt het volgende getoond:<ul><li>of er een dataretentiebeleid is voor deze rapportsuite, en</li><li>hoe lang de data door Adobe worden bewaard voordat ze worden verwijderd. De standaard dataretentieperiode is 25 maanden.</li></ul>**Opmerking**: Adobe Analytics kan u niet helpen bij het verwerken van aanvragen voor de Data Privacy API, dat wil zeggen, het verwerken van verzoeken om toegang of verwijdering die u van uw eindgebruikers ontvangt, als de bewaarperiode voor gegevens niet is ingesteld. Neem contact op met de Customer Success Manager om de periode voor dataretentie in te stellen. |
| **[!UICONTROL Groups]** | Groeperingsfunctionaliteit is momenteel niet geïmplementeerd. |
| Linkerzijbalk | Klik op het trechterpictogram om de zijbalk te openen of te sluiten. De [!UICONTROL Organization Mapping] geeft het aantal rapportsuites weer dat in elk van de beschreven categorieën valt. De [!UICONTROL Data Retention Policy] de sectie toont elk uniek beleid van het gegevensbehoud momenteel op zijn plaats voor uw organisatie en het aantal rapportsuites die dat behoudbeleid werden toegewezen. |
| **[!UICONTROL Export to CSV]** | Als u het selectievakje naast een of meer rapportsuites selecteert, wordt de optie Exporteren naar CSV weergegeven. Met deze optie kunt u een CSV-bestand downloaden met alle huidige labeldefinities voor alle variabelen voor alle geselecteerde rapportsuites. We adviseren dat uw juridische team uw labelkeuzes controleert, en deze optie maakt die controle mogelijk. U kunt het CSV-bestand met het team delen, zodat ze de controle niet hoeven uit te voeren terwijl ze zijn aangemeld bij de Data Governance-gebruikersinterface. |

{style=&quot;table-layout:auto&quot;}
