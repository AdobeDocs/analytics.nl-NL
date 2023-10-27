---
title: Sessies in Adobe Analytics oplossen
description: Leer hoe u problemen kunt oplossen wanneer u zich afmeldt bij Adobe Analytics.
feature: Analytics Basics
exl-id: 191250ef-8313-47be-9717-046cce870998
source-git-commit: d64f6687dd6e6f688d332926e6d90fa699cac968
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 0%

---

# Sessies in Adobe Analytics oplossen

Deze pagina gaat over het oplossen van problemensessies, wat betekent dat u zich met succes kunt aanmelden maar problemen hebt die aangemeld blijven. Als er problemen optreden bij het aanmelden bij Adobe Analytics, raadpleegt u [Aanmelden bij Adobe Analytics oplossen](troubleshoot-login.md).

Bijna alle op zitting-gebaseerde kwesties komen uit het aangepaste collectieve netwerk van een organisatie voort. Als u zich bij Adobe Analytics kunt aanmelden maar problemen hebt met het aanmelden, gebruikt u dit artikel om de oorzaak te achterhalen.

## Bepaal of de kwestie aan het netwerk van uw organisatie toe te schrijven is

Vele organisaties stellen extra netwerkeigenschappen op om veiligheid, zoals volmachtsservers of firewalls te verbeteren. Deze aanpassingen kunnen soms de mogelijkheid verstoren om een actieve sessie in Adobe Analytics te behouden.

Om te bepalen als het collectieve netwerk u met wordt verbonden problemen met het gebruiken van Adobe Analytics veroorzaakt, gebruik uw login van het Experience Cloud geloofsbrieven op een apparaat buiten uw collectief netwerk. De voorbeelden van apparaten kunnen door uw huisnetwerk of het gegevensplan van een mobiel apparaat zijn. Als u van pagina aan pagina met succes kunt bewegen zonder het programma worden geopend, is het netwerk van uw organisatie waarschijnlijk de reden waarom u uit Adobe Analytics wordt geregistreerd.

## Problemen door proxy

De Adobe gebruikt een vergunningskopbal wanneer het doen van verzoeken aan Adobe. Sommige volmachten, zoals de Veilige Gateway van het Web van Edge (vroeger het Vervagen ecoat), de informatie van de strippen kritieke vergunningskopbal die door Adobe Analytics wordt gebruikt. Wanneer de Adobe de vergunningskopbal niet ziet, verloopt de zitting.

Om dit probleem op te lossen, raadt de Adobe aan samen te werken met het IT-team van uw organisatie om de machtigingsheader toe te staan via de proxy van uw organisatie.

>[!NOTE]
>
>Hoewel leden van de gemeenschap Analytics de volgende verbindingen nuttig hebben gevonden, zijn zij niet in het bezit van Adobe. Houd rekening met deze opmerking wanneer u de inhoud ervan bekijkt.

Hier vindt u informatie over proxy&#39;s en verificatieheaders:

* [Vorm Upstream Authentificatie van de Volmacht in een Plaatsing van de Keten van de Volmacht op een Toestel ProxySG of ASG](https://techdocs.broadcom.com/us/en/symantec-security-software/web-and-network-security/edge-swg/7-3/authentication_co.html)
* [Gebruikersgegevens doorsturen naar een server achter het ProxySG-apparaat](https://knowledge.broadcom.com/external/article/165859/how-to-forward-user-credentials-to-a-ser.html)
