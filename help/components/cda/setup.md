---
title: Apparaatanalyse instellen
description: Configureer een virtuele rapportsuite om CDA in te schakelen.
exl-id: e6d4e0c2-6b85-4f89-b51f-c0eed7a4e3da
translation-type: tm+mt
source-git-commit: 005cb590f4f7d31d3de801437a0ba6fa25b2ea64
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Apparaatanalyse instellen

Als aan alle voorwaarden is voldaan, voert u de volgende stappen uit om Apparaatanalyse op andere apparaten in te schakelen. U moet tot een groep van de Admin van het Profiel van het Product behoren of beheerdervoorrechten in Adobe Analytics hebben om deze stappen te volgen.

>[!IMPORTANT]
>
>Aan alle voorwaarden moet worden voldaan voordat u deze stappen uitvoert. Als niet aan alle voorwaarden wordt voldaan, is de functie niet beschikbaar of werkt deze niet. Zie [overzichtspagina](overview.md) en de gewenste het stitching methode ([Op gebied-gebaseerde het stitching](field-based-stitching.md) of [Apparaatgrafiek](device-graph.md), respectievelijk) voor eerste vereisten en beperkingen.

## Open een ticket met de klantenservice om CDA beschikbaar te stellen op uw rapportenpakket voor alle apparaten

CDA is provisioned op uw cross-device rapportsuite door Adobe engineering. Neem contact op met de klantenservice om dit proces te starten en bereid te zijn de volgende informatie te verstrekken:

* Uw Adobe Experience Cloud org-id (een alfanumerieke tekenreeks die eindigt met @AdobeOrg)
* De rapportsuite-id voor de rapportsuite voor verschillende apparaten die u wilt inschakelen met CDA
* Welke methode van CDA wilt u gebruiken (op gebied-gebaseerde het stitching, Adobe privé grafiek, of Adobe coop grafiek)
* Als u op het veld gebaseerde stitching wilt gebruiken, de eigenschap of de eVar die de gebruikersnaam bevat
* Uw voorkeur voor afspeelfrequentie en terugkijklengte. De opties omvatten een replay eens per week met een 7 dagen terugkijkvenster, of een replay elke dag met een 1 dag terugkijkvenster.

Als u de klantenservice deze informatie verschaft, werken zij samen met Adobe Engineering om uw gekozen rapportenpakket in te schakelen voor CDA-verwerking.

## Maak een virtuele-rapportsuite voor meerdere apparaten om de apparaatweergave te bekijken

Beheerders die toegang hebben tot het maken van virtuele rapportsuites, kunnen als volgt virtuele CDA-rapportensuites maken:

1. Navigeer naar [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) en meld u aan met uw AdobeID-referenties.
2. Klik op het pictogram met het 9-raster bovenaan en klik vervolgens op Analytics.
3. Houd de muis boven Componenten en klik vervolgens op Virtuele rapportsets.
4. Klik op Toevoegen.
5. Voer een naam in voor uw virtuele-rapportsuite en zorg ervoor dat de CDA-compatibele rapportsuite is geselecteerd.
6. (Optioneel) Pas een segment toe op de virtuele rapportsuite. Bijvoorbeeld, kunt u een segment toepassen dat de virtuele rapportreeks tot data beperkt nadat CDA werd aangezet en het stitching begon. Dit segment staat gebruikers toe om slechts gestikte datumwaaiers binnen VRS te zien.
7. Klik op het selectievakje &#39;Tijdverwerking rapport inschakelen&#39;, waarmee u meer opties kunt inschakelen, waaronder Apparaatanalyse.
8. Klik op het selectievakje &#39;Gebruikersbezoeken op apparaten plaatsen&#39;.
9. Klik op Doorgaan, voltooi de configuratie van de virtuele rapportsuite en klik op Opslaan.

![CDA-selectievakje](assets/cda-checkbox.png)

## Toevoegingen en wijzigingen aan virtuele-rapportsuites voor meerdere apparaten

Houd rekening met de volgende wijzigingen wanneer Apparaatanalyse is ingeschakeld voor een virtuele rapportsuite:

* Er verschijnt een nieuw apparaatpictogram naast de naam van de virtuele rapportsuite. Dit pictogram is exclusief voor virtuele rapportsuites op meerdere apparaten.
* Er is een nieuwe dimensie beschikbaar met het label [Identified state](../dimensions/identified-state.md). Deze dimensie bepaalt of de Experience Cloud-id op die hit bekend is door de apparaatgrafiek op dat moment.
* Er zijn nieuwe meetgegevens beschikbaar met de labels [Mensen](../metrics/people.md) en [Unieke apparaten](../metrics/unique-devices.md).
* De metrische [Unieke bezoekers](../metrics/unique-visitors.md) is niet beschikbaar, aangezien het met &quot;Mensen&quot;en &quot;Unieke Apparaten&quot;wordt vervangen.
* Bij het maken van segmenten wordt de segmentcontainer &#39;Visitor&#39; vervangen door een container &#39;Person&#39;.
