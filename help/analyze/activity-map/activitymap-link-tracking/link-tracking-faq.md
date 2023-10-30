---
description: Veelgestelde vragen over het volgen van koppelingen in Activity Map.
title: Veelgestelde vragen over link tracking
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: User, Admin
exl-id: b6ccdf91-98ce-413f-842d-c5423598ed49
source-git-commit: a0b8f61c3728c5867640ce20768614c8d79ca657
workflow-type: tm+mt
source-wordcount: '516'
ht-degree: 1%

---

# Veelgestelde vragen over link tracking

Veelgestelde vragen over het volgen van koppelingen in Activity Map.

>[!CAUTION]
>
>Door Activity Map bijhouden in te schakelen, **u kunt persoonlijk identificeerbare gegevens (PII) verzamelen.** Deze gegevens kunnen op zichzelf of met andere informatie worden gebruikt om één persoon te identificeren, contact op te nemen of te vinden, of om een persoon in context te identificeren.

Hier zijn enkele bekende gevallen waarin PII-gegevens kunnen worden verzameld met behulp van Activity Map bijhouden:

* `Mailto` koppelingen. Een mailto-koppeling is een type HTML-koppeling waarmee de standaardmailclient op de computer wordt geactiveerd voor het verzenden van een e-mail.
* `User ID` koppelingen die worden weergegeven in de kop- of voettekst van een website nadat de gebruiker zich heeft aangemeld.
* Voor financiële instellingen kan het rekeningnummer als een link worden weergegeven. Als u erop klikt, wordt de tekst van de koppeling verzameld.
* Op websites voor gezondheidszorg kunnen ook PII-gegevens als koppelingen worden weergegeven. Als u op deze koppelingen klikt, wordt de tekst van de koppeling verzameld en worden er dus PII-gegevens verzameld.

## Wanneer vindt het bijhouden van koppelingen plaats?

Koppeling naar Activity Map en regio-identificatie treedt op wanneer gebruikers op een pagina klikken.

## Wat wordt standaard bijgehouden?

Als een klikgebeurtenis op een element voorkomt, moet het element sommige controles overgaan om te bepalen als het AppMeasurement het als verbinding zal behandelen. Dit zijn de controles:

* Is dit `A` of `AREA` tag met een `href` eigenschap?
* Is er een `onclick` kenmerk dat een `s_objectID` variabele?
* Is dit `INPUT` tag of `SUBMIT` knop met een waarde of onderliggende tekst?
* Is dit `INPUT` tag met type `IMAGE` en `src` eigenschap?
* Is dit `BUTTON`?

Als het antwoord op om het even welke bovenstaande vragen ja is, dan wordt het element behandeld als verbinding en zal worden gevolgd.

>[!IMPORTANT]
>
>Knoplabels met het kenmerktype=&quot;button&quot; worden door AppMeasurement niet als koppelingen beschouwd. U kunt in plaats hiervan type=&quot;button&quot; op de knoptags verwijderen en rol=&quot;button&quot; of submit=&quot;button&quot; toevoegen.

>[!IMPORTANT]
>
>Een ankertag met een &quot;href&quot; die begint met &quot;#&quot; wordt per AppMeasurement beschouwd als een interne doellocatie, niet als een koppeling (omdat u de pagina niet verlaat). Standaard houdt Activity Map deze interne doellocaties niet bij. Er worden alleen koppelingen bijgehouden waarmee de gebruiker naar een nieuwe pagina navigeert.

## Hoe houdt Activity Map andere visuele HTML-elementen bij?

a. Via de `s.tl()` functie.

Als de klik heeft plaatsgevonden via een `s.tl()` de aanroeping, dan zal de Activity Map deze klikgebeurtenis ook ontvangen en zal bepalen als `linkName` tekenreeksvariabele gevonden. Tijdens `s.tl()` uitvoering, zal dat linkName als identiteitskaart van de Verbinding van de Activity Map worden geplaatst. Het aangeklikte element dat voortkwam uit `s.tl()` er zal een oproep worden gedaan om de regio te bepalen . Voorbeeld:

```
<img onclick="s.tl(true,'o','abc')" src="someimageurl.png"/>
```

b. Via de `s_objectID` variabele. Voorbeeld:

    &quot; 
    
    &lt;img onclick=&quot;s_objectID=&amp;#39;abc&amp;#39;;&quot; src=&quot;someimageurl.png&quot; />
    &lt;a href=&quot;some-url.html&quot; onclick=&quot;s_objectID=&amp;#39;abc&amp;#39;;&quot;>
    Tekst hier koppelen
    &lt;/a>
    
    &quot;

>[!IMPORTANT]
>
>Een volgpuntkomma (;) is vereist bij gebruik `s_objectID` in Activity Map.

## Kunt u mij enkele voorbeelden geven van koppelingen die worden bijgehouden?

### Voorbeeld 1

```
  <a href="/home>Home</a>
```

### Voorbeeld 2

```
 <input type="submit" value="Submit"/>
```

### Voorbeeld 3

```
  <input type="image" src="submit-button.png"/>
```

### Voorbeeld 4

```
    <p onclick="var s_objectID='custom link id';">
      <span class="title">Current Market Rates</span>
      <span class="subtitle">1.45USD</span>
    </p>
```

### Voorbeeld 5

```
    <div onclick="s.tl(true,'o','custom link id')">
      <span class="title">Current Market Rates</span>
      <span class="subtitle">1.45USD</span>
    </div>
```

## Kunt u mij enkele voorbeelden geven van koppelingen die NIET worden bijgehouden?

1. Reden: ankertag heeft geen geldige waarde `href`:
   `<a name="innerAnchor">Section header</a>`

1. Reden: Geen van beide `s_ObjectID` noch `s.tl()` aanwezig:

   ```
   <p onclick="showPanel('market rates')">
     <span class="title">Current Market Rates</span>
     <span class="subtitle">1.45USD</span>
   </p>
   ```

1. Reden: Geen van beide `s_ObjectID` noch `s.tl()` aanwezig:

   ``` 
   <input type="radio" onclick="changeState(this)" name="group1" value="A"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="B"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="C"/>
   
   ```  
   
1. Reden: er ontbreekt een formulierinvoerelement in de eigenschap &quot;src&quot;:

   `<input type="image"/>`

