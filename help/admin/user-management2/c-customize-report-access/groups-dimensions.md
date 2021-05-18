---
description: Pas gebruikerstoegang op een korrelig niveau, met inbegrip van eVars, verkeersrapporten, oplossingsrapporten, en het kleven rapporten aan.
keywords: groepen;machtigingen
subtopic: Users and groups
title: Toestemmingen voor dimensies aanpassen
feature: Admin Tools
uuid: aaf164ad-3863-4129-864e-39ec71c6a8eb
exl-id: 51c4193a-426e-46a0-8494-163b58588157
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 13%

---

# Toestemmingen voor dimensies aanpassen

>[!IMPORTANT]
>
>Gebruiker- en productbeheer gaat over naar de [Admin Console](https://helpx.adobe.com/nl/enterprise/using/admin-console.html). Adobe geeft een melding wanneer het uw tijd is om gebruikers te migreren. Nadat alle klanten zijn gemigreerd, wordt Help-inhoud voor **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL User management]** ingetrokken.

Pas gebruikerstoegang op een korrelig niveau, met inbegrip van eVars, verkeersrapporten, oplossingsrapporten, en het kleven rapporten aan.

**[!UICONTROL User Management]** >  **[!UICONTROL Groups]** >  **[!UICONTROL Report Access]** >  **[!UICONTROL Dimensions]** >  **[!UICONTROL Customize]**

>[!IMPORTANT]
>
>Sommige dimensies zijn momenteel niet toegestaan. Deze afmetingen zijn: Lengte mobiele bladwijzer; nummer mobiele apparatuur; mobiele DRM; Mobiele informatiediensten; Mobile Java VM; Decoratie van mobiele post; Mobiele netprotocollen; mobiel besturingssysteem; Mobiele druk om te praten.
>
>Deze afmetingen zijn beschikbaar voor alle gebruikers, ongeacht andere toestemmingen.

De instellingen op deze pagina hebben betrekking op de rapportsuites die zijn geselecteerd op de pagina [!UICONTROL Define User Groups].

![](assets/permissions-dimensions.png)

Lees de volgende informatie over de categorie Dimension voor machtigingen.

* eVars 1-250 zijn afzonderlijk toegestaan.
* Alle verkeersrapporten zijn dimensies.
* Video- en mobiele rapporten zijn dimensies en andere rapporten over analysemogelijkheden (Experience Manager, Advertising Cloud, Sociaal, enzovoort.)
* Er zijn plakrapporten beschikbaar als een gebruiker toegang heeft tot de bovenliggende dimensie.
* Alle huidige afmetingen en metriek binnen aangepaste groepen zijn automatisch gemigreerd naar de nieuwe categorieën. Als metriek is ingeschakeld voor een bestaande groep, krijgt deze standaard alle nieuw toegestane afmetingen (eVars en inhoud behouden) en maatstaven.
* Indelingsrechten (voorheen, SAINT): Toegang tot classificaties wordt bepaald door toegang tot de [variabele](https://docs.adobe.com/content/help/en/analytics/components/classifications/c-classifications.html) waarop de classificatie is gebaseerd.

Voor meer informatie, zie [De toestemmingsveranderingen van de Gebruiker en van de Groep](https://docs.adobe.com/content/help/en/analytics/admin/user-product-management/user-management/permissions-changes.html).

**Dimension aanpassen**

De volgende items zijn dimensies die u kunt toestaan.

<table id="table_F37D74A1619A4560A5F5651E855DAF1C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijvingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="/help/admin/admin/conversion-var-admin/conversion-var-admin.md"> eVars </a> </p> </td> 
   <td colname="col2"> <p>eVars 1-250 zijn afzonderlijk toegestaan. Vars zijn aangepaste conversievariabelen die u gebruikt om de succeswaarden van de segmentconversie in aangepaste rapporten te segmenteren. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/nl-NL/analytics/implementation/vars/page-vars/evar.html"> Props </a> </p> </td> 
   <td colname="col2"> <p>Props zijn variabelen voor aangepast verkeer. </p> <p>Zie <a href="https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/evar.html"> Verkeersprofielen en conversievars </a> in Analytics Implementation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/page-variables.html"> Hiërarchie </a> </p> </td> 
   <td colname="col2"> <p> De hiërarchische variabele (hierN) bepaalt de locatie van een pagina in de hiërarchie of de paginastructuur van uw site. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/en/analytics/implementation/vars/page-vars/page-variables.html"> Listvar  </a> </p> </td> 
   <td colname="col2"> <p> Net als bij de werking van List Props staan lijstvariabelen meerdere waarden binnen dezelfde afbeeldingsaanvraag toe. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Standaard </p> </td> 
   <td colname="col2"> <p>Verwijst naar standaardafmetingen (out-of-the-box) in Analytics. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://helpx.adobe.com/support/experience-manager.html"> AEM </a> </p> </td> 
   <td colname="col2"> <p>Adobe Experience Manager </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://helpx.adobe.com/support/advertising-cloud.html"> AMO  </a> </p> </td> 
   <td colname="col2"> <p>Adobe Advertising Cloud </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/nl-NL/analytics/analyze/activity-map/activity-map.html"> Activity Map </a> </p> </td> 
   <td colname="col2"> <p> Rapportagedimensies voor Activity Mappen: Activity Map pagina; Activity Map link; regio Activity Map; Activity Map koppeling per regio; Activity Map XY </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/nl-NL/media-analytics/using/media-overview.html"> Mobiel </a> </p> </td> 
   <td colname="col2"> <p>Adobe Mobile Services </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Comscore </p> </td> 
   <td colname="col2"> <p>Deze partnerintegratie is niet meer actief. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="https://docs.adobe.com/content/help/en/media-analytics/using/media-overview.html"> Nielsen  </a> </p> </td> 
   <td colname="col2"> <p>Deze partnerintegratie is niet meer actief. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Sociaal </p> </td> 
   <td colname="col2"> <p>Niet gebruikt. </p> </td> 
  </tr> 
 </tbody> 
</table>
