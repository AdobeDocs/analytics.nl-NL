---
description: 'null'
title: Aanbevolen werkwijzen labelen
uuid: d1e9bfff-9b04-4e3e-9b4e-a6e527b1b2e3
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Aanbevolen werkwijzen labelen

>[!NOTE] Herinner dat het Etiketteren moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer de nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. Het kan ook nodig zijn om de labeling te herzien wanneer integratie van nieuwe oplossingen is ingeschakeld, omdat deze nieuwe variabelen toegankelijk kunnen maken waarvoor een label nodig kan zijn. Een nieuwe implementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, wat ook updates van labels kan vereisen.

## Direct vs. indirect identificeerbare id&#39;s {#section_030799AA1397433FBA61A2BC60A7A750}

Voordat u kunt achterhalen welke labels moeten worden toegepast op welke variabelen/velden, is het eerst nodig dat u de id&#39;s begrijpt die u in de analysegegevens vastlegt en dat u bepaalt welke labels u wilt gebruiken voor de privacyverzoeken voor gegevens. De Privacy van gegevens breidt het werkingsgebied uit van wat als identiteitskaart kan worden beschouwd Id&#39;s vallen in twee brede klassen: rechtstreeks identificeerbaar (identiteitslabel: I1) en indirect identificeerbaar (identiteitslabel: I2).

* **Een rechtstreeks identificeerbare ID (I1)**: Geef de persoon een naam of geef hem rechtstreeks contact op. Voorbeelden zijn de naam van iemand (zelfs een algemene naam zoals John Smith die door honderden personen kan worden gedeeld), een van zijn e-mailadressen of telefoonnummers, enz. Een postadres zonder naam kan als rechtstreeks identificeerbaar worden beschouwd, ook al kan het alleen een huishouden of bedrijf identificeren en niet een specifieke persoon binnen dat huishouden of bedrijf.
* **Een indirect identificeerbare ID (I2)**: Kan een persoon niet zelf identificeren, maar kan worden gecombineerd met andere informatie (die al dan niet in uw bezit is) om iemand te identificeren. De voorbeelden zouden een aantal van de klantenloyaliteit omvatten, of identiteitskaart die door het systeem van CRM van een bedrijf wordt gebruikt dat voor elk van hun klanten uniek is. Onder Gegevensprivacy kunnen de anonieme id&#39;s die zijn opgeslagen in de door Analytics gebruikte traceercookies, worden beschouwd als indirect identificerend, ook al kunnen zij alleen een apparaat identificeren in plaats van een individu; op een gedeeld apparaat kunnen deze cookies geen onderscheid maken tussen verschillende gebruikers van het systeem. Terwijl het cookie bijvoorbeeld niet kan worden gebruikt om een computer met het cookie te vinden, kunnen de cookies die iemand toegang tot de computer heeft en het cookie opzoekt, vervolgens weer aan de computer worden gekoppeld.

   Een IP adres wordt ook beschouwd als onrechtstreeks identificeerbaar, omdat op om het even welke bepaalde instantie in tijd, het slechts aan één enkel apparaat zou kunnen worden toegewezen. Nochtans, kan ISPs en vaak de IP adressen voor de meeste gebruikers regelmatig veranderen, zodat in tijd een IP adres door om het even welk van hun gebruikers kan zijn gebruikt. Het is ook niet ongewoon voor vele klanten van ISP of veelvoudige werknemers binnen een zaken op het zelfde Intranet om het zelfde externe IP adres te delen. Daarom biedt Adobe geen ondersteuning voor het gebruik van een IP-adres als de id voor een privacyaanvraag voor [gegevens.](/help/admin/c-data-governance/gdpr-submit-access-delete.md#submit-requests) Nochtans, wanneer identiteitskaart die wij goedkeuren als deel van een schrappingsverzoek wordt gebruikt, zullen wij de IP adressen ook ontruimen die met die identiteitskaart voorkwamen. U moet beslissen of er andere id&#39;s zijn die u verzamelt en die in deze categorie kunnen vallen, van I1 of I2, maar niet geschikt zijn voor gebruik als onderscheidende id voor verzoeken om gegevensprivacy.

Zelfs als uw bedrijf veel verschillende id&#39;s verzamelt binnen uw analysegegevens, kunt u ervoor kiezen om alleen een subset van deze id&#39;s te gebruiken voor verzoeken om gegevensprivacy. Motivering hiervoor zijn:

* Binnen uw eigen systemen kunt u een van de id&#39;s (bijvoorbeeld een e-mailadres) toewijzen aan een andere id (bijvoorbeeld CRM-id). Dan, voor consistentie, besluit u om identiteitskaart van CRM voor de verzoeken van de Privacy van Gegevens in uw verwerking van de Privacy van Gegevens slechts te gebruiken.
* U hebt geen methode om te verifiëren dat iemand eigenlijk de persoon verbonden aan identiteitskaart is. Bijvoorbeeld, kan het zeer moeilijk zijn om te bevestigen dat een IP adres slechts ooit door één enkele persoon werd gebruikt en dat de persoon die het verzoek indient eigenlijk die persoon is.
* Sommige id&#39;s komen mogelijk overeen met meerdere personen en u wilt niet het risico lopen dat gegevens over één persoon worden geretourneerd aan iemand anders met dezelfde id. Bijvoorbeeld, zelfs als u kunt verifiëren dat de naam van iemand John Smith is, kunt u niet alle gegevens over alle John Smith in uw systeem willen terugkeren.
* Een ander voorbeeld is een apparaat-id, zoals de analytische cookie-id. Als de id voorkomt op een mobiele telefoon-app, kunt u besluiten dat alle interacties met die id beschikbaar moeten zijn voor de eigenaar van de mobiele telefoon. Als de id echter op een gedeeld apparaat wordt weergegeven, zoals een thuiscomputer of een computer in een bibliotheek of internetcafé, kunt u besluiten dat u geen onderscheid kunt maken tussen gebruikers van dat apparaat en dat het risico dat gegevens voor een andere gebruiker worden geretourneerd, te groot is om het gebruik van dit type id toe te staan.

## Aanbevolen procedures voor id&#39;s die worden ondersteund door Analytics {#section_B6481505FF1949498D4B4B35B780D050}

Gebruik deze tabel om de typen id&#39;s te bepalen die u gebruikt wanneer u privacyverzoeken voor gegevens naar Analytics verzendt. Zodra u deze informatie kent, zal het gemakkelijker zijn om de andere etiketten te bepalen u voor uw variabelen zou moeten gebruiken.

<table id="table_E25612E32A03449A8E5DA00B88FCEB9E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type id </th> 
   <th colname="col2" class="entry"> Aanbevelingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-id's </p> 
    <ul id="ul_CB43CEA3054E490585CBF3AB46F95B5B"> 
     <li id="li_9174CB3910AF4EF8BA7165DB537765A5"> <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_analytics.html"> (Verouderd) Analytics Cookie </a> </li> 
     <li id="li_7B6A9A788BBD47428315B3893FC07BC3"> <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/"> Identity Service cookie </a> (ECID), voorheen bekend als de Marketing Cloud ID (MCID) </li> 
    </ul> </td> 
   <td colname="col2"> <p>Deze cookies identificeren een apparaat of, meer bepaald, een browser voor een gebruiker van een apparaat. Voor een gedeeld apparaat waar een gemeenschappelijke login wordt gebruikt, kon deze identiteitskaart op om het even welke/alle gebruikers van het apparaat van toepassing zijn. Adobe heeft één of andere <a href="https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm"> verenigde JavaScript gecreeerd </a> die u op uw website kunt plaatsen om deze koekjes te verzamelen als u hen wilt toestaan om voor de verzoeken van de Privacy van Gegevens worden gebruikt. </p> <p>Gebruikers van de Adobe Analytics Mobile SDK hebben ook een Experience Cloud-id (ECID). Er zijn API-aanroepen in de SDK om deze id te lezen, zodat u uw app kunt verfraaien en deze kunt verzamelen voor een privacyaanvraag voor gegevens. </p> <p>Veel bedrijven beschouwen de browser cookie-id's als gedeelde apparaat-id's. Dientengevolge kunnen zij, in overleg met hun juridische teams, ervoor kiezen om hen niet als aanvaardbare identiteitskaart voor de verzoeken van de Privacy van Gegevens te steunen, of zij kunnen verkiezen om slechts een zeer beperkte hoeveelheid gegevens terug te keren wanneer deze IDs worden gebruikt of zij kunnen hen slechts voor schrappingsverzoeken goedkeuren. </p> <p>Deze cookies hebben een ID-DEVICE-label dat niet kan worden gewijzigd (evenals I2- en DEL-DEVICE-labels). De standaardconfiguratie van Adobe Analytics retourneert alleen algemene informatie over het apparaat, zoals apparaattype, besturingssysteem, browser, enzovoort. plus de tijd/data waarop uw website is bezocht bij het gebruik van deze id's. Nochtans, als u verkiest om deze IDs voor de verzoeken van de Privacy van Gegevens te steunen, zoals hieronder besproken, kunt u etiketten toevoegen of verwijderen ACC-ALL om de nauwkeurige reeks gebieden te vormen u voor een de toegangsverzoek van de Privacy van Gegevens wenst te zijn teruggekeerd. </p> <p>Vooral als de rapportsuite overeenkomt met een mobiele app en uw mobiele app een aanmelding vereist, kunt u besluiten dat de Experience Cloud-id voor het apparaat wel overeenkomt met een specifieke gebruiker. Daarom wilt u meer velden een label geven met het ACC-ALL-label, inclusief de namen van bezochte pagina's, weergegeven producten, enzovoort. </p> <p>Opmerking:  Als u de optie "expandIds" opgeeft in uw privacyverzoek, bevatten uw aanvragen altijd cookie-id's, plus eventuele andere id's die u opgeeft. Zie <a href="/help/admin/c-data-governance/gdpr-id-expansion.md"> ID-uitbreiding </a> voor meer informatie. In deze gevallen, zullen de klappen die slechts een koekjesidentiteitskaart, maar geen andere identiteitskaart hebben, slechts gegevens geëtiketteerd ACC-ALL als deel van het toegangsverzoek terugkeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Id's in aangepaste variabelen </p> </td> 
   <td colname="col2"> <p>Sommige klanten plaatsen IDs in de variabelen van het <a href="https://marketing.adobe.com/resources/help/en_US/sc/implement/props_eVars.html"> douaneverkeer (steunen) of douane omzettingsvariabelen (eVars) </a>. Terwijl meest algemeen een identiteitskaart van CRM is, omvatten anderen e-mailadressen, gebruikerslogin namen, de aantallen van de klantenloyaliteit of hashes van deze waarden. </p> 
    <ul id="ul_0B9492CF786046BB97E31CCF83A85FEA"> 
     <li id="li_D35B61CC6A8B485A8E09358A46D3F598">Als u een van deze id's wilt gebruiken voor verzoeken om gegevensprivacy, moet u het veld dat deze id-PERSON bevat een label geven. </li> 
     <li id="li_94541340B054436297C5565F074413DC">(Veel minder vaak) Als een id in een van deze aangepaste variabelen alleen een apparaat identificeert dat door meerdere personen kan worden gedeeld, kunt u in plaats daarvan een ID-DEVICE-label gebruiken. </li> 
     <li id="li_8115B999E8DA46CAB359BCF1F4A4DCAE">Deze gebieden vereisen ook I1 of I2 etiketten, en zouden een DEL-PERSON of DEL-DEVICE etiket moeten omvatten. Doorgaans komt de optie PERSON/APPARAAT van het DEL-label overeen met de optie PERSON/APPARAAT van het ID-label. </li> 
    </ul> <p> Het komt zelden voor dat een rapportsuite meer dan een of twee aangepaste variabelen bevat die id's bevatten die u wilt gebruiken om de betrokkenen te identificeren voor verzoeken om gegevensprivacy. U kunt veelvoudige variabelen hebben die I1 of I2 etiketten worden toegewezen, maar typisch slechts één of twee van deze zouden ook ID-PERSON of ID-DEVICE etiketten hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste bezoeker-id </p> </td> 
   <td colname="col2"> <p>Hoewel dit niet wijd wordt gebruikt, steunt de Analytics ook een implementatie waar een douanetoedienings identiteitskaart kan worden verstrekt, die als aanwezig in plaats van het het Volgen Cookie van de Analyse van de Oudheid wordt gebruikt. Dit veld heeft de labels I2, ID-PERSON en DEL-PERSON. </p> <p>Vele implementaties leiden deze identiteitskaart van identiteitskaart van CRM af zodat is het aanwezig slechts terwijl iemand in hun plaats wordt geregistreerd. Hierdoor kan dezelfde aangepaste bezoeker-id op verschillende apparaten worden gebruikt. Eén technisch nadeel is dat het bijhouden van gegevens die plaatsvinden voordat de gebruiker zich aanmeldt, niet kan worden gekoppeld aan het bijhouden van gegevens die zijn verzameld nadat deze zijn aangemeld. Als u in plaats daarvan de aangepaste bezoeker-id gebruikt om een apparaat te identificeren, moet u de labels ID-PERSON en DEL-PERSON wijzigen in respectievelijk ID-DEVICE en DEL-DEVICE. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aanbevolen procedures voor het instellen van labels voor verwijderen {#section_08166C99B48E49218392FAC18922C10E}

>[!NOTE] Props zijn altijd niet hoofdlettergevoelig. Vars zijn standaard niet hoofdlettergevoelig, maar kunnen via de klantenservice van Adobe worden geconfigureerd om hoofdlettergevoelig te zijn. Als u een hoofdlettergevoelige eVar hebt die een identiteitskaart bevat, is het uw verantwoordelijkheid om het juiste geval te gebruiken wanneer het voorleggen van een verzoek van de Privacy van Gegevens zodat de geval die in het verzoek wordt gebruikt het geval aanpast dat in treffers wordt gebruikt die deze IDs bevatten.

De verwijderlabels DEL-DEVICE en DEL-PERSON moeten spaarzaam worden gebruikt. Wanneer toegepast op een variabele die geen identiteitskaart bevat die als deel van het verzoek van de Privacy van Gegevens werd gebruikt, zullen de tellingen (metriek) in historische rapporten van de Analyse bijna altijd veranderen.

* Wij adviseren dat één van deze etiketten op om het even welke variabele wordt toegepast die I1, I2 of S1 wordt geëtiketteerd. Zij kunnen niet op om het even welke variabele worden toegepast die niet I1, I2 of S1 geëtiketteerd is.
* De DEL-etiketten zullen in deze variabelen resulteren die worden [geanonimiseerd](/help/admin/c-data-governance/gdpr-labels.md#data-governance-labels) (identiteitskaart zal met een willekeurige koord worden vervangen met &quot;Privacy van Gegevens&quot; vooraf wordt bepaald). Dezelfde geanonimiseerde waarde vervangt alle instanties van de oorspronkelijke waarde in alle treffers die zijn geïdentificeerd door een id die in de aanvraag wordt gebruikt. Als de oorspronkelijke waarde in dit veld een van deze id&#39;s was, worden de gegevens van het rapport niet gewijzigd.
* Over het algemeen geldt dat als een veld het label ID-DEVICE heeft, u ook het label DEL-DEVICE moet toewijzen.
* Als een veld het label ID-PERSON heeft, moet u ook het label DEL-PERSON toewijzen.
* Als een veld geen id-label heeft, maar wel identificatiegegevens bevat die u anoniem wilt maken, is het desbetreffende label (DEVICE of PERSON) afhankelijk van uw implementatie. Als u cookie-id&#39;s alleen gebruikt voor verzoeken om gegevensprivacy, moet u DEL-DEVICE gebruiken.
* Als u aangepaste id&#39;s in een ander veld gebruikt met een ID-PERSON-label, en u wilt deze alleen wissen op rijen met die id, gebruikt u DEL-PERSON.
* Als u de uitbreiding van identiteitskaart gebruikt, en alle waarde ontruimd voor alle treffers op alle geïdentificeerde apparaten dan gebruik DEL-DEVICE. U kunt in dit geval de labels DEL-DEVICE en DEL-PERSON toepassen, maar het label DEL-PERSON is onnodig omdat de ID-uitbreiding betekent dat alle rijen die overeenkomen met een persoon-id ook overeenkomen met een apparaat-id.
* Als u niet zult specificeren om de Uitbreiding van identiteitskaart te gebruiken, maar een mengeling apparaat en persoon IDs voor verschillende verzoeken zal gebruiken, dan kunt u zowel DEL-DEVICE als DEL-PERSON etiketten voor variabelen willen specificeren die zouden moeten worden geschrapt wanneer één van beide type van identiteitskaart wordt gebruikt.
* Merk op dat als een DEL-DEVICE of DEL-PERSON etiket op om het even welke variabele wordt gespecificeerd die niet ook als identiteitskaart voor dat verzoek (met inbegrip van een uitgebreide identiteitskaart) wordt gebruikt, dan unieke waarden in die variabele slechts bij treffers zullen worden geanonimiseerd waar een gespecificeerde (of uitgebreide) identiteitskaart voorkomt. Als andere treffers de zelfde waarde bevatten, zal het niet in die andere plaatsen worden bijgewerkt. Dit kan ertoe leiden dat tellingen (metriek) veranderen.

   Als u bijvoorbeeld drie hits hebt met de waarde &quot;foo&quot; in eVar7, maar slechts één daarvan bevat een id in een andere variabele die bij een delete hoort, wordt &quot;foo&quot; op die hit gewijzigd in een waarde zoals &quot;Data Privacy-123456789&quot;, terwijl deze waarde in de andere twee hits ongewijzigd blijft. Een rapport dat het aantal unieke waarden voor eVar7 toont zal nu één meer unieke waarde tonen dan het eerder deed. Een rapport dat de hoogste waarden voor eVars toont kan &quot;foo&quot;met slechts twee instanties (eerder dan 3 eerder) omvatten, en de nieuwe waarde zal ook verschijnen, met één enkele instantie.

## Beste praktijken voor het plaatsen van de Etiketten van de Toegang {#section_AC7E216F81C141FCA6A62F8836E06EE7}

Hoewel zeer weinig velden een van de andere labels hebben, is het voor een groot aantal velden gebruikelijk om ACC-labels te gebruiken. De aangewezen toegangslabels zullen afhangen van IDs u voor de verzoeken van de Privacy van Gegevens gebruikt.

<table id="table_A5B834CC08C641D99E2691A2361997E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Als u... </th> 
   <th colname="col2" class="entry"> ...Gebruik deze Aanbevelingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Alleen apparaat-id's </p> </td> 
   <td colname="col2"> <p>Als de enige id's die u gebruikt cookie-id's zijn of id's met een ID-DEVICE-label, moet u alleen het ACC-ALL-label gebruiken. </p> <p>U zult één paar dossiers voor elke toegangsverzoek krijgen, één die een rij voor elke passende klap met alle gespecificeerde ACC-ALLE gebieden en een tweede bevat een samenvatting van deze gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Persoon-id's zonder id-uitbreiding </p> </td> 
   <td colname="col2"> <p>Als u alleen aangepaste id's gebruikt die het label ID-PERSON hebben en geen id-uitbreiding uitvoeren, moet u de labels ACC-PERSON gebruiken. Nochtans, te hoeven u niet om de standaardACC-ALLE etiketten te veranderen; deze velden worden automatisch opgenomen in het toegangsverzoek . </p> <p>U zult één paar dossiers voor elk toegangsverzoek krijgen, één die een rij voor elke passende aanraakaantoning met alle gespecificeerde ACC-DEVICE en ACC-PERSON gebieden en een tweede bevat een samenvatting van deze gegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gemengde id's en/of ID-uitbreiding </p> </td> 
   <td colname="col2"> <p>Als u zowel apparaat als persoon-id's opneemt in verzoeken om gegevensprivacy, of als u aangepaste id's gebruikt (aangepaste bezoeker-id of een id in een proxy of eVar), moet u aandacht besteden aan de ACC-labels die u gebruikt. Elk toegangsverzoek zal twee paren gegevensdossiers terugkeren, één paar die gegevens van hits bevatten die een overeenkomende persoonsidentiteitskaart bevatten en een tweede die gegevens van hits bevatten die geen persoonsidentiteitskaart aanvielen, maar een apparatenidentiteitskaart aanstemden. </p> <p>De bestanden met de id van de persoon bevatten gegevens over alle treffers die overeenkomen met de id van de persoon in alle velden met een ACC-PERSON- of ACC-ALL-label (één bestand met alle overeenkomende treffers en het andere als een overzicht). </p> <p>Het bestandspaar 'apparaat-id' bevat alleen velden met een ACC-ALL-label en bevat alleen resultaten die geen overeenkomende persoon-id bevatten. Deze bestanden kunnen gegevens bevatten die zijn gegenereerd door andere gebruikers van een gedeeld apparaat. Daarom moet u zorgvuldig rekening houden met de set velden die het ACC-ALL-label bevatten. Bij de standaardlabels in Analytics wordt dit label alleen toegepast op algemene informatievelden die betrekking hebben op het apparaat (apparaattype, besturingssysteem, browser, enz.) plus de datum/tijd van elke treffer. </p> <p>U kunt ervoor kiezen om zowel de apparaatbestanden als de persoonlijke bestandssets van Adobe te ontvangen en vervolgens alleen de persoonlijke bestanden te delen, zodat gegevens die mogelijk door andere gebruikers van een gedeeld apparaat zijn gegenereerd, niet worden gedeeld. U kunt ook gegevens uit een of beide sets combineren met andere informatie die u over de betrokkene weet en deze in uw eigen indeling retourneren. </p> </td> 
  </tr> 
 </tbody> 
</table>

