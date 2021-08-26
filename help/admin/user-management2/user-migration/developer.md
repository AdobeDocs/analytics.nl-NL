---
description: Hiermee worden API's weergegeven die door de gebruikersmigratie worden beïnvloed
title: API's die worden beïnvloed door de migratie van gebruikers
uuid: 9a5d43be-e146-476b-961e-49ea0a30b500
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
source-git-commit: 7cb2489c2deaf8e75c71589895314067a010caf8
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# API&#39;s die worden beïnvloed door de gebruikersmigratie{#apis-affected-by-the-migration}

Adobe migreert alle aanmeldingsbedrijven voor Analytics ver van [!DNL my.omniture.com] naar verificatie via de Adobe Experience Cloud. Zodra een bedrijf met deze migratie begint, zullen de programmatic gebruikersverwezenlijking en het beheer door de Analytics-specifieke toestemmingen en de methodes `GetLoginKey` beschikbaar via v1.3 en v1.4 van Analytics Admin API niet meer worden gesteund. Dergelijke acties zullen nu over de Experience Cloud via [!DNL adobe.io] worden toegelaten.

## Betrokken API-methoden {#section-d19051ac26cc49aeb124f767c4760254}

De volgende API-methoden in versie 1.3 en v1.4 van de Admin API worden niet meer ondersteund wanneer u begint met de migratie van gebruikers:

* Company.GetLoginKey
* Permissions.AddLogin
* Permissions.Authenticate
* Permissions.DeleteGroup
* Permissions.DeleteLogin
* Permissions.GetGroup
* Permissions.GetGroups
* Permissions.GetLogin
* Permissions.GetLogins
* Permissions.GetReportSuiteGroups
* Permissions.RemoveLoginSegment
* Permissions.SaveGroup
* Permissions.SaveLogin
* Permissions.GetLoginSegment

## Acties die u kunt uitvoeren {#section-8b0b89a862614f729ebdbe092ce99027}

Als uw bedrijf deze methodes momenteel gebruikt, zoek een pre-migratiebericht die 31 Maart, 2018 begint. De melding wordt minstens 30 dagen verzonden voordat uw bedrijf begint met de migratie naar de Experience Cloud-verificatie. Op dat moment worden deze methoden niet meer ondersteund.

Als uw bedrijf om het even welk van deze methodes niet gebruikt, wordt geen actie vereist behalve het verzekeren u begint gebruikend deze methodes.

Voor aanvullende informatie:

* [Algemene informatie over gebruikersbeheer](https://helpx.adobe.com/enterprise/help/users.html)
* [Gebruikerbeheer-API&#39;s via adobe.io](https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html)
* [Gebruikersbeheer-API-forum](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Migratie van toegang en beheer van analysegebruikers naar Experience Cloud](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)
