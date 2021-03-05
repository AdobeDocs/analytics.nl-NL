---
description: Configureer een in Experience Cloud toegewezen rapportsuite voor gebruik in Advertising Analytics.
title: Rapportsuite voor Advertising Analytics inschakelen
uuid: 934f0e02-b5d7-4eca-93d8-92f95bd7014a
translation-type: tm+mt
source-git-commit: 5d8032a9806836e7d0ecbd7fa3652ed1fd137e89
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 10%

---


# Rapportsuite voor Advertising Analytics inschakelen

Om Advertising Analytics onderzoeksgegevens in Analytics te zien, moet u elke Experience Cloud-in kaart gebrachte rapportreeks voor Advertising Analytics het melden vormen.

1. [Wijs uw rapportsuite toe aan een organisatie](https://docs.adobe.com/content/help/nl-NL/core-services/interface/about-core-services/report-suite-mapping.html).
1. Ga naar **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]**.

1. Selecteer de rapportsuite die aan uw Experience Cloud-organisatie is toegewezen.
1. Klik op **[!UICONTROL Edit Settings]** > **[!UICONTROL Advertising Analytics Configuration]**.

   ![Rapportage](assets/aa_reporting.png)

   >[!IMPORTANT]
   >
   >AMO-id verwijst naar de Adobe Advertising Cloud-variabele waarin de zoekgegevens worden ingevoegd.

1. Stel de variabele voor de toewijzing en vervaldatum van de AMO-id-variabele in. Met conversievariabelen (eVars) kan Adobe Analytics succesgebeurtenissen toewijzen aan specifieke variabelewaarden. Soms krijgen variabelen meer dan één waarde voordat ze een succesgebeurtenis raken. In deze gevallen bepaalt de toewijzing welke variabele krediet voor de gebeurtenis krijgt.

   | Instelling | Definitie |
   |--- |--- |
   | Oorspronkelijke waarde (eerste) | De eerste waargenomen waarde krijgt volledige toewijzingskrediet, ongeacht welke waarden voor die variabele volgen. |
   | Recentste (laatste) | De laatste waargenomen waarde krijgt volledige toewijzingskrediet voor de succesgebeurtenis, ongeacht welke variabelen daarvoor werden geactiveerd. |
   | Verlopen na | Hier kunt u een tijdsperiode, of gebeurtenis, opgeven waarna de waarde van de eVar verloopt (zodat er geen krediet meer wordt ontvangen voor succesgebeurtenissen).  Als een succesgebeurtenis optreedt na het verlopen van de eVar, ontvangt de waarde None een creditering voor de gebeurtenis (er was geen eVar actief). |

1. Klik **[!UICONTROL Enable Advertising Analytics Reporting]** (eerste keer), of **[!UICONTROL Update Advertising Analytics Reporting]** (volgende tijden). Uw rapportsuite is nu gereed om zoekgegevens van Advertising Analytics te ontvangen. U bent niet klaar om [Advertising Accounts](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/aa-create-ad-account.md) te maken.

