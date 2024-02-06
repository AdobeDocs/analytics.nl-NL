---
description: Meer informatie over de voordelen en beperkingen van het gebruik van de optie Tijdstempels optioneel.
keywords: Analyseimplementatie
title: Tijdstempels optioneel
topic-fix: Developer and implementation
feature: Implementation Basics
exl-id: c6a232d1-d7ce-4f21-9e8a-45703992bc6e
source-git-commit: d3d5b01fe17f88d07a748fac814d2161682837c2
workflow-type: tm+mt
source-wordcount: '607'
ht-degree: 0%

---

# Tijdstempels optioneel

Meer informatie over de voordelen en beperkingen van het gebruik van de optie Tijdstempels optioneel.

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/335740/?quality=12)

Tijdstempels optioneel is de standaardinstelling voor alle nieuwe rapportsuites.

* Combineer tijdstempels en niet-tijdstempels gegevens in de zelfde globale rapportreeks.
* Verzend tijdstempelgegevens van een mobiele app naar een algemene rapportsuite.
* Upgrade apps om tijdstempels te gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken.

>[!NOTE]
>
>Tijdstempels Optioneel is de standaardinstelling voor alle nieuwe rapportsuites die worden gegenereerd op basis van een sjabloon. De nieuwe rapportreeksen die van een bestaande rapportreeks worden gekopieerd zullen montages van origineel erven.

Zie [Tijdstempels optioneel](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/timestamp-optional.html) voor extra opstellingsinformatie.

## Tijdstempels optioneel: tijdstempelgegevens en niet-tijdstempelgegevens integreren {#integrate}

Met de functie Tijdstempels optioneel kunt u gegevens zonder tijdstempel combineren met gegevens met een tijdstempel zonder dat er gegevensverlies optreedt. Offlinegegevens met tijdstempels die op een mobiel apparaat worden gegenereerd, kunnen worden gecombineerd met live, niet-tijdstempelgegevens van een webpagina, of worden geïntegreerd met gegevens van elk platform via een tijdstempelaanroep aan de clientzijde.

* **Tijdstempelgegevens**. Tijdstempelgegevens aan de clientzijde worden vastgelegd en rechtstreeks verzonden met de apparaatgegevens met gebruik van tijdstempelvariabelen aan de clientzijde: Javascript op een webpagina of een mobiele SDK-aanroep ( [!DNL offlineEnabled=true]) in een mobiele app.
* **Niet-tijdstempelgegevens**. Met Adobe wordt een tijdstempel ingesteld op gegevens zonder tijdstempel in een rapportsuite wanneer de gegevens op de verzamelingsservers worden geplaatst.

Een rapportsuite kan een van de volgende tijdstempelinstellingen hebben:

* Tijdstempels niet toegestaan (ondersteuning voor bezoekerID instellen)
* Vereiste tijdstempels (instellen van bezoeker-id wordt niet ondersteund)
* Tijdstempels optioneel (instelling van bezoeker-id wordt ondersteund, maar niet bij treffers met tijdstempels)

## Informatie over Tijdstempels Optionele functies {#features}

Met Tijdstempels optioneel kunt u meerdere rapportsuites integreren en rapporteren, met of zonder tijdstempels aan de clientzijde. Met Tijdstempels optioneel kunt u uw app bijwerken en tijdstempels gebruiken terwijl u nog steeds niet-tijdstempelde gegevens uit de vorige app gebruikt.

| In vorige releases... | Daarnaast.. |
|--- |--- |
| Gegevens met tijdstempel kunnen niet worden verzonden naar een niet-tijdstempelde algemene rapportsuite. Dientengevolge, werden de raakgegevens die van off-line apparaten werden verzonden gelaten vallen toen het toevoegen aan een niet-timestamped rapportreeks. <br/><br/>Dit betekent dat raakgegevens die zijn verzonden vanuit offlinegegevens, zijn verwijderd tijdens het toevoegen aan een niet-tijdstempelrapportsuite. | Voor het bijwerken van een app voor het verzamelen en gebruiken van tijdstempels hebt u een nieuwe rapportsuite nodig. <br/>U kunt niet opslaan naar de bestaande rapportsuite of bestaande gegevens integreren wanneer u uw app bijwerkt om tijdstempels te gebruiken. |

**Met Tijdstempels optioneel**, kunt u niet-tijdstempelgegevens van een live website integreren met offlinegegevens van mobiele apparaten, of uw niet-tijdstempelapp bijwerken naar een app met een tijdstempel.

## Gegevens combineren in een Global Report Suite {#combine}

Het combineren van gegevens in een globale rapportreeks kan op veelvoudige manieren, met inbegrip van multi-suite het etiketteren, de regels van Vista, en ingevoerde partijdossiers uit off-line bronnen worden gedaan.

>[!IMPORTANT]
>
>Plan zorgvuldig het ontwerp voor elke reeks componentengegevens zodat de combinatie in een globale rapportreeks steek houdt.

## Aanbevolen procedures bij het gebruik van tijdstempels {#best-pratices}

Hieronder vindt u best practices en een aantal vereisten en beperkingen die u in acht moet nemen wanneer u tijdstempels met gegevens zonder tijdstempel integreert.

* Over het algemeen moeten tijdstempels voor een bepaalde bezoeker of een bepaald bezoek in chronologische volgorde bij de Adobe aankomen.

  Gegevens die niet op volgorde staan, kunnen gegevens bevatten die te laat aankomen bij het verzamelen van offlinegegevens en laat aankomen, of uit-of-synchronisatieklokken op mobiele offlineapparaten. Buiten-de-ordegegevens kunnen tijdberekeningen (zoals tijd bestede waarden), attributie (eVar persistence), bezoekaantal/bezoek tellingen, en het kleven rapporten negatief beïnvloeden.

* Tijdstempels gebruiken wanneer u een [s.bezoekerID](/help/implement/vars/config-vars/visitorid.md) wordt niet aanbevolen. Dit kan leiden tot gegevens die niet op volgorde staan.

* Hybride apps die bestaan uit een app (tijdstempeling, offlinegegevens) die een webbrowser opent (niet-tijdstempels, live gegevens), mogen geen tijdstempels gebruiken. Dit leidt tot een onjuiste rapportage van de sessie.

  Bovendien mogen hybride apps geen bezoekers-id instellen.
