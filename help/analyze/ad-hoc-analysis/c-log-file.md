---
title: Logbestand
description: Vraag een logbestand aan voor probleemoplossing.
translation-type: tm+mt
source-git-commit: d4cb2acb4ecaecce3644a2f3cf29913440e5cd6a
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 2%

---


# Logbestand

>[!IMPORTANT]
>
>Adobe beweegt Ad Hoc Analysis op 1 maart 2021 naar de status &quot;end-of-life&quot;. [Meer informatie...](https://adobe.ly/discoverworkspace).

Wanneer het oplossen van problemenkwesties met Ad Hoc Analysis, is het soms noodzakelijk om zijn logboekdossier te verkrijgen. Adobe kan het logboekdossier gebruiken om van de worteloorzaak van de kwestie de plaats te bepalen en een resolutie te verstrekken. Het `discover.log` bestand bevat alle gebruikersinteracties, gegevens over het laden van rapporten en Java-foutberichten voor alle sessies. Alle beveiligde gegevens, zoals het wachtwoord van de gebruiker, worden gehasht. Grote logbestanden worden opgedeeld in stappen van 10 MB. Zorg ervoor dat alle bestanden zijn geselecteerd wanneer u Adobe de logbestanden verschaft.

## Windows

Haal het `discover.log` bestand voor Windows op:

1. Klik op het beginmenu en selecteer **Uitvoeren** of druk op `[Win]` + `[R]`.
2. Plak het volgende in het tekstveld en klik op **OK**:

   ```text
   %appdata%/../Local/Adobe/Discover/log
   ```

3. Markeer alle bestanden in de map, klik met de rechtermuisknop en kies **Verzenden naar > Gecomprimeerde (gecomprimeerde) map**.
4. Geef het ZIP-bestand door aan de Adobe-vertegenwoordiger.

## Mac

Ga als volgt te werk om het `discover.log` bestand voor Mac OS te verkrijgen:

1. Open de Finder en navigeer naar `/Users/your-user/.adobe/Discover/log`
2. Markeer alle bestanden in de map, klik met de rechtermuisknop en kies **Comprimeren**.
3. Geef het ZIP-bestand door aan de Adobe-vertegenwoordiger.

Als de totale grootte van een gecomprimeerde bestand groter is dan 10 MB, kan een Adobe-medewerker een tijdelijke FTP-locatie opgeven.
