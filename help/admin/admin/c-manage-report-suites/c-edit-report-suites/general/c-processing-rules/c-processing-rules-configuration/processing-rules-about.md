---
description: Met verwerkingsregels kunt u gegevens wijzigen op basis van gedefinieerde voorwaarden. Wanneer kenmerken of waarden overeenkomen met gedefinieerde voorwaarden, kunnen waarden worden ingesteld en verwijderd en kunnen gebeurtenissen worden ingesteld.
subtopic: Processing rules
title: De werking van verwerkingsregels
feature: Processing Rules
role: Admin
exl-id: 9d2d9f2d-1e16-486f-9191-2c43776374da
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---

# De werking van verwerkingsregels

Met verwerkingsregels kunt u gegevens wijzigen op basis van gedefinieerde voorwaarden. Wanneer kenmerken of waarden overeenkomen met gedefinieerde voorwaarden, kunnen waarden worden ingesteld en verwijderd en kunnen gebeurtenissen worden ingesteld.

De verwerkingsregels worden toegepast op gegevens aangezien het wordt verzameld, en de regels worden toegepast op alle gegevens die door de bibliotheken van het AppMeasurement en door de Invoeging API van Gegevens komen. De verwerkingsregels zijn ook van toepassing op de volledige gegevensbronnen en de logbestanden. Deze bronnen bevatten gegevens die een *`hit`* of een handeling die een gebruiker uitvoert. De verwerkingsregels zijn niet van toepassing op andere gegevensbronnen.

## Belangrijke concepten {#section_EB138775E7C64C74B0D1D3213F7A823C}

De volgende lijst bevat zeer belangrijke concepten u moet begrijpen wanneer het gebruiken van verwerkingsregels:

<table id="table_287C606AE26E47AA8F737411990ACEB2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Concept </p> </th> 
   <th colname="col2" class="entry"> <p>Details </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>De regels zijn op één enkele rapportreeks van toepassing. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md"> De verwerkingsregels van het exemplaar aan een andere rapportreeks </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De verwerkingsregels worden toegepast in de weergegeven volgorde. </p> </td> 
   <td colname="col2"> <p>Als een actie een waarde verandert, gebruiken de verdere voorwaarden de nieuwe waarde. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De verwerkingsregels worden onmiddellijk toegepast op de rapportsuite nadat ze zijn opgeslagen. </p> </td> 
   <td colname="col2"> <p>Wijzigingen in de verwerkingsregels moeten binnen enkele minuten na opslaan zichtbaar zijn in de rapportsuite. Bij het testen van verwerkingsregels raden we aan om te configureren <a href="/help/admin/admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md"> real-time rapporten</a> in uw reeks van het testrapport zodat kunt u de resultaten van een verwerkingsregel snel zien. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De verwerkingsregels zijn de enige manier om tot de variabelen van contextgegevens toegang te hebben. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md"> Een contextgegevensvariabele naar een eVar kopiëren </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De verwerkingsregels worden toegepast vóór de regels van VISTA en de regels van het Kanaal van de Marketing. </p> </td> 
   <td colname="col2"> <p> <a href="/help/technotes/processing-order.md"> Verwerkingsvolgorde </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dit kan niet worden uitgesloten. </p> </td> 
   <td colname="col2"> <p>U kunt de regels van VISTA gebruiken om treffers uit te sluiten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De producttekenreeks, verwijzer en gebruikersagent kunnen niet worden gewijzigd. </p> </td> 
   <td colname="col2"> <p>Referrer en user agent zijn read-only. De productreeks is niet beschikbaar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Kenmerken en classificaties van mobiele apparaten zijn niet beschikbaar. </p> </td> 
   <td colname="col2"> <p>De zoekopdracht voor mobiele apparaten vindt plaats vóór de verwerkingsregels, maar kenmerken zijn niet beschikbaar in de verwerkingsregels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Parameters van queryreeksen kunnen niet worden gelezen na de eerste 255 tekens van een URL als u JavaScript-AppMeasurement H.25.2 of eerder uitvoert. JavaScript AppMeasurement H.25.3 en hoger verstrekken volledige URL met inbegrip van alle parameters van het vraagkoord aan verwerkingsregels. </p> </td> 
   <td colname="col2"> <p>Voer een upgrade uit naar H.25.3 of hoger of lees parameters voor queryreeksen van lange URL's, client-side en store-waarden in variabelen voor contextgegevens. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De het koordwaarden van de vraag moeten in Unicode of UTF-8 worden gecodeerd om door verwerkingsregels te worden gelezen. </p> </td> 
   <td colname="col2"> <p>Dit kan van invloed zijn op multibyte-tekens die worden doorgegeven met querytekenreeksen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U bent beperkt tot 150 regels met 30 voorwaarden elk voor elke rapportreeks. </p> </td> 
   <td colname="col2"> <p>De grenzen van de verwerkingsregel zijn per rapportreeks, niet per bedrijf. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>De verwerkingsregels moeten opstelling zijn om de variabelen van contextgegevens terug te winnen alvorens de gegevens worden verzonden. </p> </td> 
   <td colname="col2"> <p>De verwerkingsregels worden toegepast terwijl serveraanroepen worden verzonden. Waarden die zijn opgeslagen in contextgegevensvariabelen worden verwijderd als ze niet worden gekopieerd met verwerkingsregels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Waardevergelijkingen in de gebruikersinterface zijn niet hoofdlettergevoelig. </p> </td> 
   <td colname="col2"> <p> <a href="/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md"> Waarden opschonen in een rapport </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Namen van contextgegevensvariabelen mogen alleen alfanumerieke tekens, onderstrepingstekens en punten bevatten. Eventuele extra tekens worden verwijderd. </p> </td> 
   <td colname="col2"> <p>De variabele met contextgegevens <code> login_page-home</code> automatisch wordt <code> login_pagehome</code>. Alle gegevens die naar de <code> login_page-home</code> variabele wordt toegewezen onder <code> login_pagehome</code>. </p> <p>Contextgegevensvariabelen die niet-ondersteunde tekens bevatten, kunnen niet worden toegevoegd aan de interface Verwerkingsregels. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Caret (^) is een speciaal karakter in het systeem van verwerkingsregels. </p> </td> 
   <td colname="col2"> <p>Gebruik twee invoegtekens (^) om overeen te komen met één invoegteken. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Voorwaarden voor verwerkingsregel {#section_387390EEE9BA4DA98698522A84326DB4}

De voorwaarden controleren paginariabelen voor een passende waarde of als een waarde aanwezig is. U kunt meerdere voorwaarden toevoegen en u kunt kiezen of aan alle voorwaarden moet worden voldaan.

U kunt een regel zonder voorwaarden maken om gedefinieerde handelingen altijd uit te voeren.

Variabelen worden niet automatisch gecontroleerd op waarden voordat handelingen worden uitgevoerd. Bijvoorbeeld, bevat Prop1 een waarde van &quot;iets&quot;, en eVar1 is leeg. Als u Prop1 op gelijke eVar1 plaatst zullen beide waarden leeg zijn. Als u dit moet vermijden, voegt u een voorwaarde toe om de aanwezigheid van een waarde te controleren.

## Handelingen voor regelverwerking {#section_E2285C9D008442C7BF136E52A9A4CC06}

Met handelingen worden paginariabelen ingesteld, paginariabelen verwijderd of gebeurtenissen geactiveerd. Handelingen kunnen ook waarden samenvoegen die in een rapport worden weergegeven.

U kunt bijvoorbeeld `category:product` door twee variabelen samen te voegen.
