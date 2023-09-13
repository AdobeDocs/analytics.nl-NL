---
title: Los de leveringstijden van het verzoek van de Data Warehouse problemen op
description: Bepaal potentiële kwesties met een verzoek van de Data Warehouse dat leveringstijden kan verlengen.
feature: Data Warehouse
exl-id: eed4d172-fffd-453f-ab5b-0fc2a79d5bd0
source-git-commit: fc6a2deabaf2012cefebf4864db19aef1825adf2
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Los de leveringstijden van het verzoek van de Data Warehouse problemen op

Een bepaald verzoek om Data Warehouse kan overal van minder dan een uur tot verscheidene dagen of meer duren. Het is moeilijk de exacte hoeveelheid tijd te schatten die nodig is om een verzoek te verwerken, vanwege de volgende factoren:

* Het datumbereik van het verzoek
* De hoeveelheid verkeer die uw rapportenreeks tijdens de gevraagde tijdspanne wordt ontvangen
* Het aantal regels binnen een segment en de variabelen binnen een segment die worden gebruikt
* Hoeveel gegevens zijn opgenomen in het segment
* Aantal gebruikte uitsplitsingen en aantal unieke waarden binnen elke uitsplitsing
* Het aantal gebruikte metriek
* Het aantal gelijktijdige verzoeken dat wordt verwerkt
* VISTA-regels, indien geconfigureerd om van toepassing te zijn op verzoeken om DataWarehouse

## Verzoeken wijzigen om levering te versnellen

Als de verzoeken van de Data Warehouse constant lange tijd vergen, denk na veranderend uw verzoeken. Het veranderen van een verzoek is de enige manier om de levering van een verzoek van de Data Warehouse te versnellen.

Om de levering van een verzoek van de Data Warehouse te versnellen, kunt u het op om het even welke volgende manieren veranderen:

* **Een segment gebruiken dat een kleiner gegevensvoorbeeld bevat**: Hoe minder gegevens een aanvraag bevat, hoe sneller een rapport wordt geretourneerd.
* **Verzoeken uitvoeren in stappen van 14 dagen of minder**: Kleinere aanvragen worden sneller verwerkt dan grote aanvragen.
* **Gebruik minder onderverdelingen:** Vele onderverdelingen in een verzoek verhogen exponentieel de tijd het neemt om het te verwerken.

## Een alternatieve methode gebruiken

Als u deze types van rapporten op een geschiktere manier vereist, overweeg de volgende alternatieven:

* **Analysis Workspace**: Hoewel onbeperkte afmetingsitems niet beschikbaar zijn, omvat deze bijna alle andere gebruiksgevallen die Data Warehouse biedt.
* **Gegevensfeed**: Neemt dagelijks alle onbewerkte gegevens in een rapportsuite en verzendt deze naar een cloudbestemming. U kunt de gegevens vervolgens in uw eigen database importeren en query&#39;s uitvoeren om de benodigde gegevens op te halen.
* **Oplossing voor Custom Engineering Services**: De Diensten van de Techniek van de Adobe kunnen een douaneoplossing voor uw organisatie tegen extra kosten verstrekken. Neem contact op met het accountteam van de Adobe voor meer informatie.
