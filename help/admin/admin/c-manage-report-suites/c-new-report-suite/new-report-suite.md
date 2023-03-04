---
description: U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.
title: Nieuwe rapportsuite - instellingen
feature: Report Suite Settings
uuid: 3508f684-11a3-4c8f-a233-bea6bafd57c0
exl-id: ea5f8543-058d-4e08-bc66-575e3a7460c2
source-git-commit: c53f886d5329e2a3b5023f9396c3aa2360a86901
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 2%

---

# Nieuwe rapportsuite - instellingen

U kunt een nieuwe rapportreeks tot stand brengen door een vooraf bepaalde malplaatje te selecteren, of door één van uw bestaande rapportreeksen te gebruiken om als model te dienen.

Beschrijvingen van de elementen die worden gebruikt wanneer [een rapportenpakket maken](/help/admin/admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md).

>[!NOTE]
>
>De [Documentatie van Virtual Report Suite](/help/components/vrs/c-workflow-vrs/vrs-create.md) toont u hoe te om virtuele rapportseries tot stand te brengen.

| Element | Beschrijving |
| --- | --- |
| Rapportsuite-id | Hiermee geeft u een unieke id op die alleen alfanumerieke tekens mag bevatten. Deze id kan na het maken niet meer worden gewijzigd. Adobe stelt het vereiste ID-voorvoegsel in en kan ook niet worden gewijzigd.  Wanneer het creëren van veelvoudige rapportreeksen, zorg ervoor dat de noemende overeenkomst u gebruikt unieke rapportreeks IDs waarborgt. |
| Titel site | Identificeert de rapportsuite in Admin Tools. Deze titel wordt ook gebruikt in de drop-down lijst van de Reeks van het Rapport in de reeksheader. |
| Tijdzone | Hiermee plant u gebeurtenissen en tijdstempelgegevens. |
| Basis-URL | (Facultatief) bepaalt het basisdomein voor de rapportreeks. Deze URL werkt als een intern filter URL als u niet uitdrukkelijk interne filters URL voor de rapportreeks bepaalt. |
| Standaardpagina | (Optioneel) De standaardwaarde voor de pagina wordt doorgehaald bij URL&#39;s die worden aangetroffen. Als uw rapport met de meest populaire pagina&#39;s URL&#39;s bevat in plaats van paginanamen, voorkomt deze instelling dat meerdere URL&#39;s voor dezelfde webpagina worden gebruikt.  De URL&#39;s `https://example.com` en `https://example.com/index.html` zijn doorgaans dezelfde pagina.<p> U kunt externe bestandsnamen verwijderen, zodat beide URL&#39;s worden weergegeven als `https://example.com` in uw rapporten. Als u deze waarde niet instelt, verwijdert Analytics automatisch de volgende bestandsnamen van URL&#39;s: `index.htm`, `index.html`, `index.cgi`, `index.asp`,  `default.htm`, `default.html`, `default.cgi`, `default.asp`, `home.htm`, `home.html`, `home.cgi`, en `home.asp`. Als u het strippen van bestandsnamen wilt uitschakelen, geeft u een standaardpaginawaarde op die nooit voorkomt in uw URL&#39;s. |
| Live-datum | Informeert Adobe van de datum dat u verwacht dat deze rapportsuite actief wordt. Als uw plaatsingsprogramma verandert, verstrek een bijgewerkte verkeersschatting gebruikend het Permanente Verwachte hulpmiddel van het Verkeer in het Beheer van het Verkeer. |
| Geschat aantal paginaweergaven per dag | Hiermee wordt het geschatte aantal paginaweergaven aangegeven dat deze rapportsuite per dag moet ondersteunen. Grote verkeersvolumes vereisen een langer goedkeuringsproces. Om vertragingen bij de verwerking te voorkomen, moet u zo nauwkeurig mogelijk met deze schatting omgaan. |
| Basisvaluta | Geeft de standaardvaluta aan die wordt gebruikt om alle monetaire gegevens op te slaan. Analytische rapportage converteert transacties in andere valuta&#39;s naar de basisvaluta, waarbij de huidige omrekeningskoers wordt gebruikt op het tijdstip dat de gegevens worden ontvangen. Analytische rapportage gebruikt de JavaScript-variabele currencyCode om de valuta van een bepaalde transactie te identificeren. |
| Ondersteuning voor multi-byte tekens uitschakelen | Hiermee schakelt u multibyte-tekenondersteuning voor de rapportsuite uit. Als u multibyte-tekenondersteuning uitschakelt, gaat het systeem ervan uit dat gegevens zich in `ISO-8859-1` gebruiken. Webpagina&#39;s moeten hun tekenset opgeven in de JavaScript-variabele charSet. <p>Bij multibyte-tekenondersteuning worden tekens in de rapportsuite opgeslagen met UTF-8. Na ontvangst zet het systeem gegevens van de tekenset van uw webpagina om in de tekenset UTF-8, zodat u elke taal in uw marketingrapporten kunt gebruiken.  Neem contact op met uw Adobe-accountteam of de klantenservice om de multibyte-tekenondersteuning voor een bestaande rapportsuite te wijzigen. |

{style=&quot;table-layout:auto&quot;}
