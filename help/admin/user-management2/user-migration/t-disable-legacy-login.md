---
description: Leer hoe u oude aanmeldingsgegevens voor Analytics-gebruikers uitschakelt.
title: Verouderde logins uitschakelen
uuid: 085874b2-10bf-4a56-a337-f3104428d71e
translation-type: tm+mt
source-git-commit: 1ec080acf65c31b077a3daf3846f233f01e011b8

---


# Verouderde logins uitschakelen{#disable-legacy-logins}

Leer hoe u oude aanmeldingsgegevens voor Analytics-gebruikers uitschakelt.

Nadat uw gebruikers zijn gemigreerd van het verouderde Analytics-gebruikersbeheersysteem naar de Adobe Admin Console, kunt u hun oude aanmeldingsgegevens uitschakelen. Als u oude aanmeldingen uitschakelt, worden gebruikers omgeleid naar de aanmeldingsgegevens voor de Experience Cloud als ze de oudere aanmelding willen gebruiken.

1. Open het gereedschap Migratie in **[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL User ID Migration]**.
1. Zoek in de [!DNL User Information] sectie het domein met de gebruikers waarmee u wilt werken en klik op **[!UICONTROL Select Users]**.
1. Selecteer de gebruikers met verouderde logins die u wilt uitschakelen.

   ![](assets/user-info.png)

   Gebruikers die hiervoor in aanmerking komen, hebben de status &quot;status&quot; *`Migrated`* onder de kolom &quot;Migratiestatus&quot;. U kunt de oudere aanmelding van een gebruiker pas uitschakelen nadat deze is gemigreerd.
1. Klik **[!UICONTROL Disable Legacy Login]** en klik vervolgens op **[!UICONTROL Done]**.

   Schakel Oudere aanmelding uit om aan te geven welke gebruikers hun oude [!DNL my.omniture.com] gebruikersnaam en wachtwoord kunnen blijven gebruiken.

   U kunt oudere aanmeldingen niet uitschakelen voor een gebruiker die nog moet worden gemigreerd. Als de functie eenmaal is uitgeschakeld, moet de gebruiker de Cloud-id van Experience gebruiken om zich aan te melden en toegang te krijgen tot Analytics.

