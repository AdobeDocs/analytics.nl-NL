---
product: analytics
audience: admin
user-guide-title: Analytics Admin-handleiding
breadcrumb-title: Beheerdershandleiding
user-guide-description: Leer over Analytics beheerderstaken, zoals het beheren van gebruikers en producten in de Admin Console van Experience Cloud, het configureren van rapportreeksen, en meer.
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 11%

---


# Adobe Analytics Admin Guide {#admin}

+ [Handleiding Analysebeheer](home.md)
+ [ de versienota&#39;s van de Analyse ](https://experienceleague.adobe.com/en/docs/analytics/release-notes/latest)
+ Adobe-beheerconsole {#admin-console}
   + [Overzicht](admin-console/home.md)
   + [Adobe Analytics First Admin Guide](admin-console/first-admin-guide.md)
   + [Beheerdersrollen in Adobe Analytics](admin-console/admin-roles-in-analytics.md)
   + Overzicht van analysehulpmiddelen {#permissions}
      + [Productprofielen voor Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Machtigingen voor productprofielen voor rapportsuite](admin-console/permissions/report-suite-tools.md)
      + [Machtigingen voor productprofielen voor Analytics Tools](admin-console/permissions/analytics-tools.md)
+ Gereedschappen voor analysebeheer {#admin-tools}
   + [Overzicht van beheerprogramma&#39;s](tools/c-admin-tools.md)
   + [Codebeheer](tools/code-manager-admin.md)
   + [Analytische inventarisatie](tools/analytics-inventory.md)
   + [Databronnen](tools/data-sources.md)
   + [Uitsluiten op IP-adres](tools/exclude-ip.md)
   + [Logboeken](tools/logs.md)
   + Activity Manager rapporteren {#reporting-activity-manager}
      + [Overzicht](tools/reporting-activity-manager/reporting-activity-overview.md)
      + [Rapportactiviteiten weergeven](tools//reporting-activity-manager/reporting-activity.md)
      + [Rapportageverzoeken annuleren](tools/reporting-activity-manager/reporting-activity-cancel-requests.md)
   + Componentmigratie {#component-migration}
      + [Voorbereiden op migratie](tools/component-migration/prepare-component-migration.md)
      + [Migratieworkflow](tools/component-migration/component-migration.md)
   + Report Suite Manager {#manage-report-suites}
      + Instellingen van een rapportsuite bewerken {#edit-report-suite}
         + Algemeen {#report-suite-general}
            + [Algemene accountinstellingen](tools/manage-rs/edit-settings/general/general-acct-settings-admin.md)
            + [Interne URL-filters](tools/manage-rs/edit-settings/general/internal-url-filter-admin.md)
            + [Kalender aanpassen](tools/manage-rs/edit-settings/general/custom-calendar.md)
            + Detectie van betaalde zoekopdracht {#paid-search-detection}
               + [Overzicht van betaalde zoekdetectie](tools/manage-rs/edit-settings/general/paid-search-detection/paid-search-detection.md)
               + [Betaalde zoekdetectie configureren](tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md)
            + Verwerkingsregels {#processing-rules}
               + [Overzicht](tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)
               + [Interface](tools/manage-rs/edit-settings/general/processing-rules/pr-interface.md)
               + [Historie weergeven](tools/manage-rs/edit-settings/general/processing-rules/pr-view-history.md)
               + [Regels kopiëren](tools/manage-rs/edit-settings/general/processing-rules/pr-copy.md)
               + [Beschikbare afmetingen en cijfers](tools/manage-rs/edit-settings/general/processing-rules/pr-variables.md)
               + [Gebruik hoofdletters](tools/manage-rs/edit-settings/general/processing-rules/pr-use-cases.md)
            + Bot-regels {#bot-removal}
               + [Bot verwijderen](tools/manage-rs/edit-settings/general/bot-removal/bot-removal.md)
               + [Begrijp en vorm beide regels](tools/manage-rs/edit-settings/general/bot-removal/bot-rules.md)
               + [Handtekeningen van gewone bot](tools/manage-rs/edit-settings/general/bot-removal/bot-signatures.md)
               + [Methoden voor botteling](tools/manage-rs/edit-settings/general/bot-removal/bot-exclusion-methods.md)
            + [Privacy-instellingen](tools/manage-rs/edit-settings/general/privacy-settings.md)
            + [Configuratie tijdstempels](tools/manage-rs/edit-settings/general/timestamp-configuration.md)
            + Server-kant doorsturen {#server-side-forwarding}
               + [Server-kant door:sturen overzicht](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf.md)
               + [GDPR/ePrivacy compliance en server-side forward](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-gdpr.md)
               + [Vereisten voor server-side door:sturen](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-requirements.md)
               + [Server-kant die gegevens en codeverwijzing door:sturen](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-reference.md)
               + [Hoe te om uw server-kant te verifiëren die implementatie door:sturen](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-verify.md)
               + [Veelgestelde vragen over het doorsturen van servers](tools/manage-rs/edit-settings/general/c-server-side-forwarding/ssf-faq.md)
         + Verkeer {#traffic-variables}
            + [verkeersvariabelen](tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md)
            + [Verkeersclassificaties](tools/manage-rs/edit-settings/c-traffic-variables/traffic-classifications.md)
            + [Aangepaste rapportbeschrijvingen](tools/manage-rs/edit-settings/c-traffic-variables/custom-desc-admin.md)
         + Conversie {#conversion-variables}
            + [Conversievariabelen](tools/manage-rs/edit-settings/conversion-var-admin/conversion-var-admin.md)
            + [Methoden zoeken](tools/manage-rs/edit-settings/conversion-var-admin/finding-methods.md)
            + [Conversie-classificaties](tools/manage-rs/edit-settings/conversion-var-admin/conversion-classifications.md)
            + Unieke bezoekersvariabele {#unique-visitor-variable}
               + [De variabele Unieke bezoeker opgeven](tools/manage-rs/edit-settings/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [Hoofdletters/kleine letters gebruiken - Bezoeker-id&#39;s extraheren](tools/manage-rs/edit-settings/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + [Gebeurtenissen met succes](tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/success-event.md)
            + [Classificatiehiërarchieën](tools/manage-rs/edit-settings/conversion-var-admin/classification-hierarchies.md)
            + [Variabelen weergeven](tools/manage-rs/edit-settings/conversion-var-admin/list-var-admin.md)
            + [Merchandising-eVars](tools/manage-rs/edit-settings/conversion-var-admin/merchandising-evars.md)
         + Marketingkanalen {#marketing-channels}
            + [Marketing Channel Manager](tools/manage-rs/edit-settings/marketing-channels/c-channels.md)
            + [Verwerkingsregels voor marketingkanalen](tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md)
            + [Classificaties marketingkanalen](tools/manage-rs/edit-settings/marketing-channels/classifications-mchannel.md)
            + [Vervaldatum marketingkanaal](tools/manage-rs/edit-settings/marketing-channels/visitor-engagement.md)
         + Verkeersbeheer {#traffic-management}
            + [Overzicht](tools/manage-rs/edit-settings/c-traffic-management/traffic-management.md)
            + [Spike plannen](tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md)
            + [ Permanent Verkeer ](tools/manage-rs/edit-settings/c-traffic-management/t-traffic-permanent.md)
         + [Standaardwaarden](tools/manage-rs/edit-settings/default-metrics.md)
         + Toepassingsbeheer {#app-management}
            + [Toepassingsrapportage](tools/manage-rs/edit-settings/app-reporting.md)
            + [Toepassingsclassificaties](tools/manage-rs/edit-settings/app-classifications.md)
         + [Mediabeheer](tools/manage-rs/edit-settings/media-management.md)
         + [Activity Map](tools/manage-rs/edit-settings/activity-map.md)
         + [AEM](tools/manage-rs/edit-settings/adobe-experience-manager.md)
         + [Adobe Campaign](tools/manage-rs/edit-settings/adobe-campaign.md)
         + [Privacyrapportage](tools/manage-rs/edit-settings/privacy-reporting.md)
         + Document Cloud Management {#doc-cloud-mgt}
            + [Document Cloud configureren met Adobe Analytics](tools/manage-rs/edit-settings/document-cloud-mgt.md)
            + [Document Cloud-rapportage configureren](tools/manage-rs/edit-settings/document-cloud-config.md)
         + [Advertising Analytics-configuratie](tools/manage-rs/edit-settings/advertising-analytics-config.md)
         + Real-time {#real-time-reports}
            + [Overzicht van realtime rapporten](tools/manage-rs/edit-settings/realtime/realtime.md)
            + [Configuratie van realtime rapporten](tools/manage-rs/edit-settings/realtime/t-realtime-admin.md)
            + [Ondersteunde metriek en afmetingen in real time](tools/manage-rs/edit-settings/realtime/realtime-metrics.md)
      + [Rapportsuites beheren](tools/manage-rs/report-suites-admin.md)
      + [Globale rapportsuites](tools/manage-rs/rollup-report-suite.md)
      + [Een zoekopdracht in een rapportsuite opslaan](tools/manage-rs/t-report-suite-saved-search.md)
      + [Rapportinstellingen downloaden](tools/manage-rs/t-download-rs-settings.md)
      + Nieuwe rapportsuite {#c-new-report-suite}
         + [Een rapportsuite maken](tools/manage-rs/new-rs/t-create-a-report-suite.md)
         + [Een groep rapportsuite maken](tools/manage-rs/new-rs/t-create-rs-group.md)
         + [Nieuwe rapportsuite - instellingen](tools/manage-rs/new-rs/new-report-suite.md)
         + [Instellingen niet gekopieerd uit een bronrapportsuite](tools/manage-rs/new-rs/settings-not-copied-from-rs.md)
      + Sjablonen voor rapportsets {#report-suite-templates}
         + [Overzicht van rapportsuite-sjablonen](tools/manage-rs/rs-templates/report-suite-templates.md)
         + [Samenvoegingsportaal](tools/manage-rs/rs-templates/aggregator-portal.md)
         + [Commerce](tools/manage-rs/rs-templates/commerce-admin.md)
         + [Inhoud en media](tools/manage-rs/rs-templates/content-media.md)
         + [Standaardsjabloon](tools/manage-rs/rs-templates/default-rs-template.md)
         + [Financiële diensten](tools/manage-rs/rs-templates/financial-services.md)
         + [Job Portal](tools/manage-rs/rs-templates/job-portal.md)
         + [Loodgeneratie](tools/manage-rs/rs-templates/lead-generation.md)
         + [Ondersteuningsmedia](tools/manage-rs/rs-templates/support-media.md)
   + Bedrijfsinstellingen {#company-settings}
      + [Overzicht van bedrijfsinstellingen](tools/company/c-company-settings.md)
      + [Beveiligingsbeheer](tools/company/security-manager.md)
      + [Webservices](tools/company/web-services-admin.md)
      + [Report Builder-rapporten](tools/company/report-builder-reports-admin.md)
      + [Single Sign-On](tools/company/single-signon-admin.md)
      + [Rapportagesuites verbergen](tools/company/c-hide-report-suites.md)
      + [Voorkeursbeheer](tools/company/preferences-manager.md)
      + [Handelingen in behandeling](tools/company/pending-actions-admin.md)
      + [Toegangsniveaus voor functies](tools/company/feature-access-levels.md)
   + Privacy-etikettering {#privacy-labeling}
      + [Overzicht](tools/privacy-labeling/labeling-overview.md)
      + [Privacy-labels voor gegevens voor componenten Analytics](tools/privacy-labeling/labels.md)
      + [De privacylabels van de rapportsuite weergeven/beheren](tools/privacy-labeling/view-settings.md)
      + [Best practices voor labelen](tools/privacy-labeling/best-practices.md)
      + [Voorbeeld van etikettering](tools/privacy-labeling/examples.md)
      + [Naamruimten](tools/privacy-labeling/namespaces.md)
   + Gebruik van serveroproep {#server-call-usage}
      + [Overzicht van het gebruik van serveroproepen](tools/server-call-usage/overage-overview.md)
      + [Huidig serveroproepgebruik weergeven](tools/server-call-usage/server-call-usage-dashboard.md)
      + [Gebruik van rapportsuite weergeven](tools/server-call-usage/report-suite-usage.md)
      + [Gebruikswaarschuwingen voor serveroproepen](tools/server-call-usage/scu-alerts.md)
      + [Veelgestelde vragen over servergebruik](tools/server-call-usage/overage-faq.md)
   + Gebruiker- en productbeheer (verouderd) {#user-product-management}
      + [Gebruiker- en productbeheer (verouderd)](tools/user-management/user-management.md)
      + [Oudere gebruikersaccounts, middelen en vervaltijden beheren](tools/user-management/users-assets.md)
      + Gebruikers migreren naar Adobe Admin Console {#migrate-users}
         + [Analyseer gebruikersmigratie naar de Admin Console](tools/user-management/user-migration/c-migration-tool.md)
         + [Gebruikersaccounts voor Analyse migreren voor Adobe-id&#39;s](tools/user-management/user-migration/t-migrate-users.md)
         + [Analytische gebruikersaccounts migreren voor bedrijfs- en federatieve id&#39;s](tools/user-management/user-migration/migrate-enterprise.md)
         + [Verouderde logins uitschakelen](tools/user-management/user-migration/t-disable-legacy-login.md)
         + [API&#39;s die door de migratie worden beïnvloed](tools/user-management/user-migration/developer.md)
+ [Admin-API](https://developer.adobe.com/analytics-apis/docs/2.0/)
