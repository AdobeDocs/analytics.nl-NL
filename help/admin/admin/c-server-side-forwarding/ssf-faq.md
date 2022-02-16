---
description: Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.
title: Veelgestelde vragen over server-side doorsturen
feature: Server-Side Forwarding
exl-id: 63103d2b-e2e8-42da-bdbd-be90abe305f7
source-git-commit: ee56267979979f8e03b1c6a0d849ccf994599024
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 1%

---

# Veelgestelde vragen over server-side doorsturen

Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.

## Servers bijhouden {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Vraag | Antwoord |
|--- |--- |
| V: Wat als ik momenteel de erfenis, het volgen van server gebaseerde server het door:sturen gebruikt? | De erfenis het volgen server gebaseerde server die server door:sturen methode zal gegevens van Analytics aan Audience Manager blijven door:sturen, nochtans als u wenst om de segmenten van de Audience Manager naar Analytics te verzenden, wordt het nieuwe op de server gebaseerde server van de rapportreeks gebaseerd door:sturen vereist. Bovendien, is er geen nadeel in het toelaten van een rapportreeks voor server het door:sturen bovenop uw het volgen serverconfiguratie - de nieuwe server-kant van de rapportsuite het door:sturen het plaatsen zal worden gebruikt wanneer er een conflict is. |
| V: Moet ik mijn erfenis het volgen server gebaseerde serverkant die aan het nieuwe op de server gebaseerde van de rapportreeks door:sturen migreren? | Wij zullen de het volgen server gebaseerde server blijven steunen die voor de voorzienbare toekomst door:sturen, echter als u uit de integratie van Audience Manager aan Analytics (segment het delen aan Analytics) wilt voordeel halen, dan zult u de nieuwe server van de rapportreeks moeten toelaten gebaseerd het door:sturen voor alle toepasselijke rapportsuites. Er is geen dringende reden om de server van het erfenis het volgen van server te onbruikbaar te maken het door:sturen van kant nochtans. |

## Tags en rapportage {#section_71391BA901AC47B9A2286281644FF281}

| Vraag | Antwoord |
|--- |--- |
| V: Wat gebeurt er als ik tags met meerdere suite op mijn site heb? Zal server-kant door:sturen dubbel mijn servervraag aan Audience Manager? | Nee, een treffer die van Analytics aan Audience Manager door:sturen zal slechts eenmaal aan Audience Manager worden doorgestuurd ongeacht het aantal rapportsuites in hit. Als u overeenkomstige gegevensbronnen in Audience Manager voor elk van de rapportreeksen in de slag hebt, zal elk geschikt van die enige slag worden bevolkt.  Houd in mening echter, dat als u momenteel cliënt-zijgegevensinzameling (DIL) gebruikt en u server-zijdoor:sturen zonder de Module van het Beheer van de Publiek te installeren toelaat, u uw servervraag aan Audience Manager ongeacht het aantal rapportsuites zult verdubbelen u in uw treffer Analytics hebt. |
| V: Wat gebeurt er als ik een gelabelde rapportsuite met meerdere suite heb die is toegewezen aan aparte Experience Cloud Orgs? | U zou nooit gegevens van één enkele Bevolking van Analytics naar twee rapportreeksen moeten verzenden die tot afzonderlijke Experience Cloud Orgs behoren, maar als dit voorkomt, zullen wij slechts de klap aan de Experience Cloud door:sturen Org die de opstelling van de Dienst van de Identiteit op de pagina aanpast. |
| V: Wat als ik multi-suite-tagging heb en slechts één van mijn rapport-suites is toegewezen aan mijn Experience Cloud Org en de andere niet? | We sturen de hit naar de overeenkomstige gegevensverzamelingsserver voor de Experience Cloud Org in de toegewezen rapportsuite. Aangezien de niet-toegewezen rapportsuite echter geen bijbehorende gegevensbron in Audience Manager heeft, worden er geen gegevens vastgelegd voor de niet-toegewezen rapportsuite in Audience Manager. |
| V: Wat als ik een rapportsuite heb die is toegewezen aan meerdere Experience Cloud Orgs? | Analytics beschouwt deze rapportsuite als niet-toegewezen en staat niet toe dat het doorsturen aan de serverzijde wordt ingeschakeld voor deze rapportsuite. Neem contact op met de klantenservice om dit toewijzingsprobleem op te lossen. |
| V: Zal de op de rapportreeks gebaseerde server kant door:sturen methode langzamer zijn dan de het volgen server gebaseerde server kant door:sturen? | Nee, de responstijd is gelijk. |
| V: Wat als wij twee Experience Cloud Orgs (of AAM instanties) hebben en gegevens tussen beide Experience Cloud Orgs willen delen? Kan ik een enkele Analytics-hit naar meerdere Experience Cloud Orgs op de server doorsturen? | Nee. Als u gegevens moet delen die onder één Experience Cloud Org aan een andere Experience Cloud Org worden verzameld, adviseren wij om het even welk toepasselijk publiek van één instantie van de Audience Manager naar een andere te verzenden gebruikend de publieksmarkt. |
| V: Zal server-kant het door:sturen in om het even welke extra het factureren in Audience Manager of Analytics resulteren? | In Analytics vindt geen extra facturering plaats. In Audience Manager worden doorgestuurde treffers als andere treffers behandeld en worden ze gefactureerd.  Daarom is het belangrijk om DIL en server-kant het door:sturen niet tezelfdertijd toegelaten te hebben, die dubbel-factureren evenals gegevensduplicatie zou kunnen veroorzaken. |

>[!MORELIKETHIS]
>
>* [Server-kant doorsturen](/help/admin/admin/c-server-side-forwarding/ssf.md)

