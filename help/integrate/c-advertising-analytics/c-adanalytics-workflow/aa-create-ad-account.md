---
title: Een advertentieaccount instellen
uuid: 4e37caa3-e4a5-43ad-97c0-12db62ad5283
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Een advertentieaccount instellen

Beheerders van Adobe Analytics kunnen nieuwe advertentierapporten maken en meerdere accounts toewijzen aan meerdere rapportsets (1:1, 1:Veel, Vele:Veel).

Beheerders kunnen ook toegang [verlenen tot niet-beheerders](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) voor het opzetten van advertentierekeningen.

![](assets/aa_accounts.png)

1. Navigeer in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Advertising Accounts]**.
1. (Alleen voor de eerste keer) Accepteer de voorwaarden van de licentieovereenkomst voor eindgebruikers.
1. Klik op **[!UICONTROL + Add]**.
1. Het [!UICONTROL New Search Engine Account] dialoogvenster wordt weergegeven:

   ![](assets/aa_new_se_account.png)

1. Vul de **[!UICONTROL Search Engine Settings]** volgende richtlijnen in:

   <table id="table_B3BE66B7D4C54766B8FFD2C6DCD657AF"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Instelling </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>U hebt twee opties: Google AdWords en Microsoft Bing Ads. </p> <p>Opmerking: Yahoo Gemini werd door Microsoft Bing geabsorbeerd op 31 maart 2019. Als gevolg hiervan is de optie Yahoo Gemini-advertentieaccount niet meer beschikbaar.  </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Accountnaam </p> </td> 
      <td colname="col2"> <p>U kunt deze accountnaam instellen op elke gewenste naam. Dit is de vriendschappelijke naam van de rekening die in UI zal verschijnen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>OAuth Token </p> </td> 
      <td colname="col2"> <p>Opmerking:  OAuth is een open norm voor toegangsdelegatie, algemeen gebruikt als manier om websites of toepassingen toegang tot hun informatie op andere websites te verlenen maar zonder hen de wachtwoorden te geven. </p> <p>Opmerking:  U zult opmerken dat u aan een derde URL (efrontier.com) zult worden verpletterd. Adobe gebruikt efrontier om het OAuth-verificatieproces voor alle drie zoekprogramma's uit te voeren. </p> <p>Opmerking:  Als u Internet Explorer 11 (of vroeger) gebruikt, zult u niet het token Oauth voor om het even welke drie onderzoeksmotoren met succes kunnen terugwinnen. Gebruik in plaats hiervan andere webbrowsers. </p> <p>Klik<span class="uicontrol"> terugwinnen Token</span> lanceert het OAuth2 authentificatieproces. Dit betekent dat u zich met uw referenties moet aanmelden bij uw Google/Bing-zoekaccount. Afhankelijk van de zoekengine die u hebt gekozen, is het proces iets anders: </p> 
        <ul id="ul_FC9B5612F6554495B04C357CB0AB72EB"> 
        <li id="li_CD54231BFF134F83B3B5B14B34A0E1D2">Google Adwords: Geef een Google-account-id op. </li> 
        <li id="li_89B9D54BAA914E5DB2959B193489582E">Microsoft Bing: Geef de Bing-account-id en de Bing-klant-id op. </li> 
        </ul> <p>Raadpleeg <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md"  > Account-ID</a> zoeken voor meer informatie over deze id's. </p> <p>Zodra u met succes het programma hebt geopend, zal het OAuth Symbolische gebied tonen 
        <systemoutput>
          Opgehaald
        </systemoutput>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. In de **[!UICONTROL Tracking]** sectie geeft u informatie over hoe de gegevens van de zoekmachine worden bijgehouden door de implementatie van Adobe Analytics. Dit is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met de gegevens van de Search Engine.
Vul de **[!UICONTROL Tracking Settings]** volgende richtlijnen in:

   <table id="table_1AB4E31456E84ABF8209B02058259C4D"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Instelling </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> 
        <ul id="ul_1C5A0502A4984E57A08417A91CCD6FFE"> 
        <li id="li_5736E38286FF494ABDDC6E85281D7F2A"> <span class="uicontrol"> Automatisch</span>: Hiermee kan de Advertising Cloud Engine bepalen hoe de volgparameters worden toegevoegd aan de trackingsjablonen/doel-URL's van de zoekmachine. Dit is de eenvoudigste benadering, maar kan niet in de beste geïntegreerde dataset resulteren. <p>Belangrijk: Als u een account voor een zoekmachine wilt configureren in de modus Automatisch, bent u verantwoordelijk voor het uitvoeren van de volgende handelingen: 
          <ul id="ul_4FF9D1E3CC4E452BA339E0A725D29FEE"> 
            <li id="li_6F3A6D6259C0420CB7E6FD2C26A1B6E0">De parameter en de waarde 's_kwcid' worden toegevoegd aan de sjablonen voor het bijhouden van accounts of aan URL's van landingspagina's in de account die wordt toegevoegd. Deze wordt aan het einde van de URL ingevoegd. Als gevolg hiervan kan aanvullende actie van uw kant vereist zijn als uw webserver een bepaald sleutelwaardepaar aan het einde van de URL vereist OF een update ter ondersteuning van een nieuw sleutelwaardepaar in de URL. </li> 
            <li id="li_A04D4AA31A934392808639E46C86573F">Daarnaast kunnen trefwoorden in de bestemmings-URL worden ingevoegd als onderdeel van de waarde "s_kwcid", dus als deze speciale tekens of symbolen bevatten, moet u bevestigen dat uw webserver deze tekens kan ondersteunen (een voorbeeld van een speciale teken is "+", dat wordt gebruikt in trefwoorden "Uitgebreide overeenkomst gewijzigd"). </li> 
          </ul> </p> </li> 
        <li id="li_EAA7A7CA1E584854A7EC1E43E13B63FE"><span class="uicontrol"> Handmatig</span>: Hiermee kunt u beheren hoe de volgende parameters worden toegevoegd aan de trackingsjablonen/doel-URL's van de zoekmachine. <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md"  > Raadpleeg deze handmatige voorbeelden voor het bijhouden van bestanden voor elke zoekfunctie</a>. </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. In de **[!UICONTROL Mapping]** sectie kiest u welke rapportsuite(s) u wilt koppelen aan dit zoekprogrammaaccount. U moet ten minste één rapportsuite opgeven voordat u het advertentieaccount kunt opslaan. U kunt veelvoudige rekeningen aan veelvoudige rapportreeksen (1:1, 1:Velen, Velen:Velen) in kaart brengen. Merk op dat de gegevens die AMO van de onderzoeksmotor trekt eenvoudig aan om het even welke in kaart gebrachte rapportreeks wordt gekopieerd, zodat is er geen splitsing van gegevens.

   >[!IMPORTANT]
   >
   >Alleen rapportsuites die zijn [toegewezen aan een Experience Cloud-organisatie](https://marketing.adobe.com/resources/help/en_US/mcloud/map-report-suite.html) , zijn beschikbaar voor selectie. Raadpleeg [Problemen met advertentieanalyse](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-troubleshooting.md)oplossen als uw rapportsuite niet wordt weergegeven.

   Voor de **[!UICONTROL Mapping Settings]** volgende richtsnoeren:

   <table id="table_AF876DC40F97403882C0AA528BD204FF"> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> Instelling </th> 
      <th colname="col2" class="entry"> Beschrijving </th> 
      </tr>
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Toewijzing van rapportsuite </p> </td> 
      <td colname="col2"> <p>De rapportsuite-toewijzing bepaalt de rapportsuite die wordt gekoppeld aan dit zoekprogrammaaccount. Met andere woorden, het bepaalt in welke rapportsuite(s) de gegevens van de zoekmachine worden verzonden. </p> <p>Als uw rapportsuite niet wordt weergegeven, kunt u deze tool gebruiken om uw rapportenpakket toe te <a href="https://marketing.adobe.com/resources/help/en_US/mcloud/map-report-suite.html"  > wijzen aan een Experience Cloud-organisatie</a> . </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Save]**.
1. Nadat u het bestand hebt opgeslagen, wordt een lijst met voorbehouden weergegeven. U wordt gevraagd te bevestigen dat u hebt gelezen en dat u deze overeenkomst begrijpt. Klik op het selectievakje en klik vervolgens op **[!UICONTROL OK]**.

   U wordt nu doorgestuurd naar de gebruikersinterface [voor](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md)beheer van advertentierekeningen, waar uw nieuwe account moet worden vermeld.

>[!NOTE] U moet ten minste 24 uur wachten voordat de zoekprogrammagegevens de analyserapporten invullen.

