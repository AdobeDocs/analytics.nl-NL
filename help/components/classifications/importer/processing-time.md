---
title: Verwerkingstijd van de indelingsimporteur
description: Begrijp het tijdkader Adobe classificatiedossiers verwerkt, en hoe te om verwerkingstijd te minimaliseren.
feature: Classifications
exl-id: 6b8b87f1-5dbc-46b8-9912-0e3086ff4b2a
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 0%

---

# Verwerkingstijd van de indelingsimporteur

De verwerkingstijd voor een classificatiebestand varieert afhankelijk van de grootte van het bestand en het totale aantal Adobe-processen van bestanden. Classificaties duren meestal niet langer dan 72 uur. Periodes van intensief classificatiegebruik in organisaties die Adobe Analytics gebruiken, kunnen er echter toe leiden dat bestanden langer duren dan 72 uur. Adobe ziet een groot gebruik van de classificatie in maanden voorafgaand aan het vakantieseizoen.

Ga als volgt te werk als u wilt zien of een classificatiebestand is voltooid:

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Classification importer]**.
2. Selecteer de rapportsuite en gegevensset in kwestie.
3. Als de verwerking nog niet voltooid is, wordt een van de volgende berichten weergegeven:

   * ![Kennisgeving](assets/icon_notice_notice.gif) Het geselecteerde rapport bevat een classificatie die wordt verwerkt.
   * ![Kennisgeving](assets/icon_notice_notice.gif) Het geselecteerde rapport heeft classificatiegegevens die nog niet aan alle servers hebben verspreid.

Als u de importtijd voor classificaties wilt minimaliseren, raadt Adobe u ten zeerste aan de volgende richtlijnen in acht te nemen:

* **Gebruik waar mogelijk de builder van de classificatieregel**: De bouwer van de classificatieregel verwerkt gegevens anders dan de traditionele classificatieimporteur. Als classificatiegegevens specifieke patronen volgen, wordt het gebruik van deze mogelijkheid ten zeerste aanbevolen.
* **Alleen gewijzigde rijen uploaden**: Deze praktijk vermindert zeer de hoeveelheid tijd het neemt om classificatiedossiers te verwerken, aangezien het niet door ongewijzigde rijen sorteert. Adobe raadt u ten zeerste aan alleen gewijzigde rijen te uploaden.
* **Vooruitzichten**: Begin zo snel mogelijk met het uploaden van classificatiegegevens, vooral als deze gegevens tijdens het vakantieseizoen worden gebruikt.
* **Classificatiebestanden waar mogelijk combineren**: Als één variabele meerdere classificaties heeft, upload één enkel dossier met alle toepasselijke classificaties. Vermijd het uploaden van meerdere classificaties voor dezelfde variabele.
* **Upload geen bestanden van meer dan 500 MB**: Als u te maken hebt met grote hoeveelheden classificatiegegevens, raadt Adobe aan bestanden te splitsen in bestanden van 100 MB tot 500 MB.
* **Vermijd het uploaden van grote hoeveelheden bestanden naar FTP**: Als u dezelfde bestanden via FTP wilt uploaden naar een groot aantal rapportbestanden, moet u het aantal bestanden beperken dat tegelijkertijd wordt geüpload. Adobe raadt aan het aantal bestanden te vermenigvuldigen met het aantal toepasselijke rapporteereeksen dat kleiner is dan 1000. Als 100 bestanden moeten worden geüpload naar een rapportsuite van 100, is het totale aantal bestanden 10.000. In plaats van alle 100 bestanden tegelijk te uploaden, moet u deze opsplitsen in 10 groepen van 10 bestanden tegelijk.
* **Kleine bestanden uploaden via de browser importer**: Als u een bestand hebt dat kleiner is dan 1 MB (minder dan 50.000 rijen), raadt Adobe u aan de importer van de browser te gebruiken. Browserimport is bijna altijd sneller dan FTP-import.
