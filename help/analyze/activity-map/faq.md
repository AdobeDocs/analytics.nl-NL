---
title: Veelgestelde vragen over Activity Map
description: Veelgestelde vragen over Activity Map.
feature: Activity Map
role: User, Admin
exl-id: 6b2767cb-6c2c-4bf3-b9a9-a23418624650
source-git-commit: 64964972410911c2bea1460039def39b7c6dfa38
workflow-type: tm+mt
source-wordcount: '1036'
ht-degree: 0%

---

# Veelgestelde vragen over Activity Map

Veelgestelde vragen over Activity Map.

+++Hoe geef ik toestemmingen aan Activity Map?

De toestemmingen om Activity Map en zijn bijbehorende afmetingen te gebruiken worden behandeld in [ Adobe Admin Console ](/help/admin/admin-console/home.md).

De [ toestemmingspunten ](/help/admin/admin-console/permissions/product-profile.md) die voor Activity Map worden vereist omvatten:

* **[!UICONTROL Analytics Tools]** > **[!UICONTROL Activity Map]**
* **[!UICONTROL Analytics Tools]** > **[!UICONTROL Segment Publishing]**
* **[!UICONTROL Dimensions]** > **[!UICONTROL Activity Map Scroll Reach]**
* **[!UICONTROL Dimensions]** > **[!UICONTROL Activity Map Link By Region]**
* **[!UICONTROL Dimensions]** > **[!UICONTROL Activity Map Region]**
* **[!UICONTROL Dimensions]** > **[!UICONTROL Activity Map Link]**
* **[!UICONTROL Dimensions]** > **[!UICONTROL Activity Map Page]**

Zie {de profieltoestemmingen van 0} Product voor Hulpmiddelen van Analytics ](/help/admin/admin-console/permissions/analytics-tools.md) voor meer informatie.[

+++

+++Hebben alle klanten van Analytics toegang tot Activity Map?

Organisaties met een contract voor Adobe Analytics Standard, Premium en Ultimate hebben toegang tot Activity Map. Deze contracttypes vertegenwoordigen de meerderheid van klanten van Adobe Analytics.

+++

+++Hoe biedt Activity Map ondersteuning voor toepassingen van één pagina (SPA)?

Om de paar seconden scant de Activity Map de webpagina op zoek naar wijzigingen. Activity Map zoekt naar nieuwe inhoud op de pagina zonder dat opnieuw hoeft te worden geladen, maar deze nieuwe inhoud wordt altijd toegewezen aan de waarde van de eerste pagina-afmetingen.

* Activity Map controleert of de zichtbaarheid van koppelingen die het kent, is gewijzigd. Als een wijziging in de zichtbaarheid wordt gevonden, wordt de kolom Aanwezigheid van koppelingen in de paginatabel voor die koppeling bijgewerkt met [!UICONTROL Displayed] of [!UICONTROL Hidden] .

* Wanneer de gebruikersinteractie tot nieuwe inhoud leidt, worden om het even welke nieuwe elementen die AppMeasurement als verbinding bepaalt toegevoegd aan de [!UICONTROL Links On Page] lijst. De Activity Map verzendt een nieuw gegevensverzoek dat deze nieuwe verbindingen omvat. De nieuwe koppelingen worden weergegeven in de tabel [!UICONTROL Links On Page] wanneer de gegevensaanvraag wordt geretourneerd.

+++

+++Verstrekt de Activity Map gegevens over verbindingen die worden bekeken maar niet geklikt?

Nee, Adobe houdt niet automatisch koppelingen bij die alleen zijn weergegeven.

+++

+++Welke browsers en versies worden door de Activity Map ondersteund?

Activity Map ondersteunt de nieuwste versie van de meeste moderne browsers.

+++

+++Verhoogt de Activity Map servervraag?

Activity Map verzendt geen servervraag door zich. In plaats daarvan worden Activity Map-contextgegevensvariabelen opgenomen in de paginaweergaveaanroepen voor Analytics op de volgende pagina. Nochtans, verzenden sommige vorige versies van Activity Map op het Web SDK een afzonderlijke vraag naar Activity Map gegevens. Als u op de recentste versie van het Web SDK bent, worden de gegevens van de Activity Map samengevoegd met de volgende gebeurtenis.

+++

+++Waarom ontbreken sommige rangtelnummers in de overlay?

Sommige koppelingen, zoals koppelingen in menu&#39;s, worden niet op de pagina weergegeven. Hierdoor worden de bijbehorende koppelingsoverlays niet weergegeven. Rank wordt berekend voor alle koppelingen op de pagina, inclusief verborgen koppelingen.

+++

+++Hoe wordt de verbindingsrangorde bepaald in het Alle Rapport van Verbindingen?

* **op Verloop en Bubble wijze**: De metrische kolom bepaalt rang. Voor verbindingen met de zelfde metrische waarde, is de rang verder gebaseerd op verbinding ID alfabetische orde.
* **op Gainer &amp; de wijze van de Gebruikers**: Het percentage bereikte kolom bepaalt rang. Voor koppelingen met dezelfde versterking is de rangorde verder gebaseerd op de alfabetische volgorde van de koppelings-id.

+++

+++Hoe werkt de Activity Map met pagina&#39;s die veelvoudige rapportreeksen gebruiken?

Standaard gebruikt Activity Map de rapportsuite die is gekoppeld aan de eerste tag op de pagina. U kunt een andere rapportsuite selecteren via het tabblad **[!UICONTROL Activity Map Settings]** > **[!UICONTROL Others]** .

+++

+++Hoe lang wordt de Activity Map gescand op Adobe Analytics op de pagina?

Activiteitenoverzicht scant tot 20 seconden na een gebeurtenis van het voltooien van een pagina op de aanwezigheid van Adobe Analytics.

+++

+++Hoe verwerkt Activity Map dynamische inhoud?

De Activity Map controleert om de 2 seconden om te zien of heeft het veranderingen in de staat van de Web-pagina zoals gevonden:

* HTML-inhoud die zichtbaar is geworden
* Verborgen HTML-inhoud
* Nieuwe HTML-inhoud die is geïnjecteerd

Als inhoud wordt verborgen of weergegeven, verandert de extensie automatisch de gewijzigde staat van de koppelingen (en dus de overlays) van verborgen in weergegeven of verborgen. Als nieuwe inhoud wordt geïnjecteerd, haalt de toepassing de bijbehorende koppelingen op, worden er analysegegevens voor opgehaald en worden er overlays voor deze koppelingen toegevoegd.

+++

+++Welke metrisch is het rapport van de Stroom van de Pagina op wordt gebaseerd?

Alle weergegeven gegevens zijn gebaseerd op paginaweergaven.

+++

+++Kan ik gegevens van de Activity Map door gegevensvoer uitvoeren?

Ja. De [ voederkolommen van Gegevens ](/help/export/analytics-data-feed/c-df-contents/datafeeds-reference.md) die de Activity Map gebruikt zijn:

* Koppeling naar Activity Map: `clickmaplink`
* Pagina Activity Mappen: `clickmappage`
* Gebied Activity Map: `clickmapregion`
* Koppeling naar regio Activity Mappen: `clickmaplinkbyregion`

+++

+++Werken de segmenten in de live modus?

Nee, segmenten werken niet in de live modus.

+++

+++Is de Activity Map compatibel met virtuele rapportsuites?

Ja. Vanwege beperkingen van de virtuele rapportsuite is de Live-modus van Activity Map echter niet compatibel met virtuele rapportsuites.

+++

+++Hoe kan ik Activity Map onbruikbaar maken?

De methode om Activity Map onbruikbaar te maken hangt van uw implementatietype af:

* **uitbreiding van SDK van het Web**: In de montages van de uitbreidingsconfiguratie, uncheck de dozen **[!UICONTROL Collect internal link clicks]**, **[!UICONTROL Collect external link clicks]**, en **[!UICONTROL Collect download link clicks]**.
* **de bibliotheek van SDK van het Web JavaScript**: Reeks [`clickCollectionEnabled` ](https://experienceleague.adobe.com/en/docs/experience-platform/web-sdk/commands/configure/clickcollectionenabled) aan `false`.
* **uitbreiding Analytics**: In de montages van de uitbreidingsconfiguratie, uncheck de geëtiketteerde doos **[!UICONTROL Use Activity Map]**.
* **AppMeasurement**: Verwijder of commentaar uit de module van de Activity Map binnen `AppMeasurement.js`, of beschrijf de vraag van de modulefunctie met een leeg lichaam:

  ```js
  function AppMeasurement_Module_ActivityMap() {}
  ```

+++

+++Wat zijn de systeemvereisten om de bekleding van de Activity Map te gebruiken?

U kunt de nieuwste versie van Chrome, Edge of Firefox gebruiken met de extensie Activity Map.

+++

+++Wat moet ik overwegen wanneer het gebruiken van Activity Map voor persoonlijk identificeerbare informatie?

Overweeg de volgende scenario&#39;s waar persoonlijk identificeerbare gegevens kunnen worden verzameld gebruikend Activity Map:

* **E-mailverbindingen**: Als een e-mailadres kan worden geklikt om de de postcliënt van de gebruiker te openen, kan de Activity Map het e-mailadres verzamelen dat werd geklikt.
* **de verbindingen van identiteitskaart van de Gebruiker**: Nadat een bezoeker het programma opent, kan de Activity Map om het even welke verbindingen registreren die de gebruiker van de bezoeker identiteitskaart bevatten.
* **Gevoelige informatieverbindingen**: Voor financiële instellingen, kan de gevoelige informatie zoals rekeningsaantal worden gevolgd als zij een verbinding zijn en de bezoekers hen klikken.
* **Verbindingen die persoonlijke informatie** bevatten: Voor gezondheidszorgwebsites, kunnen de verbindingen persoonlijke informatie bevatten. Als een bezoeker op deze koppelingen klikt, wordt de koppelingstekst door de Activity Map verzameld.

+++

+++Welke gegevens volgt de Activity Map door gebrek?

Activity Map volgt de volgende elementen:

* Een tag `<a>` of `<area>` met een eigenschap `href` . Koppelingen naar ankerlabels (`#`) worden niet standaard bijgehouden.
* Een `onclick` -kenmerk dat een `s_objectID` -variabele instelt
* Een `<input>` -tag of `submit` -knop met een waarde of onderliggende tekst
* Een `<input>` -tag met type `image` en een `src` -eigenschap
* Een `<button>` -tag zonder het kenmerk `type="button"` . Als u `<button>` -tags wilt bijhouden, kunt u in plaats daarvan ook attributen zoals `role="button"` of `submit="button"` gebruiken.

+++

+++Wat zijn sommige voorbeelden van verbindingen die de Activity Map automatisch volgt?

Hieronder volgen enkele voorbeelden waarbij de Activity Map over alle vereiste informatie beschikt om een koppeling bij te houden.

```html
<a href="home.html">Home</a>

<input type="submit" value="Submit"/>

<input type="image" src="submit-button.png"/>

<p onclick="var s_objectID='Market rates';">
  <span class="title">Current Market Rates</span>
  <span class="subtitle">1.45 USD</span>
</p>

<div onclick="s.tl(true,'o','Chat button')">
  <span class="title">Chat with an agent now</span>
  <span class="subtitle">Current wait: 0 minutes</span>
</div>
```

+++

+++Wat zijn sommige voorbeelden van verbindingen die de Activity Map NIET automatisch volgt?

Hieronder volgen enkele voorbeelden waarbij Activity Map klikken niet bijhoudt.

```html
<!-- Anchor tag does not have a valid href -->
<a name="innerAnchor">Section header</a>

<!-- Neither s_objectID or tl() method present -->
<p onclick="showPanel('stock price')">
  <span class="title">Current company stock price</span>
  <span class="subtitle">987.65 USD</span>
</p>

<!-- Neither s_objectID or tl() method present -->
<input type="radio" onclick="changeState(this)" name="group1" value="A"/>
<input type="radio" onclick="changeState(this)" name="group1" value="B"/>
<input type="radio" onclick="changeState(this)" name="group1" value="C"/>

<!-- src property missing on a form input element -->
<input type="image"/>
```

+++
