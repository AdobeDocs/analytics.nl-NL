---
description: Hiermee worden API's weergegeven die door de gebruikersmigratie worden beïnvloed
title: API's die worden beïnvloed door de migratie van gebruikers
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
source-git-commit: a17297af84e1f5e7fe61f886eb3906c462229087
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# API&#39;s die worden beïnvloed door de gebruikersmigratie{#apis-affected-by-the-migration}

Adobe migreert alle aanmeldingsbedrijven voor Analytics ver van [!DNL my.omniture.com] en op verificatie via de Adobe Experience Cloud. Zodra een bedrijf met deze migratie begint, programmatic gebruikersverwezenlijking en beheer door de Analytics-Specifieke toestemmingen en `GetLoginKey` methoden die beschikbaar zijn via v1.3 en v1.4 van de API voor Analytics Admin worden niet meer ondersteund. Dergelijke acties worden nu in de hele Experience Cloud ingeschakeld via [!DNL adobe.io].

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
* [Gebruikerbeheer-API&#39;s via adobe.io](https://developer.adobe.com/UMAPI/)
* [Gebruikersbeheer-API-forum](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [Migratie van toegang en beheer van analysegebruikers naar Experience Cloud](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html)
