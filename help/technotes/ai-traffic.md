---
description: Begrijp hoe te om over verkeer van AI praatbots te melden
title: Verkeer van AI-chatbots analyseren
feature: Metrics, Data Configuration and Collection
source-git-commit: d16214865a037efe41b9f95682758daa577a12ed
workflow-type: tm+mt
source-wordcount: '638'
ht-degree: 0%

---

# Analyseer verkeer van conversatieAI hulpmiddelen

Adobe Analytics biedt hulpprogramma&#39;s voor het analyseren van AI-verkeer op uw website.

Wanneer het analyseren van AI verkeer, moet u eerst de types van AI verkeer begrijpen die kunnen voorkomen en welke types drukken produceren. Vervolgens kunt u het verkeer in Analysis Workspace analyseren.

## Inzicht in AI-verkeer

### De typen AI-verkeer begrijpen

AI-verkeer op uw website kan plaatsvinden in een van de volgende omstandigheden:

* **tijdens pretraining**: komt zelden voor, wanneer de inhoud van uw website wordt geschraapt en in de AI opleidingsgegevens wordt opgenomen.

* **wanneer het antwoorden aan op bestelling herinneringen**: komt het moment voor de gebruiker AI met een vraag veroorzaakt en AI praatbot antwoordt. De AI-chatbot voert een webzoekopdracht uit en de inhoud van uw website is opgenomen in het antwoord. (Dit type interacties wordt soms ook wel &#39;Retrieval-Augmented Generation (RAG)&#39; genoemd.)

  Sommige AI-chatbotreacties bevatten koppelingen naar het bronmateriaal op uw site en andere niet.

* **wanneer het uitvoeren van agentische werkschema&#39;s**: komt voor wanneer een AI agent uw website bezoekt wanneer het klikken door een reeks Web-pagina&#39;s in browser om op een gebruikersverzoek te antwoorden. In dit geval handelt de AI als agent voor de gebruiker die het verzoek indiende.

### Begrijp wanneer de klappen voor verkeer AI worden geproduceerd

Er wordt een hit gegenereerd op een webpagina wanneer JavaScript op de pagina wordt uitgevoerd. Afhankelijk van het type AI-verkeer dat op uw site plaatsvindt, wordt JavaScript mogelijk wel of niet uitgevoerd.

| AI-verkeerstype | Hiermee worden treffers gegenereerd | Overwegingen |
|---------|----------|---------|
| **Pretraining** | Ja | Deze taken worden tijdens de voortraining gegenereerd wanneer de inhoud van uw website in de AI wordt opgenomen. Voortraining komt echter zelden voor en inhoud die deel uitmaakt van de voortraining van een AI kan in toekomstige reacties telkens opnieuw worden gebruikt zonder dat u nog meer resultaten op uw website hoeft te genereren. <p>Met andere woorden, een enkele hit die optreedt tijdens de voortraining van een AI kan telkens opnieuw worden gebruikt voor meerdere reacties op aanvraag zonder dat er extra resultaten op uw website worden gegenereerd.</p><p>Voor informatie over hoe te om dit type van AI verkeer in Analysis Workspace te analyseren, zie [ AI verkeer analyseren gebruikend bot opsporing ](#analyze-ai-traffic-using-bot-detection).</p> |
| **op bestelling herinneringen** | Nee | De AI-reactie genereert geen treffers omdat de reactie een combinatie van:<ul><li>De vooraf opgeleide gegevens <br/> Informatie is reeds inbegrepen in de vooraf opgeleide kennis van AI, zodat voert AI geen JavaScript op pagina&#39;s uit.</li><li>Op bestelling Webonderzoek <br/> vindt slechts onbewerkte HTML van de Web-pagina tijdens het Webonderzoek, zodat voert AI geen JavaScript op pagina&#39;s uit.</li></ul> |
| **het materiaalverbindingen van Source in AI reacties** | Ja | Deze knoppen worden gegenereerd wanneer een gebruiker op de koppeling naar het bronmateriaal klikt dat in de AI-reactie is opgenomen. Er wordt geen hit gegenereerd als een koppeling is opgenomen in de reactie en de gebruiker niet op de koppeling heeft geklikt. <p>Sommige AI-chatbotreacties bevatten koppelingen naar het bronmateriaal en andere niet. </p><p>Voor informatie over hoe te om dit type van AI verkeer in Analysis Workspace te analyseren, zie [ AI verkeer door Verwijzertype ](#analyze-ai-traffic-by-referrer-type) analyseren.</p> |
| **Agentische werkschema&#39;s** | Ja | Deze onderbrekingen worden op elke pagina gegenereerd wanneer de AI-agent namens de gebruiker door de workflow klikt. <p>Voor informatie over hoe te om dit type van AI verkeer in Analysis Workspace te analyseren, zie [ AI verkeer door Verwijzertype ](#analyze-ai-traffic-by-referrer-type) analyseren.</p> |

## AI-verkeer in Analysis Workspace analyseren

### AI-verkeer analyseren op verwijzertype

Met de dimensie Type referentie in Analysis Workspace kunt u de volgende typen AI-verkeer analyseren:

* Source-materiaalkoppelingen in AI-reacties

* Agentische workflows

De het type van Referteur dimensie omvat het [ Conversational AI hulpmiddelpunt ](/help/components/dimensions/referrer-type.md#conversational-ai-tools). Dit item bevat een vooraf gedefinieerde lijst met AI-chatbots.

Voor meer informatie, zie [ het type van Referateur ](/help/components/dimensions/referrer-type.md).

### AI-verkeer analyseren met behulp van botdetectie

U kunt beide detectie in Analysis Workspace gebruiken om AI-verkeer te analyseren dat afkomstig is van voortraining.

