---
title: Trackingcode
description: De naam van de code of campagne voor bijhouden.
translation-type: tm+mt
source-git-commit: 178e372e63c436268a1f7028d986504983430b2f
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 1%

---


# Trackingcode

De dimensie &#39;Tracking Code&#39; geeft een overzicht van de namen van trackingcodes op uw site. Deze dimensie wordt typisch verzameld gebruikend de parameters van het vraagkoord. U kunt koppelingen met verschillende parameterwaarden voor queryreeksen op verschillende locaties op internet plaatsen. Deze dimensie meldt welke verbindingen het meest succesvol in het drijven van verkeer aan uw plaats waren.

## Deze dimensie vullen met gegevens

Deze dimensie wint gegevens van het [`v0` vraagkoord](/help/implement/validate/query-parameters.md) in beeldverzoeken terug. AppMeturement verzamelt deze gegevens met behulp van de [`campaign`](/help/implement/vars/page-vars/campaign.md) variabele.

## Dimension-items

Dimension-items bevatten de namen van trackingcodes op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken.

## Vergelijk de het Volgen codedimensie met de kanalen van de Marketing die volgcodes verzamelen

Sommige gebruikers die de verwerkingsregels van het opstellings marketing kanaal vormen een regel die alle waarden neemt die in de het Volgen codedimensie worden gebruikt. Hoewel een uitstekende praktijk, zijn zij verschillend wegens inherente verwerking en architectuurverschillen. In de volgende lijst wordt uitgelegd waarom deze twee dimensies, hoewel ze in één oogopslag vergelijkbaar zijn, niet met elkaar kunnen worden vergeleken.

* **Eerdere kanalen in verwerkingsregels**: Als de verwerkingsregels van marketingkanalen hoger zijn in de lijst, kan het voorkomen dat hits worden toegewezen aan het marketingkanaal voor volgcodes. Bijvoorbeeld:

   1. U hebt &#39;Sociale netwerken&#39; ingesteld als de eerste regel en &#39;Trackingcodes&#39; als de tweede regel.
   2. Een gebruiker plaatst een koppeling naar uw site met een trackingcode op een sociale-mediasite en verschillende vrienden klikken op die koppeling naar uw site.

   Aangezien &#39;Sociale netwerken&#39; de eerste verwerkingsregel voor marketingkanalen is, verwijzen deze gebruikers naar het marketingkanaal &#39;Sociale netwerken&#39; en niet naar het marketingkanaal voor volgcodes.
* **Andere marketingkanalen kunnen kenmerk** stelen: Als u werkt met een standaard dimensie voor het bijhouden van codes, hoeft u zich geen zorgen te maken over andere delen van de site die de kenmerken stelen. Bij marketingkanalen kan een gebruiker echter een andere regel gebruiken, waardoor een andere toewijzing wordt verkregen. Bijvoorbeeld:
   1. U hebt &#39;Trackingcodes&#39; als eerste kanaal en &#39;Direct&#39; als tweede kanaal.
   2. Een gebruiker arriveert eerst via een trackingcode naar uw site, maar verlaat vervolgens de site.
   3. De volgende dag typen ze uw URL in hun adresbalk en kopen ze deze vervolgens.

   Het marketingkanaal voor volgcodes krijgt geen laatste aanraakkrediet voor die aankoop. In plaats daarvan zou het naar het marketingkanaal &#39;Direct&#39; gaan.
* **Vervalverschillen**: Marketing-kanalen hebben een doorlopende afloop van de betrokkenheid van bezoekers gedurende 30 dagen, ongeacht of een kanaal is aangeraakt of niet. Voor volgcodes geldt een vervaldatum die is gebaseerd op het tijdstip waarop de variabele is ingesteld. Bijvoorbeeld:
   1. U hebt een afloop van de betrokkenheid van bezoekers van 30 dagen en hebt ook de dimensie Tracking Code geconfigureerd om na 30 dagen te verlopen.
   2. Een gebruiker komt aan uw plaats door een het volgen code aan. Ze surfen naar de site en vertrekken.
   3. Drie weken later komen ze terug zonder trackingcode of marketingkanaal, en laten ze dan weer achter.
   4. Twee weken later (vijf weken na hun eerste bezoek) komen ze terug zonder trackingcode of marketingkanaal en kopen ze vervolgens een aankoop.
   De gebruiker heeft uiteindelijk meer dan 30 dagen aangeschaft, maar is nooit langer dan 30 dagen inactief geweest. U zou opbrengst zien die aan het Tracking codes marketing kanaal wordt toegeschreven, maar niet voor de standalone dimensie.
