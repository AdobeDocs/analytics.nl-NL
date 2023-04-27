---
description: Projectdeling en projectrollen in Workspace
keywords: Analysis Workspace delen
title: Projecten delen
feature: Curate and Share
role: User, Admin
exl-id: da106eb1-7f5c-469a-a8aa-8497fc3706dc
source-git-commit: 836b2c91cf401b7133d3569ae64154a24d2923f7
workflow-type: tm+mt
source-wordcount: '1655'
ht-degree: 0%

---

# Projecten delen

U kunt een Analysis Workspace-project delen met de volgende typen personen:

* Gebruikers en groepen in uw organisatie die toegang hebben tot Adobe Analytics

   U kunt de toegang Bewerken, Dupliceren of Weergeven delen

* Gebruikers en groepen in uw organisatie die geen toegang hebben tot Adobe Analytics

   Ontvangers hebben alleen-lezen toegang

* Personen buiten uw organisatie

   Ontvangers hebben alleen-lezen toegang

Alle [kromming](curate.md) Wanneer ontvangers het project openen, wordt u deze toepassing vóór het delen weergegeven.

Hier volgt een video-overzicht van het delen van projecten:

>[!VIDEO](https://video.tv.adobe.com/v/36207/?quality=12)


## Delen met Analysis Workspace-gebruikers en -groepen in uw organisatie {#Add}

U kunt een project delen met bestaande Analysis Workspace-gebruikers of -groepen in uw organisatie. Wanneer u een project deelt zoals beschreven in deze sectie, moeten de gebruikers u met delen reeds toegang tot Adobe Analytics hebben.

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

1. Ga naar het project dat u wilt delen, dan klik **[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]**.
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

1. Klik op **[!UICONTROL Share]**. (Als het project al is gedeeld, klikt u op [!UICONTROL **Bijwerken**].)

   of

   Klikken **[!UICONTROL Curate and Share]** om automatisch projectcuratie toe te passen. (Als het project al is gedeeld, klikt u op **[!UICONTROL Curate & Update]**.) Meer informatie over [projectcursus](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/curate.html).

## Een koppeling naar een project delen

Houd rekening met het volgende wanneer u een koppeling deelt zoals wordt beschreven in deze sectie:

* Ontvangers die de koppeling gebruiken, moeten zich aanmelden bij Adobe Analytics voordat ze toegang krijgen tot het project.

* Als aan een ontvanger geen rol wordt toegewezen en een ontvanger ontvangt [link](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/shareable-links.html) aan het project wordt hun standaard een rol toegekend . Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**.

De projectkoppeling delen met gebruikers in uw organisatie:

1. Sla het project op. Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd uw project op te slaan voordat u een koppeling deelt.

1. Selecteren **[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** selecteert u vervolgens **[!UICONTROL Copy]** naast de **[!UICONTROL Share by link]** veld.

   ![](assets/share-proj-modal.png)

1. Deel de koppeling met gebruikers in uw organisatie. U kunt het bijvoorbeeld in een e-mail, op een interne website, enzovoort plakken.

## Een project delen met iedereen (geen aanmelding vereist) {#share-public-link}

{{release-limited-testing-section}}

U kunt [alleen-lezen toegang](/help/analyze/analysis-workspace/curate-share/view-only-projects.md) naar Analysis Workspace-projecten voor mensen die geen toegang hebben tot Adobe Analytics. Dit kan het volgende omvatten:

* Personen buiten uw organisatie

* Personen binnen uw organisatie die niet zijn voorzien van Adobe Analytics

>[!NOTE]
>
>Houd rekening met het volgende wanneer u een Analysis Workspace-project deelt met mensen die geen toegang hebben tot Adobe Analytics:
>
>* De capaciteit om een project op deze manier te delen kan door de beheerder van Analytics worden onbruikbaar gemaakt, zoals die in wordt beschreven [Voorkeuren](/help/analyze/analysis-workspace/user-preferences.md). Als u een project niet kunt delen zoals die in deze sectie wordt beschreven, heeft uw beheerder Analytics deze capaciteit onbruikbaar gemaakt.
>
>* Projecten met meer dan 50 uitgebreide visualisaties kunnen niet worden gedeeld met mensen die geen toegang hebben tot Adobe Analytics.
>
>* Gebruikers met wie u deelt, kunnen alle filters weergeven die tijdens het project op het project zijn toegepast [kromming](curate.md).
> 
>* Gebruikers met wie u deelt, kunnen het datumbereik van het project wijzigen. De datumwaaier u voor het project plaatst wordt getoond door gebrek.


Een Analysis Workspace-project delen met mensen die geen toegang hebben tot Adobe Analytics:

1. Open het Analysis Workspace-project dat u wilt delen.

1. Klik op **[!UICONTROL Share]** > **[!UICONTROL Share with anyone]**.

   Als er niet-opgeslagen wijzigingen zijn, wordt u gevraagd uw project op te slaan.

   <!-- Add screen shot of new modal -->

1. De optie **[!UICONTROL Link is active]** als deze optie nog niet is ingeschakeld.

   Als u deze optie selecteert, wordt een koppeling naar het project gemaakt die met iedereen kan worden gedeeld. U kunt toegang tot het project op elk ogenblik onbruikbaar maken door deze optie onbruikbaar te maken.

   De eigenaar van het project is ook de eigenaar van deze verbinding. De eigendom van de verbinding kan aan een andere gebruiker slechts worden overgebracht wanneer de projecteigendom, zoals die in wordt beschreven wordt overgebracht [Gebruikerselementen overdragen of verlopen van account instellen](/help/admin/admin/user-management2/users-assets.md) in de handleiding Analytics Admin.

1. Geef op of u de volgende beveiligingsoptie wilt inschakelen (deze optie kan worden beheerd door de beheerder van Analytics):

   * **[!UICONTROL Require Experience Cloud authentication]:**

      Wanneer deze optie is ingeschakeld, hebben alleen gebruikers die zich kunnen aanmelden bij de Adobe Experience Cloud-organisatie waar het project dat u deelt, is gemaakt, toegang tot het project.

      Analysebeheerders kunnen deze voorkeur voor het bedrijf, zoals die in wordt beschreven vormen [Voorkeuren](/help/analyze/analysis-workspace/user-preferences.md). U zou de volgende scenario&#39;s, afhankelijk van kunnen ontmoeten hoe de beheerder deze optie vormde:

      * Als deze optie niet zichtbaar is, heeft de beheerder van Analytics deze functie niet ingeschakeld.

      * Als deze optie is ingeschakeld en gedimd, vereist de beheerder van Analytics Experience Cloud-verificatie voor iedereen die Analysis Workspace-projecten opent.

1. Naast de **[!UICONTROL Share with anyone (no login required)]** veld, klikt u op de knop **Koppeling kopiëren** pictogram ![Koppelingspictogram kopiëren](assets/copy-link-icon.png) om de koppeling naar het systeemklembord te kopiëren.

1. Deel de koppeling met de personen die u toegang tot het project wilt geven. U kunt de koppeling bijvoorbeeld in een e-mail plakken.

   Iedereen met wie u de koppeling deelt, kan het Analysis Workspace-project bekijken.

1. (Optioneel) U kunt op de knop **Nieuwe koppeling genereren** pictogram ![Koppelingspictogram genereren](assets/regenerate-link.png) om toegang van gebruikers te verwijderen die eerder een verbinding aan het project ontvingen. Er wordt een nieuwe koppeling gegenereerd die u kunt delen met gebruikers die toegang willen krijgen tot het project.

1. Selecteren **[!UICONTROL Close]** om het dialoogvenster Delen te sluiten. Uw wijzigingen worden automatisch opgeslagen.

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
| Welke ervaring krijgt een ontvanger als deze een projectverbinding opent? | Ontvangers krijgen de rol die u hen in de deelmodus hebt geplaatst. Als aan een ontvanger geen rol wordt toegewezen en een koppeling naar het project wordt ontvangen (**[!UICONTROL Share]** > **[!UICONTROL Share with Workspace users]** selecteert u vervolgens **[!UICONTROL Copy]** naast de **[!UICONTROL Share by link]** (veld), worden deze standaard in een rol geplaatst. Ontvangen beheerders **[!UICONTROL Can edit]** en niet-beheerders ontvangen **[!UICONTROL Can duplicate]**. |
