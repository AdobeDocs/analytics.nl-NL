---
description: U kunt Dynamisch tagbeheer implementeren met behulp van een of meer beschikbare hostopties.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;hosting;hosting options;akamai;self hosting;self-hosting;ftp delivery;ftp hosting;library download
title: hostopties configureren
topic: Developer and implementation
uuid: 04268f2d-e76f-4fe4-8fcc-f0db3a016502
translation-type: tm+mt
source-git-commit: 3fe3442eae1bdd8b90acffc9c25d184714613c16

---


# hostopties configureren

U kunt de toepassing implementeren [!UICONTROL Dynamic Tag Management] met een of meer beschikbare hostopties.

[!UICONTROL Dynamic Tag Management] bevat een aantal opties voor het hosten van de vereiste JavaScript-bestanden.

Voor gedetailleerde informatie over ontvangen, zie de [Inbedden Code en het Hosten Opties](https://docs.adobe.com/content/help/en/dtm/using/client-side/client-side-information.html) in de Documentatie van het [!UICONTROL Dynamic Tag Management] Product.

Selecteer op het tabblad Insluiten een hostoptie.

<table id="table_229298207DB64838B6F2477DFFAE073F"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Hostoptie </th> 
   <th colname="col2" class="entry"> Beschrijving </th> 
   <th colname="col3" class="entry"> Implementatie </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Akamai </p> </td> 
   <td colname="col2"> <p> De eenvoudigste te implementeren hostoptie. </p> <p>Globaal verdeeld leveringsnetwerk. </p> <p>Voegt extra derdeinfrastructuurgebiedsdelen (DNS raadpleging, beschikbaarheid Akamai) toe. </p> <p>Raadpleeg <a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/deployment.html#concept_722B01555D0441ACBB052BC34DC5B67D"> Akamai</a> in de documentatie over producten voor dynamisch tagbeheer voor meer informatie. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_EF148EF091A645B3962B084963B3C0B0"> 
     <li id="li_7ECE0C331EEE4907A563D581DF1DFEFE">Met Dynamisch tagbeheer worden aangepaste JavaScript-bibliotheken gegenereerd. </li> 
     <li id="li_8E2C858290EF4665B2F45ACAFA121CB3">Met Dynamic Tag Management worden de aangepaste JavaScript-bibliotheken geëxporteerd naar Akamai. </li> 
     <li id="li_CE88B10B6E844A56BBB8C575A9363BA9">De doelwebsite verwijst rechtstreeks naar de door Akamai gehoste Dynamic Tag Management-bibliotheken op paginaniveau. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zelfhosting: FTP-levering </td> 
   <td colname="col2"> <p>Een <span class="term"> push</span> -benadering waarbij met Dynamic Tag Management aangepaste JavaScript-bibliotheken rechtstreeks via het FTP-protocol worden geëxporteerd naar de host van de webinhoudserver. </p> <p>Voor deze oplossing zijn een FTP-server en gebruikersgegevens beschikbaar op de webinhoudserver om wijzigingen in de aangepaste Dynamic Tag Management-bibliotheken te publiceren. </p> <p>Zie <a href="https://docs.adobe.com/help/en/dtm/using/client-side/deployment.html#task_A7B37CB2C89941A4A4D1F9AF06FC493D"> FTP</a> in de documentatie over producten voor dynamisch tagbeheer voor meer informatie. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_60348F9C991D4F2B9457006B0F98C834"> 
     <li id="li_24A141C3C7074BF9897C022A22CAE78C">Met Dynamisch tagbeheer worden aangepaste JavaScript-bibliotheken gegenereerd. </li> 
     <li id="li_E1E0843060F7447E853EA416A0B033BE">Met Dynamic Tag Management worden de aangepaste JavaScript-bibliotheken via FTP naar de hostserver geëxporteerd. </li> 
     <li id="li_EAF5D2ABD03B4911A0CFA464AD8791CE">De doelwebsite verwijst lokaal naar de aangepaste Dynamic Tag Management-bibliotheken. </li> 
    </ol> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> Zelfhosting: Bibliotheek downloaden </td> 
   <td colname="col2"> <p>Een <span class="term"> pull</span> -benadering waarbij de toepassing aangepaste JavaScript-bibliotheken exporteert <!-- to Amazon S3-->. Daar kunnen de bibliotheken door een ontvangen server-zijproces worden betreden. </p> <p>Bovendien zijn de bibliotheken rechtstreeks via het web beschikbaar via de Dynamic Tag Management-interface. </p> <p>Deze oplossing vereist een handmatige ophaling en publicatie van de Dynamic Tag Management-bibliotheken of het maken van een geautomatiseerd proces dat de bibliotheken van Akamai naar de webinhoudserver haalt. </p> <p>Deze benadering neemt de meeste tijd in beslag om op te zetten, maar is ook de veiligste en meest flexibele optie. </p> <p>Als u wilt controleren of naar de nieuwste versie van het bibliotheekbestand wordt verwezen, gebruikt u de opdracht </p> <p>Zie<a href="https://docs.adobe.com/content/help/en/dtm/using/client-side/deployment.html#task_B7A42F3B1D3E4B71B0BADD17C181F22A"> Bibliotheek downloaden</a> in de documentatie over producten voor dynamisch tagbeheer voor meer informatie. </p> </td> 
   <td colname="col3"> 
    <ol id="ol_F40B721306FE473496BD657262DFD585"> 
     <li id="li_4EA4D6B555CE4E9CA476C7550C18C061">Met Dynamisch tagbeheer worden aangepaste JavaScript-bibliotheken gegenereerd. </li> 
     <li id="li_BA40EBD7AD1546F29D8A209034D06477">Met Dynamic Tag Management worden de aangepaste JavaScript-bibliotheken geëxporteerd naar Akamai. </li> 
     <li id="li_E107E69E386A40F3B067F9991C2979AF">Aangepaste dynamische tagbeheerbibliotheken worden handmatig of programmatisch naar de webinhoudsserver verplaatst. </li> 
     <li id="li_0809038453B544168A20CE09D7E5AC59">De doelwebsite verwijst lokaal naar de aangepaste Dynamic Tag Management-bibliotheken. </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

U kunt meerdere hostingopties gebruiken. U kunt uw gefaseerde bestanden bijvoorbeeld hosten met Akamai, maar uw productiesite zelf hosten. Elk hostingtype heeft een eigen insluitcode en er kan slechts één insluitcode aan een pagina worden toegevoegd.
