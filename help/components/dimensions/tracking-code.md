---
title: Trackingcode
description: De naam van de code of campagne voor bijhouden.
feature: Dimensions
exl-id: e4f70552-6946-4974-a9e2-928faf563ecd
source-git-commit: 6d0771f7b8779d7a9d3bcea73a430ba3a9093e3e
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 1%

---

# Trackingcode

De dimensie &#39;Tracking Code&#39; geeft een overzicht van de namen van trackingcodes op uw site. U kunt koppelingen met verschillende parameterwaarden voor queryreeksen op verschillende locaties op internet plaatsen. Deze dimensie helpt u begrijpen welke verbindingen het meest succesvol in het drijven van verkeer aan uw plaats waren.

Tekenreeksen voor bijhouden van code worden vaak toegevoegd in e-mails, advertenties, berichten op sociale media en andere marketingactiviteiten die uw organisatie gebruikt.

## Deze dimensie vullen met gegevens

Deze dimensie haalt gegevens van terug [`v0` querytekenreeks](/help/implement/validate/query-parameters.md) in afbeeldingsaanvragen. AppMeturement verzamelt deze gegevens met de [`campaign`](/help/implement/vars/page-vars/campaign.md) variabele.

## Dimension-items

Dimension-items bevatten de namen van trackingcodes op uw site. Uw organisatie bepaalt welke specifieke afmetingspunten u wilt gebruiken. Zie [Campagne bijhouden](/help/implement/use-cases/campaign-tracking.md) voor meer informatie .

## Vergelijk de het Volgen codedimensie met de kanalen van de Marketing die volgcodes verzamelen

Sommige gebruikers die de verwerkingsregels van het opstellings marketing kanaal vormen een regel die alle waarden neemt die in de het Volgen codedimensie worden gebruikt. Hoewel een uitstekende praktijk, zijn zij verschillend wegens inherente verwerking en architectuurverschillen. In de volgende lijst wordt uitgelegd waarom deze twee methoden, hoewel in één oogopslag gelijk, het gedrag van de attributie kunnen wijzigen.

### Eerdere kanalen in verwerkingsregels

Als de verwerkingsregels van marketingkanalen hoger zijn in de lijst, kan het voorkomen dat hits worden toegewezen aan het marketingkanaal voor volgcodes. Bijvoorbeeld:

1. U hebt &#39;Sociale netwerken&#39; ingesteld als de eerste regel en &#39;Trackingcodes&#39; als de tweede regel.
2. Een gebruiker plaatst een koppeling naar uw site met een trackingcode op een sociale-mediasite en verschillende vrienden klikken op die koppeling naar uw site.

Aangezien &#39;Sociale netwerken&#39; de eerste verwerkingsregel voor marketingkanalen is, verwijzen deze gebruikers naar het marketingkanaal &#39;Sociale netwerken&#39; en niet naar het marketingkanaal voor volgcodes.

### Andere marketingkanalen kunnen via laatste aanraking worden aangewezen

Als u werkt met een standaard dimensie voor het bijhouden van codes, hoeft u zich geen zorgen te maken over andere delen van de site die de kenmerken stelen. Bij marketingkanalen kan een gebruiker echter een andere regel gebruiken, waardoor een andere toewijzing wordt verkregen. Bijvoorbeeld:
1. U hebt &#39;Trackingcodes&#39; als eerste kanaal en &#39;Direct&#39; als tweede kanaal.
2. Een gebruiker arriveert eerst via een trackingcode naar uw site, maar verlaat vervolgens de site.
3. De volgende dag typen ze uw URL in hun adresbalk en kopen ze deze vervolgens.

In dit voorbeeld krijgt het marketingkanaal voor volgcodes geen laatste aanraakkrediet voor die aankoop. In plaats daarvan zou het naar het marketingkanaal &#39;Direct&#39; gaan.


### Vervalverschillen

Marketing-kanalen hebben een doorlopende afloop van de betrokkenheid van bezoekers gedurende 30 dagen, ongeacht of een kanaal is aangeraakt of niet. Voor volgcodes geldt een vervaldatum die is gebaseerd op het tijdstip waarop de variabele is ingesteld. Bijvoorbeeld:
1. U hebt een afloop van de betrokkenheid van bezoekers van 30 dagen en hebt ook de dimensie Tracking Code geconfigureerd om na 30 dagen te verlopen.
2. Een gebruiker komt aan uw plaats door een het volgen code aan. Ze surfen naar de site en vertrekken.
3. Drie weken later komen ze terug zonder trackingcode of marketingkanaal, en laten ze dan weer achter.
4. Twee weken later (vijf weken na hun eerste bezoek) komen ze terug zonder trackingcode of marketingkanaal en kopen ze vervolgens een aankoop.

De gebruiker heeft uiteindelijk meer dan 30 dagen aangeschaft, maar is nooit langer dan 30 dagen inactief geweest. In dit geval, zou u opbrengst zien die aan het Tracking codes marketing kanaal wordt toegewezen, maar niet voor de het Volgen codedimensie zelf.



