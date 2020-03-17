---
description: Variabelen voor privacyrapportage in Data Privacy.
title: Privacy Reporting Variables
topic: Admin tools
translation-type: tm+mt
source-git-commit: ddbd724231850c816e7b2b2e56dc139d31276d0c

---


# Privacy Reporting Variables

Om extra hulp bij het beheren van privacygegevens te verlenen, is een reeks gereserveerde variabelen beschikbaar die samen met specifieke contextgegevensvariabelen moeten worden gebruikt.
Deze variabelen voor privacyrapportage bieden een gebruiksvriendelijk raamwerk voor het vastleggen van de privacystatus bij elke treffer voor analysemogelijkheden.

## Variabelen

* Afmelden voor beheer van toestemming
   * Gereserveerde variabele: List Prop
   * Type: Door komma&#39;s gescheiden tekenreeks
   * Bevat:
      * `contextData.['cm.ssf']=1` weergegeven als SSF
      * `contextData.['opt.dmp']=N` weergegeven als DMP
      * `contextData.['opt.sell']=N` weergegeven als SELL

* Inschakelen voor beheer van toestemming
   * Gereserveerde variabele: List Prop
   * Type: Door komma&#39;s gescheiden tekenreeks
   * Bevat:
      * `contextData.['opt.dmp']=Y` weergegeven als DMP
      * `contextData.['opt.sell']=Y` weergegeven als SELL

## Rapportage

U kunt de optie Privacy Reporting Variables inschakelen via een nieuwe privacyinstelling die beschikbaar is in de beheerconsole voor analysemogelijkheden.

Elke rapportsuite kan als volgt worden geconfigureerd:
1. Klik in Rapporten en Analyse op **[!UICONTROL Admin > Report Suites]**.
1. Selecteer de rapportsuite(s) waar u mediagegevens verzamelt en klik op **[!UICONTROL Edit Settings > Privacy Management]**.

   ![](assets/rsm-privacy-select.png)

1. Klik op de **[!UICONTROL Enable Data Privacy Reports]** knop.

   > [!NOTE] Als deze variabelen eenmaal zijn ingeschakeld, kunnen ze niet worden uitgeschakeld.

   ![](assets/rsm-privacy-enable.png)

1. Zodra toegelaten, zult u een bevestigingsbericht zien.

   ![](assets/rsm-privacy-config.png)

1. De gereserveerde variabelen zijn nu beschikbaar voor analyse in Rapporten &amp; Analytics en Workspace. Zie Afmelden bij voorkeur voor beheer van toestemming en Inschakelen.

   ![](assets/consent-management.png)

## Implementatie

Er zijn drie contextgegevensvariabelen vooraf gedefinieerd om te werken met de voor privacyrapportage gereserveerde variabelen.  Het is aan elke implementatieingenieur om te bepalen hoe te om het plaatsen van deze variabelen te beheren en voort te zetten.

Zie [Contextgegevensvariabelen](https://docs.adobe.com/help/en/analytics/implementation/javascript-implementation/variables-analytics-reporting/context-data-variables.html) voor algemene richtlijnen voor het implementeren van contextgegevensvariabelen.

### SSF

* Contextgegevens: `contextData.['cm.ssf']`
* Geaccepteerde waarden:
   * 1 - Wanneer u de waarde &quot;1&quot; verzendt, geeft dit aan dat Server Side Forwarding zich in de status &quot;opt-out&quot; bevindt. De waarde &quot;1&quot; in combinatie met deze variabele blokkeert het delen van deze hit met Adobe Audience Manager. Zie [AAM ePrivacy Compliance](https://docs.adobe.com/help/en/analytics/integration/audience-analytics/audience-analytics-workflow/ssf-gdpr.html).
   * 0 - Optioneel. Gebruik de waarde &quot;0&quot; voor klanten die hebben ingestemd met gerichte marketing. Als u de variabele niet instelt, krijgt u ook dezelfde resultaten.

### DMP

* Contextgegevens: `contextData.['opt.dmp']`
* Geaccepteerde waarden:
   * N - Wanneer de waarde &quot;N&quot; wordt verzonden, geeft dit aan dat de consument ervan afziet gegevens te delen naar platforms voor gegevensbeheer.  **Opmerking**: Met ingang van 15 januari 2020, die deze variabele aan &quot;N&quot;plaatst blokkeert server-zijdelings het delen van deze hit aan AAM.
   * Y - Wanneer de waarde &quot;Y&quot; wordt verzonden, geeft dit aan dat de consument ervoor kiest om gegevens te delen naar platforms voor gegevensbeheer.

### SELL

* Contextgegevens: `contextData.['opt.sell']`
* Geaccepteerde waarden:
   * N - Wanneer de waarde &quot;N&quot; wordt verzonden, geeft dit aan dat de consument ervoor kiest de gegevens niet te delen of aan derden te verkopen.
   * Y - Wanneer de waarde &quot;Y&quot; wordt verzonden, geeft dit aan dat de consument ervoor kiest de gegevens te delen of aan derden te verkopen.
