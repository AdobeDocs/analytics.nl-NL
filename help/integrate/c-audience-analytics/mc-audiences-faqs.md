---
description: Antwoorden op vragen die u zou kunnen hebben wanneer het uitvoeren van Audience Analytics.
solution: Experience Cloud
title: Veelgestelde vragen voor Audience Analytics
feature: Audience Analytics
exl-id: 86e7967c-030c-44d6-8294-e7e6d41f6fc3
source-git-commit: 266cf18050d60f08f7e170c56453d1e1d805cb7b
workflow-type: tm+mt
source-wordcount: '1126'
ht-degree: 0%

---

# Veelgestelde vragen

Antwoorden op vragen die u zou kunnen hebben wanneer het uitvoeren van Audience Analytics.

## Veelgestelde vragen over wetgeving {#section_B51CFC961C0B45A2BE5F4A4404620764}

<table id="table_22037CCB516C4231BF5820004FBB351A"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <b>V: Hoe weet ik of ik Persoonlijk Identificeerbare Informatie (PII) in mijn Analytische gegevens heb? Zo ja, wat doe ik eraan?</b> </td> 
   <td colname="col2"> 
    <ul id="ul_71E0ECD5981D4B65BCDA065BE07A43AA"> 
     <li id="li_F8FF61A4D7B54BA39DAA6F28DB51D749">Als u e-mails/adressen/etc. in een hulpmiddel of eVar hebt, denk na hashing de gegevens tijdens inzameling. </li> 
     <li id="li_57A8B4C7BB784FFCBC1DC363B35D9FF7">Als uw land IP adres als PII beschouwt, <a href="https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/exclude-ip.html"  > IP-verduistering inschakelen </a>. </li> 
     <li id="li_C7AA02B831AE47A59E783623126A7789">Bespreek met uw Analysebeheerder wat u verzamelt. </li> 
     <li id="li_F6AAE868141E486AB8CAB291BD8EDB71">Bespreek met uw Juridische Afgevaardigde wat zij PII achten. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <b>Q: Hoe weet ik of mijn rapportsuites onsite personalisatie, of offsite/onsite het richten doen?</b> </td> 
   <td colname="col2"> 
    <ul id="ul_F0984CEF80DB4B589716BC55549E32B8"> 
     <li id="li_9BC3819784A9408F846D60FF0F20AAF9">Dit geldt niet voor het verzenden van Adobe Analytics-gegevens naar Adobe Audience Manager. </li> 
     <li id="li_050A1BF9978E436895B5C7E33A82527D">Vraag uzelf: Zal u een Analytics-Gedeeld segment met een dimensie MCA terug naar het Experience Cloud delen? </li> 
     <li id="li_C52D969681B94F4AAA18FDEB21EC5B49">Exporteert u (bijvoorbeeld via gegevensfeeds) naar een Business Intelligence (BI)-systeem dat voor deze doeleinden wordt gebruikt? </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Adobe Audience Manager-specifieke veelgestelde vragen {#section_6BDF746BA6464359A6A89A64EB025D12}

<table id="table_15B44592161240BDA79F3B020EA9CC9D"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: Hoe creeer ik een bestemming Analytics in Audience Manager?</b> </p> </td> 
   <td colname="col2"> Zie <a href="https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/destinations/experience-cloud-destinations/create-analytics-destination.html"  > Een analysedoel configureren in Adobe Audience Manager </a>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Na het creëren van en het bewaren van een bestemming van de Analyse, hoe lang zal het duren tot de gegevens in mijn geselecteerde rapportreeksen verschijnen?</b> </p> </td> 
   <td colname="col2"> <p>Het kan enkele uren duren om nieuwe gegevens in uw rapportensuites te plaatsen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Ik heb een nieuwe bestemming van Analytics gecreeerd, maar ik zie het niet in de sectie van Toewijzingen van de Bestemming van mijn beschikbare segmenten. Waar ging die bestemming heen of hoe vind ik het?</b> </p> </td> 
   <td colname="col2"> <p>Een bestemming Analytics verdwijnt uit de sectie van de Toewijzingen van de Bestemming van een segment wanneer u selecteert <span class="uicontrol"> Automatisch alle huidige en toekomstige segmenten toewijzen </span> optie in <span class="uicontrol"> Segmenttoewijzingen </span>. </p> <p><img placement="break" align="left"  src="assets/auto-mapping.png" id="image_670ED5A306784FCBA8A0B336AC1F0FC6" width="300px" /> </p> <p>Selecteer <span class="uicontrol"> Segmenten handmatig toewijzen </span> in plaats van de automatische optie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>V: Zal dit me alle informatie geven van Adobe Audience Manager, in Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Nr, slechts gegevens met betrekking tot mensen die aan uw plaats tijdens of na het inschakelen van het Publiek van de Audience Manager en tijdens/na segmentkwalificatie komen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>V: Zal dit me een per segment totaal adresseerbaar publiek geven?</b> </p> </td> 
   <td colname="col2"> <p>Niet echt. Het zal u het aantal bezoekers in dat segment vertellen die aan uw plaats tijdens of na segmentkwalificatie kwamen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>V: Hoe verschilt dit van de oude cookie-bestemming tot Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Segmenten worden gekwalificeerd voor en geretourneerd in real-time - op dezelfde hit. </p> <p>Vriendelijke namen worden automatisch weergegeven. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Wat als sommige van mijn verslagen persoonlijke gegevens hebben en sommigen niet?</b> </p> </td> 
   <td colname="col2"> <p>Tip: Maak twee bestemmingen - voeg de reeksen van het persoonlijke gegevensrapport aan één bestemming toe en de reeksen van het niet-persoonlijke gegevensrapport aan andere. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Analytische specifieke veelgestelde vragen {#section_67BFB1B1E48D4113A38B075C020931BA}

<table id="table_19AEAE0A3575423CB4F5F164DB5626D5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>V: Zal dit integratieoppervlak een dimensie of segment zijn in Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Als afmetingen: publiek-id en naam publiek. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Waar kan ik deze dimensies gebruiken in Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Bijna overal; ze worden behandeld net als elke andere dimensie die in Analytics wordt verzameld. Er is één uitzondering: op dit moment zijn de gegevens niet in Data Workbench. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Waarom zie ik geen gegevens die door Analytics komen?</b> </p> </td> 
   <td colname="col2"> <p>U hebt waarschijnlijk conflicterende Adobe Audience Manager-privacybesturingselementen tussen gegevensbron en doel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Waarom ontbreken sommige van mijn segmenten in Analytics, hoewel ik verkoos om alle segmenten te verzenden?</b> </p> </td> 
   <td colname="col2"> 
    <ul id="ul_B8938FD08C6F4F2387EDADDEF8089319"> 
     <li id="li_50A9BDF612304062913370F16BC882EF">Uw Adobe Audience Manager-besturingselementen voor gegevensuitvoer op de bestemming en in de gegevensbronnen van de segmenten zijn mogelijk tegenstrijdig, waardoor bepaalde segmenten niet kunnen worden verzonden. </li> 
     <li id="li_AF5D6F883D6F4D3192E0BF23CF12ADEA">Als u de eigenschappen van derdegegevens in uw segmenten gebruikt, kunnen die segmenten niet aan bestemmingen (een reeks rapportreeksen) worden gedeeld die persoonlijke gegevens bevatten. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Waarom zie ik "Audience limit Rebence" in mijn Analytics-rapport? (Opmerking: dit wordt ook weergegeven als Audience ID = -1 en "::max_audiences_exceeded::" in Data Warehouse)</b> </p> </td> 
   <td colname="col2"> <p>Door gebrek, verzendt de Audience Analytics integratie voor Adobe Audience Manager alle segmenten die een bezoeker voor, op een per-raakbasis, aan Analytics kwalificeert. Als een bezoeker tot meer dan 150 segmenten van Adobe Audience Manager op één hit behoort, <b>150 meest recente gekwalificeerde segmenten</b> worden verzonden naar Analytics, terwijl de resterende lijst wordt afgekapt. </p> <p>Een extra vlag wordt verzonden naar Analytics die erop wijst dat de segmentlijst werd beknot, en vertoningen zoals "de grens van het publiek bereikte"in de dimensie van de Naam van het Publiek en "-1"in de dimensie van identiteitskaart van het Publiek. </p> <p>Hoewel het onwaarschijnlijk is dat een bezoeker bij een bepaald resultaat voor meer dan 150 segmenten in aanmerking komt, kan dit een klein percentage van de tijd zijn. Als de limiet van het publiek is bereikt in de rapportage, hebt u twee opties: </p> 
    <ul id="ul_8E290B2E32DC49738F6FD00CB0CE2BBB"> 
     <li id="li_12F498981EA949B5BCBD40ECC954C339"><b>Optie 1</b>: Ga door met het laten werken van de integratie in de toestand 'uit-van-de-box', waarbij u de 150 meest recente gekwalificeerde segmenten voor een bepaalde bezoeker verzendt. </li> 
     <li id="li_CA4D5747AA4A4452929097807B604959"><b>Optie 2</b>: Kies in Adobe Audience Manager de 150 segmenten die het belangrijkst zijn voor uw bedrijf voor de integratie. Adobe Audience Manager controleert vervolgens alleen bezoekers op die 150 segmenten. Het nadeel van deze benadering is dat u slechts die 150 segmenten over alle bezoekers ontvangt. Anderzijds kan de Optie 1-benadering onbeperkte segmenten bieden vanwege het per-raaktype van de integratie. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Zullen extra servervraag aan Analytics voor deze integratie in rekening worden gebracht?</b> </p> </td> 
   <td colname="col2"> <p>Nee. Adobe Audience Manager-soorten publiek worden opgenomen in de detectieserver van Analytics. Dit veroorzaakt geen extra servervraag aan (primaire of secundaire) Analytics. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Veelgestelde vragen over doorsturen op de server (SSF) {#section_ADDE84ABCA0D4906B6235E92D185E0C6}

<table id="table_B7067B70FF85498896801F58D716202F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><b>Q: Als ik erfenis SSF uitgevoerd heb, moet ik ook naar Analytics Admin gaan en rapportreeks SSF aanzetten?</b> </p> </td> 
   <td colname="col2"> <p>Ja. In de de bestemmingsopstelling van Adobe Audience Manager, zult u slechts rapportsuites zien die SSF hebben aangezet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>Q: Waarom kan ik niet bepaalde rapportsuites voor SSF in Analytics Admin aanzetten?</b> </p> </td> 
   <td colname="col2"> <p>Alleen suites die zijn toegewezen aan uw Experience Cloud Org kunnen worden ingeschakeld. </p> </td> 
  </tr> 
 </tbody> 
</table>

Zie voor meer veelgestelde vragen over dit onderwerp [Veelgestelde vragen over doorsturen op de server](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md).

## Algemene veelgestelde vragen {#section_E55410BBFB624AAFB87ADCF7F036DDA3}

<table id="table_1F7C0C785F9C472286A96F8C25E8440B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Q: Waarom telt de segmentbezoeker verschillend tussen Audience Manager en Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Zie <a href="/help/integrate/c-audience-analytics/visitor-count-reconciliation.md"  > Verschillen in aantal bezoekers </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Wat is het verschil tussen "publiek" in Adobe Audience Manager en "segmenten" in Analytics?</b> </p> </td> 
   <td colname="col2"> <p>Zie <a href="/help/integrate/c-audience-analytics/aam-analytics-segments.md"  > Segmenten begrijpen in Analytics en Audience Manager </a>. </p> <p>Het Adobe Audience Manager-publiek wordt verzonden en gedeeld als 'dimensie'-componenten die in Analytics moeten worden gebruikt. Zij zullen niet verschijnen als segmenten in de Bouwer van het Segment, bijvoorbeeld, maar als afmetingen die u segmenten kunt bouwen met. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Wat is het verschil tussen klantkenmerken en klantgegevens die vanuit Adobe Audience Manager zijn geïntegreerd?</b> </p> </td> 
   <td colname="col2"> <p>Kenmerken van de klant zijn niet gebaseerd op tijd; ze zijn retroactief en gaan verder. Geïntegreerde Adobe Audience Manager-gegevens zijn alleen op tijd gebaseerd en gaan door. Bovendien, zijn de klantenattributen een raadplegingstabel voor Experience Cloud bezoeker IDs, terwijl de integratie van Adobe Audience Manager gegevens is die in elke slag voor een bezoeker worden vastgemaakt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><b>V: Hoe zit het met de oude aanpak van dit probleem, bijvoorbeeld de oude bèta- of Consulting-plug-in cookie-bestemmingen?</b> </p> </td> 
   <td colname="col2"> <p>Wij adviseren dat u de nieuwe integratie uitvoert en oude bestemmingen verwijdert. </p> </td> 
  </tr> 
 </tbody> 
</table>
