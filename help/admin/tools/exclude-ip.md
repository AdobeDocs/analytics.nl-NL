---
title: Uitsluiten op IP-adres
description: Voorkomen dat gegevens die door bepaalde IP-adressen worden gegenereerd, in rapporten worden weergegeven.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
role: Admin
source-git-commit: 4b4febd839682d88164b2f505245441d18ef2543
workflow-type: tm+mt
source-wordcount: '312'
ht-degree: 0%

---

# Uitsluiten op IP-adres

U kunt gegevens van specifieke IP adressen, zoals interne website activiteiten, plaats het testen en werknemersgebruik, van uw rapporten uitsluiten. Het uitsluiten van gegevens verbetert rapportnauwkeurigheid door IP adresgegevens uit te sluiten. Bovendien, kunt u gegevens uit ontkenning van de dienst of andere kwaadwillige gebeurtenissen verwijderen die rapportgegevens kunnen scheeftrekken.

Om gegevens door IP adres uit te sluiten, kunt u uitsluitingen vormen zoals hieronder beschreven, of u kunt [ uw firewall ](/help/technotes/ip-addresses.md) vormen.

## Vorm uitsluitingen door IP adres

>[!NOTE]
>
>Wanneer het vormen van uitsluitingen door IP adres, overweeg het volgende:
>
>* Hits uitgesloten door IP adres worden in rekening gebracht als [ servervraag ](/help/technotes/terms.md).
>* De privé IP adressen te hoeven niet worden uitgesloten. Alleen externe IP-adressen bereiken Adobe-gegevensverzamelingsservers. Privéadressen zijn `10.*.*.*` , `192.168.*.*` , `172.[16-31].*.*` en `169.254.*.*` .
>* U kunt vervangingsindicatoren (&#42;) gebruiken om een waaier van adressen uit te sluiten. `[!DNL 0.0.*.0]` sluit bijvoorbeeld alle IP-adressen tussen `[!DNL 0.0.0.0]` en `[!DNL 0.0.255.0]` uit. U kunt tot 50 verschillende IP adressen uitsluiten.
>* Gegevens van een uitgesloten IP-adres worden uitgesloten voor nieuwe treffers die binnen 5 minuten na het instellen van de uitsluiting naar het systeem komen.
>* Gegevens voor treffers die zijn vastgelegd vóór het tijdstip waarop wijzigingen zijn aangebracht in het IP-adres, worden niet beïnvloed. De uitsluiting IP is slechts op gegevens van toepassing die zich vooruit bewegen.
>* De uitgesloten klappen zijn nog zichtbaar in [ voer van Gegevens ](/help/export/analytics-data-feed/data-feed-overview.md) (gemarkeerd als `exclude_hit = 4`).

Om uitsluitingen door IP adres te vormen:

1. Selecteer in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL All admin]** .

1. Selecteer **[!UICONTROL Exclude by IP]** op de beheerpagina.

## Gevolgen van het gebruiken van IP obfuscatie met IP uitsluiting

Het effect van het gebruiken van [ IP obfuscation ](/help/admin/tools/manage-rs/edit-settings/general/general-acct-settings-admin.md) samen met IP uitsluiting hangt van IP van elke IP van de rapportreeks het plaatsen af:

* **IP obfuscation (laatste octet)**: IP is gedeeltelijk verduisterd VÓÓR IP uitsluitingslooppas. Zorg ervoor dat IP-uitsluitingsregels altijd een `0` als laatste octet verwachten (jokertekens zijn geldig omdat ze `0` bevatten).
* **IP obfuscation (verwijder IP)**: IP is volledig verduisterd NA IP uitsluitingslooppas. Geen IP de aanpassingen van de uitsluitingsregel zijn noodzakelijk.
