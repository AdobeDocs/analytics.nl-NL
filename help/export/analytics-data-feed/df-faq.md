---
description: Antwoorden op veelgestelde vragen over gegevensfeeds in Adobe Analytics.
keywords: Gegevensfeed;taak;vóór kolom;na kolom;hoofdlettergevoeligheid
title: Veelgestelde vragen over gegevensfeeds
feature: Data Feeds
exl-id: 1bbf62d5-1c6e-4087-9ed9-8f760cad5420
source-git-commit: bac8d17de1d442484ae1cf8c038ad853343ddb6b
workflow-type: tm+mt
source-wordcount: '1463'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensfeeds

Veelgestelde vragen over gegevensfeeds.

## Moeten voedernamen uniek zijn?{#unique}

Adobe Analytics voorkomt niet dat bestanden met gegevensinvoer worden overschreven.

Om te voorkomen dat gegevensdoorvoerbestanden worden overschreven, raden we aan dat alle gegevensdoorvoerbestanden die naar dezelfde locatie worden verzonden, unieke bestandsnamen hebben.

De namen van de gegevensdoorvoerbestanden bestaan uit de volgende kenmerken van de gegevensdoorvoer:

* Identiteitskaart van de Reeks van het rapport (RSID)

* Exportdatum

Om het even welke twee voer die voor zelfde RSID en data worden gevormd heeft de zelfde dossiernaam. Als deze feeds op dezelfde locatie worden geleverd, overschrijft het ene bestand het andere.

Als u wilt voorkomen dat een bestand wordt overschreven, moet u rekening houden met de volgende tijdelijke oorzaken:

* Het leveringspad wijzigen
* Wijzig indien mogelijk de datums
* Wijzig indien mogelijk de rapportsuite

## Wanneer worden gegevens verwerkt? {#processed}

Vóór de verwerking van uur of daggegevens, wacht de gegevensvoer tot alle klappen die gegevensinzameling binnen het tijdsbestek (dag of uur) zijn ingegaan uit zijn geschreven aan gegevenspakhuis. Daarna, verzamelen de gegevensvoer de gegevens met tijdstempels die binnen het tijdskader vallen, het comprimeert, en verzendt het via FTP. Voor uurvoer worden de dossiers typisch geschreven aan gegevenspakhuis binnen 15-30 min na het uur, maar er is geen vastgestelde tijdspanne. Als er geen gegevens zijn met tijdstempels die binnen de tijdlijn vallen, probeert het proces het volgende tijdkader opnieuw. Het huidige gegevensinvoerproces gebruikt het veld `date_time` om te bepalen welke resultaten tot het uur behoren. Dit gebied is gebaseerd op de tijdzone van de rapportreeks.

## Wat is het verschil tussen kolommen met een voorvoegsel `post_` en kolommen zonder voorvoegsel `post_` ? {#post}

Kolommen zonder het voorvoegsel `post_` bevatten precies dezelfde gegevens als die naar de gegevensverzameling zijn verzonden. Kolommen met een voorvoegsel `post_` bevatten de waarde na verwerking. De voorbeelden die een waarde kunnen veranderen zijn veranderlijke persistentie, verwerkingsregels, de regels van VISTA, muntomzetting, of andere server-zijlogica Adobe van toepassing is. Adobe raadt aan waar mogelijk de `post_` -versie van een kolom te gebruiken.

Als een kolom geen versie `post_` bevat (bijvoorbeeld `visit_num` ), kan de kolom worden beschouwd als een postkolom.

## Hoe verwerken gegevensfeeds hoofdlettergevoeligheid? {#case}

In Adobe Analytics worden de meeste variabelen voor rapportagedoeleinden als niet-hoofdlettergevoelig beschouwd. &#39;sneeuw&#39;, &#39;sneeuw&#39;, &#39;SNOW&#39; en &#39;sNow&#39; worden bijvoorbeeld allemaal beschouwd als dezelfde waarde. Hoofdlettergevoeligheid blijft behouden in gegevensfeeds.

Als u verschillende variaties ziet van dezelfde waarde tussen kolommen die niet na het plaatsen worden weergegeven (bijvoorbeeld &#39;sneeuw&#39; in de voorkolom en &#39;sneeuw&#39; in de postkolom), gebruikt uw implementatie zowel waarden in hoofdletters als in kleine letters op uw site. De gevalvariatie in de postkolom werd eerder overgegaan en in het virtuele koekje opgeslagen, of rond de zelfde tijd voor die rapportreeks verwerkt.

## Worden bots gefilterd door de regels van de Admin console bot inbegrepen in gegevensvoer? {#bots}

De voer van gegevens omvat geen bots die door [ worden gefiltreerd Admin consolebot regels ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/bot-removal/bot-removal.html?lang=nl-NL).

## Waarom zie ik meerdere `000` waarden in de kolom `event_list` of `post_event_list` gegevensinvoer? {#values}

Sommige spreadsheeteditors, met name Microsoft Excel, laten grote aantallen automatisch rond. De kolom `event_list` bevat vele komma-afgebakende aantallen, soms veroorzakend Excel om het als groot aantal te behandelen. De laatste cijfers worden afgerond op `000` .

Adobe raadt u aan `hit_data.tsv` -bestanden niet automatisch te openen in Microsoft Excel. Gebruik in plaats daarvan het dialoogvenster Gegevens importeren van Excel en zorg ervoor dat alle velden worden behandeld als tekst.

## Zijn kolommen als `hitid_high`, `hitid_low`, `visid_high` en `visid_low` gegarandeerd uniek voor de hit of het bezoek? {#hitid}

In bijna alle gevallen identificeert de samenvoeging van `hitid_high` en `hitid_low` een treffer op unieke wijze. Hetzelfde concept geldt voor het samenvoegen van `visid_high` en `visid_low` voor bezoeken. Nochtans, kunnen de verwerkingsanomalieën slechts zelden twee klusjes veroorzaken om het zelfde raakidentiteitskaart te delen. Adobe raadt u aan geen workflows voor gegevensinvoer te maken die onflexibel zijn als elke hit uniek is.

## Waarom ontbreekt informatie van de domeinkolom voor sommige dragers? {#domain}

Sommige mobiele dragers (zoals T-Mobile en O1) verstrekken geen domeininfo voor omgekeerde DNS raadplegingen meer. Daarom zijn die gegevens niet beschikbaar voor domeinrapportering.

## Waarom kan ik &quot;Uurly&quot;-bestanden niet extraheren uit gegevens die ouder zijn dan zeven dagen? {#hourly}

Voor gegevens die ouder zijn dan 7 dagen, worden de &quot;Uur&quot;dossiers van een dag gecombineerd in één enkel &quot;Dagelijks&quot;dossier.

Voorbeeld: Op 9 maart 2021 wordt een nieuwe gegevensfeed gemaakt en de gegevens van 1 januari 2021 tot 9 maart worden als &quot;Uur&quot; geleverd. De &quot;Uurly&quot;-bestanden vóór 2 maart 2021 worden echter gecombineerd tot één &quot;Dagelijks&quot; bestand. U kunt alleen &#39;Uurly&#39;-bestanden extraheren uit gegevens die jonger zijn dan 7 dagen na de aanmaakdatum. In dit geval, van 2 maart tot en met 9 maart.

## Wat is de impact van de zomertijd op de uurgegevens? {#dst}

Voor bepaalde tijdzones verandert de tijd tweemaal per jaar als gevolg van definities van zomertijd (DST). Het voer van gegevens respecteert de tijdzone waarvoor de rapportreeks wordt gevormd. Als de tijdzone voor de rapportreeks één is die geen DST gebruikt, blijft de dossierlevering normaal als een andere dag verdergaan. Als de tijdzone van de rapportreeks één is die DST gebruikt, wordt de dossierlevering veranderd voor het uur waarin de tijdverandering voorkomt (gewoonlijk 2 :00 am).

Bij het maken van STD -> DST-tijdovergangen (&quot;Voorjaar vooruit&quot;) ontvangt de klant slechts 23 bestanden. Het uur dat in de overgang van DST wordt overgeslagen wordt weggelaten. Bijvoorbeeld, als de overgang bij 2 AM voorkomt, krijgen zij een dossier voor het 1 :00 uur en een dossier voor het 3 :00 uur. Er is geen 2 :00 dossier omdat, bij 2 :00 STD, het 3 :00 DST wordt.

Bij het maken van DST -> STD-overgangen (&quot;Terugvallen&quot;) krijgt de klant 24 bestanden. Het uur van de overgang omvat echter eigenlijk twee uur aan gegevens. Bijvoorbeeld, als de overgang bij 2 :00 am voorkomt, wordt het dossier voor 1 :00 vertraagd met één uur, maar het bevat gegevens voor twee uren. Het bevat gegevens van 1 :00 DST aan 2 :00 STD (die 3 :00 DST) zou zijn geweest. Het volgende dossier begint bij 2 :00 STD.

## Hoe behandelt Analytics de mislukte FTP-overdracht? {#ftp-failure}

Als een FTP-overdracht mislukt (als gevolg van een afgewezen aanmelding, een verbroken verbinding, een quotumfout of een andere uitgave), probeert Adobe automatisch verbinding te maken en de gegevens maximaal drie keer te verzenden. Als de fouten aanhouden, wordt de feed gemarkeerd als mislukt en wordt een e-mailmelding verzonden.

Als een overdracht mislukt, kunt u een taak opnieuw uitvoeren totdat deze is gelukt.

Als u kwesties hebt die een gegevensvoer krijgen om op uw plaats van FTP te verschijnen, zie [ problemen oplossen gegevensvoer ](troubleshooting.md).

## Hoe kan ik een baan opnieuw sturen? {#resend}

Nadat u het leveringsprobleem hebt geverifieerd/gecorrigeerd, voert u de taak opnieuw uit om de bestanden op te halen.

## Wat is de instelling BucketOwnerFullControl voor Amazon S3-gegevensfeeds? {#BucketOwnerFullControl}

**BucketOwnerFullControl** verstrekt dwars-rekeningsrechten om voorwerpen in andere emmers tot stand te brengen.

Het algemene gebruiksgeval voor Amazon S3 is dat de Amazon Web Services (AWS) accounteigenaar een emmer maakt en vervolgens een gebruiker maakt die toestemming heeft om objecten in dat emmertje te maken en vervolgens referenties voor die gebruiker verschaft. In dit geval behoren de objecten van een gebruiker tot dezelfde account en heeft de rekeninghouder impliciet volledige controle over het object (lezen, verwijderen, enzovoort). Dit proces is vergelijkbaar met de manier waarop FTP-levering werkt.

Met AWS kan een gebruiker ook objecten in een emmertje maken die bij een andere gebruikersaccount horen. Twee AWS-gebruikers, gebruikerA en userB, behoren bijvoorbeeld niet tot dezelfde AWS-account, maar willen objecten maken in andere emmers. Als userA tot een emmer genoemd &quot;bucketA leidt,&quot;kunnen zij een emmerbeleid tot stand brengen dat uitdrukkelijk userB toestaat om voorwerpen in bucketA tot stand te brengen alhoewel de gebruiker niet het emmertje bezit. Dit beleid kan voordelig zijn omdat het userA en userB niet vereist om geloofsbrieven uit te wisselen. In plaats daarvan, verstrekt userB userA met hun rekeningsaantal, en userA leidt tot een emmerbeleid dat hoofdzakelijk zegt &quot;laat userB voorwerpen in bucketA tot stand brengen&quot;.

Objecten nemen echter geen rechten over van het bovenliggende emmertje. Daarom als userB een voorwerp aan de emmer van userA uploadt, bezit userB nog steeds dat voorwerp, en, door gebrek, wordt userA geen toestemmingen verleend aan dat voorwerp alhoewel userA het emmertje bezit. UserB moet userA toestemmingen uitdrukkelijk verlenen omdat userB nog de eigenaar van objecten is. Om deze toestemming te verlenen, moet userB het voorwerp met een BucketOwnerFullControl ACL uploaden, die specificeert dat de bucket eigenaar (userA) volledige toestemmingen aan het voorwerp (lezen, schrijven, schrappen, etc.) wordt verleend, alhoewel het voorwerp &quot;bezeten&quot;door userB is.

>[!NOTE]
>
>Adobe Analytics bepaalt niet of het emmertje een beleid heeft dat het geven van volledige controle van nieuwe voorwerpen vereist, of zelfs als de emmereigenaar in een verschillende rekening is dan de gebruiker die de gegevens schrijft. In plaats daarvan, voegt de Analytics automatisch de emmereigenaar aan `BucketOwnerFullControl` ACL met elke voer toe uploadt.

