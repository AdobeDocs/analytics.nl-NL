---
title: Problemen met levertijden van Data warehouse-aanvragen oplossen
description: Bepaal potentiële problemen met een verzoek van Data warehouse dat leveringstijden kan verlengen.
translation-type: tm+mt
source-git-commit: 6778dd290424651dc959224daa0eef8ebd8196e5
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 0%

---


# Problemen met levertijden van Data warehouse-aanvragen oplossen

Een gegeven Data warehouse verzoek kan overal van minder dan een uur tot verscheidene dagen of meer duren. Het is moeilijk de exacte hoeveelheid tijd te schatten die nodig is om een verzoek te verwerken, vanwege de volgende factoren:

* Het datumbereik van het verzoek
* De hoeveelheid verkeer die uw rapportenreeks tijdens de gevraagde tijdspanne wordt ontvangen
* Het aantal regels binnen een segment en de variabelen binnen een segment die worden gebruikt
* Hoeveel gegevens zijn opgenomen in het segment
* Het aantal gebruikte uitsplitsingen en het aantal unieke waarden binnen elke uitsplitsing
* Het aantal gebruikte metriek
* Het aantal gelijktijdige verzoeken dat wordt verwerkt
* VISTA-regels, indien geconfigureerd om van toepassing te zijn op DataWarehouse-verzoeken

Als u voortdurend ziet dat data warehouse-verzoeken veel tijd in beslag nemen, kunt u uw verzoeken als volgt wijzigen:

* **Gebruik een segment met een kleiner gegevensvoorbeeld**: Hoe minder gegevens een aanvraag bevat, hoe sneller een rapport wordt geretourneerd.
* **Voer aanvragen in stappen van 14 dagen of minder** uit: Kleinere aanvragen worden sneller verwerkt dan grote aanvragen.
* **Gebruik minder onderverdelingen:** Vele onderverdelingen in een verzoek van Data warehouse verhogen exponentieel de tijd het aan proces neemt.

>[!IMPORTANT]
>
> *Er is geen manier om de levering van een Data warehouse verzoek te versnellen.*

Als u deze types van rapporten op een geschiktere manier vereist, overweeg de volgende alternatieven:

* **Analysis Workspace**: Hoewel de onbeperkte afmetingspunten niet beschikbaar zijn, omvat het bijna alle andere gebruiksgevallen die Data warehouse verstrekt.
* **Gegevensinvoer**: Neemt alle ruwe gegevens in een rapportreeks dagelijks en verzendt het naar een plaats van FTP. U kunt deze gegevens vervolgens in uw eigen database importeren en query&#39;s uitvoeren om de gegevens te verkrijgen die u zoekt.
* **Oplossing** voor Custom Engineering Services: De Diensten van de Techniek van Adobe kunnen een douaneoplossing voor uw organisatie tegen extra kosten verstrekken. Neem contact op met de accountmanager van uw organisatie voor meer informatie.
