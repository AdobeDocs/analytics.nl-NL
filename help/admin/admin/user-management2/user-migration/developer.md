---
description: Hiermee worden API's weergegeven die door de gebruikersmigratie worden beïnvloed
title: API's die worden beïnvloed door de migratie van gebruikers
feature: Admin Tools
exl-id: 82d0a1cd-1e25-4157-9bb9-bba1049fdc48
role: Admin, Developer
source-git-commit: b90356050a6ff39e1688a10f6aa0af284284e2a6
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---

# API&#39;s die worden beïnvloed door de gebruikersmigratie{#apis-affected-by-the-migration}

Adobe migreert alle aanmeldingsbedrijven voor Analytics van [!DNL my.omniture.com] naar verificatie via de Adobe Experience Cloud. Zodra een bedrijf met deze migratie begint, worden het creëren en het beheer van programmatische gebruikers via de Analytics-specific toestemmingen en `GetLoginKey` methodes beschikbaar via v1.3 en v1.4 van Analytics Admin API niet meer gesteund. Dergelijke handelingen worden nu in het hele Experience Cloud ingeschakeld via [!DNL adobe.io] .

## Betrokken API-methoden {#methods}

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

## Acties die u kunt uitvoeren {#actions}

Als uw bedrijf deze methodes momenteel gebruikt, zoek een pre-migratiebericht die 31 Maart, 2018 begint. De melding wordt minstens 30 dagen verzonden voordat uw bedrijf begint met de migratie naar de verificatie van het Experience Cloud. Op dat moment worden deze methoden niet meer ondersteund.

Als uw bedrijf om het even welk van deze methodes niet gebruikt, wordt geen actie vereist behalve het verzekeren u begint gebruikend deze methodes.

Voor aanvullende informatie:

* [ Algemene Info van het Beheer van de Gebruiker ](https://helpx.adobe.com/nl/enterprise/help/users.html)
* [ het Beheer API van de Gebruiker Forum ](https://community.adobe.com/t5/enterprise-teams/bd-p/enterprise-and-teams)
* [ Migratie van de Toegang en het Beheer van de Gebruiker van Analytics aan Experience Cloud ](https://experienceleague.adobe.com/docs/analytics/admin/user-product-management/user-management/migrate-users/c-migration-tool.html?lang=nl-NL)
