---
title: Problemen met importmodule voor classificatie
description: Algemene upload problemen bij gebruik van de classificatieimporteur.
feature: Classifications
exl-id: de3e9eca-9264-4711-b73a-4a1a3dd16715
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# Problemen met importmodule voor classificatie

De meest voorkomende problemen bij het uploaden van classificatiegegevens naar Adobe.

## Onjuiste bestandsindeling of extensie

Voor classificaties zijn een specifiek bestandstype en een specifieke indeling vereist om het uploaden te voltooien. Als het niet correct wordt opgeslagen, veroorzaakt het een fout en verwerkt geen rijen. De geretourneerde fout komt vaak voor *&quot;De eerste kolom moet de sleutel zijn&quot;*, maar kan een willekeurig aantal fouten zijn. Controleer het volgende:

* **Een spreadsheet (.xlsx) in plaats van een .tab- of .txt-bestand uploaden**: U kunt het foutbericht ophalen *&quot;De eerste kolom moet de sleutel zijn&quot;* wanneer u classificatiebestanden in een onjuiste indeling uploadt. De rubriceringsimporter weet niet hoe te om .xls of .xlsx dossiers te behandelen. Stel in het dialoogvenster Opslaan als in Excel het juiste type Opslaan als in:
   * Gebruik in Windows de bestandsindeling `Text (Tab delimited) (*.txt)`
   * Gebruik in Mac de bestandsindeling `Windows Formatted Text`.
* **De bestandsnaamextensie wijzigen nadat deze als een werkboek is opgeslagen**: Wanneer u probeert de naam van een bestandsextensie rechtstreeks te wijzigen, wordt een ongeldig werkboek gegenereerd. Gebruik slechts sparen van Excel als functie of geef classificaties in een tekstredacteur zoals Blocnote+ uit.
* **Hoofdletters gebruiken**: Extensies in hoofdletters (zoals `fileupload.TXT`) werken niet. Wijzig de naam van het bestand in een kleine extensie (`fileupload.txt`).
* **Niet-overeenkomende tekencodering**: Zorg ervoor dat de codering van het geüploade bestand overeenkomt met de oorspronkelijke codering wanneer de sjabloon is gedownload. Als u een UTF-16-bestand uploadt toen het oorspronkelijk in UTF-8 was gecodeerd, resulteren uploads in onverwachte resultaten. Adobe raadt aan bestanden te uploaden met UTF-8 zonder bytevolgordetekens.

## Ongeldige bestandsinhoud

Als het uploadbestand de juiste indeling heeft, probeert de uploader zoveel mogelijk geldige rijen te importeren. Enkele algemene problemen met classificatiegegevens:

* **Rijen die al zijn geclassificeerd**: Wanneer wordt geprobeerd rijen te uploaden die al met dezelfde waarde zijn geclassificeerd, retourneert de importer rijen die geen effect hadden. Dit resultaat wordt verwacht, aangezien classificaties een sleutelwaarde met dezelfde classificatie niet opnieuw classificeren. Het is een melding in plaats van een fout. U hoeft zich geen zorgen te maken als u niet alle rijen in een exportbestand wijzigt. Adobe raadt alleen gewijzigde rijen aan.
* **Koptekst komt niet overeen met de variabele die wordt geüpload**: Als u een classificatiesjabloon downloadt voor de dimensie van de code Volgend en probeert deze te uploaden naar een eVar-classificatie, mislukt dit. Gebruik exportbestanden alleen voor de specifieke variabelen waaruit ze zijn geëxporteerd.
* **Een sleutel of classificatiewaarde bevat de waarde 0**: Classificaties kunnen de waarde 0 niet onderscheiden van een lege cel, zodat deze waarde niet kan worden geclassificeerd. Zie [Veelgestelde vragen over classificaties](../faq.md).
* **Het classificatiebestand bevat komma&#39;s of speciale tekens**: Zie [Veelgestelde vragen over classificaties](../faq.md).
* **Extra tabbladen in het geüploade bestand**: Soms kan bij het bewerken van classificatiebestanden per ongeluk een extra tabblad worden weggeplakt. Voor een correcte verwerking van elke rij is een identiek aantal tabbladen vereist. Als u wilt controleren op extra tabbladen in het bestand, markeert u alle tekst in een teksteditor en zorgt u ervoor dat er aan het einde geen rijen meer ruimte hebben.
* **Er bestaan dubbele sleutelwaarden in het bestand**: Elke sleutelwaarde kan slechts één classificatie per kolom hebben. Als u probeert dezelfde waarde meerdere keren te classificeren, genereert de importer een fout.
* **Subclassificaties bestaan en zijn onjuist geconfigureerd**: Indien er subclassificaties bestaan, controleer het volgende:
   * Alle subclassificatiewaarden hebben een bovenliggende classificatiewaarde
   * Geen twee subclassificaties verwijzen naar dezelfde bovenliggende classificatiewaarde
* **Kolom komt niet overeen**: U kunt het foutbericht ophalen *&quot;De toets op regel heeft te veel kolommen&quot;* als er een ongeldig aantal kolommen op een bepaalde rij staat. U hebt bijvoorbeeld 3 kolommen in het uploaden van de classificatie en de variabele heeft slechts één classificatie. Valideer uw uploadbestand om ervoor te zorgen dat het aantal kolommen niet groter is dan het aantal classificaties dat voor die variabele is geconfigureerd.

## FTP-import problemen oplossen

De volgende oorzaken komen vaak voor bij FTP-classificaties die geen geüploade bestanden verwerken:

* **Ontbrekend .fin-bestand**: Maak een leeg tekstdocument op uw bureaublad en wijzig de naam van de bestandsextensie van .txt in .fin. De naam van dit .fin-bestand moet overeenkomen met de naam van het classificatiebestand in kwestie. Als uw FTP-bestandsnaam bijvoorbeeld `fileupload.tab`, geef uw .fin-bestand een naam `fileupload.fin`. Nadat het .fin-bestand is geüpload, verdwijnen beide bestanden.
* **.fin-bestand uploaden vóór classificatiebestand**: Soms wordt een .fin gecreeerd alvorens het classificatiedossier wordt gebeëindigd uploadend aan de plaats van FTP. De verwerking kan mislukken wanneer bestanden buiten bestelling worden geüpload. Verwijder beide bestanden, voeg eerst het classificatiebestand toe en daarna het .fin-bestand nadat het classificatiebestand volledig is geüpload.
* **Bestandsgrootte is te groot**: Adobe beveelt aan de bestandsgrootte van classificatiebestanden zo klein mogelijk te houden om een snelle verwerking te garanderen.
* **Bestaande bestanden worden al verwerkt**: Als er meerdere bestanden zijn geüpload voor dezelfde variabele en rapportsuite, stopt het oude bestand met de verwerking ten gunste van de nieuwe. Als classificaties worden geüpload met meerdere bestanden, wacht u op bevestiging dat bestaande bestanden klaar zijn met verwerken voordat u nieuwe bestanden uploadt.
* **Geüploade bestanden worden niet in de hoofdmap geplaatst**: Bestanden die naar de FTP-site Adobe zijn geüpload, moeten in de hoofdmap worden geplaatst. Als classificatieimportbestanden in submappen worden geplaatst, worden ze niet opgehaald of verwerkt.

Neem contact op met de klantenservice van Adobe als u nog steeds problemen hebt met het uploaden van een classificatiebestand.
