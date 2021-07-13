---
description: Veelgestelde vragen over het volgen van koppelingen in Activity Map.
title: Veelgestelde vragen over link tracking
uuid: 10172073-b98b-4950-8397-67a18b37b3b4
feature: Activity Map
role: User, Admin
exl-id: b6ccdf91-98ce-413f-842d-c5423598ed49
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 1%

---

# Veelgestelde vragen over link tracking

Veelgestelde vragen over het volgen van koppelingen in Activity Map.

>[!CAUTION]
>
>Als u het bijhouden van Activity Mappen inschakelt, **verzamelt u mogelijk PII-gegevens (Persoonlijk identificeerbare gegevens).** Deze gegevens kunnen op zichzelf of met andere informatie worden gebruikt om één persoon te identificeren, contact op te nemen of te vinden, of om een persoon in context te identificeren.

Hier zijn enkele bekende gevallen waarin PII-gegevens kunnen worden verzameld met behulp van Activity Map bijhouden:

* `Mailto` koppelingen. Een mailto-koppeling is een type HTML-koppeling waarmee de standaardmailclient op de computer wordt geactiveerd voor het verzenden van een e-mail.
* `User ID` koppelingen die worden weergegeven in de kop- of voettekst van een website nadat de gebruiker zich heeft aangemeld.
* Voor financiële instellingen kan het rekeningnummer als link worden weergegeven. Als u erop klikt, wordt de tekst van de koppeling verzameld.
* Op websites voor gezondheidszorg kunnen ook PII-gegevens als koppelingen worden weergegeven. Als u op deze koppelingen klikt, wordt de tekst van de koppeling verzameld en worden er dus PII-gegevens verzameld.

## Wanneer vindt het bijhouden van koppelingen plaats?

Koppeling naar Activity Map en regio-identificatie treedt op wanneer gebruikers op een pagina klikken.

## Wat wordt standaard bijgehouden?

Als een klikgebeurtenis op een element voorkomt, moet het element sommige controles overgaan om te bepalen als AppMeasurement het als verbinding zal behandelen. Dit zijn de controles:

* Is dit een `A` of `AREA` markering met een `href` bezit?
* Is er een `onclick` attribuut dat een `s_objectID` variabele plaatst?
* Is dit een `INPUT` markering of `SUBMIT` knoop met een waarde of kindtekst?
* Is dit een `INPUT` markering met type `IMAGE` en een `src` bezit?
* Is dit een `BUTTON`?

Als het antwoord op om het even welke bovenstaande vragen ja is, dan wordt het element behandeld als verbinding en zal worden gevolgd.

>[!IMPORTANT]
>
>Knoplabels met het kenmerktype=&quot;button&quot; worden door AppMeasurement niet als koppelingen beschouwd. U kunt in plaats hiervan type=&quot;button&quot; op de knoptags verwijderen en rol=&quot;button&quot; of submit=&quot;button&quot; toevoegen.

>[!IMPORTANT]
>
>Een ankertag met een &quot;href&quot; die begint met &quot;#&quot; wordt door AppMeasurement beschouwd als een interne doellocatie, niet als een koppeling (omdat u de pagina niet verlaat). Standaard houdt Activity Map deze interne doellocaties niet bij. Er worden alleen koppelingen bijgehouden waarmee de gebruiker naar een nieuwe pagina navigeert.

## Hoe houdt Activity Map andere visuele HTML-elementen bij?

a. Via de functie `s.tl()`.

Als de klik via een `s.tl()` aanroeping voorkwam, dan zal de Activity Map ook deze klikgebeurtenis ontvangen en zal bepalen als een `linkName` koordvariabele werd gevonden. Tijdens `s.tl()` uitvoering, zal dat linkName als identiteitskaart van de Verbinding van de Activity Map worden geplaatst. Het aangeklikte element dat de `s.tl()` vraag voortkwam zal worden gebruikt om het gebied te bepalen. Voorbeeld:

```
<img onclick="s.tl(true,'o','abc')" src="someimageurl.png"/>
```

b. Via de variabele `s_objectID`. Voorbeeld:

    &quot;
    
    &lt;a>&lt;img>&lt;/a>
    
    &lt;a>Tekst hier&lt;/a>
    
    
    &lt;a> koppelen&lt;/a>&quot;

>[!IMPORTANT]
>
>Een volgpuntkomma (;) is vereist wanneer u `s_objectID` in Activity Map gebruikt.

## Kunt u mij enkele voorbeelden geven van koppelingen die worden bijgehouden?

### Voorbeeld 1

```
  <a hef="/home?lang=en>Home</a>
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

1. Reden: Ankertag heeft geen geldige `href`:
   `<a name="innerAnchor">Section header</a>`

1. Reden: Noch `s_ObjectID` noch `s.tl()` aanwezig:

   ```
   <p onclick="showPanel('market rates')">
     <span class="title">Current Market Rates</span>
     <span class="subtitle">1.45USD</span>
   </p>
   ```

1. Reden: Noch `s_ObjectID` noch `s.tl()` aanwezig:

   ``` 
   <input type="radio" onclick="changeState(this)" name="group1" value="A"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="B"/>
   <input type="radio" onclick="changeState(this)" name="group1" value="C"/>
   
   ```  
   
1. Reden: In de eigenschap &quot;src&quot; ontbreekt een formulierinvoerelement:

   `<input type="image"/>`
