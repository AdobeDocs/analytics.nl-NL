---
description: Leer hoe u oude aanmeldingsgegevens voor Analytics-gebruikers uitschakelt.
title: Verouderde logins uitschakelen
feature: Admin Tools
exl-id: 3e619700-722d-429b-94dc-7aa162e114c0
role: Admin
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Verouderde logins uitschakelen

Leer hoe u oude aanmeldingsgegevens voor Analytics-gebruikers uitschakelt.

Nadat uw gebruikers zijn gemigreerd van het verouderde Analytics-gebruikersbeheersysteem naar de Adobe Admin Console, kunt u hun oude aanmeldingsgegevens uitschakelen. Als u oude aanmeldingsgegevens uitschakelt, worden gebruikers omgeleid naar de Experience Cloud-aanmelding als ze de oude aanmeldingsgegevens proberen te gebruiken.

1. Open het gereedschap Migratie in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User ID Migration]** .
1. Zoek in de sectie [!DNL User Information] naar het domein met de gebruikers waarmee u wilt werken en klik vervolgens op **[!UICONTROL Select Users]** .
1. Selecteer de gebruikers met verouderde logins die u wilt uitschakelen.

   ![](/help/admin/tools/user-management/user-migration/assets/user-info.png)

   De in aanmerking komende gebruikers hebben de status *`Migrated`* onder de kolom Migratiestatus. U kunt de oudere aanmelding van een gebruiker pas uitschakelen nadat deze is gemigreerd.
1. Klik op **[!UICONTROL Disable Legacy Login]** en vervolgens op **[!UICONTROL Done]** .

   Schakel Oudere aanmelding uit om aan te geven welke gebruikers hun oude gebruikersnaam en wachtwoord voor [!DNL my.omniture.com] kunnen blijven gebruiken.

   U kunt oudere aanmeldingen niet uitschakelen voor een gebruiker die nog moet worden gemigreerd. Als deze optie is uitgeschakeld, moet de gebruiker zijn Experience Cloud-id gebruiken om zich aan te melden en toegang te krijgen tot Analytics.
