---
title: Apparaatanalyse instellen
description: Configureer een virtuele rapportsuite om CDA in te schakelen.
exl-id: e6d4e0c2-6b85-4f89-b51f-c0eed7a4e3da
feature: CDA
role: Admin
source-git-commit: cfa5cc02ba3a7349b51a904f29bab533c0f1c603
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# Apparaatanalyse instellen

{{available-existing-customers}}

Als aan alle voorwaarden is voldaan, voert u de volgende stappen uit om Apparaatanalyse op andere apparaten in te schakelen. U moet tot een groep van de Admin van het Profiel van het Product behoren of beheerdervoorrechten in Adobe Analytics hebben om deze stappen te volgen.

>[!IMPORTANT]
>
>Aan alle voorwaarden moet worden voldaan voordat u deze stappen uitvoert. Als niet aan alle voorwaarden wordt voldaan, is de functie niet beschikbaar of werkt deze niet. Zie de [&#x200B; overzichtspagina &#x200B;](overview.md) en de gewenste het stitching methode ([&#x200B; Op gebied-gebaseerd het stitching &#x200B;](field-based-stitching.md) of [&#x200B; grafiek van het Apparaat &#x200B;](device-graph.md), respectievelijk) voor eerste vereisten en beperkingen.

## 1. Open een ticket met de klantenservice om CDA te laten voorzien op uw rapportenpakket voor andere apparaten

CDA is provisioned op uw cross-device rapportsuite door Adobe engineering. Neem contact op met de klantenservice om dit proces te starten en bereid te zijn de volgende informatie te verstrekken:

* Uw Adobe Experience Cloud org-id (een alfanumerieke tekenreeks die eindigt met @AdobeOrg)
* De rapportsuite-id voor de rapportsuite voor verschillende apparaten die u wilt inschakelen met CDA
* Welke methode van CDA wilt u gebruiken (Op gebied-gebaseerde het Stikken of Grafiek van het Apparaat van de Adobe)
* Als u op het veld gebaseerde stitching wilt gebruiken, de eigenschap of de eVar die de gebruikersnaam bevat
* Uw voorkeur voor afspeelfrequentie en terugkijklengte. De opties omvatten een replay eens per week met een 7 dagen terugkijkvenster, of een replay elke dag met een 1 dag terugkijkvenster.
De standaardinstelling is wekelijks opnieuw afspelen met een terugkijkvenster van 7 dagen. In dit geval kunnen gegevens in de laatste week worden gewijzigd (aangezien deze geleidelijk worden bijgewerkt).

Zodra u de klantenservice deze informatie verschaft, werken zij samen met Adobe Engineering om uw gekozen rapportenpakket in te schakelen voor CDA-verwerking.

## 2. Maak een virtueel rapportenpakket voor alle apparaten om de apparaatweergave te bekijken

Beheerders die toegang hebben tot het maken van virtuele rapportsuites, kunnen als volgt virtuele CDA-rapportensuites maken:

1. Navigeer aan [&#x200B; Experience.adobe.com &#x200B;](https://experiencecloud.adobe.com) en login gebruikend uw geloofsbrieven van AdobeID.
2. Klik op het pictogram met het 9-raster bovenaan en klik vervolgens op Analytics.
3. Houd de cursor boven **[!UICONTROL Components]** en klik vervolgens op **[!UICONTROL Virtual report suites]** .
4. Klik toevoegen.
5. Voer een naam in voor uw virtuele-rapportsuite en zorg ervoor dat de CDA-compatibele rapportsuite is geselecteerd.
6. (Optioneel) Pas een segment toe op de virtuele rapportsuite. Bijvoorbeeld, kunt u een segment toepassen dat de virtuele rapportreeks tot data beperkt nadat CDA werd aangezet en het stitching begon. Dit segment staat gebruikers toe om slechts gestikte datumwaaiers binnen de Virtuele rapportreeks te zien.
7. Klik op het selectievakje &#39;Tijdverwerking rapport inschakelen&#39;, waarmee u meer opties kunt inschakelen, waaronder Apparaatanalyse.
8. Klik op het selectievakje &#39;Gebruikersbezoeken op apparaten plaatsen&#39;.
9. Klik op Doorgaan, voltooi de configuratie van de virtuele rapportsuite en klik op Opslaan.

![&#x200B; CDA checkbox &#x200B;](assets/cda-checkbox.png)

## Toevoegingen en wijzigingen aan virtuele-rapportsuites voor meerdere apparaten

Houd rekening met de volgende wijzigingen wanneer Apparaatanalyse is ingeschakeld voor een virtuele rapportsuite:

* Er verschijnt een nieuw apparaatpictogram naast de naam van de virtuele rapportsuite. Dit pictogram is exclusief voor virtuele rapportsuites op meerdere apparaten.
* Een nieuwe afmeting geëtiketteerd [&#x200B; Geïdentificeerde staat &#x200B;](../dimensions/identified-state.md) is beschikbaar.
* De nieuwe metriek geëtiketteerde [&#x200B; Mensen &#x200B;](../metrics/people.md), [&#x200B; Unieke Apparaten &#x200B;](../metrics/unique-devices.md), [&#x200B; Geïdentificeerde mensen &#x200B;](../metrics/identified-people.md), [&#x200B; Niet-geïdentificeerde mensen &#x200B;](../metrics/unidentified-people.md), en [&#x200B; Mensen met identiteitskaart van het Experience Cloud &#x200B;](../metrics/people-with-exp-cloud-id.md) zijn beschikbaar.
* De metrische [&#x200B; Unieke Bezoekers &#x200B;](../metrics/unique-visitors.md) is niet beschikbaar, aangezien het met &quot;Mensen&quot;en &quot;Unieke Apparaten&quot;wordt vervangen.
* Bij het maken van segmenten wordt de container van het segment &#39;Visitor&#39; vervangen door een container &#39;Person&#39;.
