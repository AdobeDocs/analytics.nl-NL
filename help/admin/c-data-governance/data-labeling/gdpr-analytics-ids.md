---
description: Begrijp de id's die zijn vastgelegd in de analysegegevens en bepaal welke u wilt gebruiken voor de aanvragen voor gegevensprivacy.
title: Best practices voor labelen
feature: Data Governance
exl-id: 00da58b0-d613-4caa-b9c1-421b1b541f47
source-git-commit: a36654fcf10712e0d12917bad832bb46f343d6fd
workflow-type: tm+mt
source-wordcount: '2695'
ht-degree: 79%

---

# Best practices voor labelen

>[!NOTE]
>
>Herinner dat het etiketteren moet worden herzien telkens als een nieuwe rapportreeks wordt gecreeerd of wanneer de nieuwe variabele binnen een bestaande rapportreeks wordt toegelaten. U dient de labeling mogelijk ook te herzien wanneer integraties van nieuwe oplossingen worden ingeschakeld, omdat deze nieuwe variabelen kunnen laten zien waarvoor een label nodig is. Een herimplementatie van uw mobiele apps of websites kan de manier veranderen waarop bestaande variabelen worden gebruikt, waardoor eveneens updates van labels nodig kunnen zijn.

## Direct of indirect identificeerbare id&#39;s {#direct-vs-indirect}

Voordat u kunt achterhalen welke labels op welke variabelen/velden moeten worden toegepast, moet u eerst de id&#39;s begrijpen die u in de Analytics-data vastlegt, en beslissen welke u gebruikt voor Data Privacy-aanvragen. Data Privacy breidt het bereik uit van wat als id kan worden beschouwd. Id&#39;s vallen in twee brede klassen: rechtstreeks identificeerbaar (identiteitslabel: I1) en indirect identificeerbaar (identiteitslabel: I2).

* **Een rechtstreeks identificeerbare id (I1)**: noemt de persoon bij naam of biedt een directe methode om contact op te nemen. Voorbeelden zijn de iemands naam (zelfs een algemene naam zoals John Smith die door honderden personen kan worden gedeeld), een van zijn of haar e-mailadressen of telefoonnummers, enz. Een postadres zonder naam kan als rechtstreeks identificeerbaar worden beschouwd, ook al identificeert het alleen een huishouden of bedrijf in plaats van een bepaalde persoon binnen dat huishouden of bedrijf.
* **Een indirect identificeerbare id (I2)**: kan een persoon niet zelf identificeren, maar kan worden gecombineerd met andere informatie (die al dan niet in uw bezit is) om iemand te identificeren. De voorbeelden van indirect identificeerbare identiteitskaart omvatten een aantal van de klantenloyaliteit, of identiteitskaart die door het systeem van CRM van een bedrijf wordt gebruikt dat voor elk van hun klanten uniek is. Onder Data Privacy kunnen de anonieme id&#39;s die zijn opgeslagen in de door Analytics gebruikte trackingcookies, worden beschouwd als indirect identificerend, ook al kunnen ze alleen een apparaat identificeren en geen individu; op een gedeeld apparaat kunnen deze cookies geen onderscheid maken tussen verschillende gebruikers van het systeem. Het cookie kan bijvoorbeeld niet worden gebruikt om een computer met het cookie te vinden, maar als iemand toegang tot de computer heeft en het cookie opzoekt, kunnen de Analytics-cookiedata vervolgens wel weer aan de computer worden gekoppeld.

   Een IP adres wordt ook beschouwd als indirect identificeerbaar, omdat het op om het even welk bepaald ogenblik slechts aan één enkel apparaat zou kunnen worden toegewezen. Maar ISP’s kunnen de IP-adressen van de meeste gebruikers regelmatig veranderen en dat doen ze ook, zodat in de loop van de tijd een IP-adres door elk van hun gebruikers kan zijn gebruikt. Het is ook niet ongewoon dat vele klanten van een ISP of meerdere medewerkers binnen een bedrijf op hetzelfde intranet hetzelfde externe IP-adres delen. Daarom biedt Adobe geen ondersteuning voor het gebruik van een IP-adres als de id voor een privacyaanvraag voor gegevens. Wanneer echter een id die wij accepteren, wordt gebruikt als onderdeel van een verwijderingsaanvraag, zullen we de IP-adressen die bij deze id zijn voorgekomen, eveneens wissen. U moet beslissen of er andere verzamelde id&#39;s bestaan die in deze categorie kunnen vallen, van I1 of I2, maar die niet geschikt zijn voor gebruik als onderscheidende ID voor verzoeken om privacy van gegevens.

Zelfs als uw bedrijf binnen uw Analytics-data veel verschillende id&#39;s verzamelt, kunt u ervoor kiezen om uitsluitend een subset van deze id&#39;s te gebruiken voor Data Privacy-aanvragen. Dit kan de volgende redenen hebben:

* Binnen uw eigen systemen kunt u een van de id&#39;s (bijvoorbeeld een e-mailadres) toewijzen aan een andere id (bijvoorbeeld een CRM-id). Ter wille van de consistentie besluit u vervolgens om alleen de CRM-id te gebruiken voor Data Privacy-aanvragen in uw Data Privacy-verwerking.
* U hebt geen methode om te verifiëren of iemand werkelijk de persoon is die aan de id is gekoppeld. Het kan bijvoorbeeld heel lastig zijn om te controleren of een IP-adres uitsluitend door één persoon is gebruikt werd gebruikt en of de persoon die de aanvraag verzendt, inderdaad deze persoon is.
* Sommige id&#39;s komen mogelijk overeen met meerdere personen en u wilt niet het risico lopen dat gegevens over één persoon worden geretourneerd aan iemand anders met dezelfde id. Zelfs als u bijvoorbeeld kunt verifiëren dat iemand John Smith heet, wilt u waarschijnlijk toch niet alle data over alle John Smiths in uw systeem retourneren.
* Een ander voorbeeld is een apparaat-id, zoals de Analytics-cookie-id. Als de id voorkomt in een mobiele-telefoon-app, kunt u besluiten dat alle interacties met die id beschikbaar moeten zijn voor de eigenaar van de mobiele telefoon. Als de id echter op een gedeeld apparaat wordt weergegeven zoals een thuiscomputer of een computer in een bibliotheek of een internetcafé, kunt u besluiten dat u geen onderscheid kunt maken tussen de gebruikers van dat apparaat, en dat het risico dat data voor een andere gebruiker worden geretourneerd, te groot is om het gebruik van dit type id toe te staan.

## Aanbevolen procedures voor id&#39;s die worden ondersteund door Analytics {#best-practices-an}

Gebruik deze tabel om te bepalen welke soorten id&#39;s u gaat gebruiken wanneer u Data Privacy-aanvragen naar Analytics verzendt. Zodra u deze informatie hebt, wordt het gemakkelijker om de andere labels te bepalen die u voor uw variabelen moet gebruiken.

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
     <li id="li_9174CB3910AF4EF8BA7165DB537765A5"> <a href="https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html"> (Verouderd) Analytics-cookie </a> </li> 
     <li id="li_7B6A9A788BBD47428315B3893FC07BC3"> <a href="https://experienceleague.adobe.com/docs/id-service/using/home.html"> Identity Service-cookie </a> (ECID), vroeger Marketing Cloud-id (MCID) genoemd </li> 
    </ul> </td> 
   <td colname="col2"> <p>Deze cookies identificeren een apparaat of, specifieker, een browser voor een gebruiker van een apparaat. Voor een gedeeld apparaat waar een gemeenschappelijke aanmelding wordt gebruikt, zou deze id kunnen gelden voor alle gebruikers van het apparaat. Adobe heeft een bepaald <a href="https://developer.adobe.com/experience-platform-apis/references/privacy-service/"> gecombineerd JavaScript </a> gemaakt dat u op uw website kunt plaatsen om deze cookies te verzamelen als u wilt dat ze worden gebruikt voor Data Privacy-aanvragen. </p> <p>Gebruikers van de Adobe Analytics Mobile SDK hebben ook een Experience Cloud ID (ECID). Er zijn API-calls in de SDK om deze id te lezen, zodat u uw app deze kunt laten verzamelen voor een Data Privacy-aanvraag. </p> <p>Veel bedrijven beschouwen de browsercookie-id's als gedeelde apparaat-id's. Dientengevolge kunnen zij, in overleg met hun juridische teams, ervoor kiezen deze niet te ondersteunen als aanvaardbare id's voor verzoeken om gegevensprivacy. Ze kunnen er ook voor kiezen slechts een zeer beperkte hoeveelheid gegevens te retourneren wanneer deze id's worden gebruikt of alleen voor verwijderingsverzoeken. </p> <p>Deze cookies hebben een ID-DEVICE-label dat niet kan worden gewijzigd (evenals I2- en DEL-DEVICE-labels). De standaardconfiguratie van Adobe Analytics retourneert alleen algemene informatie over het apparaat zoals apparaattype, besturingssysteem, browser, enzovoort. plus de tijd/datums waarop uw website is bezocht met gebruik van deze id's. Als u er echter voor kiest om deze id's te ondersteunen voor Data Privacy-aanvragen zoals hieronder besproken, kunt u ACC-ALL-labels toevoegen of verwijderen om precies de veldenreeks te configureren die u wilt laten retourneren voor een Data Privacy-toegangsaanvraag. </p> <p>Als de rapportsuite overeenkomt met een mobiele app waarvoor een aanmelding is vereist, kunt u besluiten dat de Experience Cloud-id voor het apparaat wel overeenkomt met een specifieke gebruiker. In dat geval wilt u wellicht meer velden een label geven met het ACC-ALL-label, inclusief de namen van de bezochte pagina's, de weergegeven producten enzovoort. </p> <p>Opmerking:  Als u de optie “expandIds” opgeeft in uw Data Privacy-aanvraag, bevatten uw aanvragen altijd cookie-id's, plus eventuele andere id's die u opgeeft. Zie <a href="/help/admin/c-data-governance/gdpr-id-expansion.md"> Id-uitbreiding </a> voor meer informatie. In deze gevallen zullen de treffers die alleen een cookie-id hebben, maar geen andere id, alleen data retourneren met het label ACC-ALL als deel van de toegangsaanvraag. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Id's in aangepaste variabelen </p> </td> 
   <td colname="col2"> <p>Sommige klanten plaatsen id's in <a href="https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/evar.html"> aangepaste traffic variabelen (props) of aangepaste conversievariabelen (eVars) </a>. De meest voorkomende is een CRM-id, maar andere zijn e-mailadressen, gebruikersnamen voor aanmelding, klantloyaliteitsnummers of hashes van deze waarden. </p> 
    <ul id="ul_0B9492CF786046BB97E31CCF83A85FEA"> 
     <li id="li_D35B61CC6A8B485A8E09358A46D3F598">Als u een van deze id's wilt gebruiken voor Data Privacy-aanvragen, moet u het veld waar het in staat, een ID-PERSON-label geven. </li> 
     <li id="li_94541340B054436297C5565F074413DC">(Veel minder vaak) Als een id in een van deze aangepaste variabelen alleen een apparaat identificeert dat door meerdere personen kan worden gedeeld, kunt u in plaats daarvan een ID-DEVICE-label gebruiken. </li> 
     <li id="li_8115B999E8DA46CAB359BCF1F4A4DCAE">Deze velden vereisen ook I1- of I2-labels, en zouden een DEL-PERSON- of DEL-DEVICE-label moeten hebben. Meestal komt de optie PERSON/DEVICE van het DEL-label overeen met de optie PERSON/DEVICE van het ID-label. </li> 
    </ul> <p> Het komt zelden voor dat een rapportsuite meer dan een of twee aangepaste variabelen bevat die id's bevatten die u wilt gebruiken om gegevensonderwerpen te identificeren voor verzoeken om gegevensprivacy. U kunt meerdere variabelen hebben waaraan I1- of I2-labels zijn toegewezen, maar meestal zijn er maar een of twee daarvan die ook een ID-PERSON- of ID-DEVICE-label hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste bezoekers-id </p> </td> 
   <td colname="col2"> <p>Hoewel het gebruik hiervan niet wijd verspreid is, ondersteunt Analytics ook een implementatie waarbij een aangepaste bezoekers-id kan worden verstrekt, die (mits aanwezig) wordt gebruikt in plaats van het verouderde Analytics-trackingcookie. Dit veld heeft de labels I2, ID-PERSON en DEL-PERSON. </p> <p>Vele implementaties leiden deze identiteitskaart uit een identiteitskaart van CRM af zodat het slechts aanwezig is terwijl iemand in hun plaats wordt geregistreerd. Hierdoor kan dezelfde aangepaste bezoekers-id op verschillende apparaten worden gebruikt. Eén technisch nadeel is dat de tracking vóór aanmelding door de gebruiker niet kan worden gekoppeld aan de tracking die wordt verzameld nadat de gebruiker zich heeft zijn aangemeld. Als u in plaats daarvan de aangepaste bezoekers-id gebruikt om eenvoudig een apparaat te identificeren, moet u het ID-PERSON- en DEL-PERSON-label wijzigen in ID-DEVICE DEL-DEVICE. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Aanbevolen procedures voor het instellen van labels voor verwijderen {#best-practices-delete}

>[!NOTE]
>
>Props zijn altijd niet-hoofdlettergevoelig. eVars zijn standaard niet-hoofdlettergevoelig, maar kunnen via de klantenservice van Adobe worden geconfigureerd om wel hoofdlettergevoelig te zijn. Als u een hoofdlettergevoelige eVar hebt met een id, is het uw verantwoordelijkheid om de juiste hoofd- en/of kleine letters te gebruiken bij het verzenden van een Data Privacy-aanvraag, zodat de gebruikte letters in de aanvraag overeenkomen met de letters in de treffers voor deze id&#39;s.

De verwijderingslabels DEL-DEVICE en DEL-PERSON moeten spaarzaam worden gebruikt. Wanneer ze worden toegepast op een variabele die geen id bevat die als deel van de Data Privacy-aanvraag is gebruikt, zullen de tellingen (cijfers) in historische rapporten van Analytics bijna altijd veranderen.

* We adviseren om een van deze labels toe te passen op elke variabele met het label I1, I2 of S1. Deze kunnen niet worden toegepast op een variabele die niet het label I1, I2 of S1 heeft.
* De DEL-labels zullen ertoe leiden dat deze variabelen worden [geanonimiseerd](/help/admin/c-data-governance/data-labeling/gdpr-labels.md#data-governance-labels) (de id wordt vervangen door een willekeurige tekenreeks met als voorvoegsel “Data Privacy-”). Dezelfde geanonimiseerde waarde vervangt alle instanties van de oorspronkelijke waarde in alle treffers die zijn geïdentificeerd door een id die in de aanvraag wordt gebruikt. Als de oorspronkelijke waarde in dit veld een van deze id&#39;s was, veranderen de cijfers in het rapport niet.
* Over het algemeen geldt dat als een veld het label ID-DEVICE heeft, u ook het label DEL-DEVICE moet toewijzen.
* Als een veld het label ID-PERSON heeft, moet u ook het label DEL-PERSON toewijzen.
* Als een veld geen id-label heeft, maar wel identificatiedata bevat die u anoniem wilt maken, is het betreffende label (DEVICE of PERSON) afhankelijk van uw implementatie. Als u cookie-id&#39;s alleen gebruikt voor Data Privacy-aanvragen, moet u DEL-DEVICE gebruiken.
* Als u aangepaste id&#39;s gebruikt in een ander veld met een ID-PERSON-label, en u dit deze alleen wilt wissen op rijen waar deze id voorkomt, gebruikt u DEL-PERSON.
* Als u id-uitbreiding gebruikt en alle waarden wilt wissen voor alle treffers op alle geïdentificeerde apparaten, gebruik dan DEL-DEVICE. U kunt in dit geval zowel het label DEL-DEVICE als het label DEL-PERSON toepassen, maar het label DEL-PERSON is onnodig omdat de id-uitbreiding betekent dat alle rijen die overeenkomen met een persoons-id, ook overeenkomen met een apparaat-id.
* Als u niet het gebruik van de Uitbreiding van identiteitskaart specificeert, maar een mengeling apparaat en persoon IDs voor verschillende verzoeken zal gebruiken, dan kunt u zowel DEL-DEVICE als DEL-PERSON etiketten voor variabelen willen specificeren die zouden moeten worden geschrapt wanneer één van beide type van identiteitskaart wordt gebruikt.
* Bedenk dat, als een DEL-DEVICE- of DEL-PERSON-label wordt opgegeven voor elke variabele die niet ook wordt gebruikt als id voor deze aanvraag (inclusief een uitgebreide id), dan zullen unieke waarden in deze variabele alleen worden geanonimiseerd bij treffers waar een opgegeven (of uitgebreide) id voorkomt. Als andere treffers dezelfde waarde bevatten, wordt dit niet op deze andere plaatsen bijgewerkt. Dit kan ertoe leiden dat tellingen (cijfers) veranderen.

   Als u bijvoorbeeld drie treffers hebt met de waarde “foo” in eVar7, maar slechts één daarvan ook een id in een andere variabele bevat die een match heeft voor verwijdering, wordt “foo” in deze treffer gewijzigd in een waarde als “Data Privacy-123456789”, terwijl deze waarde in de andere twee treffers ongewijzigd blijft. Een rapport met het aantal unieke waarden voor eVar7 toont nu één unieke waarde meer dan daarvoor. Een rapport dat de hoogste waarden voor eVars toont, kan “foo” met slechts twee instanties bevatten (in plaats van 3, zoals vroeger), en de nieuwe waarde zal ook worden getoond, met één instantie.

## Beste praktijken voor het plaatsen van de etiketten van de Toegang {#best-practices-access}

Hoewel heel weinig velden een van de andere labels hebben, komt het vaak voor dat een groot aantal velden ACC-labels heeft. Welke toegangslabels juist zijn, hangt af van de id&#39;s die u gebruikt voor Data Privacy-aanvragen.

<table id="table_A5B834CC08C641D99E2691A2361997E4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Als u... </th> 
   <th colname="col2" class="entry"> ...deze aanbevelingen gebruikt </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Alleen apparaat-id's </p> </td> 
   <td colname="col2"> <p>Als de enige id's die u gebruikt, cookie-id's zijn, of id's met een ID-DEVICE-label, moet u alleen het ACC-ALL-label gebruiken. </p> <p>U zult één paar dossiers voor elke toegangsverzoek krijgen, één die een rij voor elke passende klap met alle gespecificeerde ACC-ALLE gebieden en andere bevat een samenvatting van deze gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Persoons-id's zonder id-uitbreiding </p> </td> 
   <td colname="col2"> <p>Als u alleen aangepaste id's gebruikt met het label ID-PERSON die geen id-uitbreiding hebben, moet u ACC-PERSON-labels gebruiken. U hoeft echter niet de standaard ACC-ALL-labels te wijzigen; deze velden worden automatisch opgenomen in de toegangsaanvraag. </p> <p>U krijgt één paar bestanden voor elke toegangsaanvraag, één met een rij voor elke overeenkomende treffer met alle gespecificeerde ACC-DEVICE- en ACC-PERSON-velden, en een tweede met een overzicht van deze data. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gemengde id's en/of id-uitbreiding </p> </td> 
   <td colname="col2"> <p>Als u in Data Privacy-aanvragen zowel apparaat- als persoons-id’s opneemt, of als u aangepaste id's gebruikt (aangepaste bezoekers-id of een id in een prop of eVar), moet u opletten welke ACC-labels u gebruikt. Elk toegangsverzoek zal twee paren gegevensdossiers terugkeren, één paar die gegevens van klappen bevatten die een overeenkomende persoonsidentiteitskaart bevatten en andere die gegevens van klappen bevatten die geen persoonsidentiteitskaart aanvielen, maar een apparatenidentiteitskaart aanpaste. </p> <p>De bestanden met persoons-id bevatten data van alle treffers die overeenkomen met de persoons-id's met alle velden met een ACC-PERSON- of een ACC-ALL-label (één bestand met alle overeenkomende treffers en het andere als overzicht). </p> <p>Het bestandspaar met apparaat-id bevat alleen velden met een ACC-ALL-label en bevat alleen treffers die geen overeenkomende persoons-id bevatten. Deze bestanden kunnen gegevens bevatten die zijn gegenereerd door andere gebruikers van een gedeeld apparaat. Denk daarom zorgvuldig na over de set velden die het ACC-ALL-label bevatten. Bij de standaardlabeling in Analytics wordt dit label uitsluitend toegepast op generieke informatievelden die met het apparaat te maken hebben (apparaattype, besturingssysteem, browser, enzovoort.) plus de datum/tijd van elke treffer. </p> <p>U kunt ervoor kiezen om zowel de apparaatbestandsreeksen als de persoonsbestandsreeksen van Adobe te ontvangen en vervolgens alleen de persoonsbestanden te delen, zodat data die mogelijk door andere gebruikers van een gedeeld apparaat zijn gegenereerd, niet worden gedeeld. Of u wilt gegevens uit een of beide sets combineren met andere informatie die u over het onderwerp kent en deze in uw eigen indeling retourneren. </p> </td> 
  </tr> 
 </tbody> 
</table>
