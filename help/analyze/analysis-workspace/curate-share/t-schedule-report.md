---
description: Een Analysis Workspace-project verzenden via e-mail of het plannen voor levering.
keywords: Analysis Workspace
title: Projecten plannen
feature: Curate and Share
role: User, Admin
exl-id: 2d6854f7-8954-4d55-b2be-25981cfb348b
source-git-commit: 9b0b62691600a682bc53a3aa3b50b8addad32a41
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 0%

---

# Projecten plannen

Vanuit de werkruimte **Menu Delen**, kunt u Analysis Workspace-projecten via e-mail naar geselecteerde ontvangers verzenden. Bestanden kunnen in CSV- of PDF-indeling worden verzonden.

## Bestand nu verzenden

Een bestand direct via e-mail naar ontvangers verzenden:

1. Klikken **Delen > Bestand nu verzenden**.
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. Klikken **Nu verzenden**.
1. (Optioneel) Klik op **Planningsopties tonen** om een leveringsschema op te geven.

![Bestand nu verzenden](assets/send-file-now.png)

## Bestand verzenden volgens schema

Een bestand volgens een terugkerend schema via e-mail naar ontvangers verzenden:

1. Klikken **Delen > Bestand verzenden volgens schema**.
1. Geef het bestandstype op (CSV of PDF).
1. (Optioneel) Voeg een beschrijving toe die in de e-mail wordt opgenomen om uit te leggen welk bestand wordt ontvangen.
1. Voeg ontvangers of groepen toe. U kunt ook e-mailadressen invoeren.
1. Geef het bereik op waarover de planning moet worden geleverd door Starten op en Eindigen op de invoer te wijzigen. De einddatum moet binnen een jaar zijn vanaf de dag dat het schema wordt opgesteld of gewijzigd.
1. Geef de leveringsfrequentie op. Elke frequentie maakt verschillende aanpassingen mogelijk.
1. Klikken **Verzenden volgens schema**.

![](assets/send-on-schedule.png)

## Geplande projectmanager

Geplande Analysis Workspace-projecten kunnen worden beheerd in het kader van **Analyse > Componenten > Geplande projecten**.

In de Geplande Manager van Projecten, kunt u terugkomende projectprogramma&#39;s uitgeven en schrappen. Zoek naar een programma in de onderzoeksbar of door de filteropties in het linkerspoor te gebruiken. U kunt filteren op tag, goedgekeurde schema&#39;s, eigenaars en meer.

![](assets/scheduled-project-manager2.png)

| Veld | Beschrijving |
| --- | --- |
| Favorieten | Als u het sterpictogram selecteert, wordt dit schema een favoriet. |
| Plan-id | Deze id wordt vooral gebruikt voor foutopsporingsdoeleinden. |
| Titel en beschrijving | Titel en beschrijving van dit project. |
| Eigenaar | De persoon die het project heeft gemaakt en bezit. |
| Tags | (facultatief) het etiketteren is een goede manier om projecten te organiseren. Alle gebruikers kunnen labels maken en een of meer tags toepassen op een project. U kunt echter alleen labels zien voor de projecten die u hebt of die met u zijn gedeeld. |
| Afgeleverd aan | De ontvanger(s) van dit geplande project. |
| Vervaldatum | De standaardvervaldatum is één jaar vanaf de aanmaakdatum. |
| Frequentie | Hoe vaak wilt u dat dit planningsproject naar de ontvanger(s) wordt verzonden. |
| Uitvoeringstijd | Op welk tijdstip van de dag dit geplande project wordt verzonden. |
| Aantal query&#39;s | Het aantal vragen tegen dit project. |

## Gemeenschappelijke acties

Het volgende is gemeenschappelijke acties in de Geplande Manager van Projecten:

| Handeling | Beschrijving |
|---|---|
| **Tijdschema bewerken** | Klik op de titel van de planning om de leveringsinstellingen bij te werken. |
| **Schema verwijderen** | Selecteer het geplande project in de lijst en klik dan Schrapping van het menu. Hiermee verwijdert u het geselecteerde schema voor het project. het project zelf wordt niet verwijderd . |
| **Tags toevoegen** | Selecteer het geplande project in de lijst en kies &quot;Tag&quot; of &quot;Goedkeuren&quot; om uw schema&#39;s te ordenen en ze gemakkelijker te maken om naar te zoeken. |
| **Ontbroken schema&#39;s weergeven** | Navigeer naar de linkertrack > Overige filters > Kan geen mislukte planningen zien. |
| **Verlopen schema&#39;s weergeven** | Navigeer naar de linkerrail > Andere filters > Verlopen om programma&#39;s te zien die zijn verlopen. Klik de titel van het programma aan opstelling een nieuw leveringsprogramma. |
| **Plan-id weergeven** | Navigeer naar kolomopties rechtsboven en voeg de kolom Id van planning toe aan de tabel. De geplande id is vaak handig voor foutopsporing. |

De Geplande Manager van Projecten toont de punten die een specifieke gebruiker heeft gecreeerd. Als de gebruikersaccount in de toepassing is uitgeschakeld, worden alle geplande leveringen gestopt. De geplande projecteigendom kan worden **overgedragen** aan een nieuwe gebruiker onder **Beheer > Gebruikers en middelen voor analyse > Middelen voor gegevensoverdracht**.
