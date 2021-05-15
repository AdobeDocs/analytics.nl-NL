---
description: Veelgestelde vragen over gegevensfeeds
keywords: Gegevensfeed;taak;vóór kolom;na kolom;hoofdlettergevoeligheid
title: Veelgestelde vragen over gegevensfeeds
exl-id: 1bbf62d5-1c6e-4087-9ed9-8f760cad5420
source-git-commit: 7312b61b8d73f45afa3eb9aac73cc4d5fd39bc82
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensfeeds

Veelgestelde vragen over gegevensfeeds.

## Moeten voedernamen uniek zijn?{#section_EF38BB51A7E240D69DAD4C07A34D9AD5}

Namen van gegevensdoorvoerbestanden bestaan uit de rapportsuite-id en de datum. Om het even welke twee voer die voor zelfde RSID en datum(s) worden gevormd zal het zelfde dossier - naam hebben. Als deze feeds op dezelfde locatie worden geleverd, overschrijft het ene bestand het andere. Om te voorkomen dat een bestand wordt overschreven, kunt u geen feed maken die een bestaande feed op dezelfde locatie kan overschrijven.

Wanneer u een feed probeert te maken terwijl een andere feed met dezelfde bestandsnaam bestaat, wordt het volgende bericht weergegeven:

Als deze fout optreedt, moet u rekening houden met de volgende tijdelijke oorzaken:

* Het leveringspad wijzigen
* Wijzig indien mogelijk de datums
* Wijzig indien mogelijk de rapportsuite

## Wanneer worden gegevens verwerkt? {#section_6346328F8D8848A7B81474229481D404}

Vóór de verwerking van uur of daggegevens, wacht de gegevensvoer tot alle klappen die gegevensinzameling binnen het tijdsbestek (dag of uur) zijn ingegaan uit zijn geschreven aan gegevenspakhuis. Daarna, verzamelt de gegevensvoer de gegevens met timestamps die binnen het tijdskader vallen, het comprimeert, en verzendt het via FTP. Voor uurvoer worden de dossiers typisch geschreven aan gegevenspakhuis binnen 15-30 min na het uur, maar er is geen vastgestelde tijdspanne. Als er geen gegevens zijn met tijdstempels die binnen de tijdlijn vallen, probeert het proces het volgende tijdkader opnieuw. Het huidige gegevensvoederproces gebruikt `date_time` gebied om te bepalen welke treffers tot het uur behoren. Dit gebied is gebaseerd op de tijdzone van de rapportreeks.

## Wat is het verschil tussen kolommen met een `post_` prefix en kolommen zonder een `post_` prefix?

Kolommen zonder het voorvoegsel `post_` bevatten gegevens precies zoals deze naar gegevensverzameling zijn verzonden. Kolommen met het voorvoegsel `post_` bevatten de waarde na verwerking. De voorbeelden die een waarde kunnen veranderen zijn veranderlijke persistentie, verwerkingsregels, de regels van VISTA, muntomzetting, of andere server-zijlogica Adobe van toepassing. Adobe raadt aan waar mogelijk de `post_`-versie van een kolom te gebruiken.

Als een kolom geen `post_` versie (bijvoorbeeld, `visit_num`) bevat, dan kan de kolom als een postkolom worden beschouwd.

## Hoe verwerken gegevensfeeds hoofdlettergevoeligheid?

In Adobe Analytics worden de meeste variabelen voor rapportagedoeleinden als niet-hoofdlettergevoelig beschouwd. &#39;sneeuw&#39;, &#39;sneeuw&#39;, &#39;SNOW&#39; en &#39;sNow&#39; worden bijvoorbeeld allemaal beschouwd als dezelfde waarde. Hoofdlettergevoeligheid blijft behouden in gegevensfeeds.

Als u verschillende variaties ziet van dezelfde waarde tussen kolommen die niet na het plaatsen worden weergegeven (bijvoorbeeld &#39;sneeuw&#39; in de voorkolom en &#39;sneeuw&#39; in de postkolom), gebruikt uw implementatie zowel waarden in hoofdletters als in kleine letters op uw site. De gevalvariatie in de postkolom werd eerder overgegaan en in het virtuele koekje opgeslagen, of rond de zelfde tijd voor die rapportreeks verwerkt.

## Worden bots gefilterd door de regels van de Admin console bot inbegrepen in gegevensvoer?

Gegevensfeeds omvatten geen bots die zijn gefilterd door [Regels voor Admin-console bot](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/bot-removal/bot-removal.html).

## Waarom zie ik veelvoudige `000` waarden in `event_list` of `post_event_list` de kolom van de gegevensvoer?

Sommige spreadsheeteditors, met name Microsoft Excel, afronden automatisch grote aantallen. De `event_list` kolom bevat vele komma-afgebakende aantallen, soms veroorzakend Excel om het als groot aantal te behandelen. De laatste cijfers worden afgerond op `000`.

Adobe raadt u aan `hit_data.tsv`-bestanden niet automatisch te openen in Microsoft Excel. Gebruik in plaats daarvan het dialoogvenster Gegevens importeren van Excel en zorg ervoor dat alle velden worden behandeld als tekst.

## Waarom ontbreekt informatie van de domeinkolom voor sommige dragers? {#section_B7508D65370442C7A314EAED711A2C75}

Sommige mobiele dragers (zoals T-Mobile en O1) verstrekken geen domeininfo voor omgekeerde DNS raadplegingen meer. Daarom zijn die gegevens niet beschikbaar voor domeinrapportering.

## Waarom kan ik &quot;Uurly&quot;-bestanden niet extraheren uit gegevens die ouder zijn dan zeven dagen?

Voor gegevens die ouder zijn dan 7 dagen, worden de &quot;Uur&quot;dossiers van een dag gecombineerd in één enkel &quot;Dagelijks&quot;dossier.

Voorbeeld: Op 9 maart 2021 wordt een nieuwe gegevensfeed gemaakt en de gegevens van 1 januari 2021 tot en met 9 maart worden als &quot;Uur&quot; geleverd. De &quot;Uurly&quot;-bestanden van vóór 2 maart 2021 worden echter gecombineerd tot één &quot;Dagelijks&quot;-bestand. U kunt alleen &#39;Uurly&#39;-bestanden extraheren uit gegevens die jonger zijn dan 7 dagen na de aanmaakdatum. In dit geval, van 2 maart tot en met 9 maart.

## Wat is de impact van de zomertijd op de uurgegevens? {#section_70E867D942054DD09048E027A9474FFD}

Voor bepaalde tijdzones verandert de tijd tweemaal per jaar als gevolg van definities van zomertijd (DST). Het voer van gegevens respecteert de tijdzone waarvoor de rapportreeks wordt gevormd. Als de tijdzone voor de rapportreeks één is die geen DST gebruikt, blijft de dossierlevering normaal als een andere dag verdergaan. Als de tijdzone van de rapportreeks één is die DST gebruikt, wordt de dossierlevering veranderd voor het uur waarin de tijdverandering (gewoonlijk 2:00 am) voorkomt.

Bij het maken van STD -> DST-tijdovergangen (&quot;Voorjaar vooruit&quot;) ontvangt de klant slechts 23 bestanden. Het uur dat in de overgang van DST wordt overgeslagen wordt weggelaten. Als de overgang bijvoorbeeld plaatsvindt om 2 uur &#39;s nachts, krijgen ze een bestand voor 1 uur en een bestand voor 3 uur. Er is geen 2:00-bestand omdat het bij 2:00 STD 3:00 DST wordt.

Bij het maken van DST -> STD-overgangen (&quot;Terugvallen&quot;) krijgt de klant 24 bestanden. Het uur van de overgang omvat echter eigenlijk twee uur aan gegevens. Als de overgang bijvoorbeeld om 2:00 uur plaatsvindt, wordt het bestand voor 1:00 met één uur vertraagd, maar bevat het gegevens voor twee uur. Het bevat gegevens van 1:00 DST aan 2:00 STD (die 3:00 DST zou zijn geweest). Het volgende bestand begint bij 2:00 STD.

## Hoe behandelt Analytics de mislukte FTP-overdracht? {#section_4BD44E9167F0494FB2B379D2BA132AD8}

Als een FTP-overdrachtfout optreedt (aanmelden geweigerd, verbinding verbroken, quota overschreden, enz.), probeert Adobe automatisch verbinding te maken en de gegevens maximaal drie keer te verzenden. Als de fouten aanhouden, wordt de feed gemarkeerd als mislukt en wordt een e-mailmelding verzonden.

Als een overdracht mislukt, kunt u een taak opnieuw uitvoeren totdat deze is gelukt.

Zie [Taken oplossen](jobs-troubleshooting.md) als er problemen zijn met het weergeven van een gegevensfeed op uw FTP-site.

## Hoe kan ik een baan opnieuw sturen? {#section_BFD4447B0B5946CAAEE4F0F03D42EDFD}

Nadat u het leveringsprobleem hebt geverifieerd/gecorrigeerd, voert u de taak opnieuw uit om de bestanden op te halen.

## Wat is de instelling BucketOwnerFullControl voor Amazon S3-gegevensfeeds? {#section_6797EBBB7E6D44D4B00C7AEDF4C2EE1D}

Het gemeenschappelijke gebruiksgeval voor Amazon S3 is dat de de rekeningseigenaar van het Web van Amazon van de Diensten (AWS) een emmertje creeert, dan tot een gebruiker leidt die toestemming heeft om voorwerpen in dat emmertje tot stand te brengen, en dan geloofsbrieven voor die gebruiker verstrekt. In dit geval behoren de objecten van een gebruiker tot dezelfde account en heeft de rekeninghouder impliciet volledige controle over het object (lezen, verwijderen, enz.). Dit proces is vergelijkbaar met de manier waarop FTP-levering werkt.

Met AWS kan een gebruiker ook objecten in een emmertje maken die bij een andere gebruikersaccount horen. Bijvoorbeeld, als twee gebruikers AWS, gebruikerA en userB, niet tot de zelfde rekening behoren AWS maar voorwerpen in andere emmers willen tot stand brengen. Als userA tot een emmer leidt, zeg bucketA, kan hij of zij een emmerbeleid tot stand brengen dat uitdrukkelijk userB toestaat om voorwerpen in bucketA tot stand te brengen alhoewel de gebruiker niet het emmertje bezit. Dit beleid kan voordelig zijn omdat het niet die userA en userB vereist om geloofsbrieven uit te wisselen. In plaats daarvan, verstrekt userB userA met hun rekeningsaantal, en userA leidt tot een emmerbeleid dat hoofdzakelijk zegt &quot;laat userB voorwerpen in bucketA tot stand brengen&quot;.

**** BucketOwnerFullController biedt cross-account rechten om objecten in andere emmers te maken. Als userB een voorwerp aan de emmer van userA uploadt, nog bezit userB dat voorwerp, en, door gebrek, wordt userA geen toestemmingen verleend aan dat voorwerp alhoewel userA het emmertje bezit. Dit komt doordat objecten geen machtigingen van het bovenliggende emmertje overnemen. UserB moet userA toestemmingen uitdrukkelijk verlenen omdat userB nog de eigenaar van objecten is. Om deze toestemming te verlenen, moet userB het voorwerp met een BucketOwnerFullControl ACL uploaden, die specificeert dat de bucket eigenaar (userA) volledige toestemmingen aan het voorwerp (lezen, schrijven, schrappen, enz.) wordt verleend, alhoewel het voorwerp &quot;bezeten&quot;door userB is.

>[!MORELIKETHIS]
>
>* [Taken oplossen](jobs-troubleshooting.md)

