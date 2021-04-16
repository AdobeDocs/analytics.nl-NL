---
description: Vereisten om de DFA gegevensschakelaar met Adobe Analytics te gebruiken.
keywords: DFA
title: Vereisten
feature: Data Connectors
uuid: b5f5e30c-e269-41a4-9236-5ddc404bfd94
exl-id: aa47c54f-d98a-47cb-806f-3f16d783c207
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 1%

---

# Vereisten{#prerequisites}

Ga als volgt te werk voordat u de Adobe Data Connectors-integratie voor DFA start:

* Bepaal of u wilt integreren met versie 1.5 van de integratie of wacht op versie 2.0. Dit besluit is afhankelijk van welke eigenschappen in uw DFA rekening worden gebruikt, en het tijdkader waarin u wilt integreren.
* Bepaal hoe DFA Advertisers aan Adobe Analytics rapportsuites in kaart zullen brengen. Bijvoorbeeld, als u veelvoudige Advertisers DFA en veelvoudige rapportsuites hebt, zult u moeten beslissen welke Advertisers met welk rapport passen.
* Voer de code van de gegevensinzameling van Adobe op alle pagina&#39;s uit u wilt volgen, gebruikend versie H.22 of later van de code van de gegevensinzameling.
* Ken Advertiser ID voor een DFA rekening die deel van de Configuratie uitmaakt van de Vullingslicht u wilt integreren. De integratie importeert automatisch alle Advertisers die zich binnen de Configuratie van de Vullinglight bevinden.
* Gebruikersnaam en wachtwoord voor uw DFA-account kennen.
* Koppel elke DFA-adverteerder aan slechts één Adobe Analytics-rapportsuite. Het etiketteren aan veelvoudige rapportreeksen wordt niet gesteund met de standaard Genesis integratie voor DFA.
* Voeg een klikthrough parameter van het vraagkoord aan de het landen pagina voor elke Plaatsing DFA toe die deel van de integratie zal uitmaken. Deze parameter van het vraagkoord is noodzakelijk om Click-through behoorlijk te tellen.
* Vorm uw Plaatsen DFA zodat zij bezoekers niet door veelvoudige domeinen opnieuw richten. Een Plaatsing mag respondenten bijvoorbeeld niet doorverwijzen naar een microsite die wordt gehost onder www.xyz.com als de microsite deze vervolgens doorstuurt naar een andere site, www.fgh.com. Als de campagnereactie meerdere domeinen omvat, kunnen doorklikken en mening-door gegevens worden opgeblazen en misleidend.
* Identificeer een douanevariabele in Rapporten &amp; Analytics om uw campagneinformatie te houden.
* Identificeer een Rapporten &amp; eVar van Analytics om mening-door informatie DFA op te slaan. Gebruik deze eVar alleen voor deze DFA-integratie.
* Identificeer de gebeurtenissen van Rapporten &amp; van de Analyse waar u Impressies wilt opslaan en gegevens klikken. U kunt de naam van deze gebeurtenissen desgewenst wijzigen.
* (Optioneel) Identificeer de gebeurtenissen Reports &amp; Analytics die DFA Cost-gegevens zullen opslaan. U kunt de naam van deze gebeurtenissen desgewenst wijzigen.
* (Optioneel) Identificeer een gebeurtenis voor aangepaste variabelen en succesmeldingen voor Rapporten en Analytics waarin DFA-fouten en -onderbrekingen worden opgeslagen. Deze variabelen helpen om problemen te diagnostiseren die zich met de integratie zouden kunnen voordoen.
* (Optioneel) Maak een speciaal e-mailaccount voor het ontvangen van informatie en meldingen in verband met de integratie van gegevensconnectors voor DFA.
