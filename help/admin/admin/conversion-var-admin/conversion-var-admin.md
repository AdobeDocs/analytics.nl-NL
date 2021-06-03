---
description: De Custom Insight-conversievariabele (of -eVar) wordt in de Adobe-code op geselecteerde webpagina's van uw site geplaatst. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op bezoek-gebaseerd zijn en functioneren gelijkaardig aan koekjes. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.
keywords: eVar
title: Conversievariabelen (eVar)
feature: Admin Tools
uuid: 1eed0cb1-0735-4142-be21-43f264216b50
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '1577'
ht-degree: 0%

---

# Conversievariabelen (eVars)

De Custom Insight-conversievariabele (of -eVar) wordt in de Adobe-code op geselecteerde webpagina&#39;s van uw site geplaatst. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op bezoek-gebaseerd zijn en functioneren gelijkaardig aan koekjes. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.

Wanneer een eVar aan een waarde voor een bezoeker wordt geplaatst, onthoudt Adobe automatisch die waarde tot het verloopt. Eventuele succesgebeurtenissen die een bezoeker tegenkomt terwijl de waarde eVar actief is, worden geteld bij de waarde eVar.

Vars kunnen het beste worden gebruikt om oorzaak en effect te meten, zoals:

* Welke interne campagnes de inkomsten beïnvloedden
* Welke banneradvertenties uiteindelijk hebben geresulteerd in een registratie
* Het aantal keren dat een interne zoekopdracht is gebruikt voordat een bestelling is gemaakt

Als verkeersmeting of het kleven gewenst is, wordt het gebruiken van verkeersvariabelen geadviseerd.

>[!NOTE]
>
>Er kan slechts één waarde worden opgeslagen in een eVar in een afbeeldingsaanvraag. Als de veelvoudige waarden in een waarde van de eVar worden gewenst, adviseren wij dat u [variabelen van de Lijst (lijstvars)](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html) uitvoert.

## Conversievariabelen - beschrijvingen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Beschrijvingen van velden die worden gebruikt wanneer [conversievariabelen bewerken](/help/admin/admin/conversion-var-admin/t-conversion-variables-admin.md).

<table id="table_E48D50926E6B492183300CA58A886927"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Element </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Naam </span> </p> </td> 
   <td colname="col2"> <p>De vriendelijke naam van de conversievariabele. Deze naam is hoe naar de eVar wordt verwezen in algemene rapportering, en zal de naam van het rapport in het linkermenu zijn. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Type</span> </p> <p>(alleen eVar) </p> </td> 
   <td colname="col2"> <p>Het type van veranderlijke waarde: </p> <p> <b>Tekstreeks</b>:</span> legt tekstwaarden vast die op uw site worden gebruikt. Dit is het meest gangbare type eVar en de standaardinstelling. De methode werkt op dezelfde manier als andere variabelen, waarbij de waarde erin een statische tekenreeks is. Als u zaken zoals interne campagnes of interne onderzoekssleutelwoorden volgt, is dit het geadviseerde plaatsen. </p> <p> <b>Teller</b>:</span> Telt het aantal keren dat een actie vóór de succesgebeurtenis voorkomt. Als u bijvoorbeeld een eVar gebruikt om interne zoekopdrachten op uw site bij te houden, stelt u deze waarde in op <span class="uicontrol"> Tekstreeks</span> om het gebruik van zoektermen te volgen. Stel deze waarde in op <span class="uicontrol"> Teller</span> om het aantal uitgevoerde zoekopdrachten te tellen, ongeacht de gebruikte zoektermen. U kunt bijvoorbeeld een teller gebruiken om het aantal keren te volgen dat iemand uw interne zoekopdracht heeft gebruikt voordat hij een aankoop doet. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Toewijzing  </span> </p> </td> 
   <td colname="col2"> <p>Bepaalt hoe Analytics kredieten voor een succesgebeurtenis toewijst als een variabele veelvoudige waarden vóór de gebeurtenis ontvangt. Tot de ondersteunde waarden behoren: </p> <p> <b>Recentste versie</b>: De laatste waarde van de eVar ontvangt altijd krediet voor succesgebeurtenissen tot die eVar verloopt. </p> <p> <b>Oorspronkelijke waarde</b>: De eerste eVar krijgt altijd krediet voor succesgebeurtenissen tot die eVar verloopt. </p> <p> <b> Lineair</b>:Hiermee worden succesgebeurtenissen op gelijke wijze toegewezen voor alle eVar-waarden. Aangezien de Lineaire toewijzing waarden slechts binnen een bezoek nauwkeurig verdeelt, gebruik Lineaire toewijzing met een eVar van Bezoek. </p> <p>Opmerking:  Als u van of naar Lineair schakelt, worden historische gegevens niet weergegeven. Het mengen van toewijzingstypes in de rapporteringsinterface kan tot misverklaarbare gegevens in rapporten leiden. Zo kan lineaire toewijzing inkomsten verdelen over een aantal verschillende eVar. Na het terugkeren naar de meest recente toewijzing, zou 100% van die opbrengst met de meest recente enige waarde worden geassocieerd. Deze koppeling kan leiden tot onjuiste conclusies van gebruikers. </p> <p>Om de kans op verwarring bij het rapporteren te vermijden, maakt Analytics de historische gegevens niet aan de interface beschikbaar. U kunt deze weergeven als u de opgegeven eVar wilt wijzigen in de oorspronkelijke toewijzingsinstelling, maar u kunt de instellingen voor de eVar-toewijzing niet wijzigen om alleen toegang te krijgen tot de historische gegevens. Adobe raadt aan een nieuwe eVar te gebruiken wanneer nieuwe toewijzingsinstellingen gewenst zijn voor gegevens die al worden geregistreerd, in plaats van toewijzingsinstellingen te wijzigen voor een eVar waarin al een aanzienlijke hoeveelheid historische gegevens is opgebouwd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Verlopen na</span> </p> </td> 
   <td colname="col2"> <p>Geeft een tijdsperiode op, of een gebeurtenis, waarna de waarde van de eVar verloopt (ontvangt geen krediet meer voor succesgebeurtenissen). Als een succesgebeurtenis optreedt na het verlopen van de eVar, ontvangt de waarde None een creditering voor de gebeurtenis (er was geen eVar actief). </p> <p>Als u een gebeurtenis selecteert als een vervalwaarde, verloopt de variabele alleen als de gebeurtenis plaatsvindt. Als de gebeurtenis niet voorkomt, verloopt de variabele nooit. </p> <p>De beschikbare vervalopties kunnen in vier hoofdcategorieën worden ingedeeld: </p> 
    <ul id="ul_810A37C9B6624F429F2FB45C18F7B43F"> 
     <li id="li_654D9D9044EC4E61AA7ABA372DBF8A93"><b>Op pagina- of bezoekniveau.</b> Conversiegebeurtenissen buiten de paginaweergave of het bezoek zijn niet gekoppeld aan de eVar. </li> 
     <li id="li_689FBC8B4DAC41B3B0166E6586DD1990"><b>Gebaseerd op een tijdsperiode, zoals dag, week, maand, of jaar.</b> Conversiegebeurtenissen na de opgegeven periode worden niet aan de eVar gekoppeld. De vervalperiode begint wanneer de variabele wordt ingesteld. De vervaldatum is gebaseerd op de tijd waarop ze zijn ingesteld, tot de tweede (minuut, uur, dag, maand, enz.): 
      <ul id="ul_80C7E3182B6B4356B8A3CA920B81C6D5"> 
       <li id="li_F16F60319CCE406D9EDEFEC0A200BC4D">MINUTE=60 seconden </li> 
       <li id="li_45F47F3F5691415B84052B235DF3BB54">HOUR=3600 seconden (60 minuten) </li> 
       <li id="li_5288CE7D168E4C85B3D9BB67A44D32EC">DAY=86400 seconden (24 uur) </li> 
       <li id="li_60FC8BCD657745EE87B4E458CBA69583">WEEK=604800 seconden (7 dagen) </li> 
       <li id="li_7A05A66613C84F929F030310B9567CF5">MAAND=2678400 seconden (31 dagen) </li> 
       <li id="li_DCD3CABF59E34D5999B03E606B08AD85">QUARTER=8035200 seconden (93 dagen - 3 maanden van 31 dagen) </li> 
       <li id="li_54351D2899454D39A8BA205910D2CCB1">JAAR=31536000 seconden (365 dagen) </li> 
      </ul> <p> </p> <p>Als het bezoek begint om 7:00 uur op maandag en er tijdens dat bezoek om 7:15 uur een eVar is ingesteld, is de vervaldatum als volgt: </p> 
      <ul id="ul_72B311006BE6428698313D251C0940DB"> 
       <li id="li_50925D4A40AD4ACA88704A523138C5B9">Vervaldag: eVar verloopt om 7:15 op dinsdag. </li> 
       <li id="li_25846328766D4B4BAF407236C65C956C">Vervaldatum week: eVar verloopt op de volgende maandag om 7:15 uur. </li> 
       <li id="li_82DB2D7F53304623A5E1241D75C7DF94">Vervaldatum maand: eVar vervalt 31 dagen vanaf maandag om 7.15 uur. </li> 
      </ul> </li> 
     <li id="li_C132C5C5A5344B91BDF5EB6A1C717C37"><b>Specifieke conversiegebeurtenissen.</b> Alle andere conversiegebeurtenissen die na de opgegeven specifieke gebeurtenis plaatsvinden, zijn gekoppeld aan de eVar. </li> 
     <li id="li_5A782D743FB940649E6CB3E4BEA9B8B6"><b>Nooit.</b> Zolang de  <span class="varname"> </span> bezoekerIDcookie intact is, kan om het even welke hoeveelheid tijd tussen eVar en gebeurtenis overgaan. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Status</span> </p> <p>(alleen eVar) </p> </td> 
   <td colname="col2"> <p>Definieert de status van de eVar: </p> <p><b>Uitgeschakeld</b>:</span> Hiermee schakelt u de eVar uit. Hiermee verwijdert u de eVar uit de lijst met conversievariabelen. </p> <p> <b>Geen subrelaties</b>:</span> voorkomt dat de eVar wordt afgebroken met een subrelatie. </p> <p> <b>Basissubrelaties</b>:  </span>Laat u een eVar door om het even welk rapport met volledige onderverdelingen (bijvoorbeeld, Producten of Campagne) verdelen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Herstellen</span> </p> </td> 
   <td colname="col2"> <p>Hiermee wordt de bestaande waarde in de eVar opnieuw ingesteld. </p> <p>Gebruik deze instelling bij het opnieuw gebruiken van een eVar, zodat u een oude waarde kunt mengen in een nieuw rapport. Bij het opnieuw instellen worden geen historische gegevens verwijderd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Merchandising</span> </p> <p>(alleen eVar) </p> </td> 
   <td colname="col2"> <p>De variabelen van de koophandel kunnen één van twee syntaxis volgen: </p> <p> <b>Productsyntaxis</b>:</span> Koppelt de waarde van de eVar aan een product. Opmerking:  Als de Syntaxis van Producten wordt geselecteerd, is de Merchandising Bindende sectie van de Gebeurtenis gehandicapt en niet selecteerbaar voor uitgeven. Voor deze syntaxis zijn Binding Events niet van toepassing. </p> </p> <p> <b>Conversievariabele syntaxis</b>:</span> Koppelt de eVar alleen aan een product als er een bindingsgebeurtenis plaatsvindt. In dit geval selecteert u de gebeurtenissen die fungeren als Bindende gebeurtenissen. </p> <p>Als u deze instelling wijzigt zonder uw JavaScript-code dienovereenkomstig bij te werken, gaan er gegevens verloren. Zie <a href="https://experienceleague.adobe.com/docs/analytics/components/variables/merchandising-variables/var-merchandising.html"> Variabelen veranderen</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="uicontrol"> Merchandising Binding-gebeurtenis</span> </p> <p>(alleen eVar) </p> </td> 
   <td colname="col2"> <p>Als Merchandising aan <span class="uicontrol"> de Veranderlijke Syntaxis van de Omzetting </span> wordt geplaatst, binden de geselecteerde gebeurtenissen de huidige waarde van de eVar met een product. </p> <p>Om een Bindende Gebeurtenis te gebruiken, plaats <span class="uicontrol"> Toewijzing aan Meest recent</span>. Als <span class="uicontrol"> Toewijzing Originele Waarde</span> is, blijft de eerste eVar product band tot de eVar verloopt. U kunt meerdere gebeurtenissen selecteren door <code>ctrl</code> (Windows) of <code>cmd</code> (Mac) ingedrukt te houden en op meerdere items in de lijst te klikken. U kunt alleen een gebeurtenis selecteren wanneer de syntaxis van de conversievariabele is geselecteerd.</p> </td> 
  </tr> 
 </tbody> 
</table>

**Verlopen**

`eVars` verlopen na een door u opgegeven tijdsperiode. Nadat de eVar is verlopen, ontvangt het geen krediet meer voor succesgebeurtenissen. eVars kunnen ook worden geconfigureerd om te verlopen bij succesgebeurtenissen. Als je bijvoorbeeld een interne aanbieding hebt die aan het einde van een bezoek vervalt, ontvangt de interne aanbieding alleen kredieten voor aankopen of registraties die plaatsvinden tijdens het bezoek waarin ze zijn geactiveerd.

Er zijn twee manieren om een eVar te verlopen:

* U kunt instellen dat de eVar na een opgegeven tijdsperiode of gebeurtenis vervalt.
* U kunt de vervaldatum van een eVar forceren door deze opnieuw in te stellen. Dit is handig wanneer u een variabele opnieuw gebruikt.

Als u bijvoorbeeld de vervaldatum van een eVar wijzigt van 30 tot 90 dagen, blijven de verzamelde eVar behouden gedurende de nieuwe vervaldatum (in dit geval 90 dagen). Het systeem bekijkt eenvoudig de huidige die vervalbepaling en laatste vastgestelde timestamp van de eVar waarde wordt verzameld om afloop te bepalen. Alleen de optie **[!UICONTROL Reset]** vervalt waarden en doet dit onmiddellijk.

Een ander voorbeeld: Als een eVar in Mei wordt gebruikt om interne bevorderingen te weerspiegelen en na 21 dagen verloopt, en in juni wordt het gebruikt om interne onderzoekssleutelwoorden te vangen, dan zou u op 1 Juni de afloop van, of het terugstellen van, de variabele moeten dwingen. Als u dat doet, blijven de interne promotiewaarden buiten de verslagen van juni.

**Hoofdlettergevoeligheid**

Variabelen zijn niet hoofdlettergevoelig, maar worden wel weergegeven in het hoofdlettergebruik van het eerste exemplaar. Als de eerste instantie van eVar1 bijvoorbeeld is ingesteld op &quot;Aangemeld&quot;, maar alle volgende exemplaren worden doorgegeven als &quot;aangemeld&quot;, wordt in rapporten altijd &quot;Aangemeld&quot; weergegeven als de waarde van de eVar.

**Tellers**

Terwijl eVars het vaakst worden gebruikt om koordwaarden te houden, kunnen zij ook worden gevormd om als tellers te handelen. Variabelen zijn nuttig als tellers wanneer u probeert te tellen het aantal acties een gebruiker vóór een gebeurtenis neemt. U kunt bijvoorbeeld een eVar gebruiken om het aantal interne zoekopdrachten vast te leggen voordat u de aankoop doet. Telkens wanneer een bezoeker zoekt, moet de eVar de waarde &#39;+1&#39; bevatten. Als een bezoeker vier keer vóór een aankoop zoekt, ziet u een exemplaar voor elk totaal aantal: 1,00, 2,00, 3,00 en 4,00. Alleen de 4,00 ontvangen echter krediet voor het aankoopevenement (bestellingen en inkomstencijfers). Alleen positieve getallen zijn toegestaan als waarden van een eVar-teller.
