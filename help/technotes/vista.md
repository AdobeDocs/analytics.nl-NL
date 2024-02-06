---
title: VISTA-regels in Adobe Analytics
description: Meer informatie over de regels en mogelijkheden van VISTA.
exl-id: fab2acc3-b037-48f9-bb20-625ccb75b4cc
feature: Analytics Basics
source-git-commit: d3d5b01fe17f88d07a748fac814d2161682837c2
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# VISTA-regels in Adobe Analytics

De regels van VISTA zijn een afwisselende vorm van de aanpassing van douanegegevens die u tussen gegevensinzameling en verwerking kunt toepassen. Zie [Verwerkingsopdracht](processing-order.md) voor meer informatie over het exacte stadium in de gegevenspijpleiding die de VISTA-regels toepassen. De VISTA-regels hebben alleen invloed op de huidige gegevens aangezien deze worden verzameld; de bestaande gegevens worden niet gewijzigd.

Sommige veelvoorkomende gevallen van gebruik van de VISTA-regels omvatten:

* Kopieer een hit Analytics van de ene rapportsuite naar de andere en wijzig desgewenst gegevens naar de gekopieerde rapportsuite
* Uitsluiting van Aangepaste IP die de gebruiksgevallen overschrijdt die worden aangeboden door [Uitsluiten door IP](/help/admin/admin/exclude-ip.md)
* Voorwaardelijk of globaal om het even welke veranderlijke waarde wijzigen
* Variabelewaarden naar andere variabelen dupliceren
* Bestanden uploaden naar een FTP-site van een Adobe die invloed kan hebben op waarden van variabelen

Vele gevallen van gebruik van de VISTA-regels worden al aangeboden door [Verwerkingsregels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md), [Bot-regels](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md), [Virtuele rapportsuites](/help/components/vrs/vrs-about.md)of werkt uw Adobe Analytics-implementatie bij. Adobe beveelt VISTA-regels alleen aan als laatste redmiddel.

>[!IMPORTANT]
>
>Voor VISTA-regels is een overeenkomst tussen uw organisatie en Adobe Professional Services vereist. Neem contact op met het accountteam van de Adobe als u een VISTA-regel wilt maken of bijwerken.

## Een VISTA-regel maken {#create}

U moet met Adobe Professional Services werken om een VISTA-regel te maken. Neem contact op met het accountteam van de Adobe als u een VISTA-regel wilt maken.

## Bestaande VISTA-regels bekijken {#see}

De Adobe biedt geen UI aan om bestaande regels van VISTA te bekijken. Neem contact op met het accountteam of de klantenservice van de Adobe met de gewenste rapportsuite om een lijst met bestaande VISTA-regels op te halen.
