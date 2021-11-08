---
description: De Custom Insight-conversievariabele (of -eVar) wordt in de Adobe-code op geselecteerde webpagina's van uw site geplaatst. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op bezoek-gebaseerd zijn en functioneren gelijkaardig aan koekjes. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.
keywords: eVar
title: Conversievariabelen (eVar)
feature: Admin Tools
uuid: 1eed0cb1-0735-4142-be21-43f264216b50
exl-id: 822ecaff-a06c-42e1-aee8-ef4a43df4230
source-git-commit: 38fb7ec39495b2b8cde4955bd1b3c1d3487632c3
workflow-type: tm+mt
source-wordcount: '1525'
ht-degree: 0%

---

# Conversievariabelen (eVars)

De Custom Insight-conversievariabele (of -eVar) wordt in de Adobe-code op geselecteerde webpagina&#39;s van uw site geplaatst. Zijn belangrijkste doel is omzettingssuccesmetriek in douane marketing rapporten te segmenteren. Een eVar kan op bezoek-gebaseerd zijn en functioneren gelijkaardig aan koekjes. De waarden die in eVar-variabelen worden doorgegeven, volgen de gebruiker gedurende een vooraf bepaalde periode.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/28759/?quality=12)

Wanneer een eVar aan een waarde voor een bezoeker wordt geplaatst, onthoudt Adobe automatisch die waarde tot het verloopt. Eventuele succesgebeurtenissen die een bezoeker tegenkomt terwijl de waarde eVar actief is, worden geteld bij de waarde eVar.

Vars kunnen het beste worden gebruikt om oorzaak en effect te meten, zoals:

* Welke interne campagnes de inkomsten beïnvloedden
* Welke banneradvertenties uiteindelijk hebben geresulteerd in een registratie
* Het aantal keren dat een interne zoekopdracht is gebruikt voordat een bestelling is gemaakt

Als verkeersmeting of het kleven gewenst is, wordt het gebruiken van verkeersvariabelen geadviseerd.

>[!NOTE]
>
>Er kan slechts één waarde worden opgeslagen in een eVar in een afbeeldingsaanvraag. Als er meerdere waarden in een eVar-waarde zijn gewenst, raden we u aan deze te implementeren [Variabelen weergeven (lijstvariabelen)](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/page-variables.html).

## Conversievariabelen - beschrijvingen {#section_7C317BB0287A4B8EB0A1A4ECC40627BF}

Beschrijvingen van velden die worden gebruikt wanneer [conversievariabelen bewerken](/help/admin/admin/conversion-var-admin/t-conversion-variables-admin.md).

| Element | Beschrijving |
| --- | --- |
| [!UICONTROL Name] | De vriendelijke naam van de conversievariabele. Deze naam is hoe naar de eVar wordt verwezen in algemene rapportering, en zal de naam van het rapport/de dimensie in het linkermenu zijn. |
| [!UICONTROL Type]  (alleen eVar) | Het type van veranderlijke waarde:<ul><li>**[!UICONTROL Text String]**: Hiermee legt u tekstwaarden vast die op uw site worden gebruikt. Dit is het meest gangbare type eVar en de standaardinstelling. De methode werkt op dezelfde manier als andere variabelen, waarbij de waarde erin een statische tekenreeks is. Als u zaken zoals interne campagnes of interne onderzoekssleutelwoorden volgt, is dit het geadviseerde plaatsen.</li><li>**[!UICONTROL Counter]**: Telt het aantal keren dat een actie vóór de succesgebeurtenis voorkomt. Als u bijvoorbeeld een eVar gebruikt om interne zoekopdrachten op uw site bij te houden, stelt u deze waarde in op [!UICONTROL Text String] om het gebruik van zoektermen te volgen. Deze waarde instellen op [!UICONTROL Counter] om het aantal uitgevoerde zoekopdrachten te tellen, ongeacht de gebruikte zoektermen. U kunt bijvoorbeeld een teller gebruiken om het aantal keren te volgen dat iemand uw interne zoekopdracht heeft gebruikt voordat hij een aankoop doet.</li></ul> |
| [!UICONTROL Allocation] | Bepaalt hoe Analytics kredieten voor een succesgebeurtenis toewijst als een variabele veelvoudige waarden vóór de gebeurtenis ontvangt. Tot de ondersteunde waarden behoren:<ul><li>**[!UICONTROL Most Recent]**: De laatste waarde van de eVar ontvangt altijd krediet voor succesgebeurtenissen tot die eVar verloopt.</li><li>**[!UICONTROL Original Value]**: De eerste eVar krijgt altijd krediet voor succesgebeurtenissen tot die eVar verloopt.</li><li>**[!UICONTROL Linear]**: Hiermee worden succesgebeurtenissen gelijkmatig toegewezen aan alle eVar-waarden. Aangezien de Lineaire toewijzing waarden slechts binnen een bezoek nauwkeurig verdeelt, gebruik Lineaire toewijzing met een eVar van Bezoek.</li></ul> **Opmerking**: Als u van of naar Lineair schakelt, worden historische gegevens niet weergegeven. Het mengen van toewijzingstypes in de rapporteringsinterface kan tot misverklaarbare gegevens in rapporten leiden. Zo kan lineaire toewijzing inkomsten verdelen over een aantal verschillende eVar. Na het terugkeren naar de meest recente toewijzing, zou 100% van die opbrengst met de meest recente enige waarde worden geassocieerd. Deze koppeling kan leiden tot onjuiste conclusies van gebruikers.<br><br>Om verwarring bij de rapportage te voorkomen, maakt Adobe Analytics de historische gegevens niet beschikbaar voor de interface. U kunt deze weergeven als u de opgegeven eVar wilt wijzigen in de oorspronkelijke toewijzingsinstelling, maar u kunt de instellingen voor de eVar-toewijzing niet wijzigen om alleen toegang te krijgen tot de historische gegevens. Adobe raadt aan een nieuwe eVar te gebruiken wanneer nieuwe toewijzingsinstellingen gewenst zijn voor gegevens die al worden geregistreerd, in plaats van toewijzingsinstellingen te wijzigen voor een eVar waarin al een aanzienlijke hoeveelheid historische gegevens is opgebouwd. |
| [!UICONTROL Expire After] | Geeft een tijdsperiode op, of een gebeurtenis, waarna de waarde van de eVar verloopt (ontvangt geen krediet meer voor succesgebeurtenissen). Als een succesgebeurtenis optreedt na het verlopen van de eVar, ontvangt de waarde None een creditering voor de gebeurtenis (er was geen eVar actief).  Als u een gebeurtenis selecteert als een vervalwaarde, verloopt de variabele alleen als de gebeurtenis plaatsvindt. Als de gebeurtenis niet voorkomt, verloopt de variabele nooit.  De beschikbare vervalopties kunnen in vier hoofdcategorieën worden ingedeeld:<ul><li>**Op pagina- of bezoekniveau.** Conversiegebeurtenissen buiten de paginaweergave of het bezoek zijn niet gekoppeld aan de eVar.</li><li>**Gebaseerd op een tijdsperiode, zoals dag, week, maand, of jaar.** Conversiegebeurtenissen na de opgegeven periode worden niet aan de eVar gekoppeld. De vervalperiode begint wanneer de variabele wordt ingesteld. De vervaldatum is gebaseerd op de tijd waarop ze zijn ingesteld, tot de tweede (minuut, uur, dag, maand, enz.): <ul><li>MINUTE=60 seconden</li><li>HOUR=3600 seconden (60 minuten)</li><li>DAY=86400 seconden (24 uur)</li><li>WEEK=604800 seconden (7 dagen)</li><li>MAAND=2678400 seconden (31 dagen)</li><li>QUARTER=8035200 seconden (93 dagen - 3 maanden van 31 dagen)</li><li>JAAR=31536000 seconden (365 dagen)</li><br>Als het bezoek begint om 7:00 uur op maandag en er tijdens dat bezoek om 7:15 uur een eVar is ingesteld, is de vervaldatum als volgt:<li>Vervaldag: eVar verloopt om 7:15 op dinsdag.</li><li>Vervaldatum week: eVar verloopt op de volgende maandag om 7:15 uur.</li><li>Vervaldatum maand: eVar vervalt 31 dagen vanaf maandag om 7.15 uur.</li></ul><li>**Specifieke conversiegebeurtenissen.** Alle andere conversiegebeurtenissen die na de opgegeven specifieke gebeurtenis plaatsvinden, zijn gekoppeld aan de eVar.</li><li>**Nooit.** Zolang het bezoekerID-cookie intact is, kan elke hoeveelheid tijd tussen eVar en gebeurtenis worden doorgegeven.</li></ul> |
| [!UICONTROL Status]  (alleen eVar) | Definieert de [!UICONTROL eVar] status:<ul><li>**Uitgeschakeld**: Hiermee schakelt u de [!UICONTROL eVar]. Hiermee verwijdert u de [!UICONTROL eVar] in de lijst met conversievariabelen.</li><li>**Geen subrelaties**: Hiermee voorkomt u dat de [!UICONTROL eVar] door een dimensie.</li><li>**Basissubrelaties**: Hiermee kunt u een eVar afsplitsen op een volledige afmeting (bijvoorbeeld Producten of Campagne).</li></ul> |
| [!UICONTROL Reset] | Hiermee wordt de bestaande waarde in de eVar opnieuw ingesteld. Gebruik deze instelling bij het opnieuw gebruiken van een eVar, zodat u een oude waarde kunt mengen in een nieuw rapport. Bij het opnieuw instellen worden geen historische gegevens verwijderd. |
| [!UICONTROL Merchandising]  (alleen eVar) | De variabelen van de koophandel kunnen één van twee syntaxis volgen:<ul><li>**[!UICONTROL Products Syntax]**: Koppelt de waarde van de eVar aan een product. **Opmerking**: Indien [!UICONTROL Products Syntax] is geselecteerd, [!UICONTROL Merchandising Binding Event] is uitgeschakeld en kan niet worden geselecteerd voor bewerken. Voor deze syntaxis: [!UICONTROL Binding Events] niet van toepassing zijn.</li><li>**[!UICONTROL Conversion Variable Syntax]**: Koppelt de eVar alleen aan een product als een [!UICONTROL Binding Event] voorkomt. In dit geval selecteert u de gebeurtenissen die fungeren als [!UICONTROL Binding Events].  Als u deze instelling wijzigt zonder uw JavaScript-code dienovereenkomstig bij te werken, gaan er gegevens verloren. Zie [Merchandising Variables](/help/components/dimensions/evar-merchandising.md).</li></ul> |
| [!UICONTROL Merchandising Binding Event] (alleen eVar) | Als Verschuiven is ingesteld op [!UICONTROL Conversion Variable Syntax]De geselecteerde gebeurtenissen binden de huidige eVar-waarde met een product. Als u een [!UICONTROL Binding Event], set [!UICONTROL Allocation] tot [!UICONTROL Most Recent]. Indien [!UICONTROL Allocation] is ingesteld op [!UICONTROL Original Value], blijft de eerste productbinding van de eVar tot de eVar verloopt. U kunt meerdere gebeurtenissen selecteren door Ctrl (Windows) of cmd (Mac) ingedrukt te houden en op meerdere items in de lijst te klikken. U kunt alleen een gebeurtenis selecteren wanneer [!UICONTROL Conversion Variable Syntax] is geselecteerd. |

### Verlopen

`eVars` verlopen na een door u opgegeven tijdsperiode. Nadat de eVar is verlopen, ontvangt het geen krediet meer voor succesgebeurtenissen. eVars kunnen ook worden geconfigureerd om te verlopen bij succesgebeurtenissen. Als je bijvoorbeeld een interne aanbieding hebt die aan het einde van een bezoek vervalt, ontvangt de interne aanbieding alleen kredieten voor aankopen of registraties die plaatsvinden tijdens het bezoek waarin ze zijn geactiveerd.

Er zijn twee manieren om een eVar te verlopen:

* U kunt instellen dat de eVar na een opgegeven tijdsperiode of gebeurtenis vervalt.
* U kunt de vervaldatum van een eVar forceren door deze opnieuw in te stellen. Dit is handig wanneer u een variabele opnieuw gebruikt.

Als u bijvoorbeeld de vervaldatum van een eVar wijzigt van 30 tot 90 dagen, blijven de verzamelde eVar behouden gedurende de nieuwe vervaldatum (in dit geval 90 dagen). Het systeem bekijkt eenvoudig de huidige die vervalbepaling en laatste vastgestelde timestamp van de eVar waarde wordt verzameld om afloop te bepalen. Alleen de **[!UICONTROL Reset]** Deze optie vervalt waarden en doet dit onmiddellijk.

Een ander voorbeeld: Als een eVar in Mei wordt gebruikt om interne bevorderingen te weerspiegelen en na 21 dagen verloopt, en in juni wordt het gebruikt om interne onderzoekssleutelwoorden te vangen, dan zou u op 1 Juni de afloop van, of het terugstellen van, de variabele moeten dwingen. Als u dat doet, blijven de interne promotiewaarden buiten de verslagen van juni.

### Hoofdlettergevoeligheid

Vars zijn niet hoofdlettergevoelig. De hoofdletters en kleine letters die bij de rapportage worden gebruikt, zijn gebaseerd op de eerste waarde van de back-endsysteemregisters. Deze waarde kan de eerste instantie zijn die ooit wordt gezien of kan variëren met een bepaalde tijdsperiode (bijvoorbeeld maandelijks), afhankelijk van de verscheidenheid en hoeveelheid gegevens die aan de rapportsuite zijn gekoppeld.

### Tellers

Terwijl eVars het vaakst worden gebruikt om koordwaarden te houden, kunnen zij ook worden gevormd om als tellers te handelen. Variabelen zijn nuttig als tellers wanneer u probeert te tellen het aantal acties een gebruiker vóór een gebeurtenis neemt. U kunt bijvoorbeeld een eVar gebruiken om het aantal interne zoekopdrachten vast te leggen voordat u de aankoop doet. Telkens wanneer een bezoeker zoekt, moet de eVar de waarde &#39;+1&#39; bevatten. Als een bezoeker vier keer vóór een aankoop zoekt, ziet u een exemplaar voor elk totaal aantal: 1,00, 2,00, 3,00 en 4,00. Alleen de 4,00 ontvangen echter krediet voor het aankoopevenement (bestellingen en inkomstencijfers). Alleen positieve getallen zijn toegestaan als waarden van een eVar-teller.
