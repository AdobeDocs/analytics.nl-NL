---
description: Bestandsindelingen die worden ondersteund door classificatiesets
title: Bestandsindelingen voor classificatieset
feature: Classifications
source-git-commit: 2d9eb9179ace40a8d333883cea78dd67329078ab
workflow-type: tm+mt
source-wordcount: '1023'
ht-degree: 0%

---

# Bestandsindelingen voor classificatieset

Classificatiesets ondersteunen meerdere bestandsindelingen voor indelingsgegevens voor het uploaden van grote hoeveelheden. Elke indeling heeft specifieke vereisten voor het uploaden van gegevens.

Wanneer het bestand correct is opgemaakt volgens deze specificaties, kunt u het uploaden via de interface of API voor classificatiesets. Voor gedetailleerde uploadinstructies:

* **Browser uploadt**: Zie [&#x200B; Schema &#x200B;](manage/schema.md)
* **API uploadt**: Zie [&#x200B; Classificaties API van Analytics &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/classifications/)

Classificatiesets ondersteunen de volgende bestandsindelingen:

* **JSON**: De dossiers van de Nota van de Objecten van JavaScript met gestructureerde gegevens
* **CSV**: komma-gescheiden waardedossiers
* **TSV/TAB**: lusje-gescheiden waardedossiers

## Algemene bestandsvereisten

Alle bestandsindelingen moeten aan de volgende vereisten voldoen:

* **het coderen van het Dossier**: Gebruik UTF-8 zonder byte-orde tekens. Latin1-codering wordt ook ondersteund.
* **de grenzen van het Karakter**: De individuele classificatiewaarden hebben een maximumgrens van 255 bytes.
* **Zeer belangrijke vereisten**: De zeer belangrijke waarden kunnen niet leeg zijn of slechts whitespace bevatten. Als dubbele sleutels aanwezig zijn, wordt het laatste voorkomen gebruikt.

+++**JSON formaatdetails**

De JSON-bestandsindeling volgt conventies voor JSON Lines (JSONL). Het bestand moet één JSON-object per regel bevatten, waarbij elk object één classificatierecord vertegenwoordigt.

>[!NOTE]
>
>Gebruik, ondanks de volgende conventies voor JSON Lines, de bestandsextensie `.json` voor alle uploads. Het gebruik van de extensie `.jsonl` kan leiden tot fouten.

### JSON-structuur

Elk JSON-object moet het volgende bevatten:

* `key` (vereist): De unieke id voor het classificatierecord
* `data` (vereist voor updates): een object dat de namen en waarden van classificatiekolom bevat
* `action` (optioneel): De handeling die moet worden uitgevoerd. Tot de ondersteunde waarden behoren:
   * `update` (standaardwaarde)
   * `delete-field`
   * `delete-key`
* `enc` (optioneel): specificatie voor gegevenscodering. Tot de ondersteunde waarden behoren:
   * `utf8` of `UTF8` (standaardwaarde)
   * `latin1` of `LATIN1`

Alle JSON-veldnamen (`key`, `data`, `action`, `enc`) zijn hoofdlettergevoelig en moeten in kleine letters worden geschreven.

### JSON-voorbeelden

**Basis updaterecord:**

```json
{"key": "product123", "data": {"Product Name": "Basketball Shoes", "Brand": "Brand A", "Category": "Sports"}}
```

**Update met gespecificeerde het coderen:**

```json
{"key": "product456", "enc": "utf8", "data": {"Product Name": "Running Shoes", "Brand": "Brand B"}}
```

**Schrap specifieke gebieden:**

```json
{"key": "product789", "action": "delete-field", "data": {"Brand": null, "Category": null}}
```

**Schrap volledige sleutel:**

```json
{"key": "product999", "action": "delete-key"}
```

### JSON-validatieregels

* Het veld `key` is vereist en mag niet null of leeg zijn.
* Voor `update` -handelingen is het veld `data` vereist en mag het niet leeg zijn.
* Voor `delete-field` -handelingen moet het veld `data` de velden bevatten die moeten worden verwijderd.
* Voor `delete-key` -handelingen mag het veld `data` niet aanwezig zijn.
* Ondersteunde coderingswaarden zijn niet hoofdlettergevoelig en bevatten standaardnamen voor tekensets.

+++

+++**CSV formaatdetails**

CSV-bestanden (met door komma&#39;s gescheiden waarden) gebruiken komma&#39;s om classificatiegegevensvelden te scheiden.

### CSV-structuur

* **de rij van de Kopbal**: De eerste rij moet kolomkopballen bevatten en de eerste kolom moet de belangrijkste kolom zijn. De volgende kolommen zouden namen in uw schema van de classificatieset van u moeten aanpassen
* **de rijen van Gegevens**: Elke verdere rij bevat classificatiegegevens
* **Scheidingstekens**: De gebieden worden gescheiden door komma&#39;s
* **het Citeren**: De gebieden die komma&#39;s, citaten, of newlines bevatten zouden in dubbele citaten moeten worden ingesloten

### CSV-voorbeelden

**Basisclassificatiegegevens:**

```csv
Key,Product Name,Brand,Category,Price
product123,"Basketball Shoes",Brand A,Sports,89.99
product456,"Running Shoes",Brand B,Sports,79.99
product789,"Winter Jacket",Brand C,Clothing,149.99
```

**Schrap volledige sleutel:**

```csv
Key,Product Name,Brand,Category,Price
product999,~deletekey~,,,
```

**Schrap specifieke gebieden (gemengd met updates):**

```csv
Key,Product Name,Brand,Category,Price
product123,"Updated Product Name",Brand A,Sports,89.99
product456,,~empty~,~empty~,79.99
```

### CSV-opmaakregels

* Velden met komma&#39;s moeten tussen dubbele aanhalingstekens staan
* Velden met dubbele aanhalingstekens moeten zonder aanhalingstekens (`""`)
* Lege velden vertegenwoordigen null-waarden voor die classificatie
* Regelafstand en volgspaties rond velden worden automatisch bijgesneden
* Speciale tekens (tabs, nieuwe regels) in opgegeven velden blijven behouden

**de verrichtingen van de Schrapping:**
* Gebruik `~deletekey~` in elk veld om de gehele sleutel en alle classificatiegegevens te verwijderen
* Gebruik `~empty~` in specifieke velden om alleen die classificatiewaarden te verwijderen (laat andere velden intact)
* Als u `~empty~` gebruikt, kunt u verwijderingen combineren met updates in hetzelfde bestand

+++

+++**TSV/TAB formaatdetails**

TSV (Door tabs gescheiden waarden) en TAB-bestanden gebruiken tabtekens om classificatiegegevensvelden te scheiden.

### TSV/TAB-structuur

* **de rij van de Kopbal**: De eerste rij moet kolomkopballen bevatten en de eerste kolom moet de belangrijkste kolom zijn. De volgende kolommen zouden namen in uw schema van de classificatieset van u moeten aanpassen
* **de rijen van Gegevens**: Elke verdere rij bevat classificatiegegevens
* **Scheidingstekens**: De gebieden worden gescheiden door lusjekarakters (`\t`)
* **het Citeren**: Over het algemeen is geen het citeren nodig, maar sommige implementaties steunen geciteerde gebieden

### Voorbeelden van TSV/TAB

**Basisclassificatiegegevens:**

```tsv
Key    Product Name    Brand    Category    Price
product123    Basketball Shoes    Brand A    Sports    89.99
product456    Running Shoes    Brand B    Sports    79.99
product789    Winter Jacket    Brand C    Clothing    149.99
```

**Schrap volledige sleutel:**

```tsv
Key    Product Name    Brand    Category    Price
product999    ~deletekey~            
```

**Schrap specifieke gebieden (gemengd met updates):**

```tsv
Key    Product Name    Brand    Category    Price
product123    Updated Product Name    Brand A    Sports    89.99
product456        ~empty~    ~empty~    79.99
```

### Opmaakregels voor TSV/TAB

* Velden worden gescheiden door enkele tabtekens
* Lege velden (opeenvolgende tabbladen) vertegenwoordigen null-waarden
* Er is doorgaans geen speciale aanhalingstekens vereist
* De regelafstand en de volgspaties blijven behouden
* Nieuwe regeltekens binnen velden moeten worden vermeden

**de verrichtingen van de Schrapping:**
* Gebruik `~deletekey~` in elk veld om de gehele sleutel en alle classificatiegegevens te verwijderen
* Gebruik `~empty~` in specifieke velden om alleen die classificatiewaarden te verwijderen (laat andere velden intact)
* Als u `~empty~` gebruikt, kunt u verwijderingen combineren met updates in hetzelfde bestand

+++

## Foutafhandeling

Veelvoorkomende uploadproblemen en oplossingen:

### Algemene fouten in bestandsindelingen

* **Ongeldig dossierformaat**: Verifieer dat uw dossieruitbreiding het inhoudsformaat (.json, .csv, .tsv, of .tab) aanpast.
* **&quot;Onbekende kopbal&quot;**: De namen van de kolom moeten uw schema van de classificatieset (van toepassing is op alle formaten) aanpassen.

### Specifieke fouten CSV/TSV

* **&quot;Eerste kolom wordt vereist om sleutel te zijn&quot;**: Zorg ervoor uw CSV/TSV- dossier een juiste kopbalrij met de belangrijkste kolom eerst heeft.
* **&quot;Een minimum van twee kopbalpunten wordt vereist&quot;**: CSV/TSV- dossiers moeten minstens een &quot;Zeer belangrijke&quot;kolom en één classificatiekolom hebben.
* **&quot;De eerste kopbalkolom moet &quot;Sleutel&quot;worden genoemd**: De eerste kolomkopbal moet precies &quot;Sleutel&quot;zijn (hoofdletter K, hoofdlettergevoelig).
* **&quot;Lege kopballen zijn niet toegestaan&quot;**: Alle CSV/TSV kolomkopballen moeten namen hebben.
* **&quot;Het aantal kolommen kwam niet de kopballen aan&quot;**: Elke CSV/TSV- gegevensrij moet het zelfde aantal gebieden hebben zoals de kopbalrij.
* **&quot;Onjuist geformuleerd document&quot;**: Controle CSV citeert, juiste lusjescheiding in TSV dossiers, etc.

### JSON-specifieke fouten

* **&quot;Sleutel is een vereist gebied&quot;**: Alle JSON verslagen moeten een niet-leeg `"key"` gebied (kleine letters, hoofdlettergevoelig) hebben.
* **&quot;Gegevens is een vereist gebied wanneer het gebruiken van action=update&quot;**: de acties van de JSON update moeten a `"data"` gebied omvatten.
* **&quot;Gegevens is een vereist gebied wanneer het gebruiken van action=delete-field&quot;**: JSON schrapping-gebied de acties moeten specificeren welke gebieden op het `"data"` gebied te schrappen.
* **&quot;Gegevens moeten niet aanwezig zijn wanneer het gebruiken van action=delete-key&quot;**: JSON schrapping-zeer belangrijke acties kunnen geen a `"data"` gebied omvatten.
* **&quot;Niet gestaafde het coderen&quot;**: Gebruik slechts gesteunde het coderen waarden op het `"enc"` gebied (utf8, UTF8, latin1, LATIN1).
* **Ongeldige JSON syntaxis**: Zorg ervoor dat het JSON dossier correct na overeenkomsten JSONL wordt geformatteerd. Controleer ook op algemene JSON-opmaak, ontbrekende aanhalingstekens, komma&#39;s, vierkante haken, enzovoort.

### Fouten in groottebeperking

* **&quot;Sleutel overschrijdt maximumgrootte&quot;**: De individuele sleutels kunnen 255 bytes niet overschrijden.
* **de &quot;waarde van de Kolom overschrijdt maximumgrootte&quot;**: De individuele classificatiewaarden kunnen 255 bytes niet overschrijden.

## Best practices

* **grootte van het Dossier**: 50MB is de maximumdossiergrootte voor browser en API uploads.
* **verwerking van de Partij**: Voor grote datasets, overweeg het verdelen in kleinere dossiers.
* **bevestiging van Gegevens**: Test met een klein steekproefdossier alvorens grote datasets te uploaden.
* **Steun**: Houd exemplaren van uw brongegevensdossiers.
* **Incrementele updates**: Gebruik formaat JSON voor nauwkeurige controle over individuele verslagupdates en schrappingen.
