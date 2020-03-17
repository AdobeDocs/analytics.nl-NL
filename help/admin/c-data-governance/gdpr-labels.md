---
description: 'null'
title: Data Privacy Labels voor analytische variabelen
uuid: a37a1278-7a0d-4e14-ae35-43bc460e7d12
translation-type: tm+mt
source-git-commit: 12a7452337307ca019c005dc20e3b551d96e1289

---


# Data Privacy Labels voor analytische variabelen

## Waarom labels toewijzen aan uw gegevens? {#section_A075CDF3AD0744BD8CEB41CE3FB7BFB3}

Veel klanten van Adobe hebben juridische teams die de wetten van de Privacy van Gegevens (GDPR, CCPA, etc.) hebben herzien en die hun eigen conclusies hebben getrokken over de wijze waarop gegevens moeten worden verwerkt om te voldoen aan de wetgeving inzake gegevensbescherming. De juridische interpretaties kunnen per bedrijf verschillen en de gewenste instellingen voor gegevensverwerking kunnen ook per klant verschillen. Aangezien klanten verschillende voorkeuren hebben voor gegevensverwerking van gegevensprivacy en verschillende gegevenssets, kunnen Adobe-klanten als gegevenscontroller hun gewenste instellingen aanpassen voor gegevensverwerking van gegevensprivacy voor hun unieke gegevens. Hierdoor kan elke unieke klant verzoeken om privacy van gegevens verwerken op de manier die het meest zinvol is voor zijn merk en zijn unieke gegevensset.

Adobe Analytics biedt hulpprogramma&#39;s voor het labelen van gegevens op basis van gevoeligheid en contractuele beperkingen. Labels zijn belangrijk en handig voor het helpen van: (1) betrokkenen identificeren, (2) bepalen welke gegevens moeten worden geretourneerd als onderdeel van een toegangsverzoek, en (3) identificeren gegevensvelden die moeten worden verwijderd als onderdeel van een verwijderingsverzoek.

Voordat u kunt achterhalen welke labels moeten worden toegepast op welke variabelen/velden, moet u [begrijpen welke id&#39;s](/help/admin/c-data-governance/gdpr-analytics-ids.md) u in de analysegegevens vastlegt en beslissen welke u gebruikt voor de aanvragen voor gegevensprivacy.

De implementatie van Adobe Analytics Data Privacy ondersteunt de volgende labels voor identiteitsgegevens, gevoelige gegevens en gegevensbeheer.

## DULE Labels {#section_B2E78130957647338495EF37DE21D6BC}

> [!NOTE] Het Data Usage Labeling &amp; Enforcement (DULE) Framework is ontworpen om een uniforme manier te bieden voor alle Adobe Solutions/Services/Platforms om metagegevens over gegevens in de Adobe Experience Cloud vast te leggen, te communiceren en te gebruiken. De meta-gegevens helpen gegevenscontrolemechanismen wijzen op welke gegevens persoonlijke informatie is, welke gegevens gevoelige gegevens zijn, en welke contractbeperkingen met gegevens worden geassocieerd. In deze eerste versie stelt Analytics alleen de DULE-labels beschikbaar die relevant zijn voor Data Privacy. Aangezien andere producten van Adobe steun voor de etiketten van DULE uitvoeren, zullen de toekomstige versies extra gevoelige gegevensetiketten, evenals contractetiketten introduceren, die zullen helpen ervoor zorgen dat de gegevens die tussen producten worden gedeeld slechts op wettelijk toegestane manieren worden gebruikt.

## Identiteitsgegevenslabels (DULE) {#identity-data-labels}

Identiteitsgegevens &quot;I&quot;etiketten worden gebruikt om gegevens te categoriseren die een specifieke persoon kunnen identificeren of contacteren.

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
   <td colname="col2"> <p><b>Direct identificeerbaar</b>: Gegevens die specifiek rechtstreeks contact met een persoon kunnen identificeren of inschakelen, zoals een naam of e-mailadres. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_4E2AD59D119E40D28B869D0BB63B9FD9"> 
     <li id="li_AC3E99B57E3A4AE2A12BE219680AFC58">Kan niet instellen voor gebeurtenissen </li> 
     <li id="li_BB66992863C8402F8D58656293F31E71">Kan niet instellen op Verwisselingsvariabelen </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I2 </p> </td> 
   <td colname="col2"> <p><b>Onrechtstreeks identificeerbaar</b>: Gegevens die in combinatie met andere gegevens kunnen worden gebruikt om direct contact met een individu of apparaat te identificeren of in te schakelen. </p> <p>Kan een persoon niet zelf identificeren, maar kan worden gecombineerd met andere informatie (die al dan niet in uw bezit is) om iemand te identificeren. De voorbeelden omvatten een aantal van de klantenloyaliteit, of identiteitskaart die door het systeem van CRM van een bedrijf wordt gebruikt dat voor elk van hun klanten uniek is. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_A0EF0F3DC5804D4FBE228946D697ABEB"> 
     <li id="li_A592EA6DA82C4D8C80E03F02ADF4E20E">Kan niet instellen voor gebeurtenissen </li> 
     <li id="li_46CE7B1E84884CDAB356A6DF89397849">Kan niet instellen op Verwisselingsvariabelen </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Gevoelige gegevenslabels (DULE) {#sensitive-data-labels}

De gevoelige gegevens &quot;S&quot;etiketten worden gebruikt om gevoelige gegevens zoals geografische gegevens te categoriseren. In de toekomst worden extra gevoelige gegevenslabels geïntroduceerd om andere soorten gevoelige informatie te identificeren.

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
   <td colname="col2"> <p> Nauwkeurige geo-locatiegegevens met betrekking tot breedte en lengte die kunnen worden gebruikt om de exacte locatie van een voorziening te bepalen (binnen 100 meter of minder). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S2 </p> </td> 
   <td colname="col2"> <p> Geo-locatiegegevens die kunnen worden gebruikt om een breed gedefinieerd geo-fence gebied te bepalen. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Labels voor gegevensbeheer (Data Privacy) {#data-governance-labels}

Met labels voor gegevensbeheer kunnen gebruikers gegevens classificeren die privacygerelateerde overwegingen en contractuele voorwaarden weerspiegelen, zodat deze in overeenstemming zijn met de regelgeving en het bedrijfsbeleid.

**Toegangslabels voor gegevensprivacygegevens**

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
   <td colname="col2"> <p>Selecteer deze optie als deze variabele geen gegevens bevat die moeten worden opgenomen in gegevens die aan de betrokkene worden geretourneerd als onderdeel van een verzoek om toegang tot gegevensprivacy. </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ACC-ALL </p> </td> 
   <td colname="col2"> <p>Waarden in dit veld moeten worden opgenomen in <u>alle</u> verzoeken om toegang tot privacy van gegevens. </p> <p>Als deze treffer afkomstig is van een apparaat dat door meerdere personen wordt gedeeld door dit label toe te passen, geeft u als gegevenscontroller aan dat het acceptabel is om de gegevens in dit veld te delen met een persoon die toegang had tot het gedeelde apparaat. </p> </td> 
   <td colname="col3"> <p>Velden met dit label worden geretourneerd voor alle verzoeken om gegevensprivacy. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ACC-PERSON </p> </td> 
   <td colname="col2"> <p> Waarden in dit veld mogen alleen worden opgenomen voor verzoeken om toegang tot gegevensprivacy als we er redelijk zeker van zijn dat de treffer afkomstig was van de betrokkene, zoals bepaald door een aanvraag-id voor gegevensprivacy die overeenkomt met de waarde van een ID-PERSON-veld. </p> </td> 
   <td colname="col3"> <p>U moet ook een ID-PERSON-label op een variabele in deze rapportsuite hebben ingesteld en aanvragen met die id verzenden, anders wordt dit label nooit toegepast. </p> </td> 
  </tr> 
 </tbody> 
</table>

Terwijl weinig variabelen om het even welke andere etiketten zullen ontvangen, wordt verwacht dat de toegangslabels op veel van uw variabelen zullen worden toegepast. Het is echter aan u om in overleg met uw Juridische team te beslissen welke gegevens u hebt verzameld, met de betrokkenen moeten worden gedeeld.

**Gegevensprivacy labels verwijderen**

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
   <td colname="col2"> <p>In tegenstelling tot de andere labels sluiten deze labels van Verwijderen elkaar niet uit. U kunt beide of geen selecteren. Een afzonderlijk label Geen is niet nodig, omdat Geen wordt aangegeven door een van de verwijderopties niet te controleren. </p> </td> 
   <td colname="col3"> <p>Een verwijderingslabel is alleen vereist voor velden die een waarde bevatten waarmee een treffer aan de betrokkene kan worden gekoppeld (d.w.z. die identificatie van de betrokkene mogelijk maken). </p> <p> Overige persoonlijke gegevens (favorieten, browsergeschiedenis/aankoopgeschiedenis, gezondheidsomstandigheden, enz.) hoeft niet te worden verwijderd omdat de koppeling met de betrokkene wordt verbroken. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DEL-APPARAAT </p> </td> 
   <td colname="col2"> <p>Voor verzoeken om gegevensprivacy te verwijderen, mogen waarden in dit veld alleen geanonimiseerd worden voor aanvragen waarbij een opgegeven ID-DEVICE aanwezig is in de hit. </p> <p>Als dezelfde waarde voor andere hits optreedt, die niet worden verwijderd, worden die andere instanties niet gewijzigd. Dit zal in de tellingen resulteren die voor rapporten veranderen die unieke tellingen op dit gebied berekenen. Op gedeelde apparaten, kan dit herkenningstekens voor andere individuen, voorbij alleen het gegevenssubject verwijderen. </p> <p>Tellingen veranderen niet als dit veld ook een ID-DEVICE-label heeft en de waarde in dit veld is gebruikt als een ID voor het privacyverzoek. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_45C3A09E1F05492B97C3F3DEA7C78FBC"> 
     <li id="li_BAB277F92F284ADE9D7B6839BDD716E2">Ook vereist I1- of I2- of S1-label </li> 
     <li id="li_6DDFC0571457489CBA9D76F547247F20">Kan niet instellen voor gebeurtenissen </li> 
     <li id="li_E79C6DFC6C58478EAA1504E3820D512C">Kan niet instellen op Verwisselingsvariabelen </li> 
     <li id="li_B78E273212E447D49D0707E174B66DEC">Kan niet instellen voor classificaties </li> 
     <li id="li_F0F52D0DE7454557A6A97063C1FBC372">U moet verzoeken indienen gebruikend identiteitskaart-APPARAAT of reeks expandIDs aan waar, anders zal dit etiket nooit van toepassing zijn. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>DEL-PERSON </p> </td> 
   <td colname="col2"> <p>Voor verzoeken om gegevensprivacy te verwijderen, mogen waarden in dit veld alleen geanonimiseerd worden voor aanvragen waarbij een opgegeven ID-PERSON aanwezig is in de treffer. </p> <p>Als dezelfde waarde voorkomt bij andere resultaten, die niet worden verwijderd, worden die andere waarden niet gewijzigd. Dit zal in de tellingen resulteren die voor rapporten veranderen die unieke tellingen op dit gebied berekenen. Tellingen worden niet gewijzigd als dit veld ook een ID-PERSON-label heeft en de waarde in dit veld is gebruikt als een ID voor de privacyaanvraag Gegevens. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_6722E42E036E47B4B5E17DC213636D51"> 
     <li id="li_6C1A64FF68AF428A827D8C6C33E22970">Ook vereist I1- of I2- of S1-label </li> 
     <li id="li_8053533FFE874EE795C8B6043A4F73B3">Kan niet instellen voor gebeurtenissen </li> 
     <li id="li_D6700CF4D03E44DDA83C4DDBB5B70CC3">Kan niet instellen op Verwisselingsvariabelen </li> 
     <li id="li_B6C2B15484B344889DBF29B62E2EA8FD">Kan niet instellen voor classificaties </li> 
     <li id="li_3BBD0C27D9644C2B9618457A0BFC15EF">U moet ook een ID-PERSON-label op een variabele in deze rapportsuite hebben ingesteld en aanvragen met die id verzenden, anders wordt dit label nooit toegepast. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**Identiteitslabels gegevensprivacy**

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
   <td colname="col2"> <p>Deze variabele bevat geen id die wordt gebruikt voor privacyverzoeken. </p> </td> 
   <td colname="col3"> <p>U hoeft alleen een van deze andere labels in te stellen als dit veld een id bevat die u gebruikt bij het verzenden van verzoeken om toegang of het verwijderen van aanvragen via de API of UI voor gegevensprivacy. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID-APPARAAT </p> </td> 
   <td colname="col2"> <p>Dit veld bevat een id die kan worden gebruikt om een apparaat te identificeren voor een verzoek om gegevensprivacy, maar die geen onderscheid kan maken tussen verschillende gebruikers van een gedeeld apparaat. </p> <p>U te hoeven niet om dit etiket voor alle variabelen te specificeren die IDs bevatten (dat is waar de I1/I2 etiketten voor zijn). Gebruik dit label als u privacyverzoeken voor gegevens verzendt met ID's die in deze variabele zijn opgeslagen en u deze variabele wilt doorzoeken voor de opgegeven id. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_618019CB8FCA4A5C94C47636240197B2"> 
     <li id="li_0E5ADED36FF24A348FDD434E2CC8C8EE">Ook vereist I1- of I2-label </li> 
     <li id="li_20BCFF07B2BF468C8E0D477C10B2EF9F">Kan niet instellen voor gebeurtenissen </li> 
     <li id="li_0BD73EEF4184475D8E97878CF8DBEB90">Kan niet instellen op Verwisselingsvariabelen </li> 
     <li id="li_129851035C4A4BF0922296B4C3BEE39B">Kan niet instellen voor classificaties </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID-PERSON </p> </td> 
   <td colname="col2"> <p>Dit veld bevat een id die kan worden gebruikt om een geverifieerde gebruiker (een specifieke persoon) te identificeren voor een privacyverzoek. </p> <p>U te hoeven niet om dit etiket voor alle variabelen te specificeren die IDs bevatten (dat is waar de I1/I2 etiketten voor zijn). Gebruik dit label als u privacyverzoeken voor gegevens verzendt met id's die zijn opgeslagen in deze variabele en u deze variabele wilt zoeken naar de opgegeven id. </p> </td> 
   <td colname="col3"> 
    <ul id="ul_0C7EEC8FCB5C4BCDA5D48F3C98770A67"> 
     <li id="li_2E781AE8D7A046A7996C7300CA854B86">Ook vereist I1- of I2-label </li> 
     <li id="li_EB4C6430C218405DAAE81DEE010DCAA2">Kan niet instellen voor gebeurtenissen </li> 
     <li id="li_05AA67B45974474F9DA520E8B877BA11">Kan niet instellen op Verwisselingsvariabelen </li> 
     <li id="li_8A6BF4B40ED249289EAD46FE1C755FB0">Kan niet instellen voor classificaties </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Geef een naamruimte op wanneer u een variabele labelt als ID-DEVICE of ID-PERSON {#section_F0A47AF8DA384A26BD56032D0ABFD2D7}

Wanneer u een variabele als ID-DEVICE of ID-PERSON etiketteert, wordt u ertoe aangezet om een namespace te verstrekken. U kunt een eerder gedefinieerde naamruimte gebruiken of een nieuwe naamruimte definiëren.

**Een eerder gedefinieerde naamruimte gebruiken**

Als u eerder een etiket van identiteitskaart aan andere variabelen in om het even welke rapportreeksen in uw login bedrijf hebt toegewezen, kunt u één van deze bestaande namespaces selecteren. U moet de naamruimte opnieuw gebruiken als deze variabele hetzelfde type id&#39;s bevat als andere variabelen die al zijn gelabeld met deze naamruimte en u alle variabelen wilt doorzoeken wanneer u een aanvraag indient.

1. Klik op een van de bestaande naamruimten **[!UICONTROL Select Namespace]** en selecteer deze.
1. Klik op **[!UICONTROL Apply]**.

![](assets/namespace.png)

**Een nieuwe naamruimte definiëren**

U kunt ook een nieuwe naamruimte definiëren. We raden aan naamruimtetekenreeksen te beperken tot alfanumerieke tekens, plus het onderstrepingsteken, het streepje en de spatie van tekens. Ze worden omgezet in kleine letters.

1. Klik **[!UICONTROL Select Namespace]** en typ in de naamruimtetitel.

   ![](assets/namespace2.png)

1. Druk op **[!UICONTROL Enter]** om deze naamruimte toe te voegen. Pas nu wordt de knop Toepassen geactiveerd.
1. Klik op **[!UICONTROL Apply]**.

De tekenreeks die u opgeeft als naamruimte, is dezelfde tekenreeks die u moet gebruiken bij het verzenden van aanvragen via de API voor gegevensprivacy als de waarde van de parameter &quot;namespace&quot;. Het verzoek zal dan de Analytics van Adobe ertoe bewegen om alle variabelen in al uw rapportreeksen te zoeken die dit namespace voor identiteitskaart delen u met het verzoek specificeerde.

U te hoeven niet om ID-APPARAAT of ID-PERSON etiketten op alle variabelen te specificeren die IDs bevatten (dat is waar de I1/I2 etiketten voor zijn). Gebruik dit label als u privacyverzoeken voor gegevens verzendt met id&#39;s die zijn opgeslagen in deze variabele en u deze variabele wilt zoeken naar de opgegeven id. Als voorbeeld, als eVar1 een e-mailadres kan bevatten, en eVar2 een login gebruikersnaam kan bevatten, maar u slechts ooit verzoeken gebruikend de gebruikersnaam zult voorleggen, dan zou u eVar1 als I1, ACC-PERSON, DEL-PERSON, maar eVar2 als I2, ACC-PERSON, DEL-PERSON met namespace &quot;kunnen etiketteren &quot;. Vervolgens kunt u een aanvraag indienen met een JSON-blok voor een gebruikerssectie, zoals:

```
{
     "namespace": "user name",
     "type": "analytics",
     "value": "rocketman123"
}
```

Het is aanvaardbaar om zelfde namespace voor verschillende variabelen binnen de zelfde rapportreeks te gebruiken. Bijvoorbeeld, slaan sommige douaneimplementaties een CRM-identiteitskaart in zowel pro als eVar op. Als de CRM-id altijd voorkomt in een van deze (zoals de eVar), en slechts af en toe in de andere (de eigenschap) voorkomt, en nooit in de prop wanneer niet ook in de eVar, dan vereist slechts eVar een etiket van identiteitskaart en een namespace, aangezien Adobe slechts in die eVar naar identiteitskaart kan zoeken. Als de CRM-ID echter soms voorkomt in de ene variabele en soms in de andere, moeten beide dezelfde naamruimte hebben en zal Adobe beide variabelen zoeken naar instanties van de id die is opgegeven als onderdeel van een verzoek om gegevensprivacy met deze naamruimte. U moet nog steeds een DEL-label op al deze variabelen hebben, zodat de waarde anoniem blijft, ongeacht waar deze voorkomt.

Als een ander voorbeeld, zou u een identiteitskaart van CRM kunnen hebben die soms via eVar1 wordt verzonden en soms via prop7 wordt verzonden. Vervolgens hebt u een verwerkingsregel die de waarde van Var1, indien aanwezig, naar Var3 kopieert. Anders wordt de waarde van prop7 gekopieerd naar eVar3. In dit scenario, zal eVar3 altijd identiteitskaart van CRM bevatten als het gekend is, zodat slechts eVar3 een ID-PERSON etiket vereist.

> [!CAUTION] De naamruimten &quot;bezoekerId&quot; en &quot;customVisitorId&quot; zijn gereserveerd voor het identificeren van het verouderde cookie voor bijhouden van analysemogelijkheden en de bezoeker-id van de Analytics-klant. Gebruik deze naamruimten niet voor variabelen voor aangepast verkeer of conversie.

## De Types van Variabelen en de Etiketten van Gegevens Privacy/DULE die zij steunen {#section_CE7C3EDE1344466A98BC45E394B40762}

Het etiketteren van de Privacy/DULE van gegevens beïnvloedt vier brede klassen van variabelen van de Analyse. Niet alle variabelen ondersteunen alle labels. In deze tabel wordt aangegeven welke variabelen ondersteunen of niet welke labels.

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
     <li id="li_8AEF688AE9B8426C82D199E4B195330D">Merchandising Vars </li> 
     <li id="li_DFFCA65DCC6146AEB6D47476B4D4CC3B">Multigetaxeerde variabelen (mvVars) </li> 
     <li id="li_3192D08B12C249D1AAA8AAEEDE2FD7D7">Hiërarchievariabelen </li> 
    </ul> </td> 
   <td colname="col2"> <p>S1/S2 </p> <p>ACC-ALL, ACC-PERSON </p> </td> 
   <td colname="col3"> <p>I1/I2 </p> <p>ID-APPARAAT, ID-PERSON </p> <p>DEL-APPARAAT, DEL-PERSON </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Classificaties </p> </td> 
   <td colname="col2"> <p>I1/I2, S1/S2 </p> <p>ACC-ALL, ACC-PERSON, </p> </td> 
   <td colname="col3"> <p>ID-APPARAAT, ID-PERSON </p> <p>DEL-APPARAAT, DEL-PERSON </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> 
    <ul id="ul_1C2FD4D606664965A88F10818E1C11A9"> 
     <li id="li_590975F5C7304317B22C80B20718E914">Verkeersvariabelen (props) </li> 
     <li id="li_6E614B7036994434BFDA71A4424529A0">Variabelen van de handel (niet-verkoopbare eVars) </li> 
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
     <li id="li_38F7C4E18ECB42C292370713F502B8EB">Omzetafmetingen </li> 
     <li id="li_41CB61F927CB4402AAB4A62E219CD153">Aangepaste verkeersafmetingen </li> 
    </ul> </td> 
   <td colname="col2"> <p>Alle, behalve classificaties </p> </td> 
   <td colname="col3"> <p>Alles </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Classificaties </p> </td> 
   <td colname="col3"> <p>Geen / I1 / I2 </p> <p>Geen / S1 / S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Conversiegebeurtenissen </p> </td> 
   <td colname="col2"> <p>Alles </p> </td> 
   <td colname="col3"> <p>Geen / S1 / S2 </p> </td> 
   <td colname="col4"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afmetingen en gebeurtenissen van de oplossing </p> </td> 
   <td colname="col2"> <p>Koppeling activiteitenoverzicht </p> <p>Pagina Activiteitenkaart </p> </td> 
   <td colname="col3"> <p>Geen / I1 / I2 </p> <p>Geen / DEL-APPARAAT / DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Variabelen kunnen URL-parameters bevatten, die direct of indirect identificeerbare gegevens kunnen bevatten. Als uw implementatie direct of indirect identificeerbare gegevens in deze variabelen verzamelt, hebben ze geen id- of verwijderingslabels nodig. </p> <p>Als u de URL-parameters verwijdert, blijft de basis-URL behouden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Afmetingen gegevensverwerking </p> </td> 
   <td colname="col2"> <p>Aangepaste bezoeker-id </p> </td> 
   <td colname="col3"> <p>ID-APPARAAT/ID-PERSON </p> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>U kunt de labels ID of DEL niet verwijderen (ingesteld op Geen), maar u kunt ze wijzigen in de varianten DEVICE of PERSON, afhankelijk van uw aangepaste id-implementatie. </p> <p>Als u de aangepaste bezoeker-id niet gebruikt, is de instelling niet van belang. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1" morerows="1"> 
    <ul id="ul_5EB0193732D44A20AEA08CE9DFE01DBD"> 
     <li id="li_F70D969F83314A94BD8567449968EE2F">Standaardafmetingen </li> 
     <li id="li_6046764B19FF4679B51E55671C2C0ADB">Afmetingen gegevensverwerking </li> 
    </ul> </td> 
   <td colname="col2"> <p>IP-adres </p> <p>IP-adres 2 </p> </td> 
   <td colname="col3"> <p>DEL-DEVICE/DEL-PERSON </p> </td> 
   <td colname="col4"> <p>U kunt het label DEL niet verwijderen, maar u kunt het wijzigen in DEL-DEVICE, DEL-PERSON of beide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>ClickMap-actie (verouderd), </p> <p>Context ClickMap (verouderd), </p> <p>Pagina, </p> <p>Pagina-URL, </p> <p>URL van oorspronkelijke invoerpagina, </p> <p>Referrer, </p> <p>URL startpagina bezoeken </p> </td> 
   <td colname="col3"> <p>Geen / I1 / I2 </p> <p>Geen / DEL-APPARAAT / DEL-PERSON </p> </td> 
   <td colname="col4"> <p>Variabelen kunnen URL-parameters bevatten, die direct of indirect identificeerbare gegevens kunnen bevatten. Als uw implementatie direct of indirect identificeerbare gegevens in deze variabelen verzamelt, hebben ze geen id- of verwijderingslabels nodig. </p> <p>Als u de URL-parameters verwijdert, blijft de basis-URL behouden. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Verwijderverwerking {#section_F3DEE591671A4B16A8E043F91C137ECB}

De ondersteuning van Adobe Analytics voor verzoeken om gegevensprivacy te verwijderen is ontworpen om de gevolgen voor de rapportage te minimaliseren. In de meeste gevallen, zouden de metriek die in rapporten wordt getoond niet moeten veranderen. Een historisch rapport dat vóór de schrapping van de Privacy van Gegevens werd in werking gesteld zal het zelfde rapport aanpassen dat nadat de schrapping is uitgevoerd. Dit gebeurt door de verwijderde gegevens volledig los te koppelen van de betrokkene, terwijl niet-identificeerbare gegevens op hun plaats blijven zodat de gerapporteerde waarden consistent blijven.

In de volgende tabel wordt beschreven hoe verschillende variabelen worden &quot;verwijderd&quot;. Dit is geen volledige lijst.

<table id="table_A329C2E2645F4685BC208826D070A5F6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabelen </th> 
   <th colname="col2" class="entry"> Verwijderingsmethode </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>・ Verkeersvariabelen (profielen) </p> <p>・ Handelsvariabelen (eVars) </p> </td> 
   <td colname="col2"> <p>Bestaande waarde wordt vervangen door een nieuwe waarde in de vorm "Data Privacy-356396D55C4F9C7AB3FBB2F2FA223482", waarbij de hexadecimale waarde van 32 cijfers na het voorvoegsel "Data Privacy-" een cryptografisch sterk 128-bits pseudorandom getal is. Omdat het in wezen door een willekeurig koord wordt vervangen, is er geen manier om de originele waarde van deze nieuwe waarde te bepalen, en geen manier om de nieuwe waarde af te leiden wetend de originele waarde. </p> <p>Als voor een bepaalde variabele dezelfde waarde als die wordt vervangen voorkomt binnen andere treffers die ook als deel van het zelfde verzoek van de Privacy van Gegevens worden geschrapt, zullen alle instanties van die waarde met de zelfde nieuwe waarde worden vervangen. </p> <p>Als sommige instanties van een waarde worden vervangen door één verwijderingsaanvraag en een latere aanvraag andere (nieuwe) instanties van de oorspronkelijke waarde verwijdert, is de nieuwe vervangingswaarde anders dan de oorspronkelijke vervangingswaarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aankoop-id </p> </td> 
   <td colname="col2"> <p>Bestaande waarde wordt vervangen door een nieuwe waarde van de vorm "G-7588FCD8642718EC50", waarbij de 18 hexadecimale cijfers na het voorvoegsel "G-7588FCD8642718EC50" de eerste 18 cijfers van een cryptografisch sterk pseudorandom aantal zijn. Alle commentaren die op schrapping van verkeer en handelsvariabelen van toepassing zijn zijn ook hier van toepassing. </p> <p>De aankoop-id is een transactie-id die als belangrijkste doel heeft ervoor te zorgen dat een aankoop niet tweemaal wordt gecrediteerd, bijvoorbeeld wanneer iemand de pagina met aankoopbevestiging vernieuwt. De id zelf kan de aankoop koppelen aan een rij in uw eigen database waar de aankoop is opgenomen. In de meeste gevallen is het niet nodig deze id te verwijderen, zodat deze niet standaard wordt verwijderd. Als u de aankoop na de aanvraag voor het verwijderen van gegevensprivacy nog steeds aan een gebruiker kunt koppelen, moet u dit veld mogelijk verwijderen, zodat de analysegegevens voor deze bezoeker niet aan de koper kunnen worden gekoppeld. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bezoeker-id </p> </td> 
   <td colname="col2"> <p>Waarde is een 128-bits geheel getal en wordt vervangen door een cryptografisch sterke pseudowillekeurige waarde van 128 bits. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>MCID </p> <p>・ Aangepaste bezoeker-id </p> <p>・ IP-adres </p> <p>・ IP Adres 2 </p> </td> 
   <td colname="col2"> <p>Waarde wordt gewist (ingesteld op de lege tekenreeks of op 0, afhankelijk van het type van de variabele). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>・ Handeling ClickMap (verouderd) </p> <p>・ Context ClickMap (verouderd) </p> <p>・ Pagina </p> <p>・ Pagina-URL </p> <p>・ URL van oorspronkelijke invoerpagina </p> <p>・ Referrer </p> <p>・ Ga naar URL startpagina </p> </td> 
   <td colname="col2"> <p>URL-parameters worden gewist/verwijderd. Als de waarde er anders uitziet als een URL, wordt de waarde gewist (ingesteld op de lege tekenreeks). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>・ Breedtegraad </p> <p>・ Lengtegraad </p> </td> 
   <td colname="col2"> <p>Precisie wordt beperkt tot maximaal 1 km. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Variabelen die de verwachte labels voor verwijderen niet ondersteunen {#section_956B766EFFEC427E87E6CFF3A4217E86}

Deze sectie is bedoeld om informatie over variabelen van de Analyse te verduidelijken die schrapping niet steunen. Soms worden deze variabelen verwijderd door niet-analytische gebruikers (zoals het juridische team) die het type gegevens in de variabele niet begrijpen en onjuiste veronderstellingen maken op basis van de naam van de variabele. Hier is een lijst van sommige van deze variabelen en waarom zij geen schrapping vereisen, of waarom zij geen specifiek schrappingsetiket vereisen.

<table id="table_6FECF3D654514862912D371E6BE4143B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Variabele </th> 
   <th colname="col2" class="entry"> Opmerkingen </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Nieuwe bezoeker-id </p> </td> 
   <td colname="col2"> <p>De nieuwe bezoekersidentiteitskaart is een Booleaanse die de eerste keer waar is wij een bepaalde bezoekersidentiteitskaart zien. Het is niet nodig het te verwijderen zodra de bezoekersidentiteitskaart wordt geanonimiseerd. Na anonymization, zal het beantwoorden aan de eerste keer wij deze geanonimiseerde identiteitskaart hebben gezien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Postcode </p> <p>Postcode geo </p> </td> 
   <td colname="col2"> <p>Zip-codes worden alleen ingesteld voor hits uit de VS. Ze zijn niet bedoeld voor treffers uit de EU. Zelfs wanneer deze zijn ingesteld, bieden zij slechts een breed geografisch gebied dat het moeilijk maakt de betrokkene opnieuw te identificeren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Geo Latitude </p> <p>Geo Lengtegraad </p> </td> 
   <td colname="col2"> <p>Deze verstrekken een ruwe plaats die van het IP adres wordt afgeleid. De nauwkeurigheid is over het algemeen vergelijkbaar met die van een postcode, binnen enkele tientallen kilometers van de werkelijke locatie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersagent </p> </td> 
   <td colname="col2"> <p>De gebruikersagent identificeert de versie van browser die werd gebruikt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Gebruikersnaam </p> </td> 
   <td colname="col2"> <p> Specificeert de het rapportreeks van de Analyse (als aantal) die de gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ID van rapportsuite </p> </td> 
   <td colname="col2"> <p> Hier geeft u de naam op van de analytische rapportsuite die de gegevens bevat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bezoeker-id </p> <p>MCID / ECID </p> </td> 
   <td colname="col2"> <p> Deze hebben een DEL-DEVICE-label, maar het DEL-PERSON-label kan niet worden toegevoegd. Als u bij elke aanvraag <a href="/help/admin/c-data-governance/gdpr-id-expansion.md"> ID-uitbreiding</a> opgeeft, worden deze id's automatisch verwijderd voor alle verwijderingsaanvragen, ook voor aanvragen met een ID-PERSON. </p> <p>Als u geen id-uitbreiding gebruikt, maar deze cookie-id's wilt anonymiseren bij treffers die een overeenkomende id in een proxy of eVar bevatten, kunt u deze labelbeperking omzeilen door de proxy of eVar te labelen met een ID-DEVICE-label, zelfs als deze echt een persoon identificeert (alle DEL-PERSON-labels moeten ook worden gewijzigd in DEL-DEVICE-labels). In dit geval zal het aantal unieke bezoekers in de historische rapportage veranderen, aangezien slechts enkele exemplaren van de bezoeker-id of de ECID worden geanonimiseerd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>AMO-id </p> </td> 
   <td colname="col2"> <p> De Adobe Advertising Cloud-id is een oplossingstabel met een onveranderbaar DEL-DEVICE-label. Deze wordt net als de bezoeker-id en de MCID gevuld met een cookie. Deze moet uit treffers worden verwijderd wanneer deze andere id's worden verwijderd. Zie de beschrijving voor deze variabelen voor meer informatie. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Datumvelden voor toegangsverzoeken {#section_6678FB4FF42B481C9B78E64F61782397}

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
   <td colname="col1"> <p>Tijd in UTC </p> </td> 
   <td colname="col2"> <p>De tijd dat Adobe Analytics de hit heeft ontvangen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste tijd UTC </p> </td> 
   <td colname="col2"> <p>Het tijdstip waarop de hit optrad, wat voor sommige mobiele apps en andere implementaties eerder kan zijn dan het tijdstip van ontvangst. Als een netwerkverbinding bijvoorbeeld niet beschikbaar was toen deze zich voordeed, kan de toepassing de hit vasthouden en deze verzenden wanneer een verbinding beschikbaar komt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Datum en tijd </p> </td> 
   <td colname="col2"> <p>Dezelfde waarde als Custom Hit Time UTC, maar in de tijdzone van de rapportsuite in plaats van GMT.</p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tijd eerste uur GMT </p> </td> 
   <td colname="col2"> <p>De UTC-waarde voor Aangepaste tijd voor de eerste hit die is ontvangen voor de waarde voor de bezoeker-id voor deze hit. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Begintijd UTC bezoeken </p> </td> 
   <td colname="col2"> <p>De UTC-waarde voor Aangepaste tijd voor de eerste hit die is ontvangen voor het huidige bezoek voor deze bezoeker-id.</p> </td> 
  </tr> 
 </tbody> 
</table>

De code voor het produceren van de dossiers die voor de toegangsverzoeken van de Privacy van Gegevens zijn teruggekeerd vereist dat minstens één van de eerste drie timestamp variabelen in het toegangsverzoek worden omvat (heeft een ACC etiket dat op het type van verzoek van toepassing is). Als geen van deze zijn inbegrepen, dan zal de Tijd van de Aangepast Hit UTC worden behandeld alsof het een ACC-ALLE etiket heeft.

Het CSV-bestand op raakniveau dat wordt geretourneerd voor verzoeken om toegang tot gegevensprivacy, converteert de waarden in deze velden van unieke tijdstempels naar datum-/tijdvelden met de notatie YYYY-MM-DD HH:MM:SS (bijvoorbeeld 2018-05-01 13:49:22). In het overzicht-HTML-bestand worden deze tijdstempelwaarden ingekort, zodat alleen de datum YYYY-MM-DD wordt opgenomen om het aantal unieke waarden dat voor deze velden optreedt, te verminderen.
