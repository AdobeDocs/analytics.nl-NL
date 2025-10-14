---
title: Module integreren
description: Met de module Integrate kunnen Adobe-partners hun inspanningen op het gebied van gegevensverzameling integreren met uw organisatie.
feature: Appmeasurement Implementation
exl-id: 378ba77b-be81-49af-8f36-81c65bd01a53
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '878'
ht-degree: 2%

---

# Module integreren

Met de module Integrate kunnen Adobe-partners hun inspanningen op het gebied van gegevensverzameling integreren met uw organisatie. Deze integratie biedt de mogelijkheid voor een gegevensverbinding in twee richtingen. Gewoonlijk wordt het gebruik van de integrate Module aangestuurd door een Adobe-partner.

>[!NOTE]
>
>Het aanvragen van partnergegevens in uw implementatie kan vertragingen tussen paginading en gegevens verhogen die naar de servers van de de gegevensinzameling van Adobe worden verzonden. Als een bezoeker een nieuwe pagina laadt voordat gegevens worden verzonden, wordt die pagina niet opgenomen.

## Workflow voor geïntegreerde module

1. Een bezoeker van uw site laadt een pagina die een `get` -aanvraag voor partnergegevens initieert.
2. De Adobe-partner ontvangt de aanvraag `get` en verpakt de juiste variabelen in een JSON-object. Het JSON-object wordt geretourneerd.
3. Uw site ontvangt het JSON-object en roept `setVars` aan om de informatie in het JSON-object toe te wijzen aan Adobe Analytics-variabelen
4. Er wordt een verzoek om een image verzonden naar Adobe-gegevensverzamelingsservers.

## Integrate Module-implementatie

Een organisatie die met een partner van Adobe werkt kan deze stappen gebruiken met succes beginnen gebruikend de Integrate Module.

### Code integrale module verkrijgen

Voor het verkrijgen van modulecode moet een gebruiker toegang hebben tot productbeheer of tot een productprofiel dat toegang heeft tot Codebeheer. De methode om modulecode te verkrijgen is het zelfde voor alle implementatiemethodes, met inbegrip van markeringen in Adobe Experience Platform.

1. Meld u met uw Adobe ID aan bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com).
1. Klik op het pictogram met 9 vierkantjes rechtsboven in het venster en klik vervolgens op het gekleurde Analytics-logo.
1. Klik in de bovenste navigatie op **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL Code manager]** .
1. Download de nieuwste JavaScript AppMeasurement-bibliotheek.
1. Nadat het bestand is gedownload, decomprimeert u het bestand en zoekt u `AppMeasurement_Module_Integrate.js` .

### Plaats de module Integreren in uw implementatie

Voor de implementatie van de integrate-module op uw site hebt u toegang tot de Adobe Experience Platform-gegevensverzameling nodig. Als u een verouderde JavaScript-implementatie gebruikt, hebt u toegang tot de broncode van uw website nodig.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
1. Klik op de eigenschap Tag die u wilt bewerken.
1. Klik op het tabblad Extensies en klik vervolgens op Configureren onder Adobe Analytics.
1. Open de accordeon &#39;Tracker configureren met aangepaste code&#39; en klik op &#39;&lt;/> Editor openen&#39;.
1. Plak de code van de Module van de Integratie in het code modale venster. Klik op Opslaan als u klaar bent.

## Modulemethoden integreren

Zodra de Integrate Module is uitgevoerd, gebruik deze methodes om het te vormen om gegevens van de gewenste partner van Adobe te verzenden en te ontvangen.

### toevoegen

De methode `add` instantieert een partnervoorwerp, dat als tussenopslag van veranderlijke gegevens wanneer het delen van gegevens tussen partnersystemen en uw implementatie dient. Deze methode is vereist voor alle integraties. Een afzonderlijk partnervoorwerp moet voor elke unieke partner worden gebruikt als de veelvoudige partners in één enkele implementatie worden gebruikt.

```JavaScript
s.Integrate.add("<partner_name>");
```

Uw organisatie werkt typisch met een partner van Adobe om de waarde voor partnernaam te bepalen.

### baken

De methode `beacon` maakt een afbeeldingsaanvraag en wijst deze naar de opgegeven URL. Deze verzoeken om afbeeldingen verschillen van standaardverzoeken om afbeeldingen. De bakenmethode verzendt typisch gegevens naar de partner van Adobe in plaats van de servers van de gegevensinzameling van Adobe.

```JavaScript
p.beacon("<partner_url>/track?qs1=value1&qs2=value2");
```

Uw organisatie werkt typisch met de partner van Adobe om de waarde voor partnernaam te bepalen. De koorden van de vraag inbegrepen in URL zijn facultatief, en afhankelijk van partner. De module Integeren bevat automatisch een queryreeks met een willekeurig getal om te voorkomen dat de browser in cache wordt geplaatst.

### vertragen

Adobe werkt intern met teams om deze methode te documenteren.

### get

Met de methode `get` kan een client partnervariabelen importeren en opslaan in het partnerobject. Zodra het gegeven in het partnervoorwerp is, kan het aan de variabelen van Analytics worden toegewezen en in een beeldverzoek worden verzonden. Deze methode roept een URL aan, die naar een JSON-object verwijst dat de gewenste gegevens bevat.

```JavaScript
s.Integrate.<partner_name>.get("<url_to_json_object>?pid=value1&pid2=value2");
```

* **de naam van de Partner:** Uw organisatie werkt typisch met de partner van Adobe om de waarde voor partnernaam te bepalen.
* **URL aan voorwerp JSON:** URL aan een voorwerp JSON dat de partnervariabelen bevat om in een beeldverzoek op te nemen.
* **het koordparameter(s) van de Vraag:** de rekeningsinformatie van de Partner die uw organisatie in het systeem van de partner identificeert. De Adobe-partner gebruikt deze informatie om uw gegevensset te identificeren.

De module Integeren voegt automatisch meer querytekenreeksen toe aan de URL. Een var vraagkoord specificeert de naam van het voorwerp JSON de module terug van de partner verwacht. Er wordt ook een willekeurig getal toegevoegd om te voorkomen dat de browser in cache wordt geplaatst.

### klaar

Adobe werkt intern met teams om deze methode te documenteren.

### useVars

Met de methode `useVars` kan de client waarden van variabelen delen met een Adobe-partner.

```JavaScript
s.Integrate.<partner_name>.useVars = function (s,p) {
    p.<partner_var1> = s.eVar1;
    p.<partner_var2> = s.eVar2;
}
```

Uw organisatie werkt typisch met een partner van Adobe om de waarden voor partnernaam en de variabelen te bepalen die de partner gebruikt.

### setVars

Met de methode `setVars` kan de client analytische variabelen vullen met opgehaalde partnergegevens. De gegevens van de partner kunnen het resultaat van een `get` methode, een statische taak, of een ander mechanisme zijn dat het partnervoorwerp met gegevens bevolkt.

```JavaScript
s.Integrate.<partner_name>.setVars = function (s,p) {
    s.eVar1 = p.<partner_var1>;
    s.eVar2 = p.<partner_var2>;
}
```

Uw organisatie werkt typisch met een partner van Adobe om de waarden voor partnernaam en de variabelen te bepalen die de partner gebruikt.

### script

Met de methode `script` kan een Adobe-partner aanvullende JavaScript vanaf de partnersite aanroepen als aan bepaalde voorwaarden is voldaan (bijvoorbeeld als de campagnevariabele is ingesteld).

```JavaScript
p.script("<partner_url>/script?qs1=value1&qs2=value2");
```

Uw organisatie werkt typisch met de partner van Adobe om de waarde voor partnernaam te bepalen. De koorden van de vraag inbegrepen in URL zijn facultatief, en afhankelijk van partner. De module Integeren bevat automatisch een queryreeks met een willekeurig getal om te voorkomen dat de browser in cache wordt geplaatst.
