---
title: Verwerkingstijd van de indelingsimporteur
description: Begrijp het tijdkader Adobe verwerkt classificatiedossiers, en hoe te om verwerkingstijd te minimaliseren.
feature: Classifications
exl-id: 6b8b87f1-5dbc-46b8-9912-0e3086ff4b2a
source-git-commit: 4eea524bf95c9b6bc9ddc878c8c433bc1e60daee
workflow-type: tm+mt
source-wordcount: '423'
ht-degree: 0%

---

# Verwerkingstijd van de indelingsimporteur

{{classification-importer-deprecation}}

De verwerkingstijd voor een classificatiebestand hangt af van de grootte van het bestand en het totale aantal bestanden dat Adobe verwerkt. Classificaties duren meestal niet langer dan 24 uur. Periodes van intensief classificatiegebruik in organisaties die Adobe Analytics gebruiken, kunnen er echter toe leiden dat bestanden langer duren dan 24 uur. Adobe ziet het gebruik van zware classificaties in maanden voorafgaand aan het vakantieseizoen.

Ga als volgt te werk als u wilt zien of een classificatiebestand is voltooid:

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Classification importer]** .
2. Selecteer de rapportsuite en gegevensset in kwestie.
3. Als de verwerking nog niet voltooid is, wordt een van de volgende berichten weergegeven:

   * ![ Bericht ](assets/icon_notice_notice.gif) het geselecteerde rapport heeft een classificatieinvoer die verwerkt.
   * ![ Bericht ](assets/icon_notice_notice.gif) het geselecteerde rapport heeft classificatiegegevens die nog niet aan alle servers hebben verspreid.

Als u de importtijd voor classificaties wilt minimaliseren, raadt Adobe u ten zeerste aan de volgende richtlijnen in acht te nemen:

* **gebruik de bouwer van de classificatieregel wanneer mogelijk**: De bouwer van de classificatieregel verwerkt gegevens verschillend dan de traditionele classificatieimporteur. Als classificatiegegevens specifieke patronen volgen, wordt het gebruik van deze mogelijkheid ten zeerste aanbevolen.
* **uploadt slechts veranderde rijen**: Deze praktijk vermindert zeer de hoeveelheid tijd het neemt om classificatiedossiers te verwerken, aangezien het niet door ongewijzigde rijen sorteert. Adobe raadt sterk aan alleen gewijzigde rijen te uploaden.
* **Plan vooruit**: Begin het uploaden classificatiegegevens zo spoedig mogelijk, vooral als dit gegeven tijdens het vakantieseizoen wordt gebruikt.
* **combineer classificatiedossiers waar mogelijk**: Als één enkele variabele veelvoudige classificaties heeft, upload één enkel dossier met alle toepasselijke classificaties. Vermijd het uploaden van meerdere classificaties voor dezelfde variabele.
* **vermijd het uploaden van dossiers meer dan 500 MB**: Als het behandelen van grote hoeveelheden classificatiegegevens, adviseert Adobe het splitsen van dossiers in 100 MB-500 MB dossiers.
* **vermijd het uploaden van grote hoeveelheden dossiers aan FTP**: Als u van plan bent om de zelfde dossiers aan vele rapportreeksen door FTP te uploaden, beperkt het aantal dossiers die tegelijkertijd worden geupload. Adobe beveelt aan dat het aantal bestanden vermenigvuldigd met het aantal toepasselijke rapporteereeksen kleiner is dan 1000. Als u 100 bestanden moet uploaden naar 100 rapportsets, is het totale aantal bestanden 10.000. In plaats van alle 100 bestanden tegelijk te uploaden, moet u deze opsplitsen in 10 groepen van 10 bestanden tegelijk.
* **uploadt kleine dossiers via browser importeur**: Als u een dossier hebt dat minder dan 1 MB (minder dan 50.000 rijen) is, adviseert Adobe gebruikend browser importer. Browserimport is bijna altijd sneller dan FTP-import.
