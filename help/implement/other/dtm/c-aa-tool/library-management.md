---
description: Beschrijvingen van de gebieden en de opties in de montages van het Beheer van de Bibliotheek in Dynamisch Beheer van de Markering.
keywords: library management;page code;load library at;managed by adobe;custom;code hosted;s_code hosted
solution: Experience Cloud,Dynamic Tag Management
title: Bibliotheekbeheer
uuid: 4cfa47f9-ae98-4feb-a58d-a3a6e45f8d5b
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Bibliotheekbeheer

Beschrijvingen van de gebieden en de opties in de montages van het Beheer van de Bibliotheek in Dynamisch Beheer van de Markering.

**[!UICONTROL  *`Property`*]** > ![](assets/settings_gear.png) **[!UICONTROL Edit Tool]** > **[!UICONTROL Library Management]**

> [!NOTE] Als er meerdere Adobe Analytics-programma&#39;s worden gebruikt in één webeigenschap, moet elke tool een unieke naam hebben voor de variabele tracker. Dubbele namen van objectvariabelen tussen Adobe Analytics-programma&#39;s binnen één webeigenschap veroorzaken conflicten.

<table id="table_2758C770C91B4025AD74009B360D71F7"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Element </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Paginacode is al aanwezig </p> </td> 
   <td colname="col2"> <p> Met Dynamisch tagbeheer kan <span class="keyword"> Adobe Analytics</span> -paginacode niet worden geïnstalleerd als de code al aanwezig is op uw site. </p> <p>Met deze functie kunt u Dynamisch tagbeheer gebruiken om aan uw bestaande implementatie toe te voegen in plaats van helemaal opnieuw te beginnen. Zorg ervoor dat u de naam van de variabele Beheer correct instelt wanneer u dit selectievakje inschakelt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bibliotheek laden bij &lt;<span class="term"> Pagina boven</span> of <span class="term"> Pagina onder</span>&gt; </p> </td> 
   <td colname="col2"> <p>Hiermee geeft u op waar en wanneer de paginacode moet worden geladen. Ongeacht de selectie moeten alle regels die gebruikmaken van het gereedschap Analyse dezelfde instelling hebben. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Beheerd door Adobe (aanbevolen) </p> </td> 
   <td colname="col2"> <p>Schakel Dynamisch tagbeheer in om uw bibliotheek te beheren. </p> <p>Als u deze optie selecteert, wordt de volgende optie beschikbaar: </p> <p> <b>Bibliotheekversie: </b>Selecteer de meest recente versie in het menu <span class="wintitle"> Bibliotheekversie</span> . Het dynamische markeringsbeheer brengt u op de hoogte wanneer de nieuwe versies beschikbaar zijn. U kunt desgewenst terugkeren naar een vorige versie. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Aangepast </p> </td> 
   <td colname="col2"> <p>U kunt de bibliotheekcode configureren. </p> <p>Als u deze optie selecteert, worden de volgende opties beschikbaar: </p> <p> <b>Stel de rapportsuites met behulp van de onderstaande aangepaste code in: </b>Wanneer dit vakje wordt gecontroleerd, zoekt het Dynamische Beheer van de Markering naar een variabele in uw douanecode genoemd <span class="varname"> s_account</span>. Deze variabele moet een door komma's gescheiden lijst van de rapportsuites bevatten waarnaar u data wilt verzenden. </p> <p> <b>Gehoste code: </b>Kies een optie om de <span class="filepath"> s_code</span>te hosten: </p> 
    <ul id="ul_FC395283365A4BBAA8A5FE5871D16EC6"> 
     <li id="li_36D733C533CE40F1868309130551D4DE"> <b>In DTM</b>: U kunt de <span class="filepath"> s_code</span> hosten binnen Dynamisch Beheer van de Markering. Klik op Code <span class="uicontrol"></span> bewerken om het bestand rechtstreeks in de editor te knippen en te plakken. </li> 
     <li id="li_A64734C66D254079A5E16DC8DBEDA3F6"> <b>URL</b>: Als u een goed <span class="filepath"> s_code</span> dossier hebt en met het proces gelukkig om het bij te werken, kunt u URL aan het dossier hier verstrekken. Dynamisch tagbeheer gebruikt vervolgens dat <span class="filepath"> s_code</span> -bestand voor de implementatie van <span class="keyword"> Adobe Analytics</span>. </li> 
    </ul> <p> <b>Editor openen:</b> Hiermee kunt u <a href="/help/implement/other/dtm/c-aa-tool/t-appmeasurement-code.md"  >AppMeasurement-kerncode invoegen</a>. Deze code wordt automatisch ingevuld wanneer u de automatische configuratiemethode gebruikt die wordt beschreven in <a href="/help/implement/other/dtm/c-aa-tool/analytics-dtm.md"  >Adobe Analytics-instellingen</a>. </p> <p> <b>Naam van variabele Beheer: </b>Als u twee exemplaren van <span class="keyword"> Adobe Analytics</span> parallel wilt uitvoeren (één in Dynamic Tag Management en één in native), kunt u de naam van het hoofd- <span class="term"> s</span> -object wijzigen. Als u de naam van het object wijzigt, worden conflicten voorkomen. </p> </td> 
  </tr> 
 </tbody> 
</table>

