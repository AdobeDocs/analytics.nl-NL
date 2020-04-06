---
description: U kunt gegevens van specifieke IP adressen, zoals interne website activiteiten, plaats het testen en werknemersgebruik, van uw rapporten uitsluiten. Het uitsluiten van gegevens verbetert rapportnauwkeurigheid door IP adresgegevens uit te sluiten. Bovendien, kunt u gegevens uit ontkenning van de dienst of andere kwaadwillige gebeurtenissen verwijderen die rapportgegevens kunnen scheeftrekken. U kunt uitsluiting configureren of uw firewall gebruiken.
title: Exclusief door IP Adres
topic: Admin tools
uuid: 1ed6105f-e7c5-4c4f-b8f4-e5f66d0824bb
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Exclusief door IP Adres

U kunt gegevens van specifieke IP adressen, zoals interne website activiteiten, plaats het testen en werknemersgebruik, van uw rapporten uitsluiten. Het uitsluiten van gegevens verbetert rapportnauwkeurigheid door IP adresgegevens uit te sluiten. Bovendien, kunt u gegevens uit ontkenning van de dienst of andere kwaadwillige gebeurtenissen verwijderen die rapportgegevens kunnen scheeftrekken. U kunt uitsluiting configureren of uw firewall gebruiken.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Exclude by IP]**

>[!NOTE] Hits die door IP adres worden uitgesloten worden gefactureerd als [servervraag](https://marketing.adobe.com/resources/help/en_US/reference/primary_server_calls.html).

## Uitsluiten op cookie {#section_FB5A20AB5E514DA6BC596CC67F6A3A4C}

Hiermee kunt u uitsluiten dat deze computer in uw account wordt bijgehouden. Als u ervoor kiest de computer uit te sluiten, worden alle gegevens die op de computer zijn gegenereerd, niet geteld.

Met deze functie kunnen u en uw collega&#39;s uw site bezoeken zonder uw verkeersgegevens te scheeftrekken. U kunt deze eigenschap willen gebruiken als u geen statisch IP adres (zoals het hebben van een dial-up verbinding van Internet door een dienstverlener) hebt en van uw rekeningsgegevens zou willen uitsluiten.

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL Add CNAME] | Hiermee genereert u een uitschakelkoppeling waarmee u uw domein kunt uitsluiten. Neem voor hulp contact op met de ondersteunde gebruikers van uw bedrijf. <br>Uw verkeer kan van het melden in uw rapportreeksen worden uitgesloten door de optieoutpagina van uw bedrijf te bezoeken en uw browser van meting uit te sluiten. <br>Als uw implementatie cookies van derden gebruikt, is de pagina die u niet wilt gebruiken [hier](https://democorp.112.2o7.net/optout.html?locale=en_US&amp;popup=true). |

>[!NOTE] Uitsluiting door computer werkt alleen als:
>
> * Via hetzelfde werkstation hebt u toegang tot uw website.
> * De cookies worden ingeschakeld in de browser die u gebruikt.
> * Uw cookies worden niet verwijderd. Als cookies worden verwijderd, moet u uzelf opnieuw uitsluiten.


## Exclusief door IP Adres {#section_609FB6461529409D840111A32FEF5C3D}

Een IP-adres is een internetadres. Alle gebruikers van Internet worden toegewezen numerieke IP adressen (typisch door de dienstverleners van Internet) die effectief als elektronische herkenningstekens handelen.

Paginaweergaven worden geteld en unieke paginabezoekers worden geïdentificeerd aan de hand van IP-adressen. Door IP-adressen niet te tellen, kunt u voorkomen dat vaak bezoekers door Adobe worden bijgehouden. Met deze functie kunnen u en uw collega&#39;s uw site bezoeken zonder uw verkeersgegevens te scheeftrekken. U kunt maximaal 50 verschillende IP adressen uitsluiten.

U kunt jokertekenindicatoren (*) gebruiken om een bereik van adressen uit te sluiten. Bijvoorbeeld, zou alle IP adressen tussen `[!DNL 0.0.*.0]` en `[!DNL 0.0.0.0]` `[!DNL 0.0.255.0]`uitsluiten. U kunt tot 50 verschillende IP adressen uitsluiten.

## Uitsluiten door firewall {#section_3E7BFB71ADD941D39F923DB9557AD9CD}

U kunt gegevensinzameling van specifieke IP adressen via een firewall ook blokkeren.

Zie de [IP Adressen die in het artikel van de Wolk](https://marketing.adobe.com/resources/help/en_US/home/index.html#kb-adobe-ip-addresses) van de Ervaring worden gebruikt.

## Gevolgen van IP Obfuscation {#section_51B7529FFF16449CA016FDC51D87E2CA}

Als IP de verwarring wordt toegelaten, gebeurt IP de uitsluiting alvorens het IP adres wordt verduisterd, zodat te hoeven de klanten om het even wat niet te veranderen wanneer zij IP verduistering toelaten.

Als het laatste octet wordt verwijderd, wordt dat gedaan vóór IP het filtreren. Als dusdanig, wordt het laatste octet vervangen met 0, en IP de uitsluitingsregels zouden moeten worden bijgewerkt om IP adressen met nul op het eind aan te passen. Overeenkomende * moet overeenkomen met 0.
