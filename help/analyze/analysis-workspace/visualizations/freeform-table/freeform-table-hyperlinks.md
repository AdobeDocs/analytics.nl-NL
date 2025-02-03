---
title: Hyperlinks maken in een vrije-vormtabel in Analysis Workspace
description: Leer hoe u hyperlinks maakt voor dimensie-items in een vrije-vormtabel in Analysis Workspace
feature: Freeform Tables
role: User, Admin
exl-id: df846a73-e3e3-4376-844e-48153a20e5d6
source-git-commit: d7a6867796f97f8a14cd8a3cfad115923b329c7c
workflow-type: tm+mt
source-wordcount: '1739'
ht-degree: 0%

---

# Hyperlinks maken voor afmetingen in een vrije-vormtabel

U kunt hyperlinks maken voor dimensie-items, zodat hierop kan worden geklikt in een vrije-vormtabel in Analysis Workspace.

Deze functionaliteit is vooral handig bij het maken van hyperlinks voor de volgende typen dimensies:

* Items Dimensionen die URL-waarden hebben waarnaar u een koppeling wilt maken (bijvoorbeeld een pagina-URL-dimensie)

* Items van een Dimension die onderverdelingen bevatten met URL-waarden waarnaar u wilt koppelen (bijvoorbeeld een pagina-naamdimensie met een indeling van een pagina-URL-dimensie)

* Items of uitsplitsingen in Dimensionen met waarden die onderdeel zijn van een URL waarnaar u een koppeling wilt maken (bijvoorbeeld een paginanaam die deel uitmaakt van een URL)


>[!BEGINSHADEBOX]

Zie ![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ Hyperlinks voor afmeting ](https://video.tv.adobe.com/v/3430411?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]





## Hyperlinks maken voor een of meer afmetingsitems

Houd rekening met het volgende wanneer u hyperlinks maakt voor dimensie-items:

* De hyperlinks die u maakt, worden opgeslagen in de vrije-vormtabel in het Analysis Workspace-project. Hyperlinks blijven niet bestaan wanneer u dezelfde dimensie- of dimensie-items in een andere tabel of in een ander project gebruikt.

* Als u de gegevensweergave van de vrije-vormlijst wijzigt, zijn alle hyperlinks die voor dimensies of dimensie-items in de tabel zijn gemaakt, nog steeds beschikbaar, op voorwaarde dat de dimensie in de gegevensweergave bestaat.

* URL&#39;s worden niet gecontroleerd op geldigheid wanneer u de hyperlink maakt.

  Als u een hyperlink maakt met een ongeldige URL of als u een hyperlink maakt die verwijst naar een dimensie-item dat geen URL-waarde heeft (door rechtstreeks naar het dimensie-item te verwijzen of door de variabelen `$value` of `$breakdown` te gebruiken), wordt een foutbericht weergegeven voor gebruikers die op de hyperlink klikken. Hierin wordt aangegeven dat de URL ongeldig is.

* Hyperlinks die voor één enkel afmetingspunt worden gecreeerd treden hyperlinks met voeten die op de afmeting worden gecreeerd.

* De hyperlinks zijn niet functioneel in [ gedownloade dossiers van PDF ](/help/analyze/analysis-workspace/curate-share/download-send.md).

U kunt als volgt hyperlinks maken voor een of meer dimensies:

1. Voer een van de volgende handelingen uit in een vrije-vormtabel in Analysis Workspace:

   * **creeer een hyperlink voor één enkel afmetingspunt:** klik het afmetingspunt binnen de lijst met de rechtermuisknop aan waarvoor u hyperlink wilt creëren, dan selecteren [!UICONTROL **hyperlink**] creëren.

     ![ creeer hyperlink voor één enkel afmetingspunt ](assets/hyperlink-single-add.png)

     [!UICONTROL **creeer hyperlink**] dialoog wordt getoond. De naam van het dimensie-item waarvoor u een hyperlink maakt, wordt weergegeven in het dialoogvenster.

     ![ creeer hyperlink voor één enkel puntdialoog ](assets/hyperlink-dialog-single.png)

   * **creeer hyperlinks voor alle afmetingspunten in een afmetingskolom:** klik de afmetingsnaam in de kopbal van de afmetingskolom met de rechtermuisknop aan, dan uitgezocht [!UICONTROL **creeer hyperlinks voor alle afmetingspunten**].

     ![ creeer hyperlink voor een afmeting ](assets/hyperlink-multiple-add.png)

     [!UICONTROL **creeer hyperlinks voor alle afmetingspunten**] dialoog wordt getoond. De naam van de dimensie waarvoor u hyperlinks maakt, wordt weergegeven in het dialoogvenster.

     ![ creeer hyperlinks dialoog ](assets/hyperlink-dialog-multiple.png)

1. Kies een van de volgende opties:

   * [!UICONTROL **gebruik de waarde van het afmetingspunt als URL**]: Kies deze optie voor afmetingspunten die waarden URL, zoals een afmeting van Pagina URL hebben.

     Als u bijvoorbeeld een pagina-URL-dimensie gebruikt waarvan de waarde van elk dimensie-item een URL is, maakt u met deze optie een hyperlink naar de URL.

   * [!UICONTROL **creeer een douane URL**]: Specificeer of een statische of dynamische douane URL. Kies deze optie om hyperlinks te maken voor dimensie-items die geen URL-waarden hebben.

     Als u bijvoorbeeld een dimensie Paginanaam gebruikt waarbij de waarde van elk dimensie-item de naam van een pagina is (en niet een volledige URL), kunt u met deze optie een hyperlink opgeven die u wilt gebruiken als de koppeling voor het dimensie-item.

     Als u dynamische URL&#39;s wilt maken voor meerdere dimensie-items, kunt u de variabelen `$value` en `$breakdown` gebruiken in de aangepaste URL. Zie de onderstaande tabel voor meer informatie.

     Als u een aangepaste URL wilt maken, geeft u de volgende informatie op:

     | Veld | Beschrijving |
     |---------|----------|
     | [!UICONTROL **Aangepaste URL**] | Geef een aangepaste URL op die u voor de hyperlink wilt gebruiken. URL&#39;s moeten als volledig gekwalificeerde URL&#39;s worden ingevoerd. Bijvoorbeeld: https://www.example.com<p>De aangepaste URL die u maakt, kan statisch of dynamisch zijn:</p> <ul><li>**Statische URLs:** als u een hyperlink voor een individueel afmetingspunt creeert, zou statische URL voldoende kunnen zijn. <p>Neem het volgende voorbeeld: als u bijvoorbeeld een pagina-naamafmetingsitem hebt, kunt u een statische URL maken die gebruikers koppelt aan de specifieke webpagina die u aan de paginanaam wilt koppelen.</p><p>Veronderstel dat u hyperlinks voor een lijst van afmetingspunten wilt tot stand brengen, elk die met zijn respectieve definitie in de documentatie binnen een interne wiki- pagina verbinden.</p><p>U kunt dit bereiken door een statische URL te maken voor elk dimensie-item. Bijvoorbeeld:</p><p>https://wiki.internal.company_name/page_name#item_definition</p></li><li>**Dynamische URLs:** als u een hyperlink voor veelvoudige afmetingspunten of voor alle afmetingspunten in een afmetingskolom creeert, dan is dynamische URL waarschijnlijk praktischer. <p>Als u aangepaste URL&#39;s dynamisch wilt maken, neemt u variabelen in de URL op waarmee de URL dynamisch kan worden gewijzigd op basis van de waarde van de dimensie zelf of de waarde van de afbraakdimensie.</p><p>Wanneer u variabelen gebruikt, worden dimensieitems die tekens bevatten die niet geldig zijn in URL&#39;s (zoals spaties), URL-gecodeerd.</p><p>De volgende variabelen zijn beschikbaar: (**Nota**: Terwijl u deze variabelen in zelfde URL kunt gebruiken, is het waarschijnlijk gemeenschappelijker om hen afzonderlijk te gebruiken.)</p> <ul><li>**`$value`:** staat u toe om de waarde van het afmetingspunt in te voegen in URL die u specificeert. <p>Neem het volgende scenario als voorbeeld:</p><p>Stel dat u hyperlinks wilt maken voor alle pagina-naamatems in een vrije-vormtabel, waarbij de waarde van elk dimensie-item deel uitmaakt van de URL van een webpagina. In dit geval kunt u één aangepaste URL maken die dynamisch voor elk dimensie-item wordt aangepast. </p><p>U kunt dit bereiken door de variabele `$value` toe te voegen aan het einde van de aangepaste URL die u opgeeft. Bijvoorbeeld:</p> <p>https://company-name.com/browse/product#$value</p><p>Wanneer deze aangepaste URL wordt toegepast op de pagina-naamatems waarvan de waarden &quot;ProductY&quot; en &quot;ProductZ&quot; zijn, zien de gegenereerde hyperlinks er ongeveer als volgt uit: </p><p>https://company-name.com/browse/product#ProductY</p><p>en</p><p> https://company-name.com/browse/product#ProductZ </p><p>![ gebruikswaarden in hyperlinks ](assets/table-hyperlinks-vaule.png)</p><p>**Uiteinde**: Als u slechts de `$value` variabele in het gebied van Douane URL moest toevoegen, zou het het zelfde zijn als het selecteren van [!UICONTROL **Gebruik de waarde van de optie van het afmetingspunt**] wanneer het creëren van URL.</p></li><li>**`$breakdown`:** staat u toe om de waarde van het punt van de verdelingsdimensie in URL op te nemen die u specificeert. Dit staat u toe om een afmeting met een gebruikersvriendelijke naam in uw rapport (zoals een afmeting van de Naam van het Product) te gebruiken terwijl het creëren van hyperlink die op een afbraakafmeting wordt gebaseerd die minder gebruikersvriendelijk (zoals een identiteitskaart van het Product of de afmeting van URL van de Pagina) zou kunnen zijn.<p>Bij het verwijzen naar een uitsplitsingsdimensie is het het meest gebruikelijk dat er slechts één uitsplitsingspost voor een gegeven dimensie-item is. Indien er meerdere uitsplitsingsposten zijn voor een gegeven dimensie-item, wordt de waarde van de eerste uitsplitsingspost gebruikt in de URL. Als er geen uitsplitsingsitems worden weergegeven, is de URL ongeldig. Op de uitsplitsingsposten wordt dezelfde sorteervolgorde toegepast als op de tabel.</p><p>U specificeert de verdelingsafmeting op het [!UICONTROL **hieronder gebied van de Afmeting van de Onderverdeling**].</p> <p>Overweeg het voorbeeldscenario dat voor het [!UICONTROL **hieronder gebied van de Afmeting van de Onderverdeling**] wordt beschreven.</p></li></ul> |
     | [!UICONTROL **dimensie van de Onderbreking (facultatief)**] | Typ de naam van de afbraakdimensie die u wilt gebruiken en selecteer deze in de vervolgkeuzelijst. <p>Als u een afbraakdimensie op dit gebied selecteert, moet u het van verwijzingen voorzien door de `$breakdown` variabele in URL te gebruiken die u op het [!UICONTROL **Douane URL**] gebied specificeert.</p><p>Neem het volgende scenario als voorbeeld:</p><p>Veronderstel dat u hyperlinks voor alle de afmetingspunten van de Naam van het Product in een vrije lijst wilt tot stand brengen. Elk item van de productnaam bevat een uitsplitsing van een product-id-dimensie.</p></p>In dit geval, kunt u hyperlinks voor elke dimensie van de Naam van het Product tot stand brengen die gebruikers aan de productpagina door de waarde van de de verdelingsdimensie van identiteitskaart van het Product te gebruiken leidt. </p><p>U kunt dit verwezenlijken door de `$breakdown` variabele aan het eind van douane URL toe te voegen die u op het [!UICONTROL **gebied van de Douane URL**] specificeert. Bijvoorbeeld:</p><p>https://company-name.com/browse/product/$breakdown</p><p>Wanneer deze aangepaste URL wordt toegepast op de elementen van de productnaam met items voor de afbraakdimensie waarvan de waarden &quot;ProductY&quot; en &quot;ProductZ&quot; zijn, zien de gegenereerde hyperlinks er ongeveer als volgt uit:</p><p>https://company-name.com/browse/product/ProductY</p><p>en</p><p>https://company-name.com/browse/product/ProductZ</p><p>U zou dan de dimensie van identiteitskaart van het Product in het [!UICONTROL **Afmeting van de Onderbreking**] gebied selecteren </p><p>![ gebruiksuitbreidingen in hyperlinks ](assets/table-hyperlinks-breakdown.png)</p> |

1. Selecteer [!UICONTROL **creeer**].

   Gebruikers die de vrije-vormlijst bekijken zien de hyperlinked dimensiepunten. Wanneer gebruikers op een dimensie-item klikken, worden ze naar de pagina&#39;s met hyperlinks op een apart browsertabblad geleid.

   <!-- add screenshot of a table with hyperlinks.-->

1. [ sparen het project ](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md) om uw veranderingen te bewaren.

## Hyperlinks bewerken

U kunt hyperlinks bewerken die zijn gemaakt voor dimensies of dimensies-items in een vrije-vormtabel.

1. Voer een van de volgende handelingen uit in een vrije-vormtabel in Analysis Workspace:

   * **geef een hyperlink voor één enkel afmetingspunt uit:** klik het afmetingspunt binnen de lijst met de rechtermuisknop aan waar u hyperlink wilt uitgeven.

     ![ geef hyperlink voor één enkel afmetingspunt ](assets/hyperlink-single-edit.png) uit

   * **geeft hyperlinks voor alle afmetingspunten in een afmetingskolom uit:** klik de afmetingsnaam in de afmetingskolomkopbal met de rechtermuisknop aan.

     ![ geef hyperlink voor een afmeting uit ](assets/hyperlink-dimension-edit.png)

1. Selecteer [!UICONTROL **hyperlink**] van het met de rechtermuisknop aanklikken menu uitgeven.

   [!UICONTROL **geeft hyperlinks voor afmetingspunten**] dialoog uit wordt getoond.

1. Voor informatie over de configuratieopties om hyperlink uit te geven, zie Stap 3 in [ hyperlinks voor één of meerdere afmetingspunten ](#create-hyperlinks-for-one-or-more-dimension-items) sectie hierboven creëren, dan uitgezocht [!UICONTROL ****] toepassen wanneer u met uw updates wordt gebeëindigd.

1. [ sparen het project ](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md) om uw veranderingen te bewaren.

## Hyperlinks verwijderen

U kunt hyperlinks verwijderen die zijn gemaakt voor dimensie-items in een vrije-vormtabel.

>[!NOTE]
>
>Als u in een vrije-vormlijst een dimensie verwijdert die hyperlinks bevat, blijven de hyperlinks niet behouden als u dezelfde dimensie weer aan de vrije-vormtabel toevoegt.

Hyperlinks verwijderen uit dimensieitems:

1. Voer een van de volgende handelingen uit in een vrije-vormtabel in Analysis Workspace:

   * **verwijder een hyperlink uit één enkel afmetingspunt:** klik het afmetingspunt binnen de lijst met de rechtermuisknop aan waar u de hyperlink wilt verwijderen.

     ![ verwijder hyperlink uit één enkel afmetingspunt ](assets/hyperlink-single-remove.png)

   * **verwijder hyperlinks uit alle afmetingspunten in een afmetingskolom:** klik de afmetingsnaam in de afmetingskolomkopbal met de rechtermuisknop aan.

     ![ verwijder hyperlink uit een afmeting ](assets/hyperlink-dimension-remove.png)

1. Selecteer [!UICONTROL **verwijder hyperlink**] uit het met de rechtermuisknop aanklikken menu.

   De hyperlink wordt verwijderd uit het item met één dimensie (als u één dimensie-item hebt geselecteerd) of uit alle dimensie-items (als u de naam van de dimensie hebt geselecteerd in de kolomkop met dimensie).

1. [ sparen het project ](/help/analyze/analysis-workspace/build-workspace-project/save-projects.md) om uw veranderingen te bewaren.
