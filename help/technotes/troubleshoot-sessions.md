---
title: Sessies in Adobe Analytics oplossen
description: Leer hoe u problemen kunt oplossen wanneer u zich afmeldt bij Adobe Analytics.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Sessies in Adobe Analytics oplossen

Deze pagina gaat over het oplossen van problemensessies, wat betekent dat u zich met succes kunt aanmelden maar problemen hebt die aangemeld blijven. Zie [Problemen met aanmelden bij Adobe Analytics oplossen bij Adobe Analytics](troubleshoot-login.md)als zich problemen voordoen met het aanmelden.

Bijna alle op zitting-gebaseerde kwesties komen uit het aangepaste collectieve netwerk van een organisatie voort. Als u zich kunt aanmelden bij Adobe Analytics maar problemen hebt met het aanmelden, gebruikt u dit artikel om de oorzaak te achterhalen.

## Bepaal of de kwestie aan het netwerk van uw organisatie toe te schrijven is

Vele organisaties stellen extra netwerkeigenschappen op om veiligheid, zoals volmachtsservers of firewalls te verbeteren. Deze aanpassingen kunnen soms de mogelijkheid verstoren om een actieve sessie te behouden in Adobe Analytics.

Om te bepalen of het bedrijfsnetwerk waarmee u verbinding hebt problemen veroorzaakt met het gebruik van Adobe Analytics, gebruikt u uw aanmeldingsgegevens voor Experience Cloud op een apparaat buiten uw bedrijfsnetwerk. De voorbeelden van apparaten kunnen door uw huisnetwerk of het gegevensplan van een mobiel apparaat zijn. Als u van pagina aan pagina met succes kunt bewegen zonder het programma worden geopend, is het netwerk van uw organisatie waarschijnlijk de reden waarom u uit de Analytics van Adobe wordt geregistreerd.

## Problemen door proxy

Adobe gebruikt een machtigingsheader wanneer het aanvragen bij Adobe indient. Sommige proxy&#39;s, zoals Bluecoat (nu eigendom van Symantec), bevatten gegevens over de headergegevens voor kritieke autorisaties die door Adobe Analytics worden gebruikt. Als de machtigingheader niet wordt weergegeven in Adobe, verloopt de sessie.

Om dit probleem op te lossen, raadt Adobe aan samen te werken met het IT-team van uw organisatie om de header van de autorisatie toe te staan via de proxy van uw organisatie.

>[!NOTE] Hoewel leden van de gemeenschap Analytics de volgende koppelingen nuttig hebben gevonden, zijn ze niet in het bezit van Adobe. Houd rekening met deze opmerking wanneer u de inhoud ervan bekijkt.

Hier vindt u informatie over Symantec-proxy&#39;s en verificatieheaders:

* [Vorm Upstream Authentificatie van de Volmacht in een Plaatsing van de Keten van de Volmacht op een Toestel ProxySG of ASG](https://support.symantec.com/en_US/article.TECH246122.html)
* [ProxySG toestaan om serverautorisatie altijd upstream door te sturen](https://support.symantec.com/en_US/article.TECH244708.html)
