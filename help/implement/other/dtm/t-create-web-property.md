---
description: Een webeigenschap kan elke groepering van een of meer domeinen en subdomeinen met een bibliotheek met regels zijn, die in één ingesloten code is opgenomen.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;web property;property
title: Webeigenschap maken
topic: Developer and implementation
uuid: f19d5504-eb44-4d93-a387-7470ab4b3a3a
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Webeigenschap maken

Een webeigenschap kan elke groepering van een of meer domeinen en subdomeinen met een bibliotheek met regels zijn, die in één ingesloten code is opgenomen.

>[!NOTE] Alleen gebruikers met beheerdersrechten kunnen een eigenschap maken. Zie Groepen [maken en beheren in DTM](https://marketing.adobe.com/resources/help/en_US/dtm/groups.html) in de documentatie over producten voor dynamisch tagbeheer voor meer informatie over rollen.

U kunt deze middelen beheren en bijhouden met DTM. Stel dat u meerdere websites hebt die op één sjabloon zijn gebaseerd en u dezelfde elementen op al deze websites wilt bijhouden. U kunt één webeigenschap op meerdere domeinen toepassen.

Voor algemene informatie over Web eigenschappen en beste praktijken, zie de Eigenschappen [van het](https://marketing.adobe.com/resources/help/en_US/dtm/web_property.html) Web in de Dynamische Documentatie van het Product van het Beheer van de Markering.

1. Navigeer naar de bedrijfspagina en klik op **[!UICONTROL Add Property]**.

   ![](assets/dtm-create-web-property.png)

1. Vul de velden in:

   <table id="table_376D72251C4D4C4CA878D10C18D2532C"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Element </th> 
    <th colname="col2" class="entry"> Beschrijving </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Naam</span> </td> 
    <td colname="col2"> <p>De naam van uw eigenschap. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> URL</span> </td> 
    <td colname="col2"> <p>De basis-URL van de eigenschap. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Deze site omvat meerdere domeinen </span> </td> 
    <td colname="col2"> <p>U kunt domeinen toevoegen en verwijderen als u bezoekersgegevens tussen domeinen wilt behouden. Als deze optie is geselecteerd, blijven de gegevens voor het bezoek in de verschillende subdomeinen bestaan. </p> <p>Met deze instelling kunt u opgeven hoe u verkeer wilt bijhouden dat zich tussen de bijbehorende subdomeinen of domeinen verplaatst. Koppelingen naar subdomeinen worden behandeld als uitgaande koppelingen. Bezoeken naar subdomeinen worden afzonderlijk bijgehouden. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. (Optioneel) Configureer [!UICONTROL Advanced Settings].

   <table id="table_6E687FBE6ACC4301BCCD837F4DCBB9C9"> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> Element </th> 
    <th colname="col2" class="entry"> Beschrijving </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Goedkeuring van meerdere regels toestaan</span> </td> 
    <td colname="col2"> <p>Hiermee worden meerdere regels voor deze eigenschap tegelijk goedgekeurd. De standaardgoedkeuring staat slechts single-rule goedkeuring toe. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Selectieve publicatie inschakelen</span> </td> 
    <td colname="col2"> <p>Geeft aan of gebruikers mogen selecteren welke goedgekeurde regels worden gepubliceerd. Dit is de standaardoptie. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Naam van cookie bijhouden</span> </td> 
    <td colname="col2"> <p>Hiermee overschrijft u de standaardnaam voor het bijhouden van cookies. U kunt de naam die door Dynamic Tag Management wordt gebruikt, aanpassen om de status Weigeren bij te houden voor het ontvangen van andere cookies. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Time-out tag</span> </td> 
    <td colname="col2"> <p>Hiermee geeft u op hoe lang Dynamic Tag Management wacht totdat een tag wordt geactiveerd voordat de tagaanvraag wordt time-out en geannuleerd. </p> <p> Vanwege hoe Dynamic Tag Management werkt, hoeft u zich geen zorgen te maken over het hoge aantal hiervan. DTM beschikt over effectieve methoden om ervoor te zorgen dat trage tags de gebruikerservaring niet beïnvloeden. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <span class="uicontrol"> Vertraging ankerpunt</span> </td> 
    <td colname="col2"> <p>Hiermee geeft u op hoe lang Dynamisch tagbeheer wacht totdat tags worden geactiveerd op aangeklikte koppelingen voordat naar de volgende pagina wordt gegaan. De standaardwaarde is 100 milliseconden. </p> <p>Langere vertragingen verbeteren het volgen nauwkeurigheid. Adobe raadt een vertraging van 500 milliseconden of minder aan, die de gebruiker niet zal waarnemen. </p> <p>Het dynamische Beheer van de Markering zal tot de gespecificeerde tijd wachten, maar als het baken vroeger brandt, wordt de vertraging gekort. (De gebruiker zal dus niet altijd de volledige duur van de vertraging wachten.) </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Klik op **[!UICONTROL Create Property]**.
