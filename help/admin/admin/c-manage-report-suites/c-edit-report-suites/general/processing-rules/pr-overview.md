---
description: De verwerkingsregels vereenvoudigen gegevensverzameling en beheren inhoud aangezien het naar rapportering wordt verzonden.
subtopic: Processing rules
title: Overzicht van verwerkingsregels
feature: Processing Rules
role: Admin
exl-id: 0244aba2-4345-463a-8528-d4dcd2f872ff
source-git-commit: 0bed2622f54bf2f46aa57dbfad7bd55a61d6c7d0
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# Overzicht van verwerkingsregels

De regels van de verwerking staan u toe om te wijzigen hoe uw gegevens worden verzameld alvorens het aan een rapportreeks wordt geschreven.

**[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > Selecteer een rapportsuite > **[!UICONTROL Edit Settings]** > **[!UICONTROL General]** > **[!UICONTROL Processing rules]**

>[!WARNING]
>
>De verwerkingsregels beïnvloeden direct gegevensinzameling, en kunnen gegevensverlies veroorzaken als verkeerd gebruikt. Test altijd de verwerkingsregels in een ontwikkelrapport voordat u ze in een productierapportsuite inschakelt om problemen met de gegevenskwaliteit te verhelpen.

De twee gevallen van primair gebruik voor verwerkingsregels omvatten:

* **Gebruik het de implementatiewerkschema van de de contextgegevens veranderlijke**: In plaats van het direct plaatsen van variabelen in uw implementatie, kunt u [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) gebruiken om sleutel/waardeparen te plaatsen. Bijvoorbeeld, in plaats van het plaatsen:

  ```js
  s.eVar1 = "Robert Munch";
  s.eVar2 = "Books";
  s.eVar3 = "Youth";
  ```

  In plaats daarvan kunt u instellen:

  ```js
  s.contextData['author'] = "Robert Munch";
  s.contextData['section'] = "Books";
  s.contextData['genre'] = "Youth";
  ```

  U kunt de variabelen van contextgegevens aan de gewenste afmetingen en metriek in de Analytics UI dan in kaart brengen.

  Wanneer het communiceren met ontwikkelaars in uw organisatie om Analytics op een bezit uit te voeren, vereenvoudigt het gebruiken van de variabelen van contextgegevens het communicatie proces. De ontwikkelaars kunnen eenvoudig elk sleutel/waardepaar uitvoeren eens, dan kunt u als Analyseadmin ervoor zorgen dat de gegevens het aan de correcte implementatievariabele maken.

* **wijzigt gegevens aangezien het wordt verzameld**: Dit gebruiksgeval heeft een brede waaier van toepassingen, zoals tijdelijke moeilijke situaties aan gegevenskwaliteit of helpen in implementatiekloven vullen. Zie [ het gebruiksgevallen van de Regels van de Verwerking ](pr-use-cases.md) voor meer informatie en specifieke voorbeelden.

## Machtigingen

Productbeheerders hebben standaard toegang tot verwerkingsregels. U kunt toegang tot verwerkingsregels verlenen aan niet-beheerders door deze op te nemen in een productprofiel dat het machtigingsitem **[!UICONTROL Processing rules]** bevat. Zie {de profieltoestemmingen van 0} Product voor de Hulpmiddelen van de Reeks van het Rapport [ voor meer informatie.](/help/admin/admin-console/permissions/report-suite-tools.md)

## Overwegingen bij het maken of bewerken van verwerkingsregels

Houd rekening met het volgende wanneer u verwerkingsregels maakt of bewerkt:

* **Mogelijke lege waarden**: Wanneer u een regel creeert, overweeg gevallen wanneer de het beschrijven waarde leeg is. Als u bijvoorbeeld een regel hebt die eVar1 overschrijft met eVar2 en eVar2 leeg is, worden beide variabelen gewist. Adobe raadt u aan een voorwaarde toe te voegen die op een waarde van een variabele controleert voordat deze wordt gebruikt om een andere waarde te overschrijven.
* **ben onmiddellijk op sparen** van toepassing: De regels van de verwerking zijn op verzamelde gegevens van toepassing het moment dat u hen opslaat. Zij zijn niet met terugwerkende kracht van toepassing op gegevens die reeds worden verzameld.
* **de orde van de Verwerking binnen regels**: Als u veelvoudige verwerkingsregels hebt, de orde dat zij kwesties in werking stellen. Zorg ervoor dat als u een bepaalde variabele in veelvoudige regels gebruikt dat zij in de correcte orde worden uitgevoerd. Als u eVar3 in regel 1 overschrijft, is die oorspronkelijke eVar3-waarde niet beschikbaar in volgende regels.
* **de orde van de Verwerking binnen de pijpleiding van de gegevensinzameling**: Zie [ Verwerkingsvolgorde voor gegevens in Adobe Analytics ](/help/technotes/processing-order.md) om te begrijpen waar de verwerkingsregels in de algemene pijpleiding van de gegevensinzameling van toepassing zijn.
* **het Coderen**: Steek aan het coderen UTF-8 in bijna alle gevallen.
* **Gevoeligheid van het Geval**: De vergelijkingen van het koord in verwerkingsregels zijn niet case-sensitive. De tekenreekswaarden die u gebruikt om waarden te overschrijven, gebruiken dezelfde regels als het rechtstreeks vullen van de variabele.
* **Enige rapportreeks**: Wanneer u verwerkingsregels uitgeeft, zijn zij op slechts één rapportreeks van toepassing. Het selecteren van veelvoudige rapportreeksen in de manager van de Reeks van het Rapport dwingt u om één enkele rapportreeks te selecteren. Zodra u hebt gecreeerd of de gewenste verwerkingsregels uitgegeven, kunt u [ die regels kopiëren aan andere rapportsuites ](pr-copy.md).
* **Geen gegevensuitsluiting**: Het uitsluiten van gegevens is geen voorgenomen eigenschap van verwerkingsregels. Overweeg gebruikend [`abort`](/help/implement/vars/config-vars/abort.md) op het niveau van de gegevensinzameling of gebruik [ VISTA regels ](/help/technotes/vista.md) nadat het gegeven wordt verzameld.
* **Beschikbare variabelen**: Niet alle dimensies en metriek zijn beschikbaar in verwerkingsregels. Zie [ Dimensies en metriek beschikbaar aan verwerkingsregels ](pr-variables.md) voor de volledige lijst van wat wordt gesteund.
* **Aantal regels toegestaan**: Elke rapportreeks kan tot 150 regels bevatten. Elke regel kan tot 30 voorwaarden bevatten.

>[!MORELIKETHIS]
>
>![ VideoCheckedOut ](/help/assets/icons/VideoCheckedOut.svg) [ de variabelen van de de contextgegevens van de Kaart in steunen en eVars met verwerkingsregels ](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/implementation/implementation-basics/map-contextdata-variables-into-props-and-evars-with-processing-rules){target="_blank"}
