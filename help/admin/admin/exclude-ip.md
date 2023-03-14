---
title: Exclusief door IP Adres
description: Voorkomen dat gegevens die door bepaalde IP-adressen worden gegenereerd, in rapporten worden weergegeven.
exl-id: 315a3000-f043-434b-a677-d111aeed7971
feature: Admin Tools
source-git-commit: 2c0aef13bdb88b0a7aa9f100c72c21f66a14c8dd
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Exclusief door IP Adres

U kunt gegevens van specifieke IP adressen, zoals interne website activiteiten, plaats het testen en werknemersgebruik, van uw rapporten uitsluiten. Het uitsluiten van gegevens verbetert rapportnauwkeurigheid door IP adresgegevens uit te sluiten. Bovendien, kunt u gegevens uit ontkenning van de dienst of andere kwaadwillige gebeurtenissen verwijderen die rapportgegevens kunnen scheeftrekken. U kunt uitsluiting configureren of uw firewall gebruiken.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Exclude by IP]**

>[!NOTE]
>
>Hits die door IP adres worden uitgesloten worden gefactureerd [serveraanroepen](https://experienceleague.adobe.com/docs/analytics/technotes/terms.html).

U kunt jokertekens gebruiken (&#42;) om een bereik van adressen uit te sluiten. Bijvoorbeeld: `[!DNL 0.0.*.0]` zou alle IP adressen tussen uitsluiten `[!DNL 0.0.0.0]` en `[!DNL 0.0.255.0]`. U kunt tot 50 verschillende IP adressen uitsluiten.

>[!TIP]
>
>De privé IP adressen te hoeven niet worden uitgesloten. Slechts bereiken de externe IP adressen de servers van de Adobe gegevensinzameling. Privéadressen omvatten `10.*.*.*`, `192.168.*.*`, `172.[16-31].*.*`, en `169.254.*.*`.

## Gevolgen van IP Obfuscation {#section_51B7529FFF16449CA016FDC51D87E2CA}

Als IP de verwarring wordt toegelaten, gebeurt IP de uitsluiting alvorens het IP adres wordt verduisterd, zodat te hoeven de klanten om het even wat niet te veranderen wanneer zij IP verduistering toelaten.

Als het laatste octet wordt verwijderd, wordt dat gedaan vóór IP het filtreren. Als dusdanig, wordt het laatste octet vervangen met 0, en IP de uitsluitingsregels zouden moeten worden bijgewerkt om IP adressen met nul op het eind aan te passen. Overeenkomend &#42; moet overeenkomen met 0.
