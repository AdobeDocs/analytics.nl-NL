---
title: Externe e-mailtracering
description: Gebruik Adobe Analytics om e-mailinhoud bij te houden.
feature: Implementation Basics
exl-id: 9f7920e0-471c-46bc-9314-7b0a7c93fdce
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 1%

---

# Externe e-mailtracering

Bedrijven gebruiken Analytics om het succes van een e-mailcampagne te bepalen.

[!DNL Analytics] U kunt gegevens van de e-mailcampagneanalyse in verscheidene zeer belangrijke metriek, met inbegrip van het volgende melden:

| Metrisch | Beschrijving |
|---|---|
| Doorgeklikt | Hier wordt het aantal doorklikcontroles weergegeven dat van de e-mail naar de openingspagina wordt bijgehouden. |
| Aankopen en/of succesmeldingen | Hier wordt het aantal aankopen weergegeven dat het resultaat is van het e-mailbericht. |
| Orders | Hier wordt het aantal orders weergegeven dat als gevolg van het e-mailbericht is geplaatst. |
| Opbrengst | Hiermee geeft u het dollarbedrag per bezoek weer dat wordt gegenereerd uit de e-mail. |
| Conversie | Hier wordt het aantal leads, registraties of andere succesgebeurtenissen weergegeven dat uit de e-mail is gegenereerd. |

Wijzigingen in de hoofdtekst van het e-mailbericht van de HTML en de JavaScript-bibliotheek zijn vereist om de belangrijkste cijfers vast te leggen die hierboven worden weergegeven.

## Implementatie {#section_8A42A8F4A6CD4A1BAF4B9F99F709AF7A}

Er zijn verschillende stappen om de analysegegevens van de e-mailcampagne correct weer te geven. De stappen worden als volgt beschreven:

1. Maak unieke volgcodes.

   Vaak vragen gebruikers om trackingsaanbevelingen voor elke unieke campagne. Dit is volledig aan hen, gebaseerd op wat het beste werkt. Elke gebruiker is anders. Adobe raadt aan dat elke gebruiker vriendelijke volgcodes genereert, zoals in het onderstaande voorbeeld wordt getoond:

   * sc_cid=A1123A321 > &quot;A&quot; markeert gelieerde campagne
   * sc_cid=EM033007 > &quot;EM&quot; markeert e-mailcampagne
   * sc_cid=GG987123 > &quot;GG&quot; betekent Google en is een betaalde zoekcampagne

   Contact Adobe [!DNL Customer Care] voor meer informatie over het instellen en gebruiken van trackingcodes.

1. Voeg parameters voor queryreeksen toe aan HTML-e-mailkoppelingen.

   Om een gebruiker te volgen klik-door en volgende succesgebeurtenissen, moet een parameter van het vraagkoord aan elke verbinding binnen HTML e-mail worden toegevoegd. U kunt elke koppeling afzonderlijk bijhouden of alle koppelingen bij elkaar houden. Elke koppeling kan een unieke trackingcode hebben of alle koppelingen kunnen dezelfde trackingcode hebben. Bekijk de volgende hypothetische koppeling in de e-mail naar een website:

   ```js
   <a href="https://www.example.com/index.asp">Visit our home page</a>
   ```

   De volgende parameters voor de queryreeks ?sc_cid=112233B moeten aan de bovenstaande koppeling worden toegevoegd:

   ```js
   <a href= "https://www.example.com/index.asp?sc_cid=112233B">Visit our home page</a>
   ```

1. Werk de JavaScript-bibliotheek bij.

   Code wijzigen in het JavaScript-bestand, [!DNL s_code.js], kunt u vastleggen hoeveel gebruikers (en welke gebruikers) op de e-mail hebben geklikt en aan volgende succesgebeurtenissen hebben deelgenomen. U moet de JavaScript-bibliotheek in twee stappen bijwerken.

   1. Aanpassen [!DNL s_code.js] door [!UICONTROL getQueryParam].

      De [!DNL s_code.js] het dossier zou in een plaats op de server van het Web moeten worden geplaatst waar elke Web-pagina tot het kan toegang hebben. De *`doPlugins`* De functie in dit bestand moet worden gewijzigd, zodat de parameters van de queryreeks in de e-mailkoppelingen worden vastgelegd. Bijvoorbeeld:

      ```js
      /* Plugin Config */ 
      s.usePlugins=true 
      function s_doPlugins(s) { 
       /* Add calls to plugins here */ 
       // External Campaigns 
      s.campaign=s.getQueryParam('source') 
      } 
      s.doPlugins=s_doPlugins 
      ```

      Elke parameter van het vraagkoord die in een variabele moet worden gekopieerd zou één moeten hebben [!UICONTROL getQueryParam] vraag. In het bovenstaande voorbeeld, de parameter van het vraagkoord [!UICONTROL sc_cid] wordt gekopieerd naar *`campaign`*.

      Alleen de eerste aanroep naar [!UICONTROL getQueryParam] is vereist voor het vastleggen van doorklikbewerkingen. Contact Adobe [!DNL Customer Care] om deze functie te implementeren en ervoor te zorgen dat uw versie van het JavaScript-bestand de [!UICONTROL getQueryParam] insteekmodule.

   1. Zorg ervoor dat de code voor het plakken van JavaScript-tags zich op alle bestemmingspagina&#39;s bevindt. Deze code die u wilt plakken, moet verwijzen naar de versie van [!DNL s_code.js] gewijzigd in deel A.

      De volgende punten zijn belangrijk om te onthouden wanneer u de JavaScript-bibliotheek bijwerkt. Deze punten worden hieronder vermeld.

      * De parameter voor de queryreeks [!UICONTROL sc_cid] moet zichtbaar zijn in de URL op de laatste bestemmingspagina anders wordt geen klikdoorconversie geregistreerd.
      * De [!UICONTROL sc_cid] parameter is een voorbeeld van een parameter van het vraagkoord. Elke querytekenreeksparameter kan worden gebruikt en vastgelegd door de [!UICONTROL getQueryParam] insteekmodule. Zorg ervoor dat de parameters van het vraagkoord slechts voor campagne het volgen worden gebruikt. Elke keer dat de parameters in een queryreeks worden weergegeven, worden de waarden ervan gekopieerd naar *`campaign`*.

1. Gebruiken [!UICONTROL SAINT] om de codes voor het bijhouden van campagnes te classificeren.

   De [!UICONTROL SAINT Campaign Management Tool] kan worden gebruikt om volgcodes om te zetten in gebruikersvriendelijke namen. Het kan ook worden gebruikt om het succes van elke e-mailcampagne samen te vatten. Stap 5, hieronder, schetst het proces dat wordt vereist om een e-mailcampagne op te zetten.

1. Zie plakken per e-mailcampagne (optioneel).

   Pathing analysis by email campagne kan net zo worden uitgevoerd als schilderen door een andere campagne. U kunt een variabele gebruiken om het tekenen door campagne te tonen, zoals die in de volgende stappen wordt verklaard:

   1. Consult Adobe [!DNL Customer Care] om tekenen in te schakelen voor een [!UICONTROL Custom Insight] variable (prop)

   1. Kopieer de paginanaam op alle pagina&#39;s naar de opgegeven [!DNL s.prop].
   1. Voeg op de bestemmingspagina van de e-mail de naam van de e-mailcampagne aan de pop toe. Het resultaat wordt weergegeven zoals hieronder wordt getoond:

      ```js
      s.prop1="Home Page : 123456"
      ```

      Wanneer het plakken voor [!UICONTROL Custom Insight] variabele, kunt u gebruiken [!UICONTROL Path] rapporten (zoals [!UICONTROL Next Page Flow] of [!UICONTROL Fallout]) om bezoekersnavigatie vanaf de landingspagina te zien.
