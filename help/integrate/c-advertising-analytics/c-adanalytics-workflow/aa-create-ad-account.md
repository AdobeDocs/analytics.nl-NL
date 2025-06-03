---
title: Een Advertising-account instellen in Advertising Analytics
description: In dit artikel wordt uitgelegd hoe u nieuwe advertentierekeningen maakt en meerdere accounts toewijst aan meerdere rapportensuites.
feature: Advertising Analytics
exl-id: f593c714-e85f-4000-85b2-6294cad81e25
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 3%

---

# Een Advertising-account instellen

De Beheerders van Adobe Analytics kunnen nieuwe reclamerekeningen tot stand brengen en veelvoudige rekeningen in kaart brengen aan veelvoudige rapportreeksen (1:1, 1: Velen, Velen: Velen).

De beheerders kunnen ook [ toegang tot niet-admins ](/help/integrate/c-advertising-analytics/overview.md#section_FCC58EB635954A32990D4E67B52B4369) verlenen voor de opstelling van reclamerekeningen.

<!--
![](assets/aa_accounts.png)
-->

1. Navigeer in Adobe Analytics naar **[!UICONTROL Admin]** > **[!UICONTROL Advertising Accounts]** .
1. (Alleen voor de eerste keer) Accepteer de voorwaarden van de licentieovereenkomst voor eindgebruikers.
1. Selecteer **[!UICONTROL + Add]** .
1. Het dialoogvenster [!UICONTROL New search engine setting] wordt weergegeven.

   ![](assets/aa-new-se-account.png)

1. Vul de **[!UICONTROL search engine Settings]** volgende richtlijnen in:

   | Instelling | Beschrijving |
   | --- | --- |
   | **[!UICONTROL Type]** | U hebt twee opties: **[!UICONTROL Google Adwords]** en **[!UICONTROL Bing Ads]** . Opmerking: Yahoo Gemini is door Microsoft geabsorbeerd op 31 maart 2019. Als gevolg hiervan is de optie voor een Yahoo Gemini-advertentieaccount niet meer beschikbaar. |
   | Accountnaam | U kunt deze accountnaam instellen op elke gewenste naam.  Accountnaam is de vriendelijke naam van het account dat in de gebruikersinterface wordt weergegeven. |
   | OAuth Token | **Nota**: OAuth is een open norm voor toegangsdelegatie, algemeen gebruikt als manier om websites of toepassingen toegang tot informatie op websites te verlenen maar zonder wachtwoorden te verstrekken. U merkt dat u naar een externe URL (efrontier.com) wordt gerouteerd. Adobe gebruikt Adobe Media Optimizer om het OAuth-verificatieproces voor alle drie zoekprogramma&#39;s te activeren. Als u Internet Explorer 11 (of eerder) gebruikt, kunt u het token Oauth niet ophalen voor een van de drie zoekmachines. Gebruik in plaats hiervan andere webbrowsers.<p>Selecteer **[!UICONTROL Retrieve Token]** om het OAuth2-verificatieproces te starten. U wordt gevraagd u aan te melden bij uw Google Ads- of Microsoft Advertising-zoekaccount met uw gegevens. Afhankelijk van de gekozen procedure is het proces iets anders: <ul><li>Google-advertenties: Google-account-id opgeven</li><li>Microsoft Advertising: geef je account-id en je account-id op.</li></ul>Verwijs naar [ plaats van uw identiteitskaart van de Rekening ](aa-locate-account-id.md) voor informatie over deze IDs. Nadat u zich hebt aangemeld, wordt het veld **[!UICONTROL OAuth Token]** weergegeven **[!UICONTROL Retrieved]** . |

1. In de sectie **[!UICONTROL Tracking]** geeft u informatie over hoe u de gegevens kunt bijhouden met uw Adobe Analytics-implementatie. Het volgen is een vereiste stap om de gegevens van Adobe Analytics behoorlijk met de gegevens van het onderzoeksmotor te verhogen.
Vul de **[!UICONTROL Tracking Settings]** volgende richtlijnen in:

   | Instelling | Beschrijving |
   | --- | --- |
   | Type | <ul><li>**Auto**: Laat de Motor van de Wolk van de Reclame beslissen hoe de volgende parameters aan de het volgen malplaatjes/bestemming URLs van &#39;s worden toegevoegd. [!UICONTROL Auto Type Tracking] is de eenvoudigste aanpak, maar resulteert mogelijk niet in de beste geïntegreerde gegevensset.<br>**Belangrijk:** om een rekening van de onderzoeksmotor met [!UICONTROL Auto Type Tracking] te vormen, bent u verantwoordelijk voor het nemen van de volgende acties:<ul><li>De parameter `s_kwcid` en de waarde worden toegevoegd aan de sjablonen voor het bijhouden van accounts of de bestemmingspagina-URL&#39;s in de account die wordt toegevoegd. De parameter en de waarde worden ingevoegd aan het einde van de URL. Aanvullende actie is mogelijk vereist als uw webserver aan het einde van de URL een bepaald `key=value` paar nodig heeft. Of een update ter ondersteuning van een nieuw `key=value` -paar in de URL is vereist. **Nota**: Leer meer op of u deze parameter aan uw [ Beleid van de Veiligheid van de Inhoud ](https://experienceleague.adobe.com/nl/docs/id-service/using/reference/csp) zou moeten toevoegen.</li><li>Daarnaast kunnen trefwoorden in de bestemmings-URL worden ingevoegd als onderdeel van de waarde `s_kwcid` . Bevestig dat uw webserver deze tekens kan ondersteunen als de trefwoorden speciale tekens of symbolen bevatten. Een voorbeeld van veel voorkomende speciale tekens is `+` , dat wordt gebruikt in trefwoorden &#39;Grote overeenkomst gewijzigd&#39;.</li></ul></li><li>**Hand**: Laat u beheren hoe de volgende parameters aan het volgen van de motor malplaatjes/bestemmingsURLs worden toegevoegd. [ verwijs naar deze handmatige volgende voorbeelden voor elke onderzoeksmotor ](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manual-vs-automatic-tracking.md).</li></ul> |

1. Selecteer **[!UICONTROL Save]** .
1. Een disclaimer geeft een lijst met waarschuwingen weer. Bevestig dat u deze overeenkomst hebt gelezen en begrepen. Selecteer het selectievakje en selecteer vervolgens **[!UICONTROL OK]** .

   U wordt nu genomen aan de Rekeningen van Advertising [ Beheer UI ](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-manage-ad-accounts.md), waar uw onlangs gecreeerd rekening zou moeten worden vermeld.

>[!NOTE]
>
>U moet ten minste 24 uur wachten voordat de gegevens van het zoekprogramma de analyserapporten gaan vullen.
