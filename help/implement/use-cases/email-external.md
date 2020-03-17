---
title: Externe e-mailtracking
description: Gebruik Adobe Analytics om e-mailinhoud bij te houden.
translation-type: tm+mt
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651

---


# Externe e-mailtracking

Bedrijven gebruiken Analytics om het succes van een e-mailcampagne te bepalen.

[!DNL Analytics] U kunt gegevens van de e-mailcampagneanalyse in verscheidene zeer belangrijke metriek, met inbegrip van het volgende melden:

| Metrisch | Beschrijving |
|---|---|
| Doorklikken | Hier wordt het aantal doorklikcontroles weergegeven dat van de e-mail naar de openingspagina wordt bijgehouden. |
| Aankopen en/of succesmeldingen | Hier wordt het aantal aankopen weergegeven dat het resultaat is van het e-mailbericht. |
| Orders | Hier wordt het aantal orders weergegeven dat als gevolg van het e-mailbericht is geplaatst. |
| Opbrengst | Hiermee geeft u het dollarbedrag per bezoek weer dat wordt gegenereerd uit de e-mail. |
| Conversie | Hier wordt het aantal leads, registraties of andere succesgebeurtenissen weergegeven dat uit de e-mail is gegenereerd. |

Wijzigingen in de hoofdtekst van de HTML-e-mail en de JavaScript-bibliotheek zijn vereist voor het vastleggen van de belangrijkste cijfers die hierboven worden weergegeven.

## Implementatie {#section_8A42A8F4A6CD4A1BAF4B9F99F709AF7A}

Er zijn verschillende stappen om de analysegegevens van de e-mailcampagne correct weer te geven. De stappen worden als volgt beschreven:

1. Maak unieke volgcodes.

   Vaak vragen gebruikers om trackingsaanbevelingen voor elke unieke campagne. Dit is volledig aan hen, gebaseerd op wat het beste werkt. Elke gebruiker is anders. Adobe raadt elke gebruiker aan vriendelijke volgcodes te genereren, zoals in het onderstaande voorbeeld wordt getoond:

   * sc_cid=A1123A321 > &quot;A&quot; markeert gelieerde campagne
   * sc_cid=EM033007 > &quot;EM&quot; markeert e-mailcampagne
   * sc_cid=GG987123 > &quot;GG&quot; betekent Google en is een betaalde zoekcampagne
   Neem contact op met Adobe [!DNL Customer Care] voor meer informatie over het instellen en gebruiken van trackingcodes.

1. Parameters voor queryreeksen toevoegen aan HTML-e-mailkoppelingen.

   Om een gebruiker te volgen klik-door en volgende succesgebeurtenissen, moet een parameter van het vraagkoord aan elke verbinding binnen HTML e-mail worden toegevoegd. U kunt elke koppeling afzonderlijk bijhouden of alle koppelingen bij elkaar houden. Elke koppeling kan een unieke trackingcode hebben of alle koppelingen kunnen dezelfde trackingcode hebben. Bekijk de volgende hypothetische koppeling in de e-mail naar een website:

   ```js
   <a href="https://www.example.com/index.asp">Visit our home page</a>
   ```

   De volgende parameters voor de queryreeks ?sc_cid=112233B moeten aan de bovenstaande koppeling worden toegevoegd:

   ```js
   <a href= "https://www.example.com/index.asp?sc_cid=112233B">Visit our home page</a>
   ```

1. Werk de JavaScript-bibliotheek bij.

   Door code in het JavaScript-bestand te wijzigen, kunt u [!DNL s_code.js]vastleggen hoeveel gebruikers (en welke gebruikers) via de e-mail hebben geklikt en aan volgende succesgebeurtenissen hebben deelgenomen. U moet de JavaScript-bibliotheek in twee stappen bijwerken.

   1. Aanpassen [!DNL s_code.js] door aan te roepen [!UICONTROL getQueryParam].

      Het [!DNL s_code.js] dossier zou in een plaats op de server van het Web moeten worden geplaatst waar elke Web-pagina tot het kan toegang hebben. De *`doPlugins`* functie in dit bestand moet worden gewijzigd, zodat de parameters van de queryreeks in de e-mailkoppelingen worden vastgelegd. Bijvoorbeeld:

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

      Elke parameter van het vraagkoord die in een variabele moet worden gekopieerd zou één [!UICONTROL getQueryParam] vraag moeten hebben. In het bovenstaande voorbeeld, [!UICONTROL sc_cid] wordt de parameter van het vraagkoord gekopieerd in *`campaign`*.

      Alleen de eerste aanroep [!UICONTROL getQueryParam] is vereist om doorklikken vast te leggen. Neem contact op met Adobe [!DNL Customer Care] om deze functie te implementeren en ervoor te zorgen dat uw versie van het JavaScript-bestand de [!UICONTROL getQueryParam] plug-in bevat.

   1. Zorg ervoor dat de code voor het plakken van JavaScript-tags zich op alle bestemmingspagina&#39;s bevindt. Deze code moet verwijzen naar de versie van [!DNL s_code.js] gewijzigd in deel A.

      De volgende punten zijn belangrijk om te onthouden wanneer u de JavaScript-bibliotheek bijwerkt. Deze punten worden hieronder vermeld.

      * De parameter van het vraagkoord [!UICONTROL sc_cid] moet in URL op de definitieve het landen pagina zichtbaar zijn anders geen klik-door omzetting wordt geregistreerd.
      * De [!UICONTROL sc_cid] parameter is een voorbeeld van een parameter van het vraagkoord. Elke querytekenreeksparameter kan door de [!UICONTROL getQueryParam] plug-in worden gebruikt en vastgelegd. Zorg ervoor dat de parameters van het vraagkoord slechts voor campagne het volgen worden gebruikt. Elke keer dat de parameters in een queryreeks worden weergegeven, worden de waarden ervan gekopieerd naar *`campaign`*.

1. Gebruik deze optie [!UICONTROL SAINT] om de codes voor het bijhouden van campagnes te classificeren.

   U [!UICONTROL SAINT Campaign Management Tool] kunt volgcodes omzetten in gebruikersvriendelijke namen. Het kan ook worden gebruikt om het succes van elke e-mailcampagne samen te vatten. Stap 5, hieronder, schetst het proces dat wordt vereist om een e-mailcampagne op te zetten.

1. Zie plakken per e-mailcampagne (optioneel).

   Pathing analysis by email campagne kan net zo worden uitgevoerd als schilderen door een andere campagne. U kunt een variabele gebruiken om het tekenen door campagne te tonen, zoals die in de volgende stappen wordt verklaard:

   1. Raadpleeg Adobe [!DNL Customer Care] voor informatie over het inschakelen van paden voor een [!UICONTROL Custom Insight] variabele (proxy)

   1. Kopieer de paginanaam op alle pagina&#39;s naar het opgegeven [!DNL s.prop].
   1. Voeg op de bestemmingspagina van de e-mail de naam van de e-mailcampagne aan de pop toe. Het resultaat wordt weergegeven zoals hieronder wordt getoond:

      ```js
      s.prop1="Home Page : 123456"
      ```

      Wanneer het plakken voor de [!UICONTROL Custom Insight] variabele wordt toegelaten, kunt u [!UICONTROL Path] rapporten (zoals [!UICONTROL Next Page Flow] of [!UICONTROL Fallout]) gebruiken om bezoekersnavigatie van de landende pagina te zien.

