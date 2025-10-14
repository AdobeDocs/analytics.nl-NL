---
title: Uitsluiten op IP-adres
description: Voorkomen dat gegevens die door bepaalde IP-adressen worden gegenereerd, in rapporten worden weergegeven.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
role: Admin
source-git-commit: e09234ca27fbf923e026aa1f2ed0ebfed636bf7c
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# Uitsluiten op IP-adres

U kunt gegevens van specifieke IP adressen, zoals interne website activiteiten, plaats het testen en werknemersgebruik, van uw rapporten uitsluiten. Het uitsluiten van gegevens verbetert rapportnauwkeurigheid door IP adresgegevens uit te sluiten. Bovendien, kunt u gegevens uit ontkenning van de dienst of andere kwaadwillige gebeurtenissen verwijderen die rapportgegevens kunnen scheeftrekken.

Om gegevens door IP adres uit te sluiten, kunt u uitsluitingen vormen zoals hieronder beschreven, of u kunt [&#x200B; uw firewall &#x200B;](/help/technotes/ip-addresses.md) vormen.

## Vorm uitsluitingen door IP adres

>[!NOTE]
>
>Wanneer het vormen van uitsluitingen door IP adres, overweeg het volgende:
>
>* Hits uitgesloten door IP adres worden in rekening gebracht als [&#x200B; servervraag &#x200B;](/help/technotes/terms.md).
>* De privé IP adressen te hoeven niet worden uitgesloten. Alleen externe IP-adressen bereiken Adobe-gegevensverzamelingsservers. Privéadressen zijn `10.*.*.*` , `192.168.*.*` , `172.[16-31].*.*` en `169.254.*.*` .
>* U kunt vervangingsindicatoren (&#42;) gebruiken om een waaier van adressen uit te sluiten. `[!DNL 0.0.*.0]` sluit bijvoorbeeld alle IP-adressen tussen `[!DNL 0.0.0.0]` en `[!DNL 0.0.255.0]` uit. U kunt tot 50 verschillende IP adressen uitsluiten.
>* Gegevens van een uitgesloten IP-adres worden uitgesloten voor nieuwe treffers die binnen 5 minuten na het instellen van de uitsluiting naar het systeem komen.
>* Gegevens voor treffers die zijn vastgelegd vóór het tijdstip waarop wijzigingen zijn aangebracht in het IP-adres, worden niet beïnvloed.
>

Om uitsluitingen door IP adres te vormen:

1. Selecteer in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL All admin]** .

1. Selecteer **[!UICONTROL Exclude by IP]** op de beheerpagina.




## Gevolgen van IP obfuscatie {#section_51B7529FFF16449CA016FDC51D87E2CA}

Als IP de verwarring wordt toegelaten, gebeurt IP de uitsluiting alvorens het IP adres wordt verduisterd, zodat te hoeven de klanten om het even wat niet te veranderen wanneer zij IP verduistering toelaten.

Als het laatste octet wordt verwijderd, wordt dat gedaan vóór IP het filtreren. Als dusdanig, wordt het laatste octet vervangen met 0, en IP de uitsluitingsregels zouden moeten worden bijgewerkt om IP adressen met nul op het eind aan te passen. Overeenkomende &#42; moet overeenkomen met 0.
