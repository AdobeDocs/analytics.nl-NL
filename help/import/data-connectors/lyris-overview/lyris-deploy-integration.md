---
description: Beschrijft het driestappenplaatsingsproces.
title: De integratie implementeren
uuid: a3c0ef21-ed9a-44d7-bdce-19b3bd5b8b80
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# De integratie implementeren{#deploying-the-integration}

Beschrijft het driestappenplaatsingsproces.

Deze integratie implementeren is een eenvoudig proces waarvoor de volgende acties nodig zijn:

## Voltooiend de Tovenaar van de Integratie{#completing-the-integration-wizard}

Stappen om de integratiewizard te gebruiken.

Als u de integratie wilt activeren, moet u de wizard Lyris-integratie voltooien in de interface Data Connectors.

1. Navigeer naar het gebied Gegevensverbindingen (voorheen Genesis) in de Adobe Experience Cloud.

   ![](assets/data_connectors.png)

1. Klik onder **[!UICONTROL Add Integration]** Lyris HQ op **[!UICONTROL Activate]**.

   ![](assets/add_integration.png)

1. Kies onder **[!UICONTROL General Settings]** de gewenste rapportsuite en geef een naam op voor de integratie.
1. Vul alle gegevens over uw Lyris-account in onder **[!UICONTROL Custom Values]**.

   ![](assets/general_settings.png)

1. Kies de juiste gereserveerde eVars en gebeurtenissen in de vervolgkeuzemenu&#39;s.

   ![](assets/variable_mapping.png)

1. U kunt uw eigen segmenten onder **[!UICONTROL Your Segments]** - behalve de 3 geautomatiseerde segmenten van de Partner kiezen.
1. Voor deze integratie is mogelijk het downloaden van een paar gegevenspunten naar uw Lyris-account vereist. U kunt ervoor kiezen om hiervoor toegang te verlenen onder **[!UICONTROL Access Request]**.
1. Onder **[!UICONTROL Data Collection]**, kunt u verkiezen om een geautomatiseerde of handmatige oplossing (elektrisch toestel JavaScript) te hebben om vraagkoordparameters van de het landen pagina URL te verzamelen. Als u verkiest om een geautomatiseerde oplossing te hebben, ga uw parameter van het vraagkoord voor identiteitskaart van het Bericht en Ontvangersidentiteitskaart in Neem voor een JavaScript-plug-in contact op met uw Adobe Consultant.

   ![](assets/data_collection.png)

1. Desgewenst kunt u het dashboard van Lyris en de bladwijzers automatisch voor u laten genereren.

   ![](assets/dashboard_generation.png)

1. Bekijk het overzicht van de integratie en klik op **[!UICONTROL Activate]**.

## Configuratie binnen de Lyris EmailLabs{#configuration-within-the-lyris-emaillabs}

Stappen die beschrijven wat binnen Lyris na de voltooiing van de tovenaar moet vormen.

1. Nadat u de integratietovenaar hebt voltooid, moet u met het team van Lyris Professional samenwerken om de integratie in uw Lyris HQ-account te voltooien en het testen te vergemakkelijken.
1. Parameters URL-queryreeks toevoegen: Controleer of de URL-appendtekenreeks correct wordt ingevoerd in de gebieden met instellingen voor de organisatie van de gebruikersinterface. Dit zou identiteitskaart van het campagneniveau (hq_m) en ontvanger niveau ID (hq_v) moeten bevatten.

   Een voorbeeld van een tekenreeks-id is:

   ```
   hq_lid=149&hq_m=96843&hq_l=23&hq_v=7703a51905
   ```

   >[!NOTE]
   >
   >Als u het native analyseprogramma van Lyris toepast, *klikt u op Tracks* om alle vereiste variabelen te labelen die zijn toegevoegd.

## Integratie controleren{#verifying-the-integration}

Stappen om te controleren of de integratie met Lyris/Adobe Analytics is gelukt.

Zodra alle plaatsingsstappen zijn voltooid, kunt u bevestigen dat de integratie met succes gegevens overbrengt.

>[!NOTE] Het duurt een paar dagen voordat de gegevensuitwisseling begint. Neem contact op met Lyris nadat u de integratie hebt geactiveerd.

1. Navigeer naar uw Lyris-integratie binnen gegevensconnectors. Onder **[!UICONTROL Support]** tab > **[!UICONTROL Integration Activity Log]** ziet u bijvoorbeeld gebeurtenissen als **[!UICONTROL Metric data imported successfully]** en/of **[!UICONTROL Classification data imported successfully]**:

   ![](assets/integration_info.png)

1. Bekijk nu uw Lyris-berichtrapporten met de juiste meetgegevens. Selecteer in de Adobe Experience Cloud **[!UICONTROL Reports & Analytics]**.
1. Selecteer de juiste rapportsuite.
1. Selecteer onder **[!UICONTROL Custom Conversions]**, de **[!UICONTROL Message ID Reports]** en kies **[!UICONTROL Message ID/Message Name]**.

## Insteekmodulecode voor parameters voor query-tekenreeks{#query-string-param-plug-in-code}

Hiermee wordt de insteekcode van de insteekmodule Lyris weergegeven die moet worden gebruikt met Adobe Analytics.

>[!NOTE] Controleer of u de benodigde eVars hebt gereserveerd in het Admin Tool of Adobe Analytics voordat u met de onderstaande code gaat werken. Als u weet welke eVars u hebt gereserveerd, vervangt u eVarN door de betreffende eVar. bv. eVar10.

```
/* 
  * Plugin: getQueryParam 2.3 
  */ 
s.getQueryParam=new Function("p","d","u","" 
+"var s=this,v='',i,t;d=d?d:'';u=u?u:(s.pageURL?s.pageURL:s.wd.locati" 
+"on);if(u=='f')u=s.gtfs().location;while(p){i=p.indexOf(',');i=i<0?p" 
+".length:i;t=s.p_gpv(p.substring(0,i),u+'');if(t){t=t.indexOf('#')>-" 
+"1?t.substring(0,t.indexOf('#')):t;}if(t)v+=v?d+t:t;p=p.substring(i=" 
+"=p.length?i:i+1)}return v"); 
s.p_gpv=new Function("k","u","" 
+"var s=this,v='',i=u.indexOf('?'),q;if(k&&i>-1){q=u.substring(i+1);v" 
+"=s.pt(q,'&','p_gvf',k)}return v"); 
s.p_gvf=new Function("t","k","" 
+"if(t){var s=this,i=t.indexOf('='),p=i<0?t:t.substring(0,i),v=i<0?'T" 
+"rue':t.substring(i+1);if(p.toLowerCase()==k.toLowerCase())return s." 
+"epa(v)}return ''"); 
 
/*in the s_doPlugins function - Replace N with actual eVar number*/ 
s.eVarN=s.getQueryParam("<insert Lyris QS Param>");  
//places query param value from Message ID in eVarN variable s.eVarN=s.getQueryParam("<insert Lyris QS Param>");  
//places query param value from Recepient ID in eVarN variable 
```
