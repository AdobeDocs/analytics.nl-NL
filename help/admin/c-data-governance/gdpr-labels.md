---
description: Voorbeelden van gegevensprivacylabels voor Adobe Analytics-variabelen
title: Data Privacy-labels voor Analytics-variabelen
exl-id: b8c2143a-6e8e-465a-979b-aa8176e8d4e8
source-git-commit: de059ecc9f7ec2fe7ce544ee9cd48d81ad952887
workflow-type: tm+mt
source-wordcount: '3906'
ht-degree: 95%

---

# Data Privacy-labels voor Analytics-variabelen

## Waarom labels toewijzen aan uw data? {#why-label}

Veel klanten van Adobe hebben juridische teams die de wetten van de Privacy van Gegevens (GDPR, CCPA, enz.) hebben herzien. Deze teams hebben mogelijk hun eigen conclusies getrokken over de manier waarop gegevens moeten worden verwerkt om te voldoen aan de privacywetten voor gegevens. De juridische interpretaties kunnen per bedrijf verschillen en de gewenste instellingen voor dataverwerking kunnen ook per klant verschillen. Aangezien klanten verschillende voorkeuren voor Data Privacy-dataverwerking hebben en verschillende datasets, maakt Adobe het mogelijk voor klanten, als datacontrollers, hun gewenste instellingen aan te passen voor de Data Privacy-dataverwerking van hun unieke data. Hierdoor kan elke afzonderlijke klant Data Privacy-aanvragen verwerken op de manier door voor het merk en de unieke dataset van deze klant het meest zinnig is.

Adobe Analytics biedt tools voor het labelen van data op basis van de gevoeligheid en contractuele beperkingen ervan. Labels zijn belangrijk en handig voor het volgende: (1) geregistreerde personen identificeren, (2) bepalen welke data moeten worden geretourneerd als onderdeel van een toegangsaanvraag, en (3) datavelden identificeren die moeten worden verwijderd als onderdeel van een verwijderingsaanvraag.

Voordat u kunt achterhalen welke labels op welke variabelen/velden moeten worden toegepast, moet u [de id&#39;s begrijpen](/help/admin/c-data-governance/gdpr-analytics-ids.md) die u in de Analytics-data vastlegt, en beslissen welke u gebruikt voor Data Privacy-aanvragen.

De implementatie van Adobe Analytics Data Privacy ondersteunt de volgende labels voor identiteitsdata, gevoelige data en data-governance.

## DULE-labels {#dule-labels}

>[!NOTE]
>
>Het DULE-kader (Data Usage Labeling &amp; Enforcement) is ontworpen als een uniforme manier voor alle Adobe-oplossingen/services/platforms om metadata over data vast te leggen, te communiceren en te gebruiken in de hele Adobe Experience Cloud. De metadata helpen datacontrollers om aan te geven welke data persoonlijke data zijn, welke data gevoelig zijn, en welke contractbeperkingen aan data zijn gekoppeld. In deze eerste versie stelt Analytics alleen de DULE-labels beschikbaar die relevant zijn voor Data Privacy. Aangezien andere producten van Adobe ondersteuning implementeren voor DULE-labels, zullen bij toekomstige versies extra labels worden geïntroduceerd voor gevoelige data, evenals contractlabels, waardoor data die tussen producten worden gedeeld, uitsluitend worden gebruikt op wettelijk toegestane manieren.

## Identiteitsdata (DULE) {#identity-data-labels}

“I”-labels voor identiteitsdata worden gebruikt om data te categoriseren waarmee een specifieke persoon kan worden geïdentificeerd of gecontacteerd.

<table id="table_6B5368D714424E52835D5DFE189BD080"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Label </th> 
   <th colname="col2" class="entry"> Definitie </th> 
   <th colname="col3" class="entry"> Overige vereisten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>I1 </p> </td> 
   <td colname="col2"> <p><b>Direct identificeerbaar</b>: data waarmee een individu kan worden geïdentificeerd of waardoor rechtstreeks contact met een individu mogelijk wordt, zoals een naam of e-mailadres. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_4E2AD59D119E40D28B869D0BB63B9FD9"> 
     <li id="li_AC3E99B57E3A4AE2A12BE219680AFC58">Kan niet worden ingesteld voor gebeurtenissen </li> 
     <li id="li_BB66992863C8402F8D58656293F31E71">Kan niet worden ingesteld voor merchandising-eVars </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I2 </p> </td> 
   <td colname="col2"> <p><b>Indirect identificeerbaar</b>: data die in combinatie met andere data kunnen worden gebruikt om een individu of apparaat te identificeren of direct contact mogelijk te maken. </p> <p>Met zulke data kan een individu op zichzelf niet worden geïdentificeerd, maar ze kunnen wel worden gecombineerd met andere informatie (die al dan niet in uw bezit is) om iemand te identificeren. Voorbeelden zijn een klantloyaliteitsnummer of een id die door het CRM-systeem van een bedrijf wordt gebruikt en die voor elke klant uniek is. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_A0EF0F3DC5804D4FBE228946D697ABEB"> 
     <li id="li_A592EA6DA82C4D8C80E03F02ADF4E20E">Kan niet worden ingesteld voor gebeurtenissen </li> 
     <li id="li_46CE7B1E84884CDAB356A6DF89397849">Kan niet worden ingesteld voor merchandising-eVars </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Labels voor gevoelige data (DULE) {#sensitive-data-labels}

“S”-labels voor gevoelige data worden gebruikt om gevoelige data zoals geografische data te categoriseren. In de toekomst zullen extra labels voor gevoelige data worden geïntroduceerd om andere soorten gevoelige informatie te identificeren.

<table id="table_A778A508620545CCB37830E5CF1C75B7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Label </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>S1 </p> </td> 
   <td colname="col2"> <p> Nauwkeurige geolocatiedata van breedte- en lengtegraden die kunnen worden gebruikt om de exacte locatie van een apparaat te bepalen (binnen 100 meter of minder). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S2 </p> </td> 
   <td colname="col2"> <p> Geolocatiedata die kunnen worden gebruikt om een breed gedefinieerd geo-fencegebied te bepalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Data Governance-labels (Data Privacy) {#data-governance-labels}

Met Data Governance-labels kunnen gebruikers data classificeren die privacygerelateerde overwegingen en contractuele voorwaarden vertegenwoordigen waardoor deze voldoen aan regelgeving en bedrijfsbeleid.

### Data Privacy-toegangslabels

<table id="table_663EFF43A454498386F7F3E60875E0F8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Label </th> 
   <th colname="col2" class="entry"> Definitie </th> 
   <th colname="col3" class="entry"> Overige vereisten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Geen </p> </td> 
   <td colname="col2"> <p>Selecteer deze optie als deze variabele geen data bevat die moeten worden opgenomen in data die aan de geregistreerde persoon worden geretourneerd als onderdeel van een Data Privacy-toegangsaanvraag. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ACC-ALL </p> </td> 
   <td colname="col2"> <p>Waarden in dit veld moeten worden opgenomen in <u>alle</u> Data Privacy-toegangsaanvragen. </p> <p>Als deze treffer afkomstig is van een apparaat dat door meerdere personen wordt gedeeld, geeft u als datacontroller door de toepassing van dit label aan dat het acceptabel is om de data in dit veld te delen met ieder individu dat toegang heeft tot het gedeelde apparaat. </p> </td> 
   <td colname="col3"> <p>Velden met dit label worden geretourneerd voor alle Data Privacy-aanvragen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ACC-PERSON </p> </td> 
   <td colname="col2"> <p> Waarden in dit veld mogen alleen worden opgenomen voor Data Privacy-toegangsaanvragen als we redelijk zeker weten dat de treffer afkomstig was van de geregistreerde persoon, wat wordt vastgesteld doordat een Data Privacy-aanvraag-id overeenkomt met de waarde van een ID-PERSON-veld. </p> </td> 
   <td colname="col3"> <p>Er moet ook een ID-PERSON-label zijn ingesteld op een variabele in deze rapportsuite, en aanvragen verzenden met gebruikmaking van deze id verzenden, anders is dit label nooit van toepassing. </p> </td> 
  </tr> 
 </tbody> 
</table>

Weinig variabelen zullen een van de andere labels krijgen, maar de verwachting is dat de toegangslabels op veel van uw variabelen zullen worden toegepast. Het is echter aan u om in overleg met uw juridische team te beslissen welke door u verzamelde data met geregistreerde personen moeten worden gedeeld.

### Data Privacy-verwijderingslabels

<table id="table_59DFCE4D90214CB5972BDDE5B7391B4D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Label </th> 
   <th colname="col2" class="entry"> Definitie </th> 
   <th colname="col3" class="entry"> Overige vereisten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p>In tegenstelling tot de andere labels sluiten deze verwijderingslabels elkaar niet uit. U kunt een van beide, beide of geen van beide selecteren. Een afzonderlijk label Geen is niet nodig, omdat Geen al wordt aangegeven door geen van de verwijderopties te selecteren. </p> </td> 
   <td colname="col3"> <p>Een verwijderingslabel is alleen vereist voor velden met een waarde waarmee een treffer aan geregistreerde persoon kan worden gekoppeld (d.w.z. waarmee identificatie van de geregistreerde persoon mogelijk is). </p> <p> Overige persoonlijke gegevens (favorieten, browsergeschiedenis/aankoopgeschiedenis, gezondheidstoestand, enz.) hoeven niet te worden verwijderd omdat de koppeling met de geregistreerde persoon wordt verbroken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DEL-DEVICE </p> </td> 
   <td colname="col2"> <p>Voor Data Privacy-verwijderingsaanvragen mogen waarden in dit veld alleen worden geanonimiseerd voor aanvragen waarbij een opgegeven ID-DEVICE in de treffer aanwezig is. </p> <p>Als dezelfde waarde optreedt voor andere treffers die niet worden verwijderd, worden deze andere instanties niet gewijzigd. Daardoor zullen de tellingen wijzigen voor rapporten die unieke tellingen met dit veld berekenen. Op gedeelde apparaten is het mogelijk dat hierdoor identificaties voor andere individuen worden verwijderd, niet alleen de geregistreerde persoon. </p> <p>Tellingen veranderen niet als dit veld ook een ID-DEVICE-label heeft en de waarde in dit veld is gebruikt als een id voor de Data Privacy-aanvraag. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_45C3A09E1F05492B97C3F3DEA7C78FBC"> 
     <li id="li_BAB277F92F284ADE9D7B6839BDD716E2">Vereist ook label I1 of I2 of S1 </li> 
     <li id="li_6DDFC0571457489CBA9D76F547247F20">Kan niet worden ingesteld voor gebeurtenissen </li> 
     <li id="li_E79C6DFC6C58478EAA1504E3820D512C">Kan niet worden ingesteld voor merchandising-eVars </li> 
     <li id="li_B78E273212E447D49D0707E174B66DEC">Kan worden ingesteld voor classificaties </li> 
     <li id="li_F0F52D0DE7454557A6A97063C1FBC372">U moet aanvragen verzenden met gebruikmaking van een ID-DEVICE of expandID's instellen op true, anders is dit label nooit van toepassing. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DEL-PERSON </p> </td> 
   <td colname="col2"> <p>Voor Data Privacy-verwijderingsaanvragen mogen waarden in dit veld alleen worden geanonimiseerd voor aanvragen waarbij een opgegeven ID-PERSON in de treffer aanwezig is. </p> <p>Als dezelfde waarde voorkomt bij andere treffers, die niet worden verwijderd, worden deze andere waarden niet gewijzigd. Daardoor zullen de tellingen wijzigen voor rapporten die unieke tellingen met dit veld berekenen. Tellingen veranderen niet als dit veld ook een ID-PERSON-label heeft en de waarde in dit veld is gebruikt als een id voor de Data Privacy-aanvraag. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_6722E42E036E47B4B5E17DC213636D51"> 
     <li id="li_6C1A64FF68AF428A827D8C6C33E22970">Vereist ook label I1 of I2 of S1 </li> 
     <li id="li_8053533FFE874EE795C8B6043A4F73B3">Kan niet worden ingesteld voor gebeurtenissen </li> 
     <li id="li_D6700CF4D03E44DDA83C4DDBB5B70CC3">Kan niet worden ingesteld voor merchandising-eVars </li> 
     <li id="li_B6C2B15484B344889DBF29B62E2EA8FD">Kan worden ingesteld voor classificaties </li> 
     <li id="li_3BBD0C27D9644C2B9618457A0BFC15EF">Er moet ook een ID-PERSON-label zijn ingesteld op een variabele in deze rapportsuite, en aanvragen verzenden met gebruikmaking van deze id verzenden, anders is dit label nooit van toepassing. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

### Data Privacy-identiteitslabels

<table id="table_F6BBC868457443A19A7B693BD6C55B4B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Label </th> 
   <th colname="col2" class="entry"> Definitie </th> 
   <th colname="col3" class="entry"> Overige vereisten </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Geen </p> </td> 
   <td colname="col2"> <p>Deze variabele bevat geen id die wordt gebruikt voor Data Privacy-aanvragen. </p> </td> 
   <td colname="col3"> <p>U hoeft alleen een van deze andere labels in te stellen als dit veld een id bevat die u gebruikt bij het verzenden van toegangs- of verwijderingsverzoeken via de [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=en) of de gebruikersinterface. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID-DEVICE </p> </td> 
   <td colname="col2"> <p>Dit veld bevat een id die kan worden gebruikt om een apparaat te identificeren voor een Data Privacy-aanvraag, maar die geen onderscheid kan maken tussen verschillende gebruikers van een gedeeld apparaat. </p> <p>U hoeft dit label niet te specificeren voor alle variabelen die id's bevatten (daar zijn de I1/I2-labels voor). Gebruik dit label als u Data Privacy-aanvragen verzendt met id's die in deze variabele zijn opgeslagen, en u deze variabele wilt doorzoeken naar de opgegeven id. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_618019CB8FCA4A5C94C47636240197B2"> 
     <li id="li_0E5ADED36FF24A348FDD434E2CC8C8EE">Vereist ook label I1 of I2 </li> 
     <li id="li_20BCFF07B2BF468C8E0D477C10B2EF9F">Kan niet worden ingesteld voor gebeurtenissen </li> 
     <li id="li_0BD73EEF4184475D8E97878CF8DBEB90">Kan niet worden ingesteld voor merchandising-eVars </li> 
     <li id="li_129851035C4A4BF0922296B4C3BEE39B">Kan worden ingesteld voor classificaties </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID-PERSON </p> </td> 
   <td colname="col2"> <p>Dit veld bevat een id die kan worden gebruikt om een geverifieerde gebruiker (een specifieke persoon) te identificeren voor een Data Privacy-aanvraag. </p> <p>U hoeft dit label niet te specificeren voor alle variabelen die id's bevatten (daar zijn de I1/I2-labels voor). Gebruik dit label als u Data Privacy-aanvragen gaat verzenden met id's die in deze variabele zijn opgeslagen, en u deze variabele wilt doorzoeken naar de opgegeven id. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_0C7EEC8FCB5C4BCDA5D48F3C98770A67"> 
     <li id="li_2E781AE8D7A046A7996C7300CA854B86">Vereist ook label I1 of I2 </li> 
     <li id="li_EB4C6430C218405DAAE81DEE010DCAA2">Kan niet worden ingesteld voor gebeurtenissen </li> 
     <li id="li_05AA67B45974474F9DA520E8B877BA11">Kan niet worden ingesteld voor merchandising-eVars </li> 
     <li id="li_8A6BF4B40ED249289EAD46FE1C755FB0">Kan worden ingesteld voor classificaties </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

| Label | Definitie | Overige vereisten |
| --- | --- | --- |
| Geen | Deze variabele bevat geen id die wordt gebruikt voor Data Privacy-aanvragen. | U hoeft alleen een van deze andere labels in te stellen als dit veld een id bevat die u gebruikt bij het verzenden van toegangs- of verwijderingsverzoeken via het dialoogvenster [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=en) of UI. |
| ID-APPARAAT | Dit veld bevat een id die kan worden gebruikt om een apparaat te identificeren voor een Data Privacy-aanvraag, maar die geen onderscheid kan maken tussen verschillende gebruikers van een gedeeld apparaat.  U hoeft dit label niet te specificeren voor alle variabelen die id&#39;s bevatten (daar zijn de I1/I2-labels voor). Gebruik dit label als u Data Privacy-aanvragen verzendt met id&#39;s die in deze variabele zijn opgeslagen, en u deze variabele wilt doorzoeken naar de opgegeven id. | Vereist ook label I1 of I2.<ul><li>Kan niet worden ingesteld voor gebeurtenissen</li><li>Kan niet worden ingesteld voor merchandising-eVars</li><li>Kan worden ingesteld voor classificaties</li></ul> |
| ID-PERSON | Dit veld bevat een id die kan worden gebruikt om een geverifieerde gebruiker (een specifieke persoon) te identificeren voor een Data Privacy-aanvraag.  U hoeft dit label niet te specificeren voor alle variabelen die id&#39;s bevatten (daar zijn de I1/I2-labels voor). Gebruik dit label als u Data Privacy-aanvragen gaat verzenden met id&#39;s die in deze variabele zijn opgeslagen, en u deze variabele wilt doorzoeken naar de opgegeven id. | Vereist ook label I1 of I2.<ul><li>Kan niet worden ingesteld voor gebeurtenissen</li><li>Kan niet worden ingesteld voor merchandising-eVars</li><li>Kan worden ingesteld voor classificaties</li></ul> |

## Een naamruimte opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON {#section_F0A47AF8DA384A26BD56032D0ABFD2D7}

Wanneer u een variabele als ID-DEVICE of ID-PERSON labelt, wordt u gevraagd om een naamruimte op te geven. U kunt een eerder gedefinieerde naamruimte gebruiken of een nieuwe naamruimte definiëren.

### Een eerder gedefinieerde naamruimte gebruiken

Als u eerder een id-label hebt toegewezen aan andere variabelen in een van de rapportsuites in uw aanmeldingsbedrijf, kunt u één van deze bestaande naamruimten selecteren. U moet de naamruimte opnieuw gebruiken als deze variabele hetzelfde soort id&#39;s bevat als andere variabelen die al zijn gelabeld met deze naamruimte, en als u alle variabelen wilt doorzoeken bij het verzenden van een aanvraag.

1. Klik op **[!UICONTROL Select Namespace]** en selecteer een van de bestaande naamruimten.
1. Klik op **[!UICONTROL Apply]**.

![](assets/namespace.png)

### Een nieuwe naamruimte definiëren

U kunt ook een nieuwe naamruimte definiëren. We raden u aan naamruimtetekenreeksen te beperken tot alfanumerieke tekens, plus onderstrepingstekens, streepjes en spaties. Deze worden geconverteerd naar kleine letters.

1. Klik op **[!UICONTROL Select Namespace]** en typ de naamruimtetitel.

   ![](assets/namespace2.png)

1. Druk op **[!UICONTROL Enter]** om deze naamruimte toe te voegen. Nu wordt de knop Toepassen pas geactiveerd.
1. Klik op **[!UICONTROL Apply]**.

De tekenreeks die u opgeeft als naamruimte, is dezelfde tekenreeks die u moet gebruiken bij het verzenden van aanvragen via de Data Privacy-API als de waarde van de parameter “namespace”. De aanvraag heeft tot gevolg dat Adobe Analytics alle variabelen in al uw rapportsuites doorzoekt die deze naamruimte delen voor de id die u bij de aanvraag hebt opgegeven.

U hoeft de labels ID-DEVICE of ID-PERSON niet te specificeren op alle variabelen die id&#39;s bevatten (daar zijn de I1/I2-labels voor). Gebruik dit label als u Data Privacy-aanvragen gaat verzenden met id&#39;s die in deze variabele zijn opgeslagen, en u deze variabele wilt doorzoeken naar de opgegeven id. Bijvoorbeeld: als eVar1 een e-mailadres kan bevatten, en eVar2 een gebruikersaanmeldingsnaam kan bevatten, maar u altijd alleen aanvragen gaat verzenden met gebruikmaking van de gebruikersnaam, dan kunt u eVar1 labelen als I1, ACC-PERSON, DEL-PERSON, maar eVar2 als I2, ACC-PERSON, DEL-PERSON, ID-PERSON met de naamruimte “user name”. Vervolgens kunt u een aanvraag verzenden met een JSON-blok als gebruikerssectie, zoals:

```
{
     "namespace": "user name",
     "type": "analytics",
     "value": "rocketman123"
}
```

Het is aanvaardbaar om dezelfde naamruimte te gebruiken voor verschillende variabelen binnen dezelfde rapportsuite. Zo slaan sommige aangepaste implementaties een CRM-ID op in zowel een prop als een eVar. Als de CRM-id altijd voorkomt in een van hen (bijvoorbeeld eVar), en slechts af en toe in de andere (de prop), en nooit in de prop wanneer deze niet ook in de eVar voorkomt, dan heeft alleen de eVar een id-label en een naamruimte nodig, aangezien Adobe alleen in die eVar naar de id kan zoeken. Als de CRM-ID echter soms voorkomt in de ene variabele en soms in de andere, moeten beide dezelfde naamruimte hebben en zal Adobe beide variabelen doorzoeken op instanties van de id die is opgegeven als onderdeel van een Data Privacy-aanvraag met deze naamruimte. U hebt nog steeds een DEL-label nodig op al deze variabelen, zodat de waarde anoniem blijft, ongeacht waar deze voorkomt.

Een ander voorbeeld: u hebt misschien een CRM-id die soms wordt ingezonden via eVar1 en soms via prop7. Vervolgens hebt u een verwerkingsregel die de waarde van eVar1, indien aanwezig, naar eVar3 kopieert. Anders wordt de waarde van prop7 gekopieerd naar eVar3. In dit scenario bevat eVar3 altijd de CRM-id als deze bekend is, zodat alleen eVar3 een ID-PERSON-label nodig heeft.

>[!CAUTION]
>
>De naamruimten “visitorId” en “customVisitorId” zijn gereserveerd voor het identificeren van het verouderde Analytics-trackingcookie en de bezoekers-id van de Analytics-klant. Gebruik deze naamruimten niet voor variabelen voor aangepaste traffic of conversie.

## Soorten variabelen en de Data Privacy/DULE-labels die ze ondersteunen {#section_CE7C3EDE1344466A98BC45E394B40762}

Data Privacy/DULE-labeling heeft invloed op vier brede klassen van Analytics-variabelen. Niet alle variabelen ondersteunen alle labels. In deze tabel wordt aangegeven welke variabelen welke labels al of niet ondersteunen.

<table id="table_95D4416B3A8A40C28B2610D0003456E6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type variabele </th> 
   <th colname="col2" class="entry"> Ondersteunde labels </th> 
   <th colname="col3" class="entry"> Niet-ondersteunde labels </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> 
    <ul id="ul_0615B545A5AD43F2A6F25698A47AAD3E"> 
     <li id="li_A4B3E8E241B149C99F2A71B21227AD72">Aangepaste succesgebeurtenissen </li> 
     <li id="li_8AEF688AE9B8426C82D199E4B195330D">Merchandising-eVars </li> 
     <li id="li_DFFCA65DCC6146AEB6D47476B4D4CC3B">Variabelen met meer waarden (mvVars) </li> 
     <li id="li_3192D08B12C249D1AAA8AAEEDE2FD7D7">Hiërarchievariabelen </li> 
    </ul> </td> 
   <td colname="col2"> <p>S1/S2 </p> <p>ACC-ALL, ACC-PERSON </p> </td> 
   <td colname="col3"> <p>I1/I2 </p> <p>ID-DEVICE, ID-PERSON </p> <p>DEL-DEVICE, DEL-PERSON </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Classificaties </p> </td> 
   <td colname="col2"> <p>I1/I2, S1/S2 </p> <p>ACC-ALL, ACC-PERSON, </p> </td> 
   <td colname="col3"> <p>ID-APPARAAT, ID-PERSON </p> <p>DEL-APPARAAT, DEL-PERSON </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <ul id="ul_1C2FD4D606664965A88F10818E1C11A9"> 
     <li id="li_590975F5C7304317B22C80B20718E914">Traffic variables (props) </li> 
     <li id="li_6E614B7036994434BFDA71A4424529A0">Commerce-variabelen (non-merchandising-eVars) </li> 
    </ul> </td> 
   <td colname="col2"> <p>Alle labels </p> </td> 
   <td colname="col3"> - </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De meeste andere variabelen </p> <p><i>(Zie onderstaande tabel voor uitzonderingen)</i> </p> </td> 
   <td colname="col2"> <p>ACC-ALL, ACC-PERSON </p> </td> 
   <td colname="col3"> <p>I1/I2, S1/S2 </p> <p>ID-APPARAAT, ID-PERSON </p> <p>DEL-APPARAAT, DEL-PERSON </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variabelen waaraan andere labels dan ACC-ALL/ACC-PERSON kunnen worden toegewezen/gewijzigd {#section_4FA003003D1B4E2EBCFCDB1A7CD4A824}

<table id="table_0972910DB2D7473588F23EA47988381D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Groep </th> 
   <th colname="col2" class="entry"> Variabelen </th> 
   <th colname="col3" class="entry"> Aanpasbare labels </th> 
   <th colname="col4" class="entry"> Opmerking </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_62FA1BAA3B9245909509566D8C03F900"> 
     <li id="li_38F7C4E18ECB42C292370713F502B8EB">Conversiedimensies </li> 
     <li id="li_41CB61F927CB4402AAB4A62E219CD153">Aangepaste traffic-dimensies </li> 
    </ul> </td> 
   <td colname="col2"> <p>Alle, behalve classificaties </p> </td> 
   <td colname="col3"> <p>Alle </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Classificaties </p> </td> 
   <td colname="col3"> <p>Geen/I1/I2 </p> <p>Geen/S1/S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Conversiegebeurtenissen </p> </td> 
   <td colname="col2"> <p>Alle </p> </td> 
   <td colname="col3"> <p>Geen/S1/S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dimensies en gebeurtenissen van oplossingen </p> </td> 
   <td colname="col2"> <p>Activity Map-koppeling, </p> <p>Activity Map-pagina </p> </td> 
   <td colname="col3"> <p>Geen/I1/I2 </p> <p>Geen/DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Variabelen kunnen URL-parameters bevatten, die direct of indirect identificeerbare data kunnen bevatten. Als uw implementatie niet direct of indirect identificeerbare data in deze variabelen verzamelt, hebben ze geen id- of verwijderingslabels nodig. </p> <p>Als u de URL-parameters verwijdert, blijft de basis-URL behouden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dataverwerkingsdimensies </p> </td> 
   <td colname="col2"> <p>Aangepaste bezoekers-id </p> </td> 
   <td colname="col3"> <p>ID-DEVICE/ID-PERSON </p> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>U kunt de labels ID of DEL niet verwijderen (ingesteld op Geen), maar u kunt ze wijzigen in de varianten DEVICE of PERSON, afhankelijk van uw aangepaste id-implementatie. </p> <p>Als u de aangepaste bezoekers-id niet gebruikt, is de instelling niet van belang. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_5EB0193732D44A20AEA08CE9DFE01DBD"> 
     <li id="li_F70D969F83314A94BD8567449968EE2F">Standaarddimensies </li> 
     <li id="li_6046764B19FF4679B51E55671C2C0ADB">Dataverwerkingsdimensies </li> 
    </ul> </td> 
   <td colname="col2"> <p>IP-adres </p> <p>IP-adres 2 </p> </td> 
   <td colname="col3"> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>U kunt het label DEL niet verwijderen, maar u kunt het wijzigen in DEL-DEVICE, DEL-PERSON of beide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>ClickMap-actie (verouderd), </p> <p>ClickMap-context (verouderd), </p> <p>Pagina, </p> <p>Pagina-URL, </p> <p>URL van oorspronkelijke hoofdpagina, </p> <p>Referrer, </p> <p>URL-startpagina bezoeken </p> </td> 
   <td colname="col3"> <p>Geen/I1/I2 </p> <p>Geen/DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Variabelen kunnen URL-parameters bevatten, die direct of indirect identificeerbare data kunnen bevatten. Als uw implementatie niet direct of indirect identificeerbare data in deze variabelen verzamelt, hebben ze geen id- of verwijderingslabels nodig. </p> <p>Als u de URL-parameters verwijdert, blijft de basis-URL behouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verwijderingen verwerken {#section_F3DEE591671A4B16A8E043F91C137ECB}

De ondersteuning van Adobe Analytics voor Data Privacy-verwijderingsaanvragen is ontworpen om de gevolgen voor rapportage zo klein mogelijk te houden. In de meeste gevallen zouden de cijfers die in rapporten worden weergegeven, niet moeten veranderen. Een historisch rapport dat is uitgevoerd vóór de Data Privacy-verwijdering, zou overeen moeten komen met dezelfde rapportrun van na de verwijdering. Dit wordt bereikt door de verwijderde data volledig los te koppelen van de geregistreerde persoon terwijl niet-identificeerbare data blijven staan, zodat de gerapporteerde waarden consistent blijven.

In de volgende tabel wordt beschreven hoe verschillende variabelen worden “verwijderd”. Dit is geen volledige lijst.

<table id="table_A329C2E2645F4685BC208826D070A5F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabelen </th> 
   <th colname="col2" class="entry"> Verwijderingsmethode </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>• Traffic variabelen (props) </p> <p>• Commerce-variabelen (eVars) </p> </td> 
   <td colname="col2"> <p>De bestaande waarde wordt vervangen door een nieuwe waarde met de vorm “Data Privacy-356396D55C4F9C7AB3FBB2F2FA223482”, waarbij de hexadecimale waarde van 32 cijfers na het voorvoegsel “Data Privacy-” een cryptografisch sterk 128-bits pseudorandomgetal is. Omdat de waarde in feite wordt vervangen door een willekeurige tekenreeks, is er geen manier om de oorspronkelijke waarde op basis van deze nieuwe waarde te bepalen, en is er geen manier om de nieuwe waarde af te leiden voor wie de oorspronkelijke waarde kent. </p> <p>Als voor een bepaalde variabele de identieke waarde als de vervangen waarde optreedt in andere treffers die eveneens worden verwijderd als deel van dezelfde Data Privacy-aanvraag, worden alle instanties van deze waarde vervangen door dezelfde nieuwe waarde. </p> <p>Als sommige instanties van een waarde worden vervangen door één verwijderingsaanvraag, en een latere aanvraag andere (nieuwe) instanties van de oorspronkelijke waarde verwijdert, is de nieuwe vervangende waarde anders dan de oorspronkelijke vervangende waarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aankoop-id </p> </td> 
   <td colname="col2"> <p>De bestaande waarde wordt vervangen door een nieuwe waarde met de vorm “G-7588FCD8642718EC50”, waarbij de hexadecimale waarde van 18 cijfers na het voorvoegsel “G-” de eerste 18 cijfers zijn van een cryptografisch sterk 128-bits pseudorandomgetal. Alle opmerkingen die gelden voor verwijdering van traffic- en commerce-variabelen, gelden hier ook. </p> <p>De aankoop-id is een transactie-id die als belangrijkste doel heeft ervoor te zorgen dat een aankoop niet tweemaal in rekening wordt gebracht, bijvoorbeeld wanneer iemand de pagina met de aankoopbevestiging vernieuwt. De id zelf kan de aankoop koppelen aan een rij in uw eigen database waarin de aankoop is vastgelegd. In de meeste gevallen is het niet nodig deze id te verwijderen, en daarom wordt deze niet standaard verwijderd. Als u de aankoop na de Data Provacy-verwijderingsaanvraag van uw eigen data nog steeds aan een gebruiker kunt koppelen, moet u dit veld mogelijk verwijderen, zodat de Analytics-data voor deze bezoeker niet aan de koper kunnen worden gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bezoekers-id </p> </td> 
   <td colname="col2"> <p>Waarde is een 128-bits geheel getal en wordt vervangen door een cryptografisch sterke pseudorandomwaarde van 128 bits. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>• MCID </p> <p>• Aangepaste bezoekers-id </p> <p>• IP-adres </p> <p>• IP-adres 2 </p> </td> 
   <td colname="col2"> <p>Waarde wordt gewist (ingesteld op de lege tekenreeks of op 0, afhankelijk van het type variabele). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>• ClickMap-actie (verouderd) </p> <p>• ClickMap-context (verouderd) </p> <p>• Pagina </p> <p>• Pagina-URL </p> <p>• URL van oorspronkelijke hoofdpagina </p> <p>• Referrer </p> <p>• URL-startpagina bezoeken </p> </td> 
   <td colname="col2"> <p>URL-parameters worden gewist/verwijderd. Als de waarde er niet uitziet als een URL, wordt de waarde gewist (ingesteld op de lege tekenreeks). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>• Breedtegraad </p> <p>• Lengtegraad </p> </td> 
   <td colname="col2"> <p>Precisie wordt beperkt tot maximaal 1 km. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variabelen die de verwachte verwijderingslabels niet ondersteunen {#section_956B766EFFEC427E87E6CFF3A4217E86}

Deze sectie is bedoeld om informatie te verduidelijken over Analytics-variabelen die geen verwijdering steunen. Soms worden deze variabelen verwijderd door niet-Analytics-gebruikers (bijvoorbeeld het juridische team) die het type data in de variabele niet begrijpen en onjuiste gevolgtrekkingen maken op basis van de naam van de variabele. Hier volgt een lijst met een aantal van deze variabelen en waarom ze niet verwijderd hoeven te worden, of waarom ze geen specifiek verwijderingslabel nodig hebben.

<table id="table_6FECF3D654514862912D371E6BE4143B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabele </th> 
   <th colname="col2" class="entry"> Opmerkingen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nieuwe bezoekers-id </p> </td> 
   <td colname="col2"> <p>De nieuwe bezoekers-id is een booleaanse waarde die waar is als we een bepaalde bezoekers-id voor de eerste maal zien. Deze hoeft niet te worden verwijderd nadat de bezoekers-id is geanonimiseerd. Na anonimisering komt de waarde overeen met de eerste maal dat we deze geanonimiseerde id hebben gezien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Postcode </p> <p>Geopostcode </p> </td> 
   <td colname="col2"> <p>Postcodes worden alleen ingesteld voor treffers die afkomstig zijn uit de VS. Ze zijn niet ingesteld voor treffers uit de EU. Zelfs wanneer ze zijn ingesteld, bieden ze slechts een breed geografisch gebied dat het moeilijk maakt om de geregistreerde persoon opnieuw te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geobreedtegraad </p> <p>Geolengtegraad </p> </td> 
   <td colname="col2"> <p>Deze bieden een ruime locatie die van het IP-adres wordt afgeleid. De nauwkeurigheid is over het algemeen vergelijkbaar met die van een postcode, binnen tientallen kilometers van de werkelijke locatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>User Agent </p> </td> 
   <td colname="col2"> <p>De User Agent identificeert de versie van de gebruikte browser. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikers-id </p> </td> 
   <td colname="col2"> <p> Specificeert de Analytics-rapportsuite (als getal) die de data bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapportsuite-id </p> </td> 
   <td colname="col2"> <p> Hier geeft u de naam op van de Analytics-rapportsuite die de data bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bezoekers-id </p> <p>MCID/ECID </p> </td> 
   <td colname="col2"> <p> Deze hebben een DEL-DEVICE-label, maar het DEL-PERSON-label kan niet worden toegevoegd. Als u bij elke aanvraag <a href="/help/admin/c-data-governance/gdpr-id-expansion.md">Id-uitbreiding</a> opgeeft, worden deze id's automatisch verwijderd voor alle verwijderingsaanvragen, ook voor aanvragen met een ID-PERSON. </p> <p>Als u geen id-uitbreiding gebruikt, maar deze cookie-id's wilt anonimiseren bij treffers die een overeenkomende id in een prop of eVar bevatten, kunt u deze labelbeperking omzeilen door de prop of eVar te labelen met een ID-DEVICE-label, zelfs als deze werkelijk een persoon identificeert (alle DEL-PERSON-labels moeten ook worden gewijzigd in DEL-DEVICE-labels). In dit geval zal het aantal unieke bezoekers in de historische rapportage veranderen, aangezien slechts enkele exemplaren van de bezoekers-id of de ECID worden geanonimiseerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AMO-id </p> </td> 
   <td colname="col2"> <p> De Adobe Advertising Cloud-id is een oplossingsvariabele met een niet te wijzigen DEL-DEVICE-label. Deze wordt net als de bezoekers-id en de MCID ingevuld op basis van een cookie. Deze moet uit treffers worden verwijderd wanneer de andere id's worden verwijderd. Zie de beschrijving van deze variabelen voor meer informatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Datumvelden voor toegangsaanvragen {#section_6678FB4FF42B481C9B78E64F61782397}

Er zijn vijf standaardvariabelen die tijdstempels bevatten:

<table id="table_49A9255366254F799E1682C30CBD98EB"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Tijdstempel </th> 
   <th colname="col2" class="entry"> Definitie </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tijdstip treffer in UTC </p> </td> 
   <td colname="col2"> <p>Tijdstip waarop Adobe Analytics de treffer heeft ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste tijdstip treffer in UTC </p> </td> 
   <td colname="col2"> <p>Het tijdstip waarop de treffer plaatsvond, wat voor sommige mobiele apps en andere implementaties eerder kan zijn dan het tijdstip van ontvangst. Als er bijvoorbeeld geen netwerkverbinding beschikbaar was toen de treffer plaatsvond, kan de app de treffer vasthouden en deze verzenden zodra er een verbinding beschikbaar komt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datum Tijd </p> </td> 
   <td colname="col2"> <p>Dezelfde waarde als Aangepaste tijdstip treffer in UTC, maar in de tijdzone van de rapportsuite in plaats van GMT.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijdstip eerste treffer in GMT </p> </td> 
   <td colname="col2"> <p>De waarde voor Aangepaste tijdstip treffer in UTC voor de eerste treffer die is ontvangen voor de bezoekers-id-waarde voor deze treffer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begintijdstip bezoek in UTC </p> </td> 
   <td colname="col2"> <p>De waarde voor Aangepaste tijdstip treffer in UTC voor de eerste treffer die is ontvangen voor het huidige bezoek van deze bezoekers-id.</p> </td> 
  </tr> 
 </tbody> 
</table>

Voor de code voor het genereren van de bestanden die voor Data Privacy-toegangsaanvragen worden geretourneerd, moet minstens één van de eerste drie tijdstempelvariabelen in de toegangsaanvraag zijn opgenomen (een ACC-label hebben dat van toepassing is op het type aanvraag). Als geen van deze zijn opgenomen, wordt Aangepaste tijdstip treffer in UTC worden behandeld alsof het een ACC-ALL-label heeft.

Het CSV-bestand op raakniveau dat wordt geretourneerd voor verzoeken om toegang tot gegevensprivacy converteert de waarden in deze velden van unieke tijdstempels naar datum-/tijdvelden met de notatie YYYY-MM-DD HH:MM:SS (bijvoorbeeld 2018-05-01 13):49:22). In het HTML-overzichtsbestand worden deze tijdstempelwaarden afgekapt waardoor ze alleen de datum JJJJ-MM-DD bevatten, om het aantal unieke waarden te beperken dat voor deze velden kan voorkomen.
