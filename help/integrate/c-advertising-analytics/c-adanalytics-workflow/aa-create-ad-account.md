---
title: Een advertentieaccount instellen in Advertising Analytics
description: Hiermee kunt u nieuwe advertentierekeningen maken en meerdere accounts toewijzen aan meerdere rapportensuites.
exl-id: f593c714-e85f-4000-85b2-6294cad81e25
source-git-commit: 98c04c6553f6f18bb69a29ac2af0f622928b0b31
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 4%

---

# Een advertentieaccount instellen

Adobe Analytics-beheerders kunnen nieuwe advertentieaccounts maken en meerdere accounts toewijzen aan meerdere rapportsuites (1:1, 1:Veel, Vele:Veel).

Beheerders kunnen ook [toegang verlenen aan niet-beheerders](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) voor het instellen van advertentierekeningen.

![](assets/aa_accounts.png)

1. Navigeer in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Advertising Accounts]**.
1. (Alleen voor de eerste keer) Accepteer de voorwaarden van de licentieovereenkomst voor eindgebruikers.
1. Klik op **[!UICONTROL + Add]**.
1. Het dialoogvenster [!UICONTROL New Search Engine Account] wordt weergegeven:

   ![](assets/aa_new_se_account.png)

1. Vul **[!UICONTROL Search Engine Settings]** volgende richtlijnen in:

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
      <td colname="col2"> <p>U hebt twee opties: Google AdWords en Microsoft Bing Ads. </p> <p>Opmerking: Yahoo Gemini werd door Microsoft Bing geabsorbeerd op 31 maart 2019. Als gevolg hiervan is de optie voor een Yahoo Gemini-advertentieaccount niet meer beschikbaar.  </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Accountnaam </p> </td> 
      <td colname="col2"> <p>U kunt deze accountnaam instellen op elke gewenste naam. Dit is de vriendschappelijke naam van de rekening die in UI zal verschijnen. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>OAuth Token </p> </td> 
      <td colname="col2"> <p>Opmerking:  OAuth is een open norm voor toegangsdelegatie, algemeen gebruikt als manier om websites of toepassingen toegang tot hun informatie op andere websites te verlenen maar zonder hen de wachtwoorden te geven. </p> <p>Opmerking:  U zult opmerken dat u aan een derde URL (efrontier.com) zult worden verpletterd. Adobe gebruikt efrontier om het OAuth authentificatieproces voor alle drie onderzoeksmotoren te aandrijven. </p> <p>Opmerking:  Als u Internet Explorer 11 (of vroeger) gebruikt, zult u niet het token Oauth voor om het even welke drie onderzoeksmotoren met succes kunnen terugwinnen. Gebruik in plaats hiervan andere webbrowsers. </p> <p>Door te klikken op <span class="uicontrol"> Token ophalen</span> wordt het OAuth2-verificatieproces gestart. Dit betekent dat u zich met uw referenties moet aanmelden bij uw Google/Bing-zoekaccount. Afhankelijk van de zoekengine die u hebt gekozen, is het proces iets anders: </p>
      <ul id="ul_FC9B5612F6554495B04C357CB0AB72EB"> 
       <li id="li_CD54231BFF134F83B3B5B14B34A0E1D2">Google Adwords: Geef een Google-account-id op. </li> 
       <li id="li_89B9D54BAA914E5DB2959B193489582E">Microsoft Bing: Geef de Bing-account-id en de Bing-klant-id op. </li> 
       </ul> <p>Raadpleeg <a href="/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-locate-account-id.md"  > Uw account-id zoeken</a> voor informatie over deze id's. </p> <p>Zodra u met succes het programma hebt geopend, zal het OAuth Symbolische gebied <code>Retrieved</code> tonen. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. In de sectie **[!UICONTROL Tracking]** geeft u informatie over hoe de gegevens van de zoekmachine worden bijgehouden door uw Adobe Analytics-implementatie. Dit is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met de zoekengine-gegevens.
Vul **[!UICONTROL Tracking Settings]** volgende richtlijnen in:

   | Instelling | Beschrijving |
   |--- |--- |
   | Type | <ul><li>**Automatisch:** Laat de Motor van Advertising Cloud beslissen hoe de het volgen parameters aan de het volgen malplaatjes/bestemmingsURLs van de Motor van het Onderzoek worden toegevoegd. Dit is de eenvoudigste benadering, maar kan niet in de beste geïntegreerde dataset resulteren.<br>**Belangrijk:** om een rekening van de onderzoeksmotor in &quot;Auto Wijze&quot;te vormen, bent u verantwoordelijk voor het nemen van de volgende acties:<br>- De &quot;s_kwcid&quot;parameter en de waarde zullen aan de rekeningen het volgen malplaatjes of het landen pagina URLs in de rekening worden toegevoegd die. Deze wordt aan het einde van de URL ingevoegd. Als gevolg hiervan kan aanvullende actie van uw kant vereist zijn als uw webserver een bepaald sleutelwaardepaar aan het einde van de URL vereist OF een update ter ondersteuning van een nieuw sleutelwaardepaar in de URL. **Opmerking:** Meer informatie over of u deze parameter moet toevoegen aan uw  [inhoudsbeveiligingsbeleid](https://experienceleague.adobe.com/docs/id-service/using/reference/csp.html).<br>- Daarnaast kunnen trefwoorden in de bestemmings-URL worden ingevoegd als onderdeel van de waarde &quot;s_kwcid&quot;, dus als deze speciale tekens of symbolen bevatten, moet u bevestigen dat uw webserver deze tekens kan ondersteunen (een voorbeeld van een speciale teken is &quot;+&quot;, dat wordt gebruikt in trefwoorden &quot;Uitgebreide overeenkomst gewijzigd&quot;).</li><li>**Handmatig:** Hiermee kunt u beheren hoe de volgparameters worden toegevoegd aan de trackingsjablonen/doel-URL&#39;s van de zoekmachine. [Raadpleeg deze handmatige voorbeelden voor het bijhouden van bestanden voor elke zoekfunctie](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md).</li></ul> |

1. In de sectie **[!UICONTROL Mapping]** kiest u welke rapportsuite(s) u wilt koppelen aan dit zoekprogrammaaccount. U moet ten minste één rapportsuite opgeven voordat u het advertentieaccount kunt opslaan. U kunt veelvoudige rekeningen aan veelvoudige rapportreeksen (1:1, 1:Velen, Velen:Velen) in kaart brengen. Merk op dat de gegevens die AMO van de onderzoeksmotor trekt eenvoudig aan om het even welke in kaart gebrachte rapportreeks wordt gekopieerd, zodat is er geen splitsing van gegevens.

   >[!IMPORTANT]
   >
   >Alleen rapportsuites die zijn toegewezen aan een Experience Cloud-organisatie, kunnen worden geselecteerd. Raadpleeg [Problemen met Advertising Analytics oplossen](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-troubleshooting.md) als uw rapportsuite niet wordt weergegeven.

   Voor **[!UICONTROL Mapping Settings]** die deze richtlijnen volgen:

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
   <td colname="col2"> <p>De rapportsuite-toewijzing bepaalt de rapportsuite die wordt gekoppeld aan dit zoekprogrammaaccount. Met andere woorden, het bepaalt in welke rapportsuite(s) de gegevens van de zoekmachine worden verzonden. </p> </td>
   </tr> 
   </tbody> 
   </table>

1. Klik op **[!UICONTROL Save]**.
1. Nadat u het bestand hebt opgeslagen, wordt een lijst met voorbehouden weergegeven. U wordt gevraagd te bevestigen dat u hebt gelezen en dat u deze overeenkomst begrijpt. Klik op het selectievakje en klik vervolgens op **[!UICONTROL OK]**.

   U gaat nu naar Advertising Accounts [Management UI](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md), waar uw nieuwe account moet worden vermeld.

>[!NOTE]
>
>U moet ten minste 24 uur wachten voordat de zoekprogrammagegevens de analyserapporten invullen.
