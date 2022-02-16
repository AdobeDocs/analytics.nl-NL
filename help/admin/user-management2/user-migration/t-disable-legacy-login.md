---
description: Leer hoe u oude aanmeldingsgegevens voor Analytics-gebruikers uitschakelt.
title: Verouderde logins uitschakelen
feature: Admin Tools
exl-id: 3e619700-722d-429b-94dc-7aa162e114c0
source-git-commit: 0143496648e59e95c360388735def726e63ee71b
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 3%

---

# Verouderde logins uitschakelen{#disable-legacy-logins}

Leer hoe u oude aanmeldingsgegevens voor Analytics-gebruikers uitschakelt.

Nadat uw gebruikers zijn gemigreerd van het verouderde Analytics-gebruikersbeheersysteem naar de Adobe Admin Console, kunt u hun oude aanmeldingsgegevens uitschakelen. Als u oude aanmeldingspogingen uitschakelt, worden gebruikers omgeleid naar de Experience Cloud-aanmelding als ze de oude aanmelding proberen te gebruiken.

1. Het migratiehulpprogramma openen in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User ID Migration]**.
1. In de [!DNL User Information] , zoekt u het domein met de gebruikers waarmee u wilt werken, en klikt u op **[!UICONTROL Select Users]**.
1. Selecteer de gebruikers met verouderde logins die u wilt uitschakelen.

   ![](assets/user-info.png)

   De in aanmerking komende gebruikers hebben de status *`Migrated`* onder de kolom Migratiestatus. U kunt de oudere aanmelding van een gebruiker pas uitschakelen nadat deze is gemigreerd.
1. Klikken **[!UICONTROL Disable Legacy Login]** en klik vervolgens op **[!UICONTROL Done]**.

   Schakel Oudere aanmelding uit om aan te geven welke gebruikers hun bestaande versie kunnen blijven gebruiken [!DNL my.omniture.com] gebruikersnaam en wachtwoord.

   U kunt oudere aanmeldingen niet uitschakelen voor een gebruiker die nog moet worden gemigreerd. Als de Experience Cloud-id eenmaal is uitgeschakeld, moet de gebruiker zich aanmelden en toegang krijgen tot Analytics.
