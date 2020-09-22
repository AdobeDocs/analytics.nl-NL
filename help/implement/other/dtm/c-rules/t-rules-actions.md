---
description: Stel handelingen in die de voorwaarde moet activeren.
keywords: Dynamic Tag Management;rule;create rule;new rule;javascript/third party tags;set up actions for condition;add new script;non-sequential javascript;sequential javascript;non-sequential html
solution: Experience Cloud,Analytics,Target
title: Acties instellen voor voorwaarden voor activeren
uuid: 2e892f0b-7261-41ee-b849-6e3054a38de0
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 7%

---


# Acties instellen voor voorwaarden voor activeren

Stel handelingen in die de voorwaarde moet activeren.

Nadat u de voorwaarde hebt ingesteld, moet u de handelingen instellen die door de voorwaarde moeten worden geactiveerd. Deze handelingen kunnen gebeurtenissen, tags van derden en aangepaste scripts bevatten. [!DNL Analytics] In dit voorbeeld wordt beschreven hoe u scripts of tags van derden instelt.

Naast geïntegreerde gereedschappen zoals [!DNL Adobe Analytics] en Google Analytics kan Dynamic Tag Management elk type JavaScript activeren of HTML in uw site injecteren, op bepaalde pagina&#39;s of in specifieke scenario&#39;s.

Elke regel kan zoveel scripts of HTML-injecties activeren als u wilt.

>[!NOTE]
>
>Omdat DTM u toestaat om douanecode in uw pagina te injecteren, gelieve te letten op niet om cross-site scripting (XSS) kwetsbaarheid (zie de gids [van](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS)) OWASP voor meer informatie) tot stand te brengen. Het gebruik van gegevenselementen in een script vereist bijzondere aandacht. Ga er altijd van uit dat gegevenselementwaarden afkomstig kunnen zijn van een niet-vertrouwde bron.

**Handelingen instellen voor activeren van voorwaarde**

1. Klik **[!UICONTROL JavaScript / Third Party Tags]** om een nieuw manuscript aan uw regel toe te voegen.

   ![](assets/scripts-actions.png)

1. Klik op **[!UICONTROL Add New Script]**.

   ![](assets/scripts-actions2.png)

1. Geef het script een naam.
1. Geef op hoe het script moet worden geactiveerd en plak de gewenste inhoud in het tekstgebied. ![](assets/scripts-actions3.png)

1. Klik **[!UICONTROL Save Code]**, en het manuscript zal aan de rij voor de regel worden toegevoegd. ![](assets/scripts-actions4.png)

