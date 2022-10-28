---
title: VISTA-regels in Adobe Analytics
description: Meer informatie over de regels en mogelijkheden van VISTA.
source-git-commit: 1e2284fd4a62816b27b33a91f3bee2575a852107
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 0%

---


# VISTA-regels in Adobe Analytics

De regels van VISTA zijn een afwisselende vorm van de aanpassing van douanegegevens die u tussen gegevensinzameling en verwerking kunt toepassen. Zie [Verwerkingsopdracht](processing-order.md) voor meer informatie over het exacte stadium in de gegevenspijpleiding die de VISTA-regels toepassen. VISTA-regels hebben alleen invloed op actuele gegevens terwijl ze worden verzameld; bestaande gegevens worden niet gewijzigd.

Sommige veelvoorkomende gevallen van gebruik van de VISTA-regels omvatten:

* Kopieer een hit Analytics van de ene rapportsuite naar de andere en wijzig desgewenst gegevens naar de gekopieerde rapportsuite
* Uitsluiting van Aangepaste IP die de gebruiksgevallen overschrijdt die worden aangeboden door [Uitsluiten door IP](/help/admin/admin/exclude-ip.md)
* Voorwaardelijk of globaal om het even welke veranderlijke waarde wijzigen
* Variabelewaarden naar andere variabelen dupliceren
* Bestanden uploaden naar een Adobe FTP-site die de waarden van variabelen kan beïnvloeden

Vele gevallen van gebruik van de VISTA-regels worden al aangeboden door [Verwerkingsregels](/help/admin/admin/c-processing-rules/processing-rules.md), [Bot-regels](/help/admin/admin/bot-removal/bot-rules.md), [Virtuele rapportsuites](/help/components/vrs/vrs-about.md)of werkt u gewoon uw Adobe Analytics-implementatie bij. Adobe beveelt VISTA-regels alleen aan als laatste redmiddel.

>[!IMPORTANT]
>
>Voor VISTA-regels is een overeenkomst tussen uw organisatie en Adobe Professional Services vereist. Neem contact op met de accountmanager van de Adobe van uw organisatie als u een VISTA-regel wilt maken of bijwerken.

## Een VISTA-regel maken

U moet met Adobe Professional Services werken om een VISTA-regel te maken. Neem contact op met de accountmanager van de Adobe van uw organisatie als u een VISTA-regel wilt maken.

## Bestaande VISTA-regels bekijken

Adobe biedt geen interface aan om bestaande VISTA-regels te bekijken. Neem contact op met de Adobe-accountmanager of de klantenservice van uw organisatie met de gewenste rapportsuite om een lijst met bestaande VISTA-regels op te halen.