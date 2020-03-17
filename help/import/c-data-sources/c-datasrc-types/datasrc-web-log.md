---
description: Met webloggegevensbronnen kunt u standaard webserverlogbestanden importeren.
subtopic: Data sources
title: Weblogbestand
topic: Developer and implementation
uuid: a0efed57-6d1b-43d8-97ce-dc31009805e0
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Weblogbestand

Met webloggegevensbronnen kunt u standaard webserverlogbestanden importeren.

De volgende algemene logbestandstypen voor webservers worden ondersteund:

| Kolomnaam | Beschrijving |
|--- |--- |
| NCSA Common Log | Standaardinstellingen Apache |
| NCSA uitgebreid (gecombineerd) | Apache |
| W3C Extended-log | Gebruikt door IIS 4.0 en later |
| Microsoft IIS-logboek | Gebruikt door IIS 3.0 en vroeger |

De primaire gebieden van het logboekdossier die de gegevensbronnen processen omvatten IP Adres, Datum/Tijd van het verzoek, en URL. In een paar gevallen, zoals het Uitgebreide formaat NCSA, verwerkt de Gegevensbronnen ook de Referrer en de gebieden van de Agent van de Gebruiker.

U kunt webloggegevens weergeven met standaard marketingrapporten voor paginaweergaven, bezoeken en bezoekers. Omdat de rapportmetriek hoofdzakelijk op koekjes gebaseerd zijn, en de logboeken van de Webserver gebaseerd zijn op het IP adres, adviseert Adobe het invoeren van de logboeken van de Webserver in een afzonderlijke rapportreeks specifiek voor dat doel.

Raadpleeg de documentatie bij de webserver voor meer informatie over uw logbestanden van de webserver.
