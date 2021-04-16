---
description: Met Dynamisch tagbeheer kunt u kop- en voettekstcode toevoegen die het laden van JavaScript en pagina-inhoud op uw site bepaalt. U moet zowel de kop- als voettekstcode op elke pagina van uw site installeren, ongeacht de gebruikte hostoptie.
keywords: Analyse-implementatie;implementatiemethode;dynamisch tagbeheer;dtm;code;paginacode;koptekstcode;voettekstcode;embed code;embed tabblad;embed
title: Code voor kop- en voetteksten toevoegen
topic-fix: Developer and implementation
uuid: 23d89ae0-340a-4b12-91d1-953b4613c98e
exl-id: 170c28fb-8884-4c44-b586-f88a7583083e
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 2%

---

# Code voor kop- en voetteksten toevoegen

Met Dynamisch tagbeheer kunt u kop- en voettekstcode toevoegen die het laden van JavaScript en pagina-inhoud op uw site bepaalt. U moet zowel de kop- als voettekstcode op elke pagina van uw site installeren, ongeacht de gebruikte hostoptie.

Omdat Dynamisch tagbeheer een codefragment bevat in zowel de kop- als voettekst, kunt u regels uitvoeren aan het begin of einde van een pagina. Hierdoor kunt u testgereedschappen en andere technologieën implementeren terwijl u de controle over het bijhouden van uw pagina&#39;s behoudt.

Met Dynamisch tagbeheer maakt u gefaseerde en productie-insluitcodes waarmee u uw wijzigingen in de testomgeving kunt testen voordat u wijzigingen in de productieomgeving aanbrengt.

>[!IMPORTANT]
>
>Voor een geslaagde implementatie is het van essentieel belang dat u deze instructies opvolgt zoals deze worden weergegeven in de Help bij Adobe. Specifiek, moet u de kopbalcode in `<head>` sectie van uw documentmalplaatjes plaatsen. Bovendien moet u de voettekstcode net vóór de afsluitende `</body>`-tag plaatsen. Als u een van deze insluitcodes elders in de markering plaatst of asynchrone methoden gebruikt om de insluitcodes toe te voegen, of als u de insluitcodes op een of andere manier inpakt, is *geen* een ondersteunde implementatie van Dynamisch tagbeheer. De insluitcodes moeten precies worden geïmplementeerd zoals opgegeven.
>
>Een niet-ondersteunde implementatie levert onverwachte resultaten op en voorkomt dat de klantenservice en -engineering uw implementatie ondersteunen.

1. Open in de interface Dynamisch tagbeheer het tabblad [!UICONTROL Embed] en selecteer de hostingoptie (zoals Akamai) en schakel vervolgens over naar &quot;Aan&quot;.

   Stap Resultaat 1. Kopieer de kopcode voor de productie die is opgegeven op het tabblad Insluiten van Dynamisch tagbeheer en plaats deze in de sectie [!DNL HEAD] van uw site-HTML.

   ![](assets/dtm-embed.png)

   Plaats de code zo dicht mogelijk bij de tag `<head>`. Dit codefragment moet op elke pagina van uw livesite worden geplaatst.

   >[!NOTE]
   >
   >De productie ingebedde code weerspiegelt slechts de gepubliceerde punten in dat [bezit](/help/implement/other/dtm/t-create-web-property.md). Insluitcode voor plaatsing weerspiegelt echter alle items in de bijbehorende eigenschap, ongeacht de gepubliceerde of niet-gepubliceerde status. Om ongepubliceerde punten op uw productiesite te testen, laat plaatselijk het opvoeren in de console toe door de instructies in [Niet-gepubliceerde Regels van de Test voor Akamai Hosting](/help/implement/other/dtm/c-rules/t-test-rules-akamai.md) te volgen.

1. Kopieer de code voor de productievoettekst en plaats deze in de sectie [!DNL BODY] van de HTML-site.

   Plaats de code zo dicht mogelijk bij de tag `</body>`.
1. Kopieer de testkop- en voettekstcode en herhaal vervolgens de bovenstaande stappen op uw testsite.

   >[!NOTE]
   >
   >Het verschil tussen codefragmenten voor productie en staging is de toevoeging van [!DNL -staging] aan de bestandsnaam in de testversie. De voettekstcode blijft hetzelfde bij ophaling en productie.
