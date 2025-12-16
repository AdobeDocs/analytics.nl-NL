---
description: Begrijp de diverse dossierformaten die classificatiesets steunen
title: Bestandsindelingen voor classificatieset
feature: Classifications
exl-id: f3d429be-99d5-449e-952e-56043b109411
source-git-commit: 0f80bb314c8e041a98af26734d56ab364c23a49b
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 0%

---

# Bestandsindelingen voor classificatieset

Classificatiesets ondersteunen meerdere bestandsindelingen voor het uploaden van classificatiegegevens. Elke indeling heeft specifieke vereisten voor het uploaden van gegevens.

Wanneer het bestand correct is opgemaakt volgens deze specificaties, kunt u de gegevens uploaden via de interface of API voor classificatiesets. Voor gedetailleerde uploadinstructies:

* **Browser uploadt**: Zie [ uploaden ](manage/schema.md#upload) in de [ interface van het Schema ](manage/schema.md) voor een classificatiereeks.
* **API uploadt**: Zie [ Classificaties API van Analytics ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/)

Classificatiesets ondersteunen de volgende bestandsindelingen:

* **JSON**: De dossiers van de Nota van de Objecten van JavaScript met gestructureerde gegevens
* **CSV**: komma-gescheiden waardedossiers
* **TSV of TAB**: Lusje-gescheiden waardedossiers

## Algemene bestandsvereisten

Alle bestandsindelingen moeten aan de volgende vereisten voldoen:

* **het coderen van het Dossier**: Gebruik UTF-8 zonder byte-orde tekens. Latin1-codering wordt ook ondersteund.
* **de grenzen van het Karakter**: De individuele classificatiewaarden hebben een maximumgrens van 255 bytes.
* **Zeer belangrijke vereisten**: De zeer belangrijke waarden kunnen niet leeg zijn of slechts whitespace bevatten. Als dubbele sleutels aanwezig zijn, wordt het laatste voorkomen gebruikt.

+++ Details JSON-indeling

De JSON-bestandsindeling volgt conventies voor JSON Lines (JSONL). Het bestand moet één JSON-object per regel bevatten, waarbij elk object één classificatierecord vertegenwoordigt.

>[!NOTE]
>
>Gebruik, ondanks het volgen van de conventies voor JSON Lines, de bestandsextensie `.json` voor alle uploads. Het gebruik van de extensie `.jsonl` kan leiden tot fouten.

### JSON-structuur

Elk JSON-object moet het volgende bevatten:

* `key` (vereist): De unieke id voor het classificatierecord
* `data` (vereist voor updates): een object dat de namen en waarden van classificatiekolom bevat
* `action` (optioneel): De handeling die moet worden uitgevoerd. Tot de ondersteunde waarden behoren:
   * `update` (de standaardactie, wanneer geen actie is opgegeven)
   * `delete-field`
   * `delete-key`
* `enc` (optioneel): specificatie voor gegevenscodering. Tot de ondersteunde waarden behoren:
   * `utf8` of `UTF8` (standaardwaarde)
   * `latin1` of `LATIN1`

Alle JSON-veldnamen (`key`, `data`, `action`, `enc`) zijn hoofdlettergevoelig en moeten in kleine letters worden geschreven.

### JSON-validatieregels

* Het veld `key` is vereist en mag niet null of leeg zijn.
* Voor `update` -handelingen is het veld `data` vereist en mag het niet leeg zijn.
* Voor `delete-field` -handelingen moet het veld `data` de velden bevatten die moeten worden verwijderd.
* Voor `delete-key` -handelingen mag het veld `data` niet aanwezig zijn.
* Ondersteunde coderingswaarden zijn niet hoofdlettergevoelig en bevatten standaardnamen voor tekensets.

### JSON-voorbeelden

Enkele voorbeelden van JSON-records in een JSON-bestand.

#### Basis update-record

```json
{"key": "product123", "data": {"Product Name": "Basketball Shoes", "Brand": "Brand A", "Category": "Sports"}}
```

#### Bijwerken met opgegeven codering

```json
{"key": "product456", "enc": "utf8", "data": {"Product Name": "Running Shoes", "Brand": "Brand B"}}
```

#### Specifieke velden verwijderen

```json
{"key": "product789", "action": "delete-field", "data": {"Brand": null, "Category": null}}
```

#### Een volledige toets verwijderen

```json
{"key": "product999", "action": "delete-key"}
```


+++

+++ CSV-indelingsdetails

CSV-bestanden (met door komma&#39;s gescheiden waarden) gebruiken komma&#39;s om classificatiegegevensvelden te scheiden.

### CSV-structuur

* **de rij van de Kopbal**: De eerste rij moet kolomkopballen bevatten en de eerste kolom moet de belangrijkste kolom zijn. De volgende kolommen zouden namen in uw schema van de classificatieset van u moeten aanpassen
* **de rijen van Gegevens**: Elke verdere rij bevat classificatiegegevens
* **Scheidingstekens**: De gebieden worden gescheiden door komma&#39;s
* **het Citeren**: De gebieden die komma&#39;s, citaten, of newlines bevatten zouden in dubbele citaten moeten worden ingesloten

### CSV-opmaakregels

* Velden met komma&#39;s moeten tussen dubbele aanhalingstekens staan.
* Velden die dubbele aanhalingstekens bevatten, moeten aanhalingstekens omzeilen door deze te verdubbelen (`""`).
* Lege velden vertegenwoordigen null-waarden voor die classificatie.
* Voorloopspaties en volgspaties rond velden worden automatisch bijgesneden.
* Speciale tekens (tabs, newlines) in velden met een citaat blijven behouden.

### CSV-verwijderbewerkingen

* Gebruik `~deletekey~` in elk veld om de gehele sleutel en alle classificatiegegevens te verwijderen
* Gebruik `~empty~` in specifieke velden om alleen die classificatiewaarden te verwijderen (laat andere velden intact)
* Als u `~empty~` gebruikt, kunt u verwijderingen combineren met updates in hetzelfde bestand

### CSV-voorbeelden

Voorbeelden van CSV-records in een CSV-bestand.

#### Basisclassificatiegegevens

```csv
Key,Product Name,Brand,Category,Price
product123,"Basketball Shoes",Brand A,Sports,89.99
product456,"Running Shoes",Brand B,Sports,79.99
product789,"Winter Jacket",Brand C,Clothing,149.99
```

#### Een volledige toets verwijderen

```csv
Key,Product Name,Brand,Category,Price
product999,~deletekey~,,,
```

#### Specifieke velden verwijderen (gemengd met updates)

```csv
Key,Product Name,Brand,Category,Price
product123,"Updated Product Name",Brand A,Sports,89.99
product456,,~empty~,~empty~,79.99
```

+++

+++ VVV- en TAB-formaatgegevens

TSV (Door tabs gescheiden waarden) en TAB-bestanden gebruiken tabtekens om classificatiegegevensvelden te scheiden.

### TSV- en TAB-structuur

* **de rij van de Kopbal**: De eerste rij moet kolomkopballen bevatten en de eerste kolom moet de belangrijkste kolom zijn. De volgende kolommen zouden namen in uw schema van de classificatieset van u moeten aanpassen.
* **de rijen van Gegevens**: Elke verdere rij bevat classificatiegegevens.
* **Scheidingstekens**: De gebieden worden gescheiden door lusjekarakters (`\t`).
* **het Citeren**: Over het algemeen is geen het citeren nodig, maar sommige implementaties steunen geciteerde gebieden.

### Opmaakregels voor TSV en TAB

* Velden worden gescheiden door enkele tabtekens.
* Lege velden (opeenvolgende tabbladen) vertegenwoordigen null-waarden.
* Er is doorgaans geen speciale aanhalingstekens vereist.
* De voorloopspaties en de navolgende spaties blijven behouden.
* Nieuwe regeltekens binnen velden moeten worden vermeden.

### TSV- en TAB-verwijderingsbewerkingen

* Gebruik `~deletekey~` in elk veld om de gehele sleutel en alle classificatiegegevens te verwijderen.
* Gebruik `~empty~` in specifieke velden om alleen die classificatiewaarden te verwijderen (en laat andere velden intact).
* Als u `~empty~` gebruikt, kunt u verwijderingen combineren met updates in hetzelfde bestand.

### Voorbeelden van TSV en TAB

Voorbeelden van door TSV of TAB gescheiden records in een TSV- of TAB-bestand.

#### Basisclassificatiegegevens

```tsv
Key    Product Name    Brand    Category    Price
product123    Basketball Shoes    Brand A    Sports    89.99
product456    Running Shoes    Brand B    Sports    79.99
product789    Winter Jacket    Brand C    Clothing    149.99
```

#### Een volledige toets verwijderen

```tsv
Key    Product Name    Brand    Category    Price
product999    ~deletekey~            
```

#### Specifieke velden verwijderen (gemengd met updates)

```tsv
Key    Product Name    Brand    Category    Price
product123    Updated Product Name    Brand A    Sports    89.99
product456        ~empty~    ~empty~    79.99
```

+++

## Foutafhandeling

Algemene problemen en oplossingen bij het uploaden van bestanden:

### Algemene fouten in bestandsindelingen

* **Ongeldig dossierformaat**: Verifieer dat uw dossieruitbreiding het inhoudsformaat (`.json` aanpast, `.csv`, `.tsv`, of `.tab`).
* **Onbekende kopbal**: De namen van de kolom moeten uw schema van de classificatieset (op alle formaten van toepassing is) aanpassen.

### JSON-specifieke fouten

* **Sleutel is een vereist gebied**: Alle JSON- verslagen moeten een niet leeg `"key"` gebied (in kleine letters, case-sensitive) hebben.
* **Gegevens is een vereist gebied wanneer het gebruiken van action=update**: JSON de updateacties moeten a `"data"` gebied omvatten.
* **Gegevens is een vereist gebied wanneer het gebruiken van action=delete-field**: JSON schrap-gebied acties moet specificeren welke gebieden op het `"data"` gebied te schrappen.
* **Gegevens moeten niet aanwezig zijn wanneer het gebruiken van action=delete-key**: JSON schrapt-zeer belangrijke acties kunnen a `"data"` gebied niet omvatten.
* **niet gestaafde het coderen**: Gebruik slechts gesteunde het coderen waarden op het `"enc"` gebied (`utf8`, `UTF8`, `latin1`, `LATIN1`).
* **Ongeldige JSON syntaxis**: Zorg ervoor dat het JSON dossier correct na overeenkomsten JSONL wordt geformatteerd. Controleer ook op algemene JSON-opmaak, ontbrekende aanhalingstekens, komma&#39;s, vierkante haken, enzovoort.


### Specifieke fouten voor CSV en TSV

* **de eerste kolom wordt vereist om sleutel** te zijn: Zorg ervoor uw CSV of TSV dossier een juiste kopbalrij met de belangrijkste kolom eerst heeft.
* **een minimum van twee kopbalpunten wordt vereist**: CSV of TSV- dossiers moeten minstens a `Key` kolom en één classificatiekolom hebben.
* **de eerste kopbalkolom moet &quot;Sleutel&quot;worden genoemd**: De eerste kolomkopbal moet precies `Key` zijn (kapitaal `K`, case-sensitive).
* **Lege kopballen worden niet toegestaan**: Alle CSV/TSV kolomkopballen moeten namen hebben.
* **het aantal kolommen paste niet de kopballen** aan: Elke CSV of TSV gegevensrij moet het zelfde aantal gebieden zoals de kopbalrij hebben.
* **&quot;Onjuist geformuleerd document**: controleer CSV citerend, juiste lusjescheiding in TSV dossiers, en meer.


### Fouten in groottebeperking

* **Sleutel overschrijdt maximumgrootte**: De individuele sleutels kunnen 255 bytes niet overschrijden.
* **de waarde van de Kolom overschrijdt maximumgrootte**: De individuele classificatiewaarden kunnen 255 bytes niet overschrijden.

## Best practices

* **grootte van het Dossier**: 50MB is de maximumdossiergrootte voor browser en API uploads.
* **verwerking van de Partij**: Voor grote datasets, overweeg het verdelen in kleinere dossiers.
* **bevestiging van Gegevens**: Test met een klein steekproefdossier alvorens grote datasets te uploaden.
* **Steun**: Houd exemplaren van uw brongegevensdossiers.
* **Incrementele updates**: Gebruik het formaat JSON voor nauwkeurige controle over individuele verslagupdates en schrappingen.
