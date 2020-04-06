---
title: Module integreren
description: Met de module Integrate kunnen Adobe-partners hun inspanningen voor gegevensverzameling integreren met uw organisatie.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Module integreren

Met de module Integrate kunnen Adobe-partners hun inspanningen voor gegevensverzameling integreren met uw organisatie. Deze integratie biedt de mogelijkheid voor een gegevensverbinding in twee richtingen. Doorgaans wordt het gebruik van de module Integrate aangestuurd door een Adobe-partner.

>[!NOTE] Door partnergegevens in uw implementatie aan te vragen, kan de laadtijd tussen de pagina en de gegevens die naar Adobe-servers voor gegevensverzameling worden verzonden toenemen. Als een bezoeker een nieuwe pagina laadt voordat gegevens worden verzonden, wordt die pagina niet opgenomen.

## Workflow voor geïntegreerde module

1. Een bezoeker van uw site laadt een pagina die een `get` aanvraag voor partnergegevens initieert.
2. De Adobe-partner ontvangt de `get` aanvraag en verpakt de juiste variabelen in een JSON-object. Het JSON-object wordt geretourneerd.
3. Uw site ontvangt het JSON-object en roept `setVars` op de informatie in het JSON-object toe te wijzen aan Adobe Analytics-variabelen
4. Er wordt een verzoek om een afbeelding verzonden naar Adobe-gegevensverzamelingsservers.

## Integrate Module-implementatie

Een organisatie die met een partner van Adobe werkt kan deze stappen gebruiken met succes beginnen gebruikend de Module van de Integratie.

### Code integrale module verkrijgen

Voor het verkrijgen van modulecode moet een gebruiker toegang hebben tot productbeheer of tot een productprofiel dat toegang heeft tot Codebeheer. De methode voor het verkrijgen van modulecode is hetzelfde voor alle implementatiemethoden, inclusief het starten van het Adobe Experience Platform.

1. Meld u met uw Adobe-id aan bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) .
1. Klik op het pictogram van 9 vierkante pixels rechtsboven en klik vervolgens op het gekleurde Analytics-logo.
1. Klik in de bovenste navigatie op [!UICONTROL Admin] > [!UICONTROL Code Manager].
1. Download de nieuwste JavaScript AppMeasurement-bibliotheek.
1. Als het bestand is gedownload, decomprimeert u het bestand en zoekt u het `AppMeasurement_Module_Integrate.js`bestand.

### Plaats de module Integreren in uw implementatie

Voor de implementatie van de integrate-module op uw site hebt u toegang nodig tot Adobe Experience Platform Launch. Als u een oudere JavaScript-implementatie gebruikt, hebt u toegang tot de broncode van de website van uw organisatie nodig.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id.
2. Klik op de eigenschap Starten die u wilt bewerken.
3. Klik op het tabblad Extensies en klik vervolgens op Configureren onder Adobe Analytics.
4. Open de accordeon &#39;Tracker configureren met aangepaste code&#39; en klik op &#39;&lt;/> Editor openen&#39;.
5. Plak de code van de Module van de Integratie in het code modale venster. Klik op Opslaan als u klaar bent.

## Modulemethoden integreren

Zodra de Integrate Module is uitgevoerd, gebruik deze methodes om het te vormen om gegevens van de gewenste partner van Adobe te verzenden en te ontvangen.

### toevoegen

De `add` methode concretiseert een partnervoorwerp, dat als tussenopslag van veranderlijke gegevens wanneer het delen van gegevens tussen partnersystemen en uw implementatie dient. Deze methode is vereist voor alle integraties. Een afzonderlijk partnervoorwerp moet voor elke unieke partner worden gebruikt als de veelvoudige partners in één enkele implementatie worden gebruikt.

```JavaScript
s.Integrate.add("<partner_name>");
```

Uw organisatie werkt doorgaans samen met een Adobe-partner om de waarde voor de partnernaam te bepalen.

### baken

De `beacon` methode maakt een afbeeldingsaanvraag en wijst deze naar de opgegeven URL. Deze verzoeken om afbeeldingen verschillen van standaardverzoeken om afbeeldingen. De bakenmethode verzendt typisch gegevens naar de partner van Adobe in plaats van de servers van de gegevensinzameling van Adobe.

```JavaScript
p.beacon("<partner_url>/track?qs1=value1&qs2=value2");
```

Uw organisatie werkt doorgaans samen met de Adobe-partner om de waarde voor de partnernaam te bepalen. De koorden van de vraag inbegrepen in URL zijn facultatief, en afhankelijk van partner. De module Integeren bevat automatisch een queryreeks met een willekeurig getal om te voorkomen dat de browser in cache wordt geplaatst.

### vertragen

Adobe werkt intern met teams om deze methode te documenteren.

### get

De `get` methode laat een cliënt partnervariabelen invoeren en hen opslaan in het partnervoorwerp. Zodra het gegeven in het partnervoorwerp is, kan het aan de variabelen van Analytics worden toegewezen en in een beeldverzoek worden verzonden. Deze methode roept een URL aan, die naar een JSON-object verwijst dat de gewenste gegevens bevat.

```JavaScript
s.Integrate.<partner_name>.get("<url_to_json_object>?pid=value1&pid2=value2");
```

* **Naam partner:** Uw organisatie werkt doorgaans samen met de Adobe-partner om de waarde voor de partnernaam te bepalen.
* **URL naar JSON-object:** De URL naar een JSON-object dat de partnervariabelen bevat die in een afbeeldingsaanvraag moeten worden opgenomen.
* **Parameter(s) voor queryreeks:** De rekeningsinformatie van de partner die uw organisatie in het systeem van de partner identificeert. De Adobe-partner gebruikt deze gegevens om uw gegevensset te identificeren.

De module Integeren voegt automatisch meer querytekenreeksen toe aan de URL. Een var vraagkoord specificeert de naam van het voorwerp JSON de module terug van de partner verwacht. Er wordt ook een willekeurig getal toegevoegd om te voorkomen dat de browser in cache wordt geplaatst.

### klaar

Adobe werkt intern met teams om deze methode te documenteren.

### useVars

De `useVars` methode laat de cliënt veranderlijke waarden met een partner van Adobe delen.

```JavaScript
s.Integrate.<partner_name>.useVars = function (s,p) {
    p.<partner_var1> = s.eVar1;
    p.<partner_var2> = s.eVar2;
}
```

Uw organisatie werkt typisch met een partner van Adobe om de waarden voor partnernaam en de variabelen te bepalen die de partner gebruikt.

### setVars

De `setVars` methode laat de cliënt variabelen bevolken Analytics gebruikend partnergegevens die worden teruggewonnen. De gegevens van de partner kunnen het resultaat van een `get` methode, een statische taak, of een ander mechanisme zijn dat het partnervoorwerp met gegevens bevolkt.

```JavaScript
s.Integrate.<partner_name>.setVars = function (s,p) {
    s.eVar1 = p.<partner_var1>;
    s.eVar2 = p.<partner_var2>;
}
```

Uw organisatie werkt typisch met een partner van Adobe om de waarden voor partnernaam en de variabelen te bepalen die de partner gebruikt.

### script

Met de `script` methode kan een Adobe-partner extra JavaScript aanroepen vanaf de partnersite als aan bepaalde voorwaarden wordt voldaan (bijvoorbeeld als de campagnevariabele is ingesteld).

```JavaScript
p.script("<partner_url>/script?qs1=value1&qs2=value2");
```

Uw organisatie werkt doorgaans samen met de Adobe-partner om de waarde voor de partnernaam te bepalen. De koorden van de vraag inbegrepen in URL zijn facultatief, en afhankelijk van partner. De module Integeren bevat automatisch een queryreeks met een willekeurig getal om te voorkomen dat de browser in cache wordt geplaatst.
