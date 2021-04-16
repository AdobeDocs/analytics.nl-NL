---
description: Deze sectie bevat informatie over algemene kwesties.
keywords: Gegevensfeed;problemen oplossen
title: Gegevensfeeds oplossen
uuid: 4be981ab-3a61-4099-9b0d-785d2ac2492a
exl-id: 58531afe-5e0e-49b6-9c9f-9c857be8dc75
translation-type: tm+mt
source-git-commit: c6d4095fdf86be52c7921aed84b9229ac3b27f82
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---

# Gegevensfeeds oplossen

Deze sectie bevat informatie over algemene kwesties.

## Fout bij opslaan van feed {#section_EF38BB51A7E240D69DAD4C07A34D9AD5}

Namen van gegevensdoorvoerbestanden bestaan uit de rapportsuite-id en de datum. Om het even welke twee voer die voor zelfde RSID en datum(s) worden gevormd zal het zelfde dossier - naam hebben. Als deze feeds op dezelfde locatie worden geleverd, overschrijft het ene bestand het andere. Om te voorkomen dat een bestand wordt overschreven, kunt u geen feed maken die een bestaande feed op dezelfde locatie kan overschrijven.

Wanneer u een feed probeert te maken terwijl een andere feed met dezelfde bestandsnaam bestaat, wordt het volgende bericht weergegeven:

Als deze fout optreedt, moet u rekening houden met de volgende tijdelijke oorzaken:

* Het leveringspad wijzigen
* Wijzig indien mogelijk de datums
* Wijzig indien mogelijk de rapportsuite

## BucketOwnerFullControl-instelling voor Amazon S3-gegevensfeeds {#section_6797EBBB7E6D44D4B00C7AEDF4C2EE1D}

Het gemeenschappelijke gebruiksgeval voor Amazon S3 is dat de de rekeningseigenaar van het Web van Amazon van de Diensten (AWS) een emmertje creeert, dan tot een gebruiker leidt die toestemming heeft om voorwerpen in dat emmertje tot stand te brengen, en dan geloofsbrieven voor die gebruiker verstrekt. In dit geval behoren de objecten van een gebruiker tot dezelfde account en heeft de rekeninghouder impliciet volledige controle over het object (lezen, verwijderen, enz.). Dit is vergelijkbaar met de manier waarop FTP-levering werkt.

Met AWS kan een gebruiker ook objecten in een emmertje maken die bij een geheel andere gebruikersaccount horen. Bijvoorbeeld, als twee gebruikers AWS, gebruikerA en userB, niet tot de zelfde rekening behoren AWS maar voorwerpen in andere emmers willen tot stand brengen. Als userA tot een emmer leidt, zeg bucketA, kan hij of zij een emmerbeleid tot stand brengen dat uitdrukkelijk userB toestaat om voorwerpen in bucketA tot stand te brengen alhoewel de gebruiker niet het emmertje bezit. Dit kan voordelig zijn omdat het niet die userA en userB vereist om geloofsbrieven uit te wisselen. In plaats daarvan, verstrekt userB userA met hun rekeningsaantal, en userA leidt tot een emmerbeleid dat hoofdzakelijk zegt &quot;laat userB voorwerpen in bucketA tot stand brengen&quot;.

**** BucketOwnerFullController biedt cross-account rechten om objecten in andere emmers te maken. Als userB een voorwerp aan de emmer van userA uploadt, nog bezit userB dat voorwerp, en door gebrek, wordt userA geen toestemmingen verleend aan dat voorwerp alhoewel userA bezit bucket-voorwerpen geen toestemmingen van de ouderemmer erven. UserB moet userA toestemmingen uitdrukkelijk verlenen omdat userB nog de eigenaar van objecten is. Voor deze dwars-rekening uploadt, verstrekt AWS een BucketOwnerFullControl ACL door te specificeren dat het gebruik van dit ACL door de emmereigenaar (userA) en volledige toestemmingen aan het voorwerp (lezen, schrijven, schrappen, enz.) wordt verleend, alhoewel het voorwerp &quot;bezeten&quot;door userB is.

## Overdrachtsfouten {#section_4BD44E9167F0494FB2B379D2BA132AD8}

Als een FTP-overdrachtfout optreedt (aanmelden geweigerd, verbinding verbroken, quota overschreden, enz.), probeert Adobe automatisch verbinding te maken en de gegevens maximaal drie keer te verzenden. Als de fouten aanhouden, wordt de feed gemarkeerd als mislukt en wordt een e-mailmelding verzonden.

Als de overdracht mislukt, kunt u de taak opnieuw uitvoeren totdat deze is gelukt.

## Opties voor opnieuw verzenden {#section_BFD4447B0B5946CAAEE4F0F03D42EDFD}

Nadat u het leveringsprobleem hebt geverifieerd/gecorrigeerd, voert u de taak opnieuw uit om de bestanden op te halen.

## Besparing op zomertijd op het voer van Uur- Gegevens {#section_70E867D942054DD09048E027A9474FFD}

Voor bepaalde tijdzones wordt de tijd twee keer per jaar gewijzigd als gevolg van definities van zomertijd (DST). Het voer van gegevens respecteert de tijdzone waarvoor de rapportreeks wordt gevormd. Als de tijdzone voor de rapportreeks één is die geen DST gebruikt, zal de dossierlevering normaal als om het even welke andere dag verdergaan. Als de tijdzone van de rapportreeks één is die DST gebruikt, zal de dossierlevering voor het uur worden veranderd waarin de tijdverandering (gewoonlijk 2:00 am) voorkomt.

Bij het maken van STD -> DST-tijdovergangen (&quot;Voorjaar vooruit&quot;) krijgt de klant slechts 23 bestanden. Het uur dat in de overgang van DST wordt overgeslagen wordt eenvoudig weggelaten. Bijvoorbeeld, als de overgang om 2 AM voorkomt, zullen zij een dossier voor 1:00 uur krijgen, en zullen een dossier voor 3:00 uur krijgen. Er zal geen 2:00 dossier zijn, aangezien bij 2:00 STD, het 3:00 DST wordt.

Bij het maken van DST -> STD-overgangen (&quot;Terugvallen&quot;) krijgt de klant 24 bestanden. Het uur van de overgang zal echter in feite 2 uur aan gegevens omvatten. Als de overgang bijvoorbeeld om 2:00 uur plaatsvindt, wordt het bestand voor 1:00 met één uur vertraagd, maar bevat het gegevens voor twee uur. Het zal gegevens van 1:00 DST aan 2:00 STD (die 3:00 DST zou zijn geweest) bevatten. Het volgende bestand begint om 2:00 STD.

## Geen gegevens voor een tijdsperiode {#section_72510794694D42A9A75C966B812AEB0F}

U kunt naar keuze een gegevensvoer vormen om een duidelijk dossier te leveren als geen gegevens voor een specifieke periode worden verzameld. Als u deze optie inschakelt, ontvangt u een manifestbestand dat lijkt op het volgende:

```text
Datafeed-Manifest-Version: 1.0
 Lookup-Files: 0
 Data-Files: 0
 Total-Records: 0
```

## Geen Domeininfo voor Domeinrapportage {#section_B7508D65370442C7A314EAED711A2C75}

Sommige mobiele dragers (zoals T-Mobile en O1) verstrekken geen domeininfo voor omgekeerde DNS raadplegingen meer. Daarom zijn die gegevens niet beschikbaar voor domeinrapportering.

## Overzicht van gegevensverwerking {#section_6346328F8D8848A7B81474229481D404}

Vóór de verwerking van uur of daggegevens, wacht de gegevensvoer tot alle klappen die gegevensinzameling binnen het tijdsbestek (dag of uur) zijn ingegaan uit zijn geschreven aan gegevenspakhuis. Daarna, verzamelt de gegevensvoer de gegevens met timestamps die binnen het tijdskader vallen, het comprimeert, en verzendt het via FTP. Voor uurvoer worden de dossiers typisch geschreven aan gegevenspakhuis binnen 15-30 min na het uur, maar er is geen vastgestelde tijdspanne. Als er geen gegevens zijn met tijdstempels die binnen de tijdlijn vallen, probeert het proces het volgende tijdkader opnieuw. Het huidige gegevensvoederproces gebruikt `date_time` gebied om te bepalen welke treffers tot het uur behoren. Dit gebied is gebaseerd op de tijdzone van de rapportreeks.

## &quot;Uourly&quot; versus &quot;Daily&quot; gegevensfeed-indelingen

Voor gegevens die ouder zijn dan 7 dagen, worden de &quot;Uur&quot;dossiers van een dag gecombineerd in één enkel &quot;Dagelijks&quot;dossier.

Voorbeeld: Op 9 maart 2021 wordt een nieuwe gegevensfeed gemaakt en de gegevens van 1 januari 2021 tot en met 9 maart worden als &quot;Uur&quot; geleverd. De &quot;Uurly&quot;-bestanden van vóór 2 maart 2021 worden echter gecombineerd tot één &quot;Dagelijks&quot;-bestand. U kunt alleen &#39;Uurly&#39;-bestanden extraheren uit gegevens die jonger zijn dan 7 dagen na de aanmaakdatum. In dit geval, van 2 maart tot en met 9 maart.