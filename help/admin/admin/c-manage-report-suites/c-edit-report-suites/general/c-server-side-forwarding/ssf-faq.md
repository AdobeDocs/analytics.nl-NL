---
description: Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.
title: Veelgestelde vragen over het doorsturen van servers
feature: Server-Side Forwarding
exl-id: 63103d2b-e2e8-42da-bdbd-be90abe305f7
role: Admin
source-git-commit: def7d071de1765acf524a638a8f8d13ae69e1a1f
workflow-type: tm+mt
source-wordcount: '690'
ht-degree: 0%

---

# Veelgestelde vragen over het doorsturen van servers

Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.

## Servers bijhouden {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Vraag | Antwoord |
|--- |--- |
| Q: Wat als ik momenteel de erfenis, het volgen van server gebaseerde server het door:sturen gebruikt? | De erfenis het volgen server gebaseerde server die server door:sturen methode zal gegevens van Analytics aan Audience Manager blijven door:sturen, nochtans als u wenst om de segmenten van de Audience Manager naar Analytics te verzenden, wordt het nieuwe op de server gebaseerde server van de rapportreeks gebaseerd door:sturen vereist. Bovendien, is er geen nadeel in het toelaten van een rapportreeks voor server het door:sturen bovenop uw het volgen serverconfiguratie - de nieuwe server-kant van het rapportpakket het door:sturen het plaatsen zal worden gebruikt wanneer er een conflict is. |
| Q: Moet ik mijn erfenis het volgen server gebaseerde serverkant migreren die aan de nieuwe rapportreeks gebaseerd server door:sturen? | Wij zullen de het volgen server gebaseerde server blijven steunen die voor de voorzienbare toekomst door:sturen, echter als u uit de integratie van Audience Manager aan Analytics (segment het delen aan Analytics) wilt voordeel halen, dan zult u de nieuwe server van de rapportreeks moeten toelaten gebaseerd het door:sturen voor alle toepasselijke rapportsuites. Er is geen dringende reden om de server van het erfenis het volgen van server te onbruikbaar te maken het door:sturen van kant nochtans. |

## Tags en rapportage {#section_71391BA901AC47B9A2286281644FF281}

| Vraag | Antwoord |
|--- |--- |
| V: Wat gebeurt er als ik tags met meerdere suite op mijn site heb? Zal server-kant door:sturen dubbel mijn servervraag aan Audience Manager? | Nee, een treffer die van Analytics aan Audience Manager door:sturen zal slechts eenmaal aan Audience Manager worden doorgestuurd ongeacht het aantal rapportsuites in hit. Als u overeenkomstige gegevensbronnen in Audience Manager voor elk van de rapportreeksen in de slag hebt, zal elk geschikt van die enige slag worden bevolkt.  Houd in mening echter, dat als u momenteel cliënt-zijgegevensinzameling (DIL) gebruikt en u server-zijdoor:sturen zonder de Module van het Beheer van de Publiek te installeren toelaat, u uw servervraag aan Audience Manager ongeacht het aantal rapportsuites zult verdubbelen u in uw treffer Analytics hebt. |
| Q: Wat als ik multi-suite geëtiketteerde rapportsuites heb die aan afzonderlijke Experience Cloud Orgs in kaart worden gebracht? | U zou nooit gegevens van één enkele Bevolking van Analytics naar twee rapportreeksen moeten verzenden die tot afzonderlijke Orgs van het Experience Cloud behoren, maar als dit voorkomt, zullen wij slechts de klap aan het Experience Cloud door:sturen Org die de opstelling van de Dienst van de Identiteit op de pagina aanpast. |
| Q: Wat als ik multi-suite etiketteren en slechts één van mijn rapportsuites in kaart wordt gebracht aan mijn Experience Cloud Org en andere niet is? | We sturen de hit naar de overeenkomstige gegevensverzamelingsserver voor het Experience Cloud Org in de toegewezen rapportsuite. Aangezien de niet-toegewezen rapportsuite echter geen bijbehorende gegevensbron in Audience Manager heeft, worden er geen gegevens vastgelegd voor de niet-toegewezen rapportsuite in Audience Manager. |
| Q: Wat als ik een rapportsuite heb die is toegewezen aan meerdere Org&#39;s van Experiencen Cloud? | Analytics beschouwt deze rapportsuite als niet-toegewezen en staat niet toe dat het doorsturen aan de serverzijde wordt ingeschakeld voor deze rapportsuite. Neem contact op met de klantenservice om dit toewijzingsprobleem op te lossen. |
| Q: Zal de op de rapportreeks gebaseerde server side door:sturen methode langzamer zijn dan de het volgen server gebaseerde server kant door:sturen? | Nee, de responstijd is gelijk. |
| Q: Wat als wij twee Experience Cloud Orgs (of de instanties van Adobe Audience Manager) hebben en gegevens tussen beide Experience Cloud Orgs willen delen? Mag ik een enkele Analytics-hit naar meerdere Orgs-Experiencen Cloud server side forward? | Nee. Als u gegevens moet delen die onder één Experience Cloud Org aan een andere Experience Cloud Org worden verzameld, adviseren wij om het even welk toepasselijk publiek van één instantie van de Audience Manager naar een andere te verzenden gebruikend de publieksmarkt. |
| Q: Zal server-kant het door:sturen in om het even welke extra het factureren in Audience Manager of Analytics resulteren? | In Analytics vindt geen extra facturering plaats. In Audience Manager worden doorgestuurde treffers als andere treffers behandeld en worden ze gefactureerd.  Daarom is het belangrijk om DIL en server-kant het door:sturen niet tezelfdertijd toegelaten te hebben, die dubbel-factureren evenals gegevensduplicatie zou kunnen veroorzaken. |

>[!MORELIKETHIS]
>
>* [Server-kant doorsturen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)
