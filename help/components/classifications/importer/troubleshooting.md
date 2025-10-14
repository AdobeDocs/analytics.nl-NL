---
title: Problemen met importmodule voor classificatie
description: Algemene upload problemen bij gebruik van de classificatieimporteur.
feature: Classifications
exl-id: de3e9eca-9264-4711-b73a-4a1a3dd16715
source-git-commit: 4eea524bf95c9b6bc9ddc878c8c433bc1e60daee
workflow-type: tm+mt
source-wordcount: '875'
ht-degree: 0%

---

# Problemen met importmodule voor classificatie

{{classification-importer-deprecation}}

De meest voorkomende problemen bij het uploaden van classificatiegegevens naar Adobe.

## Onjuiste bestandsindeling of extensie

Voor classificaties zijn een specifiek bestandstype en een specifieke indeling vereist om het uploaden te voltooien. Als het niet correct wordt opgeslagen, veroorzaakt het een fout en verwerkt geen rijen. De teruggekeerde fout is vaak *&quot;Eerste kolom wordt vereist om de sleutel&quot;* te zijn, maar kan om het even welk aantal fouten zijn. Controleer het volgende:

* **Uploadend een spreadsheet (.xlsx) in plaats van een .tab of .txt dossier**: U kunt het foutenbericht *krijgen &quot;De eerste kolom wordt vereist om sleutel&quot;* te zijn wanneer u classificatiedossiers in een onjuist formaat uploadt. De rubriceringsimporter weet niet hoe te om .xls of .xlsx dossiers te behandelen. Stel in het dialoogvenster Opslaan als in Excel het juiste type Opslaan als in:
   * Gebruik in Windows de bestandsindeling `Text (Tab delimited) (*.txt)`
   * Gebruik in Mac de bestandsindeling `Windows Formatted Text` .
* **Veranderend de filename uitbreiding na het opslaan van het als werkboek**: Het proberen om een dossieruitbreiding direct anders te noemen produceert een ongeldig werkboek. Gebruik slechts sparen van Excel als functie of geef classificaties in een tekstredacteur zoals Blocnote+ uit.
* **Gebruikend in hoofdletters uitbreidingen**: De uitbreidingen in hoofdletters (zoals `fileupload.TXT`) werken niet. Wijzig de naam van het bestand in een kleine extensie (`fileupload.txt`).
* **Verkeerd karakter het coderen**: Ben zeker dat het coderen van de bewaarde classificatie uploadt de originele codering aanpast toen het malplaatje werd gedownload. Als u een UTF-16-bestand uploadt toen het oorspronkelijk in UTF-8 was gecodeerd, resulteren uploads in onverwachte resultaten. Adobe raadt aan bestanden te uploaden met UTF-8 zonder bytevolgordetekens.

## Ongeldige bestandsinhoud

Als het uploadbestand de juiste indeling heeft, probeert de uploader zoveel mogelijk geldige rijen te importeren. Enkele algemene problemen met classificatiegegevens:

* **Rijen die reeds geclassificeerd** zijn: Wanneer het proberen om rijen te uploaden die reeds met de zelfde waarde worden geclassificeerd, keert de importeur rijen terug die geen effect hadden. Dit resultaat wordt verwacht, aangezien classificaties een sleutelwaarde met dezelfde classificatie niet opnieuw classificeren. Het is een melding in plaats van een fout. U hoeft zich geen zorgen te maken als u niet alle rijen in een exportbestand wijzigt. Adobe raadt alleen gewijzigde rijen aan.
* **de Kopbal past niet de variabele aan die** wordt geupload: Als u een classificatiesjabloon voor de het Volgen codedimensie downloadt en probeert om het aan een classificatie van eVar te uploaden, ontbreekt het. Gebruik exportbestanden alleen voor de specifieke variabelen waaruit ze zijn geëxporteerd.
* **de sleutel of de classificatiewaarde van A bevat waarde 0**: De classificaties kunnen niet waarde 0 van een lege cel onderscheiden, zodat kan het deze waarde niet classificeren. Zie [&#x200B; Veelgestelde vragen van de Importeur van de Classificatie &#x200B;](importer-faq.md) voor meer informatie.
* **het classificatiedossier bevat komma&#39;s of speciale karakters**: Zie [&#x200B; Veelgestelde vragen van de Importeur van de Classificatie &#x200B;](importer-faq.md) voor informatie over hoe te om waarden te ontsnappen.
* **Extra lusjes in het geuploade dossier**: Soms wanneer het uitgeven van classificatiedossiers, kan een extra lusje per ongeluk binnen worden gegist. Voor een correcte verwerking van elke rij is een identiek aantal tabbladen vereist. Als u wilt controleren op extra tabbladen in het bestand, markeert u alle tekst in een teksteditor en zorgt u ervoor dat er aan het einde geen rijen meer ruimte hebben.
* **de Dubbele zeer belangrijke waarden bestaan in het dossier**: Elke zeer belangrijke waarde kan één classificatie per kolom slechts hebben. Als u probeert dezelfde waarde meerdere keren te classificeren, genereert de importer een fout.
* **Subclassificaties bestaan en verkeerd gevormd** zijn: Als de subclassificaties bestaan, controleer het volgende:
   * Alle subclassificatiewaarden hebben een bovenliggende classificatiewaarde
   * Geen twee subclassificaties verwijzen naar dezelfde bovenliggende classificatiewaarde
* **de Kolom mismatch**: U kunt het foutenbericht *krijgen &quot;de sleutel op lijn heeft teveel kolommen&quot;* als er een ongeldig aantal kolommen op om het even welke bepaalde rij zijn. U hebt bijvoorbeeld 3 kolommen in het uploaden van de classificatie en de variabele heeft slechts één classificatie. Valideer uw uploadbestand om ervoor te zorgen dat het aantal kolommen niet groter is dan het aantal classificaties dat voor die variabele is geconfigureerd.

## FTP-import problemen oplossen

De volgende oorzaken komen vaak voor bij FTP-classificaties die geen geüploade bestanden verwerken:

* **Ontbrekend .fin- dossier**: Creeer een leeg tekstdocument op uw Desktop en noem filename uitbreiding van .txt aan .fin anders. De naam van dit .fin-bestand moet overeenkomen met de naam van het classificatiebestand in kwestie. Als uw FTP-bestandsnaam bijvoorbeeld `fileupload.tab` is, geeft u het .fin-bestand `fileupload.fin` een naam. Nadat het .fin-bestand is geüpload, verdwijnen beide bestanden.
* **Uploading .fin- dossier vóór classificatiedossier**: Soms wordt .fin gecreeerd alvorens het classificatiedossier wordt gebeëindigd uploadend aan de plaats van FTP. De verwerking kan mislukken wanneer bestanden buiten bestelling worden geüpload. Verwijder beide bestanden, voeg eerst het classificatiebestand toe en daarna het .fin-bestand nadat het classificatiebestand volledig is geüpload.
* **de grootte van het Dossier is bovenmatig groot**: Adobe adviseert het houden van de grootte van het classificatiedossier zo klein mogelijk om snelle verwerking te verzekeren.
* **Bestaande dossiers verwerken reeds**: Als de veelvoudige dossiers voor de zelfde variabele en rapportreeks worden geupload, houdt het oude dossier verwerking ten gunste van nieuwe tegen. Als classificaties worden geüpload met meerdere bestanden, wacht u op bevestiging dat bestaande bestanden klaar zijn met verwerken voordat u nieuwe bestanden uploadt.
* **Geüploade dossiers die niet in wortelfolder** worden geplaatst: De dossiers die aan de plaats van FTP van Adobe worden geupload moeten in de wortelfolder worden geplaatst. Als classificatieimportbestanden in submappen worden geplaatst, worden ze niet opgehaald of verwerkt.

Neem contact op met de klantenservice van Adobe als er nog steeds problemen zijn met het uploaden van een classificatiebestand.
