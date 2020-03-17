---
description: Virtuele rapportsuites segmenteren uw gegevens van de Analyse van Adobe zodat kunt u toegang tot elk segment controleren.
title: Overzicht van virtuele-rapportsuites
uuid: 51c63c56-dd58-4c23-a997-ea6942480d22
translation-type: tm+mt
source-git-commit: ''

---


# Overzicht van virtuele-rapportsuites

Virtuele rapportsuites segmenteren uw gegevens van de Analyse van Adobe zodat kunt u toegang tot elk segment controleren.

Vele klanten hebben gegevens die in een globaal rapportpakket stromen, maar ook gegevens die in kleinere rapportseries stromen. Zij plaatsen een variabele aan veelvoudige rapportreeksen, en verzenden hun gegevens naar meer dan één rapportreeks. Dit wordt bedoeld als *multisuite het etiketteren*, of *basis/ouderrapportsuites*.

Bijvoorbeeld, zouden alle gegevens in één rapportreeks kunnen worden verzameld, maar dan kunt u de secundaire rapportreeksen opzetten zodat andere mensen in uw bedrijf toegang tot een deel van de gegevens hebben, maar niet allen. De gegevens kunnen per gebied worden verdeeld. U hebt mogelijk verschillende websites voor verschillende landen. Andere voorbeelden kunnen specifieke merken zijn die tot een groter bedrijf behoren, maar die elk hun eigen marketing teams hebben.

Met een *virtuele rapportsuite* (VRS) kunt u dit vertakkende concept reproduceren door segmenten te gebruiken in plaats van meerdere rapportsuites. De gegevens worden verzonden naar één rapportreeks, dan wordt verdeeld volgens segmenten. Gebruikend het veelvoudige merkvoorbeeld, zou u prop voor het merk kunnen plaatsen dat een punt tot behoort. Gebruikend segmenten, kunt u over de punten rapporteren die aan elke eigenschap worden toegewezen. Elk van deze segmenten wordt zijn eigen mening, effectief creërend een nieuwe rapportreeks. U verzendt geen gegevens specifiek naar dat segment, slechts naar de globale rapportreeks, maar het functioneert in uw rapporten alsof het een verschillende rapportreeks was.

Een virtuele rapportreeks erft de meeste de dienstniveaus van de reeks van het basisrapport, zoals eVar montages, de Regels van de Verwerking, Classificaties, enz. De volgende instellingen worden NIET overgeërfd:

* Identiteitskaart van de Reeks van het rapport (RSID)
* Naam rapportsuite
* Machtigingsgroepen (virtuele rapportsuites kunnen worden toegewezen aan hun eigen machtigingsgroepen)

## Voordelen van virtuele rapportsuite {#section_3420422FE6DF46EAB151FD9442AAFDC4}

De klanten betalen voor secundaire servervraag, zodat kan het elimineren van deze vraag in significante besparingen resulteren. Een virtuele rapportsuite is ook volledig retroactief. Als de algemene rapportsuite al gegevens bevat, worden de relevante gegevens automatisch opgenomen in een nieuwe virtuele rapportsuite. Een nieuwe secundaire rapportsuite zou pas beginnen met het verzamelen van gegevens nadat deze is gemaakt, zodat deze geen historische gegevens bevat. Wanneer u Analytics implementeert, hoeft u alleen gegevens naar één rapportsuite te verzenden in plaats van implementaties voor de algemene rapportsuite en elke secundaire rapportsuite te maken.

Virtuele rapportensuites helpen:

* Vereenvoudig implementatie door u toe te staan om één enkele identiteitskaart van de Reeks van het Rapport (RSID) over alle plaatsen/domeinen te gebruiken. Als alle gegevens in één rapportenpakket zijn opgenomen, kunnen klanten analyses uitvoeren terwijl we de volgende generatie Adobe Analytics uitvoeren.
* Zakelijke gebruikers in uw organisatie zien altijd alleen de gegevenssegmenten die voor hen relevant zijn.
* Verbeter veiligheid door Admin gebruikers toe te staan om gegevenstoegang gemakkelijker en korter na implementatie te controleren.
* De mogelijkheid bieden om deel te nemen aan Device Co-op
* Personmetrisch
* Een weergave van gegevens voor één klant (in de toekomst)
* De capaciteit om onbeperkte virtuele rapportsuites tot stand te brengen om gegevens te segmenteren

## Beperkingen van virtuele rapportsuite {#section_F22A6DEBDC9848429E446F4CC2C4EEDE}

Virtuele rapportsuites hebben de volgende beperkingen:

* Om het even welke beperkingen van segmenten zijn op virtuele rapportsuites van toepassing

   Een virtuele rapportsuite is niets meer dan een segment dat wordt toegepast op een rapportsuite. Omdat elke rapportreeks zijn eigen gegevenspakhuis en zijn eigen gegevensvoer heeft, leidt het gebruiken van veelvoudige rapportreeksen in sommige voordelen die de segmenten niet verstrekken.
* Rapport in realtime
* Instellingen en variabelenamen kunnen niet worden aangepast, zoals in een volledige rapportsuite

## Virtuele rapportsuite versus meerdere suite-tags {#section_317E4D21CCD74BC38166D2F57D214F78}

| Capaciteit | Virtuele rapportsuite | Meerdere versies taggen |
|--- |--- |--- |
| Biedt real-time of &quot;Current Data&quot;-rapportage | Nee | Ja |
| Werkt in alle analysegereedschappen (Analyse-werkruimte, Report Builder, Ad hoc-analyse, enz.) | Ja.   Opmerking:  U kunt deze alleen in Rapporten en Analyse bewerken en identificeren als virtuele-rapportsuite. Nochtans, kunt u hen in de drop-down van de rapportreeks in de andere hulpmiddelen selecteren. | Ja |
| Kan gegevens uploaden (via classificaties, gegevensfeeds, enz.) | Nee | Ja |
| Ondersteunt het maken van DL-rapporten, bladwijzers, dashboards, doelen, waarschuwingen, segmenten, berekende metriek... | Ja | Ja |
| Kan afzonderlijk worden toegevoegd aan machtigingengroepen | Ja | Ja |
| Kan Admin-functies gebruiken om de afzonderlijke instellingen in dit rapportpakket te wijzigen (Admin > Rapportagesuites) | Nee (instellingen worden overgenomen van bovenliggend item) | Ja |

## Virtuele rapportsets combineren en meerdere suite-tags toepassen {#section_026FA3FCD7314DD18220E73EC5702AFF}

In sommige gevallen zijn er voordelen verbonden aan zowel het gebruik van virtuele rapportsuites als het gebruik van tags met meerdere suite.

Een detailhandelaar kan bijvoorbeeld een rapportenpakket voor elk merk gebruiken, en virtuele rapportsuites voor elk merk om gegevens per regio uit te splitsen. Op dezelfde manier zou een atletische organisatie een rapportreeks voor elk team, dan virtuele rapportreeksen kunnen gebruiken om ventilatoren in de regio van het team van die buiten de regio te verdelen.
