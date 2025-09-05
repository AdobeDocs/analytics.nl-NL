---
description: Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.
title: Veelgestelde vragen over het doorsturen van servers
feature: Report Suite Settings
exl-id: 63103d2b-e2e8-42da-bdbd-be90abe305f7
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Veelgestelde vragen over het doorsturen van servers

Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.

## Servers bijhouden {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Vraag | Antwoord |
|--- |--- |
| Q: Wat als ik momenteel de erfenis, het volgen van server gebaseerde server het door:sturen gebruikt? | De oudere, op de server gebaseerde servergebaseerde methode voor het doorsturen van gegevens van Analytics naar Audience Manager blijft doorsturen, maar als u Audience Manager-segmenten naar Analytics wilt verzenden, is het nieuwe op de rapportsuite gebaseerde serverdoorsturen van gegevens vereist. Bovendien, is er geen nadeel in het toelaten van een rapportreeks voor server het door:sturen bovenop uw het volgen serverconfiguratie - de nieuwe server-kant van het rapportpakket het door:sturen het plaatsen zal worden gebruikt wanneer er een conflict is. |
| Q: Moet ik mijn erfenis het volgen server gebaseerde serverkant migreren die aan de nieuwe rapportreeks gebaseerd server door:sturen? | Wij zullen de het volgen server gebaseerde server blijven steunen die voor de nabije toekomst door:sturen, echter als u uit de integratie van Audience Manager aan Analytics (segment het delen aan Analytics) wilt voordeel halen, dan zult u het nieuwe op de server gebaseerde van de rapportreeks gebaseerde doorsturen voor alle toepasselijke rapportsuites moeten toelaten. Er is geen dringende reden om de server van het erfenis het volgen van server te onbruikbaar te maken het door:sturen van kant nochtans. |

## Tags en rapportage {#section_71391BA901AC47B9A2286281644FF281}

| Vraag | Antwoord |
|--- |--- |
| V: Wat gebeurt er als ik tags met meerdere suite op mijn site heb? Zal server-kant door:sturen dubbel mijn servervraag aan Audience Manager? | Nee, een hit die van Analytics naar Audience Manager wordt doorgestuurd, wordt slechts eenmaal doorgestuurd naar Audience Manager, ongeacht het aantal rapportsuites in de hit. Als u overeenkomstige gegevensbronnen in Audience Manager voor elk van de rapportreeksen in de treffer hebt, zal elk geschikt van die enige slag worden bevolkt.  Houd er echter rekening mee dat als u momenteel gegevensverzameling op de client gebruikt (DIL) en u het doorsturen op de server inschakelt zonder de module Audience Management te installeren, u uw serveraanroepen naar Audience Manager zal verdubbelen, ongeacht het aantal rapportsuites dat u hebt in uw hit Analytics. |
| V: Wat gebeurt er als ik een gelabelde rapportensuites met meerdere suite heb die zijn toegewezen aan afzonderlijke Experience Cloud Orgs? | U moet geen gegevens verzenden van één treffer voor Analytics naar twee rapportsuites die bij aparte Experience Cloud Orgs horen, maar als dit gebeurt, sturen we de treffer alleen door naar de Experience Cloud Org die overeenkomt met de Identity Service-instelling op de pagina. |
| V: Wat gebeurt er als ik meerdere suite-tags heb en slechts een van mijn rapporten-suites is toegewezen aan mijn Experience Cloud Org en het andere niet? | We sturen de treffer naar de overeenkomstige gegevensverzamelingsserver voor de Experience Cloud Org in uw toegewezen rapportsuite. Aangezien de niet-toegewezen rapportsuite echter geen bijbehorende gegevensbron in Audience Manager heeft, worden er geen gegevens vastgelegd voor de niet-toegewezen rapportsuite in Audience Manager. |
| Q: Wat als ik een rapportsuite heb die is toegewezen aan meerdere Experience Cloud Orgs? | Analytics beschouwt deze rapportsuite als niet-toegewezen en staat niet toe dat het doorsturen aan de serverzijde wordt ingeschakeld voor deze rapportsuite. Neem contact op met de klantenservice om dit toewijzingsprobleem op te lossen. |
| Q: Zal de op de rapportreeks gebaseerde server side door:sturen methode langzamer zijn dan de het volgen server gebaseerde server kant door:sturen? | Nee, de responstijd is gelijk. |
| V: Wat gebeurt er als we twee Experience Cloud Orgs (of Adobe Audience Manager-instanties) hebben en gegevens willen delen tussen beide Experience Cloud Orgs? Mag ik een enkele Analytics-bewerking doorsturen naar meerdere Experience Cloud Orgs? | Nee. Als u gegevens wilt delen die zijn verzameld onder Experience Cloud Org naar een andere Experience Cloud Org, raden we u aan alle relevante soorten publiek van de ene Audience Manager-instantie naar de andere te sturen via de publieksmarkt. |
| Q: Zal het door:sturen van de server in om het even welke extra facturering in Audience Manager of Analytics resulteren? | In Analytics vindt geen extra facturering plaats. In Audience Manager worden doorgestuurde treffers op dezelfde manier behandeld als andere treffers en worden ze gefactureerd.  Daarom is het belangrijk dat DIL en server-side het door:sturen niet tezelfdertijd worden toegelaten, wat dubbele facturering evenals gegevensduplicatie zou kunnen veroorzaken. |

>[!MORELIKETHIS]
>
>* [ server-kant door:sturen ](/help/admin/tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md)
