---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace delen
title: Projecten delen
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 58abc4a8410441a3c76c6737ace8e2c5ab5c1374
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# Projecten delen

U kunt een project delen met bestaande Adobe Analytics-gebruikers of -groepen in uw organisatie. Wanneer u een project deelt zoals beschreven in deze sectie, moeten de gebruikers u met delen reeds een rekening van Adobe Analytics hebben.

U kunt een specifieke rol met gebruikers of groepen delen, of u kunt een verbinding delen.

* [Een specifieke projectrol delen](#share-a-specific-project-role)

* [Een koppeling naar een project delen](#share-a-link-to-a-project)

## Een specifieke projectrol delen

Wanneer het delen van een specifieke projectrol met gebruikers en groepen in uw organisatie, overweeg het volgende:

* Projectrollen (**[!UICONTROL Can edit]**, **[!UICONTROL Can duplicate]**, en **[!UICONTROL Can view]**) is gekoppeld aan de gebruiker en specifieke project-id. De rollen van het project zijn onafhankelijk van gebruikerstoestemmingen die in [Adobe Experience Cloud-beheerconsole](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html).

* In Adobe Analytics worden groepen gedefinieerd op basis van productprofielen in de [Adobe Experience Cloud-beheerconsole](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/admin-getting-started.html). Beheerders kunnen gegevens delen met elke groep, inclusief Alles. Niet-beheerders kunnen delen met elke groep waarvan zij lid zijn, met uitzondering van &quot;Alle&quot;.

* Een gebruiker die in veelvoudige rollen wordt geplaatst krijgt altijd de hoogste ervaring. Dit kan voorkomen als een gebruiker zowel als individu als deel van een groep wordt toegevoegd. Als een gebruiker bijvoorbeeld de opdracht **[!UICONTROL Can edit]** als individu en **[!UICONTROL Can view]** als lid van een groep ontvangen zij een **[!UICONTROL Can edit]** ervaring met projecten.

* Beheerders die in het dialoogvenster **[!UICONTROL Can duplicate]** of **[!UICONTROL Can view]** de rol krijgt die beperkte ervaring wanneer zij een project openen . Indien gewenst kan een beheerder zijn rol verhogen tot **[!UICONTROL Can edit]** op elk moment **[!UICONTROL Components]>[!UICONTROL Projects]**.

Een specifieke projectrol delen met gebruikers of groepen in uw organisatie:

1. Ga naar het project dat u wilt delen, dan klik **[!UICONTROL Share]** > **[!UICONTROL Share project]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.

   ![](assets/share-proj-modal.png)

   Voor informatie over hoe te om veelvoudige projecten gelijktijdig te delen, zie [Projecten delen in de projectmanager](#share-projects-in-the-project-manager).

1. Voeg ontvangers of groepen ontvangers toe aan een van de opgegeven rolvelden:

   **Kan bewerken:** Ontvangers kunnen **[!UICONTROL Save]** veranderingen in een project en functie als mede-eigenaars. Deze rol is nuttig als u een project met andere collega&#39;s wilt cobeheren; dit omvat het uitgeven, schrappen, en het wijzigen van ontvankelijke lijsten voor een gedeeld project. <br>Opmerking: Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. Het wordt daarom aanbevolen dat slechts één gebruiker een project tegelijk bewerkt. Als projecten tegelijkertijd worden opgeslagen, blijft de laatste versie behouden.

   **Kan dupliceren:** Ontvangers kunnen **[!UICONTROL Save as]** en toegang hebben tot de linkerspoorstaaf. Projectinteracties zijn in deze rol niet beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die de gegevens van uw organisatie en hoe te om Analysis Workspace begrijpen, maar u wilt niet uw project veranderen.

   **Kan weergeven:** Ontvangers kunnen niet **[!UICONTROL Save]** of **[!UICONTROL Save as]** en hebben geen toegang tot de linkerspoorstaaf. De interactie tussen projecten is ook beperkt. Deze rol is nuttig als u een project aan gebruikers wilt delen die minder vertrouwd met de gegevensstructuur van uw organisatie, Analysis Workspace of Adobe Analytics in het algemeen zijn. U wilt echter nog steeds dat ze gegevens en inzichten in een veilige omgeving gebruiken. Meer informatie over de [Kan projectervaring bekijken](/help/analyze/analysis-workspace/curate-share/view-only-projects.md).

1. Geef op of u de volgende opties wilt inschakelen bij het delen van het project:

   * **Ingesloten projectcomponenten delen:** Deelt segmenten, berekende metriek, en datumwaaiers met alle ontvangers. Nadat deze componenten worden gedeeld, zullen deze in de drop-down Componenten van de Werkruimte van de ontvanger verschijnen. Deze instelling blijft niet bestaan. Het is een eenmalige actie op het moment van delen.

   * **Instellen als bestemmingspagina voor ontvangers:** Hiermee stelt u deze pagina in als de bestemmingspagina voor ontvangers. Deze instelling blijft niet bestaan. Het is een eenmalige actie op het moment van delen.

1. Klik op **[!UICONTROL Share]**.
U kunt ook op **[!UICONTROL Curate and Share]** om automatisch projectcuratie toe te passen. Als een project reeds is gedeeld, zullen deze knopen zeggen **[!UICONTROL Update]** en **[!UICONTROL Curate & Update]**. Meer informatie over [projectcursus](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html).

## Een koppeling naar een project delen

Houd rekening met het volgende wanneer u een koppeling deelt zoals wordt beschreven in deze sectie:

* Ontvangers die de koppeling gebruiken, moeten zich aanmelden bij Adobe Analytics voordat ze toegang krijgen tot het project.

* Als aan een ontvanger geen rol wordt toegewezen en een ontvanger ontvangt [link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) aan het project (**[!UICONTROL Share]>[!UICONTROL Get project link]**) krijgen ze standaard een rol toegewezen. Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**.

De projectkoppeling delen met gebruikers in uw organisatie:

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Share project]**. <!-- recommned changing "Share project" to "Share project internally" or something like that -->
Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd eerst uw project op te slaan.

   ![](assets/share-proj-modal.png)

1. Klikken **[!UICONTROL Copy link]** naast de **[!UICONTROL Share URL field]**.

1. Deel de koppeling met gebruikers in uw organisatie. U kunt het bijvoorbeeld in een e-mail, op een interne website, enzovoort plakken.

## Projecten delen in de projectmanager {#Manager}

Projecten kunnen ook worden gedeeld vanuit **[!UICONTROL Components]>[!UICONTROL Projects]**. U kunt één project delen volgens dezelfde stappen hierboven.  Als de veelvoudige projecten worden geselecteerd om worden gedeeld, zullen de ontvangers aan de bestaande lijst van ontvangers voor elk project worden toegevoegd.

Bijvoorbeeld:

* Project A wordt gedeeld aan ontvangers 1, 2, 3
* Project B wordt gedeeld aan ontvangers 4, 5, 6

Als Project A en B zijn geselecteerd, worden ontvangers 4 en 7 toegevoegd aan de aandelenlijsten. De nieuwe lijst van het aandeel voor elk project is nu:

* Project A: 1, 2, 3, 4, 7
* Project B: 4, 5, 6, 7

![](assets/mult-proj-sharing.png)

## Ingesloten componenten delen

Hier volgt een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/24713/?quality=12)

## Veelgestelde vragen {#FAQs}

| Vraag | Antwoord |
| --- | --- |
| Wat gebeurt er als twee editors tegelijkertijd een project opslaan? | De wijzigingen worden niet samengevoegd en de laatst opgeslagen projectversie blijft behouden. Analysis Workspace biedt momenteel geen ondersteuning voor live samenwerken. |
| Als beheerder, welke projectervaring zal ik zien? | Beheerders die in een **[!UICONTROL Can duplicate]** of **[!UICONTROL Can view]** de rol zal deze beperkte ervaring opdoen wanneer zij een project openen . Indien gewenst kan een beheerder zijn rol verhogen tot **[!UICONTROL Can edit]** op elk moment **[!UICONTROL Components]>[!UICONTROL Projects]**. |
| Wat gebeurt er als een ontvanger in één rol als individu en een andere rol als lid van een groep wordt geplaatst? | Als een ontvanger in veelvoudige rollen wordt geplaatst, zullen zij altijd de hogere ervaring ontvangen. Als een ontvanger bijvoorbeeld de opdracht **[!UICONTROL Can edit]** als individu en **[!UICONTROL Can view]** als lid van een groep ontvangen zij een **[!UICONTROL Can edit]** ervaring met projecten. |
| Welke ervaring krijgt een ontvanger als deze een projectverbinding opent? | Ontvangers krijgen de rol die u hen in de deelmodus hebt geplaatst. Als aan een ontvanger geen rol wordt toegewezen en een koppeling naar het project wordt ontvangen (**[!UICONTROL Share]>[!UICONTROL Get project link]**), worden ze standaard in een rol geplaatst. Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**. |
