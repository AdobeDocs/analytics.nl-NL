---
description: Meer informatie over de voordelen en beperkingen van het gebruik van de optie Tijdstempels optioneel.
keywords: Analytics Implementation
title: Tijdstempels optioneel gebruiken
topic: Developer and implementation
uuid: 956aaa16-6ffa-4b63-b022-a659f5143e00
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Tijdstempels optioneel gebruiken

Meer informatie over de voordelen en beperkingen van het gebruik van de optie Tijdstempels optioneel.

Tijdstempels optioneel is de standaardinstelling voor alle nieuwe rapportsuites.

* Combineer tijdstempels en niet-tijdstempels gegevens in de zelfde globale rapportreeks.
* Verzend tijdstempelgegevens van een mobiele app naar een algemene rapportsuite.
* Upgrade apps om tijdstempels te gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken.

>[!NOTE] Tijdstempels Optioneel is de standaardinstelling voor alle nieuwe rapportsuites die worden gegenereerd op basis van een sjabloon. De nieuwe rapportreeksen die van een bestaande rapportreeks worden gekopieerd zullen montages van origineel erven.

Zie [Tijdstempels Optioneel](https://marketing.adobe.com/resources/help/en_US/reference/timestamp-optional.html) voor aanvullende instellingsinformatie.

## Tijdstempels optioneel: Gegevens met tijdstempel en zonder tijdstempel integreren {#section_BF17CB593044462B993FD0D28EA56518}

Met de functie Tijdstempels optioneel kunt u gegevens zonder tijdstempel combineren met gegevens met een tijdstempel zonder dat er gegevensverlies optreedt. Offlinegegevens met tijdstempels die op een mobiel apparaat worden gegenereerd, kunnen worden gecombineerd met live, niet-tijdstempelgegevens van een webpagina, of worden geïntegreerd met gegevens van elk platform via een tijdstempelaanroep aan de clientzijde.

* **Tijdstempelgegevens**. Tijdstempelgegevens aan de clientzijde worden vastgelegd en rechtstreeks verzonden met de apparaatgegevens met gebruik van tijdstempelvariabelen aan de clientzijde: JavaScript op een webpagina of met een mobiele SDK-aanroep ( [!DNL offlineEnabled=true]) in een mobiele app.
* **Niet-tijdstempelgegevens**. Adobe stelt een tijdstempel in voor niet-tijdstempelgegevens in een rapportsuite wanneer de gegevens op de verzamelingsservers worden geplaatst.


Een rapportsuite kan een van de volgende tijdstempelinstellingen hebben:

* Tijdstempels niet toegestaan (ondersteuning voor bezoekerID instellen)
* Vereiste tijdstempels (instellen van bezoeker-id wordt niet ondersteund)
* Tijdstempels optioneel (instelling van bezoeker-id wordt ondersteund, maar niet bij treffers met tijdstempels)

## Informatie over optionele tijdstempels {#section_63B2FA9A2AB24B3993E84D2C2B4BF2CE}

Met Tijdstempels optioneel kunt u meerdere rapportsuites integreren en rapporteren, met of zonder tijdstempels aan de clientzijde. Met Tijdstempels optioneel kunt u uw app bijwerken en tijdstempels gebruiken terwijl u nog steeds niet-tijdstempelde gegevens uit de vorige app gebruikt.

| In vorige releases... | Daarnaast.. |
|--- |--- |
| Gegevens met tijdstempel kunnen niet worden verzonden naar een niet-tijdstempelde algemene rapportsuite. Dientengevolge, werden de raakgegevens die van off-line apparaten werden verzonden gelaten vallen toen het toevoegen aan een niet-timestamped rapportreeks. <br/><br/>Dit betekent dat raakgegevens die zijn verzonden vanuit offlinegegevens, zijn verwijderd tijdens het toevoegen aan een niet-tijdstempelrapportsuite. | Voor het bijwerken van een app voor het verzamelen en gebruiken van tijdstempels hebt u een nieuwe rapportsuite nodig. <br/>U kunt niet opslaan naar de bestaande rapportsuite of bestaande gegevens integreren wanneer u uw app bijwerkt om tijdstempels te gebruiken. |

**Met Tijdstempels optioneel** kunt u niet-tijdstempelgegevens van een live website integreren met offlinegegevens van mobiele apparaten, of uw app zonder tijdstempel bijwerken naar een app met een tijdstempel.

## Gegevens combineren in een Global Report Suite {#section_5BE3BDF56007402BB1F5C3144D5FE1E0}

Het combineren van gegevens in een globale rapportreeks kan op veelvoudige manieren, met inbegrip van multi-suite het etiketteren, de regels van Vista, en ingevoerde partijdossiers uit off-line bronnen worden gedaan.

>[!IMPORTANT] Plan zorgvuldig het ontwerp voor elke reeks componentengegevens zodat de combinatie in een globale rapportreeks steek houdt.

## Aanbevolen procedures bij gebruik van tijdstempels {#section_9436394E5D7E4F8A8B369B6D11BB2B2B}

Hieronder vindt u best practices en een aantal vereisten en beperkingen die u in acht moet nemen wanneer u tijdstempels met gegevens zonder tijdstempel integreert.

* Over het algemeen moeten tijdstempels voor een bepaalde bezoeker of een bepaald bezoek in chronologische volgorde bij Adobe aankomen.

   Gegevens die niet op volgorde staan, kunnen gegevens bevatten die te laat aankomen bij het verzamelen van offlinegegevens en laat aankomen, of uit-of-synchronisatieklokken op mobiele offlineapparaten. Gegevens die buiten de bestelling vallen, kunnen een negatief effect hebben op tijdberekeningen (zoals gebruikte waarden voor de tijd), attributie (persistentie van de eVar), het aantal bezoekers/bezoekers en tekenrapporten.

* Het wordt niet aanbevolen tijdstempels te gebruiken wanneer u een [s.bezoekerID](https://marketing.adobe.com/resources/help/en_US/sc/implement/visid_custom.html) instelt. Dit kan leiden tot gegevens die niet op volgorde staan.

* Hybride apps die bestaan uit een app (tijdstempeling, offlinegegevens) die een webbrowser opent (niet-tijdstempels, live gegevens), mogen geen tijdstempels gebruiken. Dit leidt tot een onjuiste rapportage van de sessie.

   Bovendien mogen hybride apps geen bezoekers-id instellen.
