---
description: Veelgestelde vragen over het volgen van koppelingen in Activity Map.
title: Veelgestelde vragen over link tracking
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: Bedrijfs Praktijk, Beheerder
translation-type: tm+mt
source-git-commit: f9d9c7dbaf5fde5bd51c929d927d4cd3f61cb63b
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 1%

---


# Veelgestelde vragen over link tracking

Veelgestelde vragen over het volgen van koppelingen in Activity Map.

>[!CAUTION]
>
>Als u het bijhouden van Activity Mappen inschakelt, **verzamelt u mogelijk PII-gegevens (Persoonlijk identificeerbare gegevens).** Deze gegevens kunnen op zichzelf of met andere informatie worden gebruikt om één persoon te identificeren, contact op te nemen of te vinden, of om een persoon in context te identificeren.

Hier zijn enkele bekende gevallen waarin PII-gegevens kunnen worden verzameld met behulp van Activity Map bijhouden:

* `Mailto` koppelingen. Een mailto-koppeling is een type HTML-koppeling waarmee de standaardmailclient op de computer wordt geactiveerd voor het verzenden van een e-mail.
* `User ID` koppelingen die worden weergegeven in de kop- of voettekst van een website nadat de gebruiker zich heeft aangemeld.
* Voor financiële instellingen kan het rekeningnummer als link worden weergegeven. Als u erop klikt, wordt de tekst van de koppeling verzameld.
* Op websites voor gezondheidszorg kunnen ook PII-gegevens als koppelingen worden weergegeven. Als u op deze koppelingen klikt, wordt de tekst van de koppeling verzameld en worden er dus PII-gegevens verzameld.

<table id="table_0951EAC617344156BAE43000CCD838AF">
 <tbody>
  <tr>
   <td colname="col1"> <b>V: Wanneer vindt het bijhouden van koppelingen plaats?</b> </td>
   <td colname="col2"> A: Koppeling naar Activity Map en regio-identificatie treedt op wanneer gebruikers op een pagina klikken. </td>
  </tr>
  <tr>
   <td colname="col1"> <b>V: Wat wordt standaard bijgehouden?</b> </td>
   <td colname="col2"> A: Als een klikgebeurtenis op een element voorkomt, moet het element sommige controles overgaan om te bepalen als AppMeasurement het als verbinding zal behandelen. Dit zijn de controles:
    <ul id="ul_81B9A5A7F8534E71AEF68F2199A154F0">
     <li id="li_49F6DDD9DC124AE5846EC5B7D7BEA20E">Is dit een <code>&lt;A&gt;</code> of <code>&lt;AREA&gt;</code> markering met een <code>"href"</code> bezit? </li>
     <li id="li_77828D24D54343E5B9A1FF7345221781">Is er een <code>"onclick"</code> attribuut dat een <code>s_objectID</code> variabele plaatst? </li>
     <li id="li_D4B0AEEEA58A4F82A1BCBD3971A60D02">Is dit een <code>&lt;INPUT&gt;</code> markering of <code>&lt;SUBMIT&gt;</code> knoop met een waarde of kindtekst? </li>
     <li id="li_F7ABE88308E1413E9B9C2224DEC91BAB">Is dit een <code>&lt;INPUT&gt;</code> markering met type <code>&lt;IMAGE&gt;</code> en een <code>"src"</code> bezit? </li>
     <li id="li_F34A0C986E8040109A1DDF88C26E56D5">Is dit een <code>&lt;BUTTON&gt;</code>? </li>
    </ul>
    Als het antwoord <b>Ja</b> op om het even welke bovenstaande vragen is, dan wordt het element behandeld als verbinding en zal worden gevolgd. <br/>
     <br/>
    Belangrijk: Knoplabels met het kenmerk  <code>type="button"</code> worden door AppMeasurement niet als koppelingen beschouwd. U kunt <code>type="button"</code> op de knoplabels verwijderen en <code>role="button"</code> of <code>submit="button"</code> toevoegen. <br/>
     <br/>
    Belangrijk: Een ankermarkering met een  <code>"href"</code> die met begint  <code>"#"</code> wordt beschouwd als een interne doelplaats door AppMeasurement, niet een verbinding (aangezien u niet de pagina verlaat.) Standaard houdt Activity Map deze interne doellocaties niet bij. Er worden alleen koppelingen bijgehouden waarmee de gebruiker naar een nieuwe pagina navigeert. </td> 
  </tr>
  <tr>
   <td colname="col1"> <b>V: Hoe houdt Activity Map andere visuele HTML-elementen bij?</b> </td>
   <td colname="col2">
    <ol id="ol_DA3AED165CFF44B08DFB386D4DEE26C5">
     <li id="li_E3E3F498F37B4FADAFDA39CCAE41511F"> <b>Via  <code>s.tl()</code> </b> <br/>
       <br/>
      functionAls de klik via een  <code>s.tl()</code> aanroeping voorkwam, dan zal de Activity Map ook deze klikgebeurtenis ontvangen en zal bepalen als een  <code>linkName</code> koordvariabele werd gevonden. Tijdens <code>s.tl()</code> uitvoering, dat <code>linkName</code> als identiteitskaart van de Verbinding van de Activity Map zal worden geplaatst. Het aangeklikte element dat de <code>s.tl()</code> vraag voortkwam zal worden gebruikt om het gebied te bepalen. <br/>
       <br/>
      Voorbeeld:  <br/>
       <br/>
      <code>&lt;img&nbsp;onclick="s.tl(true,'o','abc')"&nbsp;src="someimageurl.png"/&gt;</code><br/>
       
     </li>
     <li id="li_A93725B810FE408BA5E6B267CF8CEAE5"> <b>Via de  <code>s_objectID</code> </b> <br/>
       <br/>
      variableExample:  <br/>
       <br/>
      <code>&lt;img&nbsp;onclick="s_objectID='abc';"&nbsp;src="someimageurl.png"/&gt;</code><br/>
      <code>&lt;a&nbsp;href="some-url.html"&nbsp;onclick="s_objectID='abc';"&nbsp;&gt;</code><br/>
      <code>&nbsp;&nbsp;Link&nbsp;Text&nbsp;Here</code><br/>
      <code>&lt;/a&gt;</code> <br/>
       <br/>
      Belangrijk: Een volgpuntkomma (<code>;</code>) is vereist bij gebruik  <code>s_objectID</code> in Activity Map.
     </li>
    </ol>
   </td>
  </tr>
  <tr>
   <td colname="col1"> <b>V: Kunt u mij enkele voorbeelden geven van koppelingen die worden bijgehouden?</b> </td>
   <td colname="col2">
    <ol id="ol_697E5CE0B84D4A309DD80670697A02BA">
     <li id="li_2C511EFD10F14F438B1F3A1BAB4B45E0">
      <code>&lt;a&nbsp;href="/home"&gt;Home&lt;/a&gt;</code>
     </li>
     <li id="li_76F3DB36ED734132A2386871E6EB4929">
      <code>&lt;input&nbsp;type="submit"&nbsp;value="Submit"/&gt;</code>
     </li>
     <li id="li_10CF9EDA224645169E7CDF74956DB98B">
      <code>&lt;input&nbsp;type="image"&nbsp;src="submit-button.png"/&gt;</code>
     </li>
     <li id="li_9FA171D7F49547E798DE21869F73A402">
      <code>&lt;p&nbsp;onclick="var&nbsp;s_objectID='custom&nbsp;link&nbsp;id';"&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="subtitle"&gt;1.45USD&lt;/span&gt;</code><br/>
      <code>&lt;/p&gt;</code>
     </li>
     <li id="li_C5D77589006E4514AA6F3AEB509A0BAF">
      <code>&lt;div&nbsp;onclick="s.tl(true,'o','custom&nbsp;link&nbsp;id')"&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="subtitle"&gt;1.45USD&lt;/span&gt;</code><br/>
      <code>&lt;/div&gt;</code>
     </li>
    </ol>
   </td>
  </tr>
  <tr>
   <td colname="col1"> <b>V: Kunt u mij enkele voorbeelden geven van koppelingen die NIET worden bijgehouden?</b> </td>
   <td colname="col2">
    <ol id="ol_CDFDB572F76B4F68A64B66A6B0237547">
     <li id="li_99372060646B43EF94C13A9C682CE693">Reden: Ankertag heeft geen geldige <code>"href"</code> <br/>
       <br/>
      <code>&lt;a&nbsp;name="innerAnchor"&gt;Section&nbsp;header&lt;/a&gt;</code><br/>
       
     </li>
     <li id="li_736A5F7DC2D74B4DA1CECEE3AD10EB19">Reden: Geen <code>s_ObjectID</code> noch <code>s.tl()</code> aanwezig <br/>
       <br/>
      <code>&lt;p&nbsp;onclick="showPanel('market&nbsp;rates')"&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="title"&gt;Current&nbsp;Market&nbsp;Rates&lt;/span&gt;</code><br/>
      <code>&nbsp;&nbsp;&lt;span&nbsp;class="subtitle"&gt;1.45USD&lt;/span&gt;</code><br/>
      <code>&lt;/p&gt;</code><br/>
       
     </li>
     <li id="li_45F9ED97140F47F99F8C167BC1DC546F">Reden: Geen <code>s_ObjectID</code> noch <code>s.tl()</code> aanwezig <br/>
       <br/>
      <code>&lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="A"/&gt;</code><br/>
      <code>&lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="B"/&gt;</code><br/>
      <code>&lt;input&nbsp;type="radio"&nbsp;onclick="changeState(this)"&nbsp;name="group1"&nbsp;value="C"/&gt;</code><br/>
       
     </li>
     <li id="li_9EBFCC58F3A94F30BA62156F14B15D55">Reden: <code>"src"</code>-eigenschap mist een formulier <code>input</code>-element <br/>
       <br/>
      <code>&lt;input&nbsp;type="image"/&gt;</code><br/>
       
     </li>
    </ol>
   </td>
  </tr>
 </tbody>
</table>
