---
title: Overzicht van gegevensbronnen
description: Importeer gegevens naar Adobe Analytics met behulp van externe bestanden.
exl-id: 5ec8bc51-dfd2-497c-aebc-a32d87efc97e
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---

# Overzicht van gegevensbronnen

Met Adobe Analytics-gegevensbronnen kunt u extra online- of offlinegegevens importeren voor rapportage. Ze zijn handig om inzicht te krijgen in facetten van uw bedrijf buiten uw website en in hun interactie met uw site. De algemene workflow voor het gebruik van gegevensbronnen bestaat uit de volgende stappen:

1. Uw organisatie verzamelt gegevens uit andere bronnen. Voorbeelden zijn vooraf klikgegevens, callcentergegevens of informatie over transacties die buiten uw site zijn uitgevoerd.
1. Gegevens worden zodanig opgemaakt dat Adobe Analytics het gebruik van een door tabs gescheiden tekstbestand begrijpt.
1. U uploadt het tekstbestand naar een FTP-site-Adobe met de bijbehorende `.fin` bestand.
1. Adobe neemt het tekstbestand op en geeft die gegevens naast afmetingen en meetgegevens weer die op uw site zijn verzameld.

Adobe biedt twee algemene typen gegevensbronnen. Alle gegevensbronmalplaatjes zijn gebaseerd op één van deze twee types:

* **Samenvattingsgegevensbron**: Biedt een eenvoudige manier om gegevens op hoog niveau te importeren in Adobe Analytics. U geeft de tijdstempel, de waarde van de variabele en de bijbehorende metriek op. Die metriek voor elk afmetingspunt wordt dan dienovereenkomstig verhoogd. Het is waardevol als u offline en online gegevens naast elkaar wilt zien. Het maakt echter geen koppeling tussen online- en offlinegegevens.
* **Gegevensbron van transactie-id**: Als een hit die door een AppMeasurement en een gegevensbronrij wordt verzonden overeenkomende transactie-id&#39;s bevat, worden de afmetingen en de metrische waarden in de gegevensbron aan die hit toegevoegd.

**Volledige verwerkingsgegevensbronnen** vanaf 25 maart 2021 niet meer als gegevensbron worden aangeboden. Zie de [Aankondiging einde levensduur](full-processing-eol.md) voor meer informatie .

Adobe biedt ook de [API voor gegevensbronnen](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), waarmee u gegevensbronnen kunt maken en gegevens kunt uploaden zonder de interface van het product of een FTP-locatie te gebruiken.

## Volgende stappen

[Aan de slag met gegevensbronnen](getting-started.md): Upload een eenvoudige gegevensbron naar een pakket met ontwikkelingsrapporten.
