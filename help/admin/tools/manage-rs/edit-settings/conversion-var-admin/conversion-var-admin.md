---
description: De Custom Insight-conversievariabele (of eVar) wordt in de Adobe-code op geselecteerde webpagina's van uw site geplaatst. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op een bezoek gebaseerd zijn en op dezelfde manier functioneren als cookies. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.
keywords: eVar
title: Conversievariabelen (eVar)
feature: Admin Tools
role: Admin
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '1639'
ht-degree: 0%

---

# Conversievariabelen (eVars)

De Custom Insight-conversievariabele (of eVar) wordt in de Adobe-code op geselecteerde webpagina&#39;s van uw site geplaatst. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op een bezoek gebaseerd zijn en op dezelfde manier functioneren als cookies. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Variables]**

## Overzicht van conversievariabelen (eVars)

Voor een videooverzicht van omzettingsvariabelen, zie [ Inleiding aan omzettingsvariabelen ](https://experienceleague.adobe.com/nl/docs/analytics-learn/tutorials/analysis-workspace/dimensions/introduction-to-conversion-variables-evars) in de gids van de zelfstudies van Analytics.

Wanneer een eVar is ingesteld op een waarde voor een bezoeker, onthoudt Adobe die waarde automatisch tot deze is verlopen. Eventuele succesgebeurtenissen die een bezoeker tegenkomt terwijl de eVar-waarde actief is, worden geteld bij de eVar-waarde.

Vars kunnen het beste worden gebruikt om oorzaak en effect te meten, zoals:

* Welke interne campagnes de inkomsten beïnvloedden
* Welke banneradvertenties uiteindelijk hebben geresulteerd in een registratie
* Het aantal keren dat een interne zoekopdracht is gebruikt voordat een bestelling is gemaakt

Als verkeersmeting of het kleven gewenst is, wordt het gebruiken van verkeersvariabelen geadviseerd.

>[!NOTE]
>
>Er kan slechts één waarde in een eVar worden opgeslagen in een afbeeldingsaanvraag. Als de veelvoudige waarden in een waarde van eVar worden gewenst, adviseren wij dat u [ variabelen van de Lijst (lijstvariabelen) ](/help/implement/vars/page-vars/page-variables.md) uitvoert.

### Conversievariabelen - beschrijvingen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Beschrijvingen van gebieden die worden gebruikt wanneer [ het uitgeven omzettingsvariabelen ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md).

| Element | Beschrijving |
| --- | --- |
| [!UICONTROL Name] | De vriendelijke naam van de conversievariabele. Deze naam is hoe naar de eVar wordt verwezen in algemene rapportering, en zal de naam van het rapport/de dimensie in het linkermenu zijn. |
| [!UICONTROL Type] (alleen eVar) | Het type van veranderlijke waarde:<ul><li>**[!UICONTROL Text String]**: legt de tekstwaarden vast die op uw site worden gebruikt. Dit is het meest gangbare type eVar en de standaardinstelling. De methode werkt op dezelfde manier als andere variabelen, waarbij de waarde erin een statische tekenreeks is. Als u zaken zoals interne campagnes of interne onderzoekstrefwoorden volgt, is dit het geadviseerde plaatsen.</li><li>**[!UICONTROL Counter]**: telt het aantal keren dat een actie voor de succesgebeurtenis voorkomt. Als u bijvoorbeeld een eVar gebruikt om interne zoekopdrachten op uw site bij te houden, stelt u deze waarde in op [!UICONTROL Text String] om het gebruik van zoektermen te volgen. Stel deze waarde in op [!UICONTROL Counter] om het aantal uitgevoerde zoekopdrachten te tellen, ongeacht de gebruikte zoektermen. U kunt bijvoorbeeld een teller-eVar gebruiken om het aantal keren te volgen dat iemand uw interne zoekopdracht heeft gebruikt voordat hij een aankoop doet.</li></ul> |
| [!UICONTROL Allocation] | Bepaalt hoe Analytics kredieten voor een succesgebeurtenis toewijst als een variabele veelvoudige waarden vóór de gebeurtenis ontvangt. Tot de ondersteunde waarden behoren:<ul><li>**[!UICONTROL Most Recent]**: De laatste eVar-waarde ontvangt altijd studiepunten voor succesgebeurtenissen tot die eVar verloopt.</li><li>**[!UICONTROL Original Value]**: De eerste eVar krijgt altijd krediet voor succesgebeurtenissen tot die eVar verloopt.</li><li>**[!UICONTROL Linear]**: hiermee worden succesgebeurtenissen gelijkmatig toegewezen aan alle eVar-waarden. Aangezien de Lineaire toewijzing waarden slechts binnen een bezoek nauwkeurig verspreidt, gebruik Lineaire toewijzing met een eVar vervaldatum van Bezoek.</li></ul> **Nota**: De schakelende toewijzing aan of van Lineair verhindert historische gegevens te tonen. Het mengen van toewijzingstypes in de rapporteringsinterface kan tot misverklaarbare gegevens in rapporten leiden. Zo kan lineaire toewijzing inkomsten verdelen over een aantal verschillende eVar-waarden. Na het terugkeren naar de meest recente toewijzing, zou 100% van die opbrengst met de meest recente enige waarde worden geassocieerd. Deze koppeling kan leiden tot onjuiste conclusies van gebruikers.<br><br> om de waarschijnlijkheid van verwarring in het melden te vermijden, maakt Adobe Analytics de historische gegevens niet beschikbaar aan de interface. U kunt deze bekijken als u de opgegeven eVar weer wilt instellen op de eerste toewijzingsinstelling, maar u kunt de instellingen voor eVar-toewijzing niet wijzigen om alleen toegang te krijgen tot de historische gegevens. Adobe raadt aan een nieuwe eVar te gebruiken wanneer nieuwe toewijzingsinstellingen gewenst zijn voor gegevens die al worden geregistreerd, in plaats van toewijzingsinstellingen te wijzigen voor een eVar die al een aanzienlijke hoeveelheid historische gegevens heeft opgebouwd. |
| [!UICONTROL Expire After] | Geeft een tijdsperiode op, of een gebeurtenis, waarna de eVar-waarde vervalt (ontvangt geen krediet meer voor succesgebeurtenissen). Als er een succesgebeurtenis plaatsvindt na het verlopen van eVar, ontvangt de waarde None een creditering voor de gebeurtenis (er was geen eVar actief).  Als u een gebeurtenis selecteert als een vervalwaarde, verloopt de variabele alleen als de gebeurtenis plaatsvindt. Als de gebeurtenis niet voorkomt, verloopt de variabele nooit.  De beschikbare vervalopties kunnen in vier hoofdcategorieën worden ingedeeld:<ul><li>**bij een paginamening of bezoekniveau.** Conversiegebeurtenissen buiten de paginaweergave of het bezoek zijn niet gekoppeld aan de eVar.</li><li>**Gebaseerd op een tijdspanne, zoals dag, week, maand, of jaar.** Conversiegebeurtenissen na de opgegeven periode zijn niet gekoppeld aan de eVar. De vervalperiode begint wanneer de variabele wordt ingesteld. De vervaldatum is gebaseerd op de tijd waarop ze zijn ingesteld, tot de tweede (minuut, uur, dag, maand, enz.): <ul><li>MINUTE=60 seconden</li><li>HOUR=3600 seconden (60 minuten)</li><li>DAY=86400 seconden (24 uur)</li><li>WEEK=604800 seconden (7 dagen)</li><li>MAAND=2678400 seconden (31 dagen)</li><li>QUARTER=8035200 seconden (93 dagen - 3 maanden van 31 dagen)</li><li>JAAR=31536000 seconden (365 dagen)</li><br> als een bezoek bij 7 :00 AM op Maandag begint en eVar wordt geplaatst binnen dat bezoek bij 7 :15 AM, is de vervaldatum zoals hieronder getoond:<li>Vervaldatum dag: eVar verloopt om 7.00 uur op dinsdag.:15</li><li>Vervaldatum week: eVar verloopt op de volgende maandag om 7.00 uur.:15</li><li>Vervaldatum maand: eVar verloopt 31 dagen vanaf maandag om 7.00 uur.:15</li></ul><li>**Specifieke omzettingsgebeurtenissen.** Alle andere conversiegebeurtenissen die na de opgegeven specifieke gebeurtenis plaatsvinden, zijn gekoppeld aan de eVar.</li><li>**nooit.** Zolang het cookie bezoekerID intact is, kan elke hoeveelheid tijd tussen eVar en de gebeurtenis worden doorgegeven.</li></ul> |
| [!UICONTROL Status] (alleen eVar) | Definieert de status [!UICONTROL eVar] :<ul><li>**Gehandicapten**: Maakt [!UICONTROL eVar] onbruikbaar. Hiermee verwijdert u de [!UICONTROL eVar] uit de lijst met conversievariabelen.</li><li>**Geen Subrelations**: Verhindert u om [!UICONTROL eVar] door een dimensie te breken.</li><li>**Basis Subrelations**: Laat u eVar door om het even welke volledige afmeting (bijvoorbeeld, Producten of Campagne) verdelen.</li></ul> |
| [!UICONTROL Reset] | Hiermee wordt de bestaande waarde in de eVar opnieuw ingesteld. Gebruik deze instelling wanneer u een eVar opnieuw gebruikt, zodat u een oude waarde niet in een nieuw rapport mengt. Bij het opnieuw instellen worden geen historische gegevens verwijderd. |
| [!UICONTROL Merchandising] (alleen eVar) | De variabelen van de koophandel kunnen één van twee syntaxis volgen:<ul><li>**[!UICONTROL Products Syntax]** - Koppelt de eVar-waarde aan een product. **Nota**: Als [!UICONTROL Products Syntax] wordt geselecteerd, is de [!UICONTROL Merchandising Binding Event] sectie gehandicapt en niet verkiesbaar voor uitgeven. Voor deze syntaxis is [!UICONTROL Binding Events] niet van toepassing.</li><li>**[!UICONTROL Conversion Variable Syntax]**: Koppelt de eVar alleen aan een product als [!UICONTROL Binding Event] optreedt. In dit geval selecteert u de gebeurtenissen die als [!UICONTROL Binding Events] fungeren.  Als u deze instelling wijzigt zonder de JavaScript-code dienovereenkomstig bij te werken, gaan er gegevens verloren. Zie [ het Merchandising Variabelen ](/help/components/dimensions/evar-merchandising.md).</li></ul> |
| [!UICONTROL Merchandising Binding Event] (alleen eVar) | Als Verplaatsen is ingesteld op [!UICONTROL Conversion Variable Syntax] , binden de geselecteerde gebeurtenissen de huidige eVar-waarde aan een product. Als u een [!UICONTROL Binding Event] wilt gebruiken, stelt u [!UICONTROL Allocation] in op [!UICONTROL Most Recent] . Als [!UICONTROL Allocation] is ingesteld op [!UICONTROL Original Value] , blijft de eerste eVar-productbinding totdat de eVar verloopt. U kunt meerdere gebeurtenissen selecteren door Ctrl (Windows) of cmd (Mac) ingedrukt te houden en op meerdere items in de lijst te klikken. U kunt een gebeurtenis alleen selecteren wanneer [!UICONTROL Conversion Variable Syntax] is geselecteerd. |

### Verlopen

`eVars` verloopt na een door u opgegeven tijdsperiode. Nadat de eVar is verlopen, ontvangt het geen krediet meer voor succesgebeurtenissen. eVars kunnen ook worden geconfigureerd om te verlopen bij succesgebeurtenissen. Als je bijvoorbeeld een interne aanbieding hebt die aan het einde van een bezoek vervalt, ontvangt de interne aanbieding alleen kredieten voor aankopen of registraties die plaatsvinden tijdens het bezoek waarin ze zijn geactiveerd.

Er zijn twee manieren om een eVar te laten verlopen:

* U kunt de eVar instellen op verlopen na een opgegeven periode of gebeurtenis.
* U kunt de vervaldatum van een eVar forceren door deze opnieuw in te stellen. Dit is handig wanneer u een variabele opnieuw gebruikt.

Als u bijvoorbeeld de vervaldatum van een eVar wijzigt van 30 naar 90 dagen, blijven de verzamelde eVar-waarden behouden gedurende de nieuwe vervaldatum (in dit geval 90 dagen). Het systeem kijkt eenvoudig naar de huidige vervalbepaling en het laatste vastgestelde timestamp van de waarde van eVar verzameld om afloop te bepalen. Alleen de optie **[!UICONTROL Reset]** verloopt waarden en doet dit direct.

Een ander voorbeeld: als in mei een eVar wordt gebruikt om interne promoties te weerspiegelen en na 21 dagen verloopt, en in juni wordt deze gebruikt om interne zoektrefwoorden vast te leggen, dan moet u op 1 juni de vervaldatum van de variabele forceren of de variabele opnieuw instellen. Als u dat doet, blijven de interne promotiewaarden buiten de verslagen van juni.

### Hoofdlettergevoeligheid

Vars zijn niet hoofdlettergevoelig. De hoofdletters en kleine letters die bij de rapportage worden gebruikt, zijn gebaseerd op de eerste waarde van de back-endsysteemregisters. Deze waarde kan de eerste instantie zijn die ooit wordt gezien of kan variëren met een bepaalde tijdsperiode (bijvoorbeeld maandelijks), afhankelijk van de verscheidenheid en hoeveelheid gegevens die aan de rapportsuite zijn gekoppeld.

### Tellers

Terwijl eVars het vaakst worden gebruikt om koordwaarden te houden, kunnen zij ook worden gevormd om als tellers te handelen. Variabelen zijn nuttig als tellers wanneer u probeert te tellen het aantal acties een gebruiker vóór een gebeurtenis neemt. U kunt bijvoorbeeld een eVar gebruiken om het aantal interne zoekopdrachten vast te leggen voordat u de aankoop doet. Elke keer dat een bezoeker zoekt, moet de eVar de waarde &#39;+1&#39; bevatten. Als een bezoeker vier keer vóór een aankoop zoekt, wordt een exemplaar voor elk totaal aantal weergegeven: 1,00, 2,00, 3,00 en 4,00. Alleen de 4,00 ontvangen echter krediet voor het aankoopevenement (bestellingen en inkomstencijfers). Alleen positieve getallen zijn toegestaan als waarden van een eVar-teller.

## Conversievariabelen toevoegen of bewerken

1. Klik op **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Conversion Variables]**.
1. Klik op de pagina [!UICONTROL Conversion Variables] op **[!UICONTROL Expand]** icon [+ ] naast de conversievariabele die u wilt wijzigen.

   of

   Klik op **[!UICONTROL Add New]** om een ongebruikte eVar toe te voegen aan de rapportsuite.
1. Selecteer de velden van de conversievariabele die u wilt wijzigen.

   Zie [ Variabelen van de Omzetting - Beschrijvingen ](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md#section_7C317BB0287A4B8EB0A1A4ECC40627BF). In sommige velden kunt u rechtstreeks in het veld typen. Met andere opties kunt u een keuze maken in een vervolgkeuzelijst met ondersteunde waarden.
1. Klik op **[!UICONTROL Save]**.
