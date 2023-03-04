---
title: Los de leveringstijden van het verzoek van de Data Warehouse problemen op
description: Bepaal potentiële kwesties met een verzoek van de Data Warehouse dat leveringstijden kan verlengen.
feature: Data Warehouse
exl-id: eed4d172-fffd-453f-ab5b-0fc2a79d5bd0
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---

# Los de leveringstijden van het verzoek van de Data Warehouse problemen op

Een bepaald verzoek om Data Warehouse kan overal van minder dan een uur tot verscheidene dagen of meer duren. Het is moeilijk de exacte hoeveelheid tijd te schatten die nodig is om een verzoek te verwerken, vanwege de volgende factoren:

* Het datumbereik van het verzoek
* De hoeveelheid verkeer die uw rapportenreeks tijdens de gevraagde tijdspanne wordt ontvangen
* Het aantal regels binnen een segment en de variabelen binnen een segment die worden gebruikt
* Hoeveel gegevens zijn opgenomen in het segment
* Het aantal gebruikte uitsplitsingen en het aantal unieke waarden binnen elke uitsplitsing
* Het aantal gebruikte metriek
* Het aantal gelijktijdige verzoeken dat wordt verwerkt
* VISTA-regels, indien geconfigureerd om van toepassing te zijn op DataWarehouse-verzoeken

Als u de verzoeken van het gegevenspakhuis constant lange tijd ziet, denk na veranderend uw verzoeken om het volgende aan te passen:

* **Een segment gebruiken dat een kleiner gegevensvoorbeeld bevat**: Hoe minder gegevens een aanvraag bevat, hoe sneller een rapport wordt geretourneerd.
* **Verzoeken uitvoeren in stappen van maximaal 14 dagen**: Kleinere aanvragen worden sneller verwerkt dan grote aanvragen.
* **Gebruik minder onderverdelingen:** Vele onderverdelingen in een verzoek van de Data Warehouse verhogen exponentieel de tijd het neemt om te verwerken.

>[!IMPORTANT]
>
> *Er is geen manier om de levering van een verzoek van de Data Warehouse te versnellen.*

Als u deze types van rapporten op een geschiktere manier vereist, overweeg de volgende alternatieven:

* **Analysis Workspace**: Hoewel de onbeperkte afmetingspunten niet beschikbaar zijn, omvat het bijna alle andere gebruiksgevallen die de Data Warehouse verstrekt.
* **Gegevensfeed**: Neemt alle ruwe gegevens in een rapportreeks dagelijks en verzendt het naar een plaats van FTP. U kunt deze gegevens vervolgens in uw eigen database importeren en query&#39;s uitvoeren om de gegevens te verkrijgen die u zoekt.
* **Oplossing voor Custom Engineering Services**: De Diensten van de Techniek van Adobe kunnen een douaneoplossing voor uw organisatie tegen extra kosten verstrekken. Neem contact op met het accountteam van uw Adobe voor meer informatie.
