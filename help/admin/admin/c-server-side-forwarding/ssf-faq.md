---
description: Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.
title: Veelgestelde vragen over het doorsturen van servers
uuid: ecd0bc9b-ebf7-414e-88a2-ebba3fd75c92
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Veelgestelde vragen over het doorsturen van servers

Veelgestelde vragen over eigenschappen, functionaliteit, en kwesties met betrekking tot server-kant het door:sturen.

## Servers bijhouden {#section_28E5BECC2034484AB9726E513F2CCFB7}

| Vraag | Antwoord |
|--- |--- |
| V: Wat als ik momenteel de erfenis, het volgen van server gebaseerde server het door:sturen gebruikt? | De erfenis volgende server op server gebaseerde server die methode aan zij door:sturen zal gegevens van Analytics aan de Manager van het Publiek blijven, nochtans als u wenst om de segmenten van de Manager van het Publiek naar Analytics te verzenden, wordt het nieuwe rapport op de server gebaseerde doorsturen van de rapportreeks vereist. Bovendien, is er geen nadeel in het toelaten van een rapportreeks voor server het door:sturen bovenop uw het volgen serverconfiguratie - de nieuwe server-kant van het rapportpakket het door:sturen het plaatsen zal worden gebruikt wanneer er een conflict is. |
| V: Moet ik mijn erfenis het volgen server gebaseerde serverkant die aan het nieuwe op de server gebaseerde van de rapportreeks door:sturen migreren? | Wij zullen de het volgen server gebaseerde server blijven steunen die voor de voorzienbare toekomst door:sturen, echter als u uit de integratie van de Manager van het Publiek aan Analytics (segment het delen aan Analytics) wilt voordeel halen, dan zult u de nieuwe server van de rapportreeks moeten toelaten gebaseerd het door:sturen voor alle toepasselijke rapportsuites. Er is geen dringende reden om de server van het erfenis het volgen server gebaseerde kant onbruikbaar te maken die nochtans door:sturen. |

## Tags en rapportage {#section_71391BA901AC47B9A2286281644FF281}

| Vraag | Antwoord |
|--- |--- |
| V: Wat gebeurt er als ik tags met meerdere suite op mijn site heb? Zal server-kant door:sturen dubbel mijn servervraag aan de Manager van het Publiek? | Nee, een hit die door Analytics naar Audience Manager wordt doorgestuurd, wordt slechts eenmaal doorgestuurd naar Audience Manager, ongeacht het aantal rapportsuites in de hit. Als u overeenkomstige gegevensbronnen in de Manager van de Publiek voor elk van de rapportreeksen in de slag hebt, zal elk geschikt van die enige slag worden bevolkt.  Houd in mening echter, als u momenteel cliënt-zijgegevensinzameling (DIL) gebruikt en u server-zijhet door:sturen zonder de Module van het Beheer van de Publiek te installeren toelaat, zult u uw servervraag aan de Manager van de Publiek ongeacht het aantal rapportreeksen verdubbelen u in uw treffer Analytics hebt. |
| V: Wat gebeurt er als ik een gelabeld rapport met meerdere suite heb dat is toegewezen aan aparte Experience Cloud Orgs? | U mag geen gegevens van één treffer voor Analytics verzenden naar twee rapportsuites die horen bij aparte Experience Cloud Orgs, maar als dit wel het geval is, sturen we de hit alleen door naar de Experience Cloud Org die overeenkomt met de Identity Service setup op de pagina. |
| V: Wat gebeurt er als ik een tag met meerdere suite heb en slechts een van mijn rapportreeksen is toegewezen aan mijn Experience Cloud Org en het andere niet? | We sturen de hit naar de overeenkomstige gegevensverzamelingsserver voor de Experience Cloud Org in uw toegewezen rapportsuite. Aangezien de niet-toegewezen rapportsuite geen bijbehorende gegevensbron heeft in Audience Manager, worden er geen gegevens vastgelegd voor de niet-toegewezen rapportsuite in Audience Manager. |
| V: Wat gebeurt er als ik een rapportenpakket heb dat is toegewezen aan meerdere Experience Cloud Orgs? | Analytics beschouwt deze rapportsuite als niet-toegewezen en staat niet toe dat het doorsturen aan de serverzijde wordt ingeschakeld voor deze rapportsuite. Neem contact op met de klantenservice om dit toewijzingsprobleem op te lossen. |
| V: Zal de op de rapportreeks gebaseerde server kant door:sturen methode langzamer zijn dan de het volgen server gebaseerde server kant door:sturen? | Nee, de responstijd is gelijk. |
| V: Wat gebeurt er als we twee Experience Cloud Orgs (of AAM-instanties) hebben en gegevens willen delen tussen beide Experience Cloud Orgs? Kan ik een enkele Analytics-bewerking doorsturen naar meerdere Experience Cloud Orgs? | Nee. Als u gegevens wilt delen die zijn verzameld in het kader van de ene Experience Cloud Org naar een andere Experience Cloud Org, raden we u aan alle relevante soorten publiek van de ene instantie Audience Manager naar de andere te sturen via de publieksmarkt. |
| V: Zal het door:sturen van de server in om het even welke extra facturering in de Manager of Analyse van het Publiek resulteren? | In Analytics vindt geen extra facturering plaats. In Audience Manager worden doorgestuurde treffers op dezelfde manier behandeld als andere treffers en worden ze gefactureerd.  Daarom is het belangrijk om niet te hebben DIL en server-zijdoor:sturen tezelfdertijd wordt toegelaten, die dubbel-facturerings evenals gegevensduplicatie zou kunnen veroorzaken. |

>[!MORELIKETHIS]
>
>* [Server-kant doorsturen](/help/admin/admin/c-server-side-forwarding/ssf.md)

