---
description: 'null'
title: API's die door de migratie worden beïnvloed
uuid: 9a5d43be-e146-476b-961e-49ea0a30b500
translation-type: tm+mt
source-git-commit: ''

---


# API&#39;s die door de migratie worden beïnvloed{#apis-affected-by-the-migration}

## API&#39;s die door de migratie worden beïnvloed {#topic-8d34296a67d74b1081c3f7e8f650f3ce}

Adobe migreert alle aanmeldingsbedrijven voor Analytics op een manier van [!DNL my.omniture.com] en naar verificatie via de Adobe Experience Cloud. Zodra een bedrijf met deze migratie begint, zullen de programmatische gebruikersverwezenlijking en het beheer door de Analytics-specifieke toestemmingen en de `GetLoginKey` methodes beschikbaar via v1.3 en v1.4 van Analytics Admin API niet meer worden gesteund. Dergelijke acties worden nu in de Experience Cloud ingeschakeld via [!DNL adobe.io].

## Betrokken API-methoden {#section-d19051ac26cc49aeb124f767c4760254}

De volgende API-methoden in versie 1.3 en v1.4 van de Admin API worden niet meer ondersteund wanneer u begint met de migratie van gebruikers:

* Company.GetLoginKey
* Machtigingen.AddLogin
* Machtigingen.Verifiëren
* Machtigingen.DeleteGroup
* Machtigingen.Aanmelding verwijderen
* Machtigingen.GetGroup
* Machtigingen.GetGroup
* Machtigingen.GetLogin
* Machtigingen.GetLogins
* Machtigingen.GetReportSuitegroups
* Machtigingen.RemoveLoginSegment
* Machtigingen.SaveGroup
* Machtigingen.Aanmelding opslaan
* Machtigingen.GetLoginSegment

## Acties die u kunt uitvoeren {#section-8b0b89a862614f729ebdbe092ce99027}

Als uw bedrijf deze methodes momenteel gebruikt, zoek een pre-migratiebericht die 31 Maart, 2018 begint. De melding wordt minstens 30 dagen verzonden voordat uw bedrijf begint met de migratie naar de Experience Cloud-verificatie. Op dat moment worden deze methoden niet meer ondersteund.

Als uw bedrijf om het even welk van deze methodes niet gebruikt, wordt geen actie vereist behalve het verzekeren u begint gebruikend deze methodes.

Voor aanvullende informatie:

* [Algemene informatie over gebruikersbeheer](https://helpx.adobe.com/enterprise/help/users.html)
* [Gebruikerbeheer-API&#39;s via adobe.io](https://www.adobe.io/apis/cloudplatform/usermanagement/docs/gettingstarted.html)
* [Gebruikersbeheer-API-forum](https://forums.adobe.com/community/umapi/overview)
* [Migratie van toegang en beheer van analysegebruikers naar de cloud](https://marketing.adobe.com/resources/help/en_US/experience-cloud/admin-console/analytics-migration/)

