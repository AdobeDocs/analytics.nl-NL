---
description: Met Dynamisch tagbeheer kunt u kop- en voettekstcode toevoegen die het laden van JavaScript en pagina-inhoud op uw site bepaalt. U moet zowel de kop- als voettekstcode op elke pagina van uw site installeren, ongeacht de gebruikte hostoptie.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;code;page code;header code;footer code;embed code;embed tab;embed
title: Code voor kop- en voetteksten toevoegen
topic: Developer and implementation
uuid: 23d89ae0-340a-4b12-91d1-953b4613c98e
translation-type: tm+mt
source-git-commit: dfe8409b13fcf67eae6a0c404f83c1209f89ae12

---


# Code voor kop- en voetteksten toevoegen

Met Dynamisch tagbeheer kunt u kop- en voettekstcode toevoegen die het laden van JavaScript en pagina-inhoud op uw site bepaalt. U moet zowel de kop- als voettekstcode op elke pagina van uw site installeren, ongeacht de gebruikte hostoptie.

Omdat Dynamisch tagbeheer een codefragment bevat in zowel de kop- als voettekst, kunt u regels uitvoeren aan het begin of einde van een pagina. Hierdoor kunt u testgereedschappen en andere technologieën implementeren terwijl u de controle over het bijhouden van uw pagina&#39;s behoudt.

Met Dynamisch tagbeheer maakt u gefaseerde en productie-insluitcodes waarmee u uw wijzigingen in de testomgeving kunt testen voordat u wijzigingen in de productieomgeving aanbrengt.

>[!IMPORTANT]
>
>Voor een geslaagde implementatie is het van essentieel belang dat u deze instructies opvolgt zoals deze worden weergegeven in de Help van Adobe. Meer bepaald moet u de koptekstcode in de `<head>` sectie van uw documentsjablonen plaatsen. Bovendien moet u de voettekstcode vlak voor de afsluitende `</body>` tag plaatsen. Het plaatsen van één van beiden van deze bedcodes elders in uw prijsverhoging, of het gebruiken van asynchrone methodes om de inbedcodes toe te voegen, of het verpakken van de inbedcodes op om het even welke manier, zijn *geen* gesteunde implementaties van het Dynamische Beheer van de Markering. De insluitcodes moeten precies worden geïmplementeerd zoals opgegeven.
>
>Een niet-ondersteunde implementatie levert onverwachte resultaten op en voorkomt dat de klantenservice en -engineering uw implementatie ondersteunen.

1. Open in de interface Dynamisch tagbeheer het [!UICONTROL Embed] tabblad en selecteer de hostingoptie (zoals Akamai) en schakel vervolgens over naar &quot;Aan&quot;.

   Stap Resultaat 1. Kopieer de kopcode voor de productie die is opgegeven op het tabblad Insluiten van Dynamisch tagbeheer en plaats deze in het [!DNL HEAD] gedeelte van uw site-HTML.

   ![](assets/dtm-embed.png)

   Plaats de code zo dicht bij de [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">] -tag indien mogelijk. Dit codefragment moet op elke pagina van uw livesite worden geplaatst.

   >[!NOTE]
   >
   >In de insluitcode van de productie worden alleen de gepubliceerde items in die [eigenschap](/help/implement/other/dtm/t-create-web-property.md)weergegeven. Insluitcode voor plaatsing weerspiegelt echter alle items in de bijbehorende eigenschap, ongeacht de gepubliceerde of niet-gepubliceerde status. Om ongepubliceerde punten op uw productiesite te testen, laat plaatselijk het opvoeren in de console toe door de instructies in de [Test Unpublished Regels voor het Hosten](/help/implement/other/dtm/c-rules/t-test-rules-akamai.md)van Akamai te volgen.

1. Kopieer de code voor de productievoettekst en plaats deze in de [!DNL BODY] sectie van de HTML-site.

   Plaats de code zo dicht bij de [!DNL </body>] -tag indien mogelijk.
1. Kopieer de testkop- en voettekstcode en herhaal vervolgens de bovenstaande stappen op uw testsite.

   >[!NOTE]
   >
   >Het verschil tussen codefragmenten voor productie en staging is de toevoeging van [!DNL -staging] aan de bestandsnaam in de testversie. De voettekstcode blijft hetzelfde bij ophaling en productie.

