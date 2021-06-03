---
title: Analyses implementeren voor digitale assistenten
description: Adobe Analytics implementeren op digitale assistenten, zoals Amazon Alexa of Google Home.
exl-id: ebe29bc7-db34-4526-a3a5-43ed8704cfe9
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 0%

---

# Analyses implementeren voor digitale assistenten

Met de recente ontwikkelingen op het gebied van cloud computing, machinaal leren en de verwerking van natuurlijke talen maken digitale assistenten deel uit van het dagelijks leven. Consumenten beginnen met hun apparaten te praten en verwachten dat ze op een mensachtige manier begrijpen en reageren. Naarmate deze platforms meer ingang vinden, kunnen merken hun diensten op dezelfde realistische en levensechte manieren aan consumenten aanbieden. De consument kan bijvoorbeeld vragen stellen:

* &quot;Alexa, vraag mijn auto wanneer hij een olieverslag nodig heeft.&quot;
* &quot;Cortana, wat is het saldo van mijn betaalrekening?&quot;
* &quot;Siri, stuur John $20 voor het avondeten vanaf mijn bankapp.&quot;

Deze pagina biedt een overzicht van hoe u Adobe Analytics het beste kunt gebruiken om dit soort ervaringen te meten en te optimaliseren.

## Overzicht van architectuur voor digitale ervaring

![Digital Assistant-workflow](assets/Digital-Assitants.png)

De meeste digitale assistenten volgen tegenwoordig een vergelijkbare architectuur op hoog niveau:

1. **Apparaat**: Er is een apparaat (zoals een Amazon Echo of een telefoon) met een microfoon waarmee de gebruiker een vraag kan stellen.
1. **Digitale assistent**: Dat apparaat communiceert met de dienst die de digitale medewerker macht. Op dit punt wordt de toespraak geconverteerd naar begrijpelijke machineteknoppen en worden de details van het verzoek geparseerd. Zodra de intent van de gebruiker wordt begrepen, geeft de digitale medewerker de intent en de details van het verzoek tot app door die het verzoek behandelt.
1. **&quot;App&quot;**: De app kan een toepassing zijn op de telefoon of een spraak-app. De app reageert op de aanvraag. Het antwoordt aan de digitale medewerker en de digitale medewerker antwoordt dan aan de gebruiker.

## Waar moet ik analyses uitvoeren?

Een van de beste plaatsen om Analytics te implementeren is in de app. De app ontvangt de intentie en de details van de digitale assistent en bepaalt vervolgens hoe moet worden gereageerd.

Tijdens een aanvraag zijn er twee keer gegevens die nuttig kunnen zijn voor het verzenden van gegevens naar Adobe Analytics.

1. Wanneer de aanvraag naar uw app wordt verzonden.
1. Nadat de reactie van de app is geretourneerd.

Als u alleen maar geïnteresseerd bent in het opnemen van wat er met de klant is gebeurd voor toekomstige optimalisatie, stuurt u een verzoek naar Adobe Analytics nadat het antwoord is geretourneerd. U krijgt de volledige context van wat het verzoek was en hoe het systeem reageerde.

## Nieuwe installaties

Voor sommige digitale medewerkers, krijgt u een bericht wanneer iemand de vaardigheid installeert, vooral wanneer de authentificatie betrokken is. Adobe raadt aan een Install-gebeurtenis te verzenden door de variabele `a.InstallEvent=1` van de contextgegevens in te stellen. Deze functie is niet beschikbaar voor alle digitale assistenten, maar is handig wanneer u deze functie gebruikt om de retentie te bekijken. De volgende codesteekproef verzendt de Install gebeurtenis, installeert Datum, en waarden AppID in de variabelen van contextgegevens.

```text
GET
/b/ss/examplersid/1?vid=[UserID]&c.a.InstallEvent=1&c.a.InstallDate=2017-04-24&c.a.AppID=Spoofify1.0&c.OSType=Alexa&pageName=install
HTTP/1.1
Host:
<xref href="https://example.data.adobedc.net">
  example.data.adobedc.net
 Cache-Control: no-cache
</xref href="https:>
```

## Meerdere assistenten of meerdere apps

Uw organisatie wil waarschijnlijk apps voor meerdere platforms. De beste manier is om bij elke aanvraag een toepassings-id op te nemen. Deze variabele kan in de `a.AppID` variabele van contextgegevens worden geplaatst. Volg de notatie van `[AppName] [BundleVersion]`, bijvoorbeeld BigMac voor Alexa 1.2:

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.Launches=1&c.Product=AmazonEcho&c.OSType=Alexa&pageName=install  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify2.0&c.a.Launches=1&c.Product=GoogleHome&c.OSType=Android&pageName=install  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

## Identificatie gebruiker/bezoeker

Adobe Analytics gebruikt [Adobe Experience Cloud Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) om interacties in de tijd aan dezelfde persoon te koppelen. De meeste digitale assistenten retourneren een `userID` die u kunt gebruiken om de activiteit voor verschillende gebruikers te behouden. In de meeste gevallen is deze waarde wat u kunt doorgeven als een unieke id. Sommige platforms retourneren een id die langer is dan de 100 toegestane tekens. In deze gevallen, adviseert Adobe dat u het unieke herkenningsteken aan een vaste lengtewaarde gebruikend een standaard het hakken algoritme, zoals MD5 of Sha1 hakt.

Het gebruiken van de Dienst van identiteitskaart verstrekt de meeste waarde wanneer u ECIDs over verschillende apparaten (bijvoorbeeld, Web aan digitale medewerker) in kaart brengt. Als uw app een mobiele toepassing is, gebruikt u de SDK&#39;s van het Experience Platform ongewijzigd en verzendt u de gebruikers-id met de methode `setCustomerID`. Als uw app echter een service is, gebruikt u de door de service opgegeven gebruikers-id als de ECID en stelt u deze in op `setCustomerID`.

```text
GET /b/ss/examplersid/1?vid=[UserID]&pageName=[intent]  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

## Sessies

Omdat digitale assistenten conversatief zijn, hebben ze vaak het concept van een sessie. Bijvoorbeeld:

**Consumenten:** &quot;Ok Google, bel een taxi voor mij&quot;

**Google:**: &quot;Natuurlijk, hoe laat zou je willen?&quot;

**Consumenten:** &quot;8:30 pm&quot;

**Google:**  &quot;Geluiden goed, de driver is om 20:30 uur&quot;

De zittingen zijn belangrijk om context te houden, en de hulp verzamelt meer details om de digitale medewerker natuurlijker te maken. Wanneer het uitvoeren van Analytics op een gesprek, zijn er twee dingen om te doen wanneer een nieuwe zitting is begonnen:

1. **Naar Audience Manager** gaan: Krijg de relevante segmenten die een gebruiker een deel van is zodat u de reactie kunt aanpassen. (Deze persoon komt momenteel bijvoorbeeld in aanmerking voor de multikanaalskorting.)
2. **Verzenden in een nieuwe sessie of startgebeurtenis**: Wanneer u de eerste reactie naar Analytics verzendt, neemt u een startgebeurtenis op. Gewoonlijk kan dit worden verzonden door contextgegevens van `a.LaunchEvent=1` in te stellen.

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.LaunchEvent=1&c.Intent=[intent]&pageName=[intent]  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

## Intenten

Elk van de digitale assistenten heeft algoritmen die intenties detecteren en vervolgens de intentie doorgeven aan de &quot;App&quot;, zodat de app weet wat ze moeten doen. Deze intenties vormen een beknopte weergave van het verzoek.

Als een gebruiker bijvoorbeeld zegt: &quot;Siri, Stuur John $20 voor het avondeten vanuit mijn bankapp&quot;, dan kan de intentie iets zijn als *sendMoney*.

Door elk van deze verzoeken als een eVar in te dienen, kunt u tekenrapporten uitvoeren over elk van de intents voor conversatie-apps. Zorg ervoor dat uw toepassing aanvragen ook zonder intentie kan verwerken. Adobe raadt aan &#39;Geen intentie opgegeven&#39; door te geven aan de gegevensvariabele van de intentcontext, in plaats van de variabele weg te laten.

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1
Host: example.sc.adobedc.net
Cache-Control: no-cache
```

of

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.a.LaunchEvent=1&c.Intent=No_Intent_Specified&pageName=[intent]  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

## Parameters/sleuven/entiteiten

Naast de intentie hebben digitale assistenten vaak een set sleutel-/waardeparen die details van de intentie geven. Deze kunnen groeven, entiteiten of parameters worden genoemd. &quot;Siri, Send John $20 for diner gisteravond from my banking app&quot; zou bijvoorbeeld de volgende parameters hebben:

* Who = John
* Bedrag = 20
* Waarom = Diner

De app bevat meestal een eindig aantal van deze waarden. Als u deze waarden wilt bijhouden in Analytics, stuurt u ze naar contextgegevensvariabelen en wijst u elk van de parameters toe aan een eVar.

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Penmo1.0=1&c.a.LaunchEvent=1&c.Intent=SendPayment&c.Amount=20.00&c.Reason=Dinner&c.ReceivingPerson=John&c.Intent=SendPayment&pageName=[intent]  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

## Foutstatussen

Soms verschaft de digitale assistent uw app invoer die deze niet kan verwerken. Bijvoorbeeld &quot;Siri, Stuur John 20 tassen steenkool voor diner gisteravond vanuit mijn bankapp&quot;

Wanneer deze situatie zich voordoet, vraagt uw app om opheldering. Verstuur bovendien gegevens naar Adobe die aangeven dat de toepassing een foutstatus heeft en een eVar die aangeeft welk type fout is opgetreden. Zorg ervoor dat u fouten opneemt waar de invoer niet correct is en fouten opneemt waar de app een probleem heeft.

```text
GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Penmo1.0&c.Error=1&c.ErrorName=InvalidCurrency&pageName=[intent]  HTTP/1.1
Host: example.data.adobedc.net
Cache-Control: no-cache
```

## Apparaatmogelijkheden

Terwijl de meeste platforms niet het apparaat blootstellen dat de gebruiker aan sprak, stellen zij de mogelijkheden van het apparaat bloot. Bijvoorbeeld audio, scherm, video, enz. Deze informatie is handig omdat hiermee de typen inhoud worden gedefinieerd die kunnen worden gebruikt bij interactie met uw gebruikers. Bij het meten van apparaatmogelijkheden kunt u deze het beste samenvoegen (in alfabetische volgorde).

Voorbeeld: `":Audio:Camera:Screen:Video:"`

De voorloopdubbele en navolgende dubbele punten helpen u bij het maken van segmenten. Geef bijvoorbeeld alle resultaten weer met de mogelijkheden `:Audio:`.

* [Amazon-](https://developer.amazon.com/public/solutions/alexa/alexa-skills-kit/docs/alexa-skills-kit-interface-reference) mogelijkheden met Amazon Alexa
* [Google-](https://developers.google.com/actions/assistant/surface-capabilities) mogelijkheden via Handelingen op Google

## Voorbeelden

| Persoon | Apparaatreactie | Handeling/intentie | Verzoek om GET |
|---|---|---|---|
| Spoofify installeren | Geen reactie | Installeren | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.InstallEvent=1&c.a.InstallDate=[currentDate]&c.a.AppID=Spoofify1.0&c.OSType=Alexa&c.Intent=Install&pageName=Install  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
| Spoofiel afspelen | &quot;Oké, Spoofify spelen&quot; | Afspelen | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.a.LaunchEvent=1&c.Intent=Play&pageName=PlayApp  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
| Ander nummer | &quot;Oké, welk liedje wil je?&quot; | ChangeSong | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangeSong&pageName= Ask%20For%20Song  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
| &quot;Baby Shark&quot; afspelen | &quot;Oké, &#39;Baby Shark&#39; afspelen van PinkFong&quot; | ChangeSong | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangeSong&pageName=Action%20Play%20Song&c.SongID=[012345]  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
| Afspeellijst wijzigen | &quot;Oké, welke afspeellijst wilt u?&quot; | ChangePlaylist | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangePlaylist&pageName=Ask%20For%20Playlist  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
| Speel mijn favoriete liedjesspeellijst | &quot;Oké, je favoriete muziektoneelschrijver afspelen&quot; | ChangePlaylist | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=ChangePlaylist&pageName=Action%20Play%20Playlist&c.Playlist=My%20Favorite%20Songs  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
| Muziek uitschakelen | Geen reactie, muziek schakelt uit | Uit | `GET /b/ss/examplersid/1?vid=[UserID]&c.a.AppID=Spoofify1.0&c.Intent=Off&pageName=Music%20Off  HTTP/1.1`<br>`Host: example.data.adobedc.net`<br>`Cache-Control: no-cache` |
