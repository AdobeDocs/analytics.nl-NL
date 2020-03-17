---
description: Creeer, beheer, en bekijk het gebruik van gegevensbronnen in een rapportreeks.
subtopic: Data sources
title: Gegevensbronbeheer
topic: Developer and implementation
uuid: ccfa4a1c-7c56-421b-8ee6-a42b334659b1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Gegevensbronbeheer

Creeer, beheer, en bekijk het gebruik van gegevensbronnen in een rapportreeks.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Data Sources]**.

## Tab maken {#section_74603FDA3D8842E49F1A51624A06DE20}

Het [!UICONTROL Create] lusje laat u een nieuwe gegevensbron voor de momenteel geselecteerde rapportreeks vormen. Wanneer u een gegevensbron activeert, [!UICONTROL Data Sources Wizard] begeleidt u door het proces om een malplaatje van Gegevensbronnen tot stand te brengen, en leidt tot een plaats van FTP voor het uploaden van gegevens.

De selectie die u maakt op het tabblad Maken bepaalt de eerste velden in de sjabloon die wordt gemaakt. Zie Een [sjabloon](/help/import/c-data-sources/datasrc-template/t-datasrc-creating-data-sources-file.md)voor importbestanden genereren.

## Tab beheren {#section_DD559A6701CA45F1A85E56F840F48DBE}

<table id="table_F74696EC855441328CFE0BF49C20D9B0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Option </p> </th> 
   <th colname="col2" class="entry"> <p>Beschrijving </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Verwerking opnieuw starten </p> </td> 
   <td colname="col2"> <p>Start de gegevensbronverwerking opnieuw die eerder is gestopt als gevolg van fouten of waarschuwingen. De verwerking gaat door tot de volgende fout wordt ontmoet. Gegevensbronnen stoppen de verwerking van een gegevensbronbestand alleen wanneer u <span class="uicontrol"> Stopverwerking op fouten</span>selecteert. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Volledige verwerking </p> </td> 
   <td colname="col2"> <p>Instrueert Gegevensbronnen om het even welke open bezoeken in het dossier te sluiten en verwerking van het Brondossier van Gegevens te beëindigen alsof het volledig is. Dit is nuttig wanneer u bezoeken hebt die veelvoudige dossiers van Gegevensbronnen overspannen. Dit geldt alleen voor <a href="/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md"   > volledige verwerking</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Deactiveren </p> </td> 
   <td colname="col2"> <p> Als u een gegevensbron deactiveert, wordt deze verwijderd. Als bestanden op de server zijn verwerkt, wordt de verwerking voortgezet totdat deze zijn voltooid. Bestanden die nog niet zijn begonnen met de verwerking worden niet verwerkt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Verwerking stoppen bij fouten/waarschuwingen </p> </td> 
   <td colname="col2"> <p> Instrueert de Motor van de Verwerking van Gegevensbronnen om verwerking tegen te houden wanneer het een fout ontmoet. De gegevensbron hervat de verwerking pas als u Verwerking opnieuw starten selecteert. De optie Verwerking stoppen bij waarschuwingen is alleen van toepassing op <a href="/help/import/c-data-sources/c-datasrc-types/datasrc-full-processing.md"   > Volledige verwerking</a>. </p> <p>Wanneer de Gegevensbronnen een dossierfout ontmoeten, brengt het u op de hoogte van de fout. Het systeem verplaatst het gegevensbronbestand met de fout naar een map met de naam <span class="filepath"> files_with_errors</span> op de FTP-server. Nadat u het probleem hebt opgelost, leg het dossier van Gegevensbronnen voor verwerking opnieuw voor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Configureren </p> </td> 
   <td colname="col2"> <p>Hiermee kunt u de gegevensbronsjabloon of andere instellingen voor deze gegevensbron wijzigen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>FTP-info </p> </td> 
   <td colname="col2"> <p>Geeft de FTP-informatie voor deze gegevensbron weer. Gebruik deze informatie om tot het gegevensbronmalplaatje toegang te hebben, en gegevens van de Gegevensbron te verzenden. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bestandsnaam </p> </td> 
   <td colname="col2"> <p>De naam van het geüploade bestand </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Status </p> </td> 
   <td colname="col2"> <p> De huidige status van het bestand. Mogelijke statuswaarden zijn onder andere: </p> 
    <ul id="ul_56A0BF8C1BE249F6BB39B0D11DA3997F"> 
     <li id="li_BAB359E08EDE4E0298C0362258789603">In wachtrij (stap 1 van 3): Het bestand bestaat, maar de verwerking is nog niet gestart. Als het bestand niet binnen 30 minuten wordt weergegeven, controleert u of het bijbehorende <span class="filepath"> .fin</span> -bestand aanwezig is </li> 
     <li id="li_A09A14F42CB74F01B694799740B3DA17">Voorbereiden (stap 2 van 3): Het bestand wordt gecontroleerd op fouten of waarschuwingen </li> 
     <li id="li_793FDCDB64CF434D82CAF5B6E9BDE557">Verwerking (stap 3 van 3): Het bestand wordt verwerkt </li> 
     <li id="li_1D8C4B241FF0453EAF7DDFD8354C5573">Mislukt: Het bestand is niet verwerkt door fouten </li> 
     <li id="li_A52507602FB4492B83A70AF6449A539A">Geslaagd: Het bestand is volledig verwerkt </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Tabblad Bestandslogbestand {#section_B7AC7EE8CAD740A59DD53CF1919373F0}

Het dossierlogboek omvat een onderzoekseigenschap die u naar informatie door de Naam van de Gegevensbron, het Type van Gegevensbron, dossier - naam, ontvangen datum, of status laat zoeken.
