---
description: Voordat u deze integratie activeert, moet u de volgende items controleren op uw implementatie van Adobe Analytics® en uw e-mailsoftware.
title: Voordat u deze integratie activeert
uuid: fdc762bc-24e3-4c0a-904d-d4be2a4f3a20
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Voordat u deze integratie activeert {#before-you-activate-this-integration}

Voordat u deze integratie activeert, moet u de volgende items controleren op uw implementatie van Adobe Analytics® en uw e-mailsoftware.

Dit zorgt ervoor dat de juiste beste praktijken of voorwaarden aanwezig zijn voordat de activering plaatsvindt, wat zal resulteren in een optimale en succesvolle integratie.

## Vereisten voor Adobe Analytics{#adobe-analytics-requirements}

Lees de volgende informatie over de integratie van deze gegevensconnectors in relatie tot Adobe Analytics:

* **Specifiek voor rapportsuite:** Houd er rekening mee dat deze integratie specifiek is voor rapporten. Zorg ervoor dat u de gewenste rapportsuite hebt geselecteerd voordat u de integratie activeert en dat de rapportsuite gegevens bevat.
* **Beschikbare en geconfigureerde analytische variabelen:** Voor deze integratie zijn 10 aangepaste gebeurtenissen en 1 aangepaste eVar vereist. Zie Variabelen voor [analytische integratie](appfigures-before-activation.md#analytics-integration-variables).

* **Report Suite geïnitialiseerd met Live-gegevens:** Als u een gloednieuwe rapportsuite voor deze integratie maakt, moet deze enige gegevens (ten minste één hit) hebben ontvangen via de vereisten voor live tracering van appFigures. Als er geen live-gegevens zijn opgenomen, kan de rapportsuite geen geïntegreerde App Store-gegevens ontvangen.

* **Bestaande integratie met App Store:** Deze integratie vult gegevens voor 13 maanden terug. Neem contact op met de vertegenwoordiger van uw app om te voorkomen dat er overlappingen optreden met eerdere App store-gegevens die u mogelijk hebt. Laat ze weten op welke datum u de gegevens voor het laatst hebt ontvangen. appFigures past de back fill period dienovereenkomstig aan.

## appFigures-vereisten{#appfigures-requirements}

Lees de volgende informatie over de integratie van deze gegevensconnectors zoals deze betrekking heeft op appFigures:

* **Huidige klant van appFigures:** Voor deze integratie moet u zowel Adobe als appFigures gebruiken. Als u momenteel geen gebruiker van het Enterprise Plan appFigures bent, hebt u niet de benodigde informatie om de integratiewizard te voltooien. Ga naar appFigures op internet voor meer informatie.
* **appFigures-accountsleutel:** Een appFigures-accountsleutel is vereist om de appFigures-gegevensconnector te activeren. Deze accountsleutel kan worden gegenereerd in de sectie &quot;Invoegtoepassingen&quot;. Zie [Vorm de Integratie](../appfigures-overview/t-appfigures-integration.md) voor meer informatie.

* **Voltooiing** van gegevens: De gegevens voor downloaden, verkopen en classificeren worden elke dag gesynchroniseerd gedurende de afgelopen 7 dagen. Na 7 dagen worden de gegevens als definitief beschouwd en niet langer bijgewerkt.

## Prijzen{#pricing}

Deze integratie van gegevensconnectors omvat prijsoverwegingen die u zich van bewust moet zijn.

De volgende secties bevatten meer informatie:

### Prijsoverwegingen van Adobe {#section-2d1c79c895a5479bad8fdd97961ba6a3}

Er zijn momenteel geen kosten om deze integratie te activeren. Nochtans, zou u een lichte toename van de servervraag wegens de invoer van gegevensbronnen kunnen zien.

### prijsoverwegingen appFigures {#section-c6afad08c34b43e3a7a3637eea3328c3}

Er zijn momenteel geen kosten verbonden aan deze integratie. Deze integratie is momenteel alleen beschikbaar voor Enterprise-klanten. Neem [contact op met appFigures](https://appfigures.com/support/contact) voor meer informatie.

## Variabelen voor analytische integratie{#analytics-integration-variables}

De integratie van gegevensconnectors voor appFigures gebruikt variabelen van de Analyse om diverse appFigures metriek te volgen.

In de volgende tabel worden de variabelen Analytics beschreven die automatisch zijn geactiveerd voor de integratie appFigures.

### Vereiste variabelen {#section-3ca8dc46bab0436cba0c9ef827c8356a}

>[!NOTE] Deze integratie gebruikt specifieke variabelen voor gegevens van de toepassingsopslag, zodat te hoeven u om geen variabelen en gebeurtenissen van de douanehandel toe te wijzen.

| Type variabele | Naam | Populatiemethode | Beschrijving |
|---|---|---|---|
| eVar | Object-id App Store | Geïmporteerd uit appFigures. | Configureer deze eVar met Bezoek vervaldatum, Meest recente toewijzing en elementaire subrelaties. |
| gebeurtenis (numeriek) | Downloads App Store | Geïmporteerd uit appFigures. | Het aantal mobiele toepassingsdownloads. |
| gebeurtenis (numeriek) | Aankopen App Store (in app) | Geïmporteerd uit appFigures. | Het aantal aankopen en abonnementen in de app. |
| gebeurtenis (numeriek) | App Store Rank | Geïmporteerd uit appFigures. | Hiermee definieert u de berekende metrische gemiddelde appFigures. Niet rechtstreeks gebruikt. |
| gebeurtenis (numeriek) | Rank Divisor App Store | Geïmporteerd uit appFigures. | Hiermee definieert u de berekende metrische gemiddelde appFigures. Niet rechtstreeks gebruikt. |
| gebeurtenis (numeriek) | Classificatie App Store | Geïmporteerd uit appFigures. | Hiermee definieert u de berekende metrische gemiddelde appFigures. Niet rechtstreeks gebruikt. |
| gebeurtenis (numeriek) | Beoordelingsdivisie voor App Store | Geïmporteerd uit appFigures. | Hiermee definieert u de berekende metrische gemiddelde appFigures. Niet rechtstreeks gebruikt. |
| event (valuta) | Opbrengsten van App Store (in app) | Geïmporteerd uit appFigures. | Het bedrag van in-app inkomsten min de opslagkosten. |
| event (valuta) | Opbrengst van App Store (één korting) | Geïmporteerd uit appFigures. | Totale opbrengsten uit aankopen van apps minus de winkelkosten. |
| event (valuta) | Royalty&#39;s voor App Store (in app) | Geïmporteerd uit appFigures. | Niet gebruikt |
| event (valuta) | Royalty&#39;s App Store (één korting) | Geïmporteerd uit appFigures. | Niet gebruikt |
