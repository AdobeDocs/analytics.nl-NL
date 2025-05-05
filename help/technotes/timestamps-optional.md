---
description: Meer informatie over de voordelen en beperkingen van het gebruik van de optie Tijdstempels optioneel.
keywords: Analyseimplementatie
title: Tijdstempels optioneel
topic-fix: Developer and implementation
feature: Implementation Basics
exl-id: c6a232d1-d7ce-4f21-9e8a-45703992bc6e
source-git-commit: 59757bf8953c9cd7bc8dff89f29c13396b70696d
workflow-type: tm+mt
source-wordcount: '600'
ht-degree: 0%

---

# Tijdstempels optioneel

Meer informatie over de voordelen en beperkingen van het gebruik van de optie Tijdstempels optioneel.

<!-- Hide video as it is not adding a lot according to feedback from customer in feedback report January 2025.

>[!BEGINSHADEBOX]

See ![VideoCheckedOut](/help/assets/icons/VideoCheckedOut.svg) [Timestamps Optional](https://video.tv.adobe.com/v/335740?quality=12&learn=on){target="_blank"} for a demo video.

>[!ENDSHADEBOX]
-->


Tijdstempels optioneel is de standaardinstelling voor alle nieuwe rapportsuites.

* Combineer tijdstempels en niet-tijdstempels gegevens in de zelfde globale rapportreeks.
* Verzend tijdstempelgegevens van een mobiele app naar een algemene rapportsuite.
* Upgrade apps om tijdstempels te gebruiken zonder dat u een nieuwe rapportsuite hoeft te maken.

>[!NOTE]
>
>Tijdstempels Optioneel is de standaardinstelling voor alle nieuwe rapportsuites die worden gegenereerd op basis van een sjabloon. De nieuwe rapportreeksen die van een bestaande rapportreeks worden gekopieerd zullen montages van origineel erven.

Zie [ Tijdstempels Facultatieve ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/timestamp-optional.html?lang=nl-NL) voor extra opstellingsinformatie.

## Tijdstempels optioneel: tijdstempelgegevens en niet-tijdstempelgegevens integreren {#integrate}

Met de functie Tijdstempels optioneel kunt u gegevens zonder tijdstempel combineren met gegevens met een tijdstempel zonder dat er gegevensverlies optreedt. Offlinegegevens met tijdstempels die op een mobiel apparaat worden gegenereerd, kunnen worden gecombineerd met live, niet-tijdstempelgegevens van een webpagina, of worden geïntegreerd met gegevens van elk platform via een tijdstempelaanroep aan de clientzijde.

* **gegevens van de tijdstempel**. Tijdstempelgegevens aan de clientzijde worden vastgelegd en rechtstreeks verzonden met de apparaatgegevens met gebruik van tijdstempelvariabelen aan de clientzijde: Javascript op een webpagina of een mobiele SDK-aanroep ( [!DNL offlineEnabled=true] ) in een mobiele app.
* **niet-timestamp gegevens**. Met Adobe wordt een tijdstempel ingesteld op gegevens zonder tijdstempel in een rapportsuite wanneer de gegevens op de verzamelingsservers worden geplaatst.

Een rapportsuite kan een van de volgende tijdstempelinstellingen hebben:

* Tijdstempels niet toegestaan (ondersteuning voor bezoekerID instellen)
* Vereiste tijdstempels (instellen van bezoeker-id wordt niet ondersteund)
* Tijdstempels optioneel (instelling van bezoeker-id wordt ondersteund, maar niet bij treffers met tijdstempels)

## Informatie over Tijdstempels Optionele functies {#features}

Met Tijdstempels optioneel kunt u meerdere rapportsuites integreren en rapporteren, met of zonder tijdstempels aan de clientzijde. Met Tijdstempels optioneel kunt u uw app bijwerken en tijdstempels gebruiken terwijl u nog steeds niet-tijdstempelde gegevens uit de vorige app gebruikt.

| In vorige releases... | Daarnaast.. |
|--- |--- |
| Gegevens met tijdstempel kunnen niet worden verzonden naar een niet-tijdstempelde algemene rapportsuite. Dientengevolge, werden de raakgegevens die van off-line apparaten werden verzonden gelaten vallen toen het toevoegen aan een niet-timestamped rapportreeks. <br/><br/> dientengevolge, raakgegevens die van off-line gegevens werden verzonden werden gelaten vallen toen het toevoegen aan een niet-timestamped rapportreeks. | Voor het bijwerken van een app voor het verzamelen en gebruiken van tijdstempels hebt u een nieuwe rapportsuite nodig. <br/> u kon niet aan de bestaande rapportreeks bewaren of bestaande gegevens integreren wanneer het bijwerken van uw app om timestamps te gebruiken. |

**met Facultatieve Tijdstempels**, kunt u niet-timestamped gegevens van een levende website met off-line gegevens van mobiele apparaten integreren, of uw niet-timestamped app aan een timestamped app bijwerken.

## Gegevens combineren in een Global Report Suite {#combine}

Het combineren van gegevens in een globale rapportreeks kan op veelvoudige manieren, met inbegrip van multi-suite het etiketteren, de regels van Vista, en ingevoerde partijdossiers uit off-line bronnen worden gedaan.

>[!IMPORTANT]
>
>Plan zorgvuldig het ontwerp voor elke reeks componentengegevens zodat de combinatie in een globale rapportreeks steek houdt.

## Aanbevolen procedures bij het gebruik van tijdstempels {#best-pratices}

Hieronder vindt u best practices en een aantal vereisten en beperkingen die u in acht moet nemen wanneer u tijdstempels met gegevens zonder tijdstempel integreert.

* Over het algemeen moeten tijdstempels voor een bepaalde bezoeker of een bepaald bezoek in chronologische volgorde bij de Adobe aankomen.

  Gegevens die niet op volgorde staan, kunnen gegevens bevatten die te laat aankomen bij het verzamelen van offlinegegevens en laat aankomen, of uit-of-synchronisatieklokken op mobiele offlineapparaten. Buiten-de-ordegegevens kunnen tijdberekeningen (zoals tijd bestede waarden), attributie (eVar persistence), bezoekaantal/bezoek tellingen, en het kleven rapporten negatief beïnvloeden.

* Het gebruiken van timestamps wanneer het plaatsen van a [ s.bezoekorID ](/help/implement/vars/config-vars/visitorid.md) wordt niet geadviseerd. Dit kan leiden tot gegevens die niet op volgorde staan.

* Hybride apps die bestaan uit een app (tijdstempeling, offlinegegevens) die een webbrowser opent (niet-tijdstempels, live gegevens), mogen geen tijdstempels gebruiken. Dit leidt tot een onjuiste rapportage van de sessie.

  Bovendien mogen hybride apps geen bezoekers-id instellen.
