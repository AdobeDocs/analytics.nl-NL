---
title: De huidige Adobe Analytics-releaseopmerkingen weergeven
description: Opmerkingen bij de release Latest Analytics
source-git-commit: e19299820a03783215d8425b937a0935311d9e7b
workflow-type: tm+mt
source-wordcount: '861'
ht-degree: 5%

---


# Opmerkingen bij de nieuwste Adobe Analytics-release

**Januari 2022**

Meer informatie over de nieuwste release-updates voor [Adobe Experience Cloud-producten](https://business.adobe.com/products/adobe-experience-cloud-products.html). De nieuwste zelfhulpdocumentatie, zelfstudies en cursussen over Experience League.

## Nieuwe functies in Adobe Analytics {#aa-features}

| Functie | Beschrijving | Doeldatum |
| ----------- | ---------- | ------- |
| N.v.t. |  | Zie [Algemene beschikbaarheid](https://experienceleague.adobe.com/docs/analytics/technotes/releases.html?lang=en) |

{style=&quot;table-layout:auto&quot;}

## Oplossingen in Adobe Analytics en Customer Journey Analytics {#aa-fixes}

* Probleem verholpen waarbij de publiek-id ontbrak aan dimensie-items. (AN-262038; AN-279315)
* Probleem verholpen waardoor gebruikers een opgeslagen [!DNL Target] project in Workspace. (AN-277461; AN-275825; AN-266397)
* Probleem verholpen waarbij niet-ingeschakelde functies zichtbaar waren in de gebruikersinterface. (AN-262006)
* Probleem verholpen dat optrad bij het wijzigen van de datum met het datumveld in Workspace. Dit leidde tot de [!UICONTROL End Time] van 23:59 tot 12:00 uur. (AN-277269; AN-277481)
* Probleem verholpen waarbij de gebruikersinterface van het segment werd onderbroken bij het toevoegen van nieuwe segmenten aan een reeds geladen segment. (AN-260827)
* Probleem verholpen waarbij gebruikers geen toegang hadden tot gedeelde werkruimteprojecten. (AN-267529)
* Er is een foutbericht toegevoegd dat aangeeft wanneer een verschuivende datumreeks een begindatum later dan de einddatum heeft. (AN-270488)
* Problemen met diverse gegevensfeeds verholpen. (AN-275876; AN-270512; AN-277284; AN-277290; AN-274893; AN-274606; AN-269651)
* Probleem verholpen waarbij datumbereiken in grafieken datumfilters in tabellen negeren. (AN-263999)
* Probleem verholpen waarbij geplande rapporten vroegtijdig werden verzonden vanwege zomertijd. (AN-276410; AN-276305)
* Probleem verholpen met downloaden van project naar `.csv` bestand is mislukt in Workspace. (AN-275834)

### Extra correcties in Adobe Analytics

AN-253294; AN-254976; AN-255377; AN-255561; AN-258550; AN-259336; AN-263935; AN-265094; AN-269441; AN-269486; AN-269855; AN-271166; AN-271588; AN-272088; AN-272249; AN-272859; AN-272873; AN-272885; AN-273229; AN-273913; AN-274237; AN-274472; AN-274491; AN-274619; AN-274766; AN-275248; AN-275259; AN-275271; AN-275315; AN-275388; AN-275418; AN-275597; AN-275643; AN-275650; AN-275651; AN-275675; AN-275682; AN-275704; AN-275711; AN-275796; AN-275834; AN-275923; AN-275941; AN-276044; AN-276125; AN-276157; AN-276397; AN-276597; AN-276789; AN-276834; AN-276861; AN-276870; AN-276963; AN-276975; AN-277000; AN-277044; AN-277093; AN-277200; AN-277215; AN-277271; AN-277281; AN-277362; AN-277419; AN-277492; AN-277498; AN-277533; AN-277619; AN-277675; AN-277681; AN-277767; AN-277805; AN-277810; AN-277818; AN-277875; AN-277933; AN-277988; AN-278105; AN-278115; AN-278122; AN-278192; AN-278407; AN-278437; AN-278559; AN-278604; AN-278610; AN-278709; AN-278835; AN-278849; AN-278881; AN-279067; AN-279103; AN-279111; AN-279219; AN-279237; AN-279312

## Belangrijke berichten voor [!DNL Analytics]-beheerders {#aa-notices}

| Bericht | Toegevoegd of bijgewerkt op | Beschrijving |
| ----------- | ---------- | ---------- |
| Verlopen van de lijst van gewenste personen EOL-extensie voor verouderde integratie van Analytics OAuth/JWT | 14 januari 2022 | Aan **25 mei 2022** de [Analytics 1.3 API, 1.4 SOAP API en Legacy Analytics OAuth/JWT EOL](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/APIEOL.md) De verlenging van de lijst van gewenste personen verloopt. Het werd aangeboden klanten te voorzien die erfenis gebruiken [!DNL Adobe Analytics] OAuth/JWT geloofsbrieven extra tijd om hun cliëntintegratie te migreren aan [Adobe IMS-referenties](https://developer.adobe.com/console). Deze vervaldatum beïnvloedt (maar is niet beperkt tot) [!DNL Adobe Analytics Livestream] en [!DNL Adobe Campaign] klanten die hun vereiste IMS-migratie niet hebben voltooid. Klanten die op dit moment verouderde [!DNL Analytics] OAuth/JWT-referenties via de extensie lijst van gewenste personen en die de migratie naar IMS-referenties op 25 mei 2022 niet hebben voltooid, verliezen de toegang tot Adobe-services. Livestream-klanten kunnen naar deze [instructies](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/live-stream-api/getting_started.md) over het migreren van hun clienttoepassingen naar IMS-referenties. [!DNL Campaign] klanten kunnen hun Adobe account team bereiken over de upgrade naar de nieuwste versie van [!DNL Campaign]. |
| EOL voor [!DNL Reports & Analytics] | 4 januari 2022 | Effectief **31 december 2023**, is Adobe voornemens te stoppen [!DNL Reports & Analytics] en de bijbehorende verslagen en kenmerken. De rapporten, visualisaties en onderliggende technologie die macht [!DNL Reports & Analytics] voldoet niet meer aan de technologienormen van Adobe. Meeste [!DNL Reports & Analytics] functies zijn beschikbaar in [Analysis Workspace](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/home.html). Sinds de release van Analysis Workspace in 2015, [!DNL Reports & Analytics] functionaliteit en mogelijkheden zijn verplaatst naar Analysis Workspace en er is een drempel voor pariteit van de workflow bereikt. [Dit bericht](https://spark.adobe.com/page/6WnF8JK6IRDhf/) legt het einde van het levensproces uit. |
| SFTP-services (Secure File Transfer Protocol) upgraden | 13 januari 2022 | Aan **2 mei 2022**, [!DNL Adobe Analytics] zal de SFTP-services (Secure File Transfer Protocol) upgraden om betere beveiliging voor bestandsoverdrachten te bieden. Door deze wijziging worden sommige SFTP-clientconfiguraties niet meer ondersteund. We voegen ook enkele verbindingsopties toe die beschikbaar zijn op **1 maart 2022**. Dit heeft alleen invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Het FTP-protocol wordt niet beïnvloed. Om onderbreking van de dienst te vermijden, gelieve ervoor te zorgen dat uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de gedetailleerde veranderingen zullen zijn [hier](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/secure-file-transfer-protocol/sftp-upgrade.html). |
| _Global + China_ RDC-type | 22 november 2021 | _Global + China_ is een nieuw type van de Regionale Gegevensverzameling (RDC) dat het verpletteren van verkeer voor globale klanten gebruikend vereenvoudigt [!UICONTROL China Performance Optimization Add-On Package]. In het verleden, moest u bepalen of de gegevens aan het de inzamelingseindpunt van China of één van de Globale inzamelingseindpunten zouden moeten worden verpletterd. Nu kunt u deze RDC kiezen *type* om Adobe het optimale inzamelingseindpunt te laten bepalen dat op de geolocatie van de gebruiker wordt gebaseerd. |
| EOL voor volledige verwerking in gegevensbronnen | 18 oktober 2021 | Aan **31 januari 2022**, zal Adobe het einde van leven Volledige Verwerking beëindigen, die gebruikers toelaat om off-line klapgegevens in Analytics in te voeren. Deze mogelijkheid is beschikbaar via [API voor het invoegen van bulkgegevens](https://www.adobe.io/apis/experiencecloud/analytics/docs.html#!AdobeDocs/analytics-2.0-apis/master/bdia.md). [Meer informatie](https://experienceleague.adobe.com/docs/analytics/import/data-sources/data-types-and-categories/datasrc-fullproc-eol.html?lang=en) |

{style=&quot;table-layout:auto&quot;}

## AppMeasurement {#appm}

Voor de meest recente updates over AppMeasurement-releases (versie 2.22.4) raadpleegt u [AppMeasurement voor JavaScript-releaseopmerkingen](https://experienceleague.adobe.com/docs/analytics/implementation/appmeasurement-updates.html?lang=en).