---
product: analytics
audience: admin
user-guide-title: Analytics Admin-handleiding
breadcrumb-title: Beheerdershandleiding
user-guide-description: Leer over Analytics beheerderstaken, zoals het beheren van gebruikers en producten in de Admin Console van Experience Cloud, het configureren van rapportreeksen, en meer.
source-git-commit: 0bed2622f54bf2f46aa57dbfad7bd55a61d6c7d0
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 12%

---


# Adobe Analytics Admin Guide {#admin}

+ [Analytics Admin-handleiding](home.md)
+ [ de Nota&#39;s van de Versie van Analytics ](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html?lang=nl-NL)
+ Adobe-beheerconsole {#admin-console}
   + [Overzicht](admin-console/home.md)
   + [Adobe Analytics First Admin Guide](admin-console/first-admin-guide.md)
   + [Beheerdersrollen in Adobe Analytics](admin-console/admin-roles-in-analytics.md)
   + Overzicht van analysehulpmiddelen {#permissions}
      + [Productprofielen voor Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Machtigingen voor productprofielen voor rapportsuite](admin-console/permissions/report-suite-tools.md)
      + [Machtigingen voor productprofielen voor Analytics Tools](admin-console/permissions/analytics-tools.md)
+ Gereedschappen voor analysebeheer {#admin-tools}
   + [Overzicht van beheerprogramma&#39;s](admin/c-admin-tools.md)
   + [Codebeheer](admin/code-manager-admin.md)
   + [Analytische inventarisatie](admin/analytics-inventory.md)
   + [Databronnen](admin/data-sources.md)
   + [Uitsluiten op IP-adres](admin/exclude-ip.md)
   + [Logboeken](admin/logs.md)
   + Activity Manager rapporteren {#reporting-activity-manager}
      + [Overzicht](admin/reporting-activity-manager/reporting-activity-overview.md)
      + [Rapportactiviteiten weergeven](admin//reporting-activity-manager/reporting-activity.md)
      + [Rapportageverzoeken annuleren](admin/reporting-activity-manager/reporting-activity-cancel-requests.md)
   + Componentmigratie {#component-migration}
      + [Voorbereiden op migratie](admin/component-migration/prepare-component-migration.md)
      + [Migratieworkflow](admin/component-migration/component-migration.md)
   + Report Suite Manager {#manage-report-suites}
      + Instellingen van een rapportsuite bewerken {#edit-report-suite}
         + Algemeen {#report-suite-general}
            + [Algemene accountinstellingen](admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
            + [Interne URL-filters](admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)
            + [Kalender aanpassen](admin/c-manage-report-suites/c-edit-report-suites/general/custom-calendar.md)
            + Detectie van betaalde zoekopdracht {#paid-search-detection}
               + [Overzicht van betaalde zoekdetectie](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md)
               + [Betaalde zoekdetectie configureren](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md)
            + Verwerkingsregels {#processing-rules}
               + [Overzicht](admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md)
               + [Interface](admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-interface.md)
               + [Historie weergeven](admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-view-history.md)
               + [Regels kopiëren](admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-copy.md)
               + [Beschikbare afmetingen en cijfers](admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-variables.md)
               + [Gebruik hoofdletters](admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-use-cases.md)
            + Bot-regels {#bot-removal}
               + [Bot verwijderen](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md)
               + [Begrijp en vorm beide regels](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)
               + [Handtekeningen van gewone bot](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-signatures.md)
               + [Methoden voor botteling](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-exclusion-methods.md)
            + [Privacy-instellingen](admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md)
            + [Configuratie tijdstempels](admin/c-manage-report-suites/c-edit-report-suites/general/timestamp-optional.md)
            + Server-kant doorsturen {#server-side-forwarding}
               + [Server-kant door:sturen overzicht](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)
               + [GDPR/ePrivacy compliance en server-side forward](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-gdpr.md)
               + [Vereisten voor server-side door:sturen](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-requirements.md)
               + [Server-kant die gegevens en codeverwijzing door:sturen](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-reference.md)
               + [Hoe te om uw server-kant te verifiëren die implementatie door:sturen](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-verify.md)
               + [Veelgestelde vragen over het doorsturen van servers](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md)
         + Verkeer {#traffic-variables}
            + [verkeersvariabelen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
            + [Verkeersclassificaties](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-classifications.md)
            + [Aangepaste rapportbeschrijvingen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/custom-desc-admin.md)
         + Conversie {#conversion-variables}
            + [Conversievariabelen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md)
            + [Methoden zoeken](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/finding-methods.md)
            + [Conversie-classificaties](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-classifications.md)
            + Unieke bezoekersvariabele {#unique-visitor-variable}
               + [De variabele Unieke bezoeker opgeven](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [Hoofdletters/kleine letters gebruiken - Bezoeker-id&#39;s extraheren](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + [Gebeurtenissen met succes](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md)
            + [Classificatiehiërarchieën](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/classification-hierarchies.md)
            + [Variabelen weergeven](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md)
            + [Merchandising-eVars](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/merchandising-evars.md)
         + Marketingkanalen {#marketing-channels}
            + [Marketing Channel Manager](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)
            + [Verwerkingsregels voor marketingkanalen](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)
            + [Classificaties marketingkanalen](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md)
            + [Vervaldatum marketingkanaal](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/visitor-engagement.md)
         + Verkeersbeheer {#traffic-management}
            + [Overzicht](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/traffic-management.md)
            + [Spike plannen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md)
            + [ Permanent Verkeer ](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md)
         + [Standaardwaarden](admin/c-manage-report-suites/c-edit-report-suites/default-metrics.md)
         + Toepassingsbeheer {#app-management}
            + [Toepassingsrapportage](admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md)
            + [Toepassingsclassificaties](admin/c-manage-report-suites/c-edit-report-suites/app-classifications.md)
         + [Mediabeheer](admin/c-manage-report-suites/c-edit-report-suites/media-management.md)
         + [Activity Map](admin/c-manage-report-suites/c-edit-report-suites/activity-map.md)
         + [AEM](admin/c-manage-report-suites/c-edit-report-suites/adobe-experience-manager.md)
         + [Adobe Campaign](admin/c-manage-report-suites/c-edit-report-suites/adobe-campaign.md)
         + [Privacyrapportage](admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md)
         + Document Cloud Management {#doc-cloud-mgt}
            + [Document Cloud configureren met Adobe Analytics](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-mgt.md)
            + [Document Cloud-rapportage configureren](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-config.md)
         + [Advertising Analytics-configuratie](admin/c-manage-report-suites/c-edit-report-suites/advertising-analytics-config.md)
         + Real-time {#real-time-reports}
            + [Overzicht van realtime rapporten](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md)
            + [Configuratie van realtime rapporten](admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md)
            + [Ondersteunde metriek en afmetingen in real time](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md)
      + [Rapportsuites beheren](admin/c-manage-report-suites/report-suites-admin.md)
      + [Globale rapportsuites](admin/c-manage-report-suites/rollup-report-suite.md)
      + [Een zoekopdracht in een rapportsuite opslaan](admin/c-manage-report-suites/t-report-suite-saved-search.md)
      + [Rapportinstellingen downloaden](admin/c-manage-report-suites/t-download-rs-settings.md)
      + Nieuwe rapportsuite {#c-new-report-suite}
         + [Een rapportsuite maken](admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md)
         + [Een groep rapportsuite maken](admin/c-manage-report-suites/c-new-report-suite/t-create-rs-group.md)
         + [Nieuwe rapportsuite - instellingen](admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md)
         + [Instellingen niet gekopieerd uit een bronrapportsuite](admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md)
      + Sjablonen voor rapportsets {#report-suite-templates}
         + [Overzicht van rapportsuite-sjablonen](admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md)
         + [Samenvoegingsportaal](admin/c-manage-report-suites/c-report-suite-templates/aggregator-portal.md)
         + [Commerce](admin/c-manage-report-suites/c-report-suite-templates/commerce-admin.md)
         + [Inhoud en media](admin/c-manage-report-suites/c-report-suite-templates/content-media.md)
         + [Standaardsjabloon](admin/c-manage-report-suites/c-report-suite-templates/default-rs-template.md)
         + [Financiële diensten](admin/c-manage-report-suites/c-report-suite-templates/financial-services.md)
         + [Job Portal](admin/c-manage-report-suites/c-report-suite-templates/job-portal.md)
         + [Loodgeneratie](admin/c-manage-report-suites/c-report-suite-templates/lead-generation.md)
         + [Ondersteuningsmedia](admin/c-manage-report-suites/c-report-suite-templates/support-media.md)
   + Bedrijfsinstellingen {#company-settings}
      + [Overzicht van bedrijfsinstellingen](admin/company/c-company-settings.md)
      + [Beveiligingsbeheer](admin/company/security-manager.md)
      + [Webservices](admin/company/web-services-admin.md)
      + [Report Builder-rapporten](admin/company/report-builder-reports-admin.md)
      + [Single Sign-On](admin/company/single-signon-admin.md)
      + [Rapportagesuites verbergen](admin/company/c-hide-report-suites.md)
      + [Voorkeursbeheer](admin/company/preferences-manager.md)
      + [Handelingen in behandeling](admin/company/pending-actions-admin.md)
      + [Toegangsniveaus voor functies](admin/company/feature-access-levels.md)
   + Privacy-etikettering voor gegevensbeheer {#data-governance}
      + [Workflow Adobe Analytics Data Privacy](admin/c-data-governance/an-gdpr-workflow.md)
      + [Veelgestelde vragen](admin/c-data-governance/gdpr-faq.md)
      + Gegevensetikettering {#data-labels}
         + [Privacy-labels voor gegevens voor componenten Analytics](admin/c-data-governance/data-labeling/gdpr-labels.md)
         + [Rapportsuitedata labelen](admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md)
         + [De privacylabels van de rapportsuite weergeven/beheren](admin/c-data-governance/data-labeling/gdpr-view-settings.md)
         + [Best practices voor labelen](admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)
         + [Voorbeeld van etikettering](admin/c-data-governance/data-labeling/gdpr-labeling-example.md)
         + [Naamruimten](admin/c-data-governance/data-labeling/gdpr-namespaces.md)
      + [Vrijstelling van CNIL-toestemming](admin/c-data-governance/cnil-consent-exemption.md)
   + Gebruik van serveroproep {#server-call-usage}
      + [Overzicht van het gebruik van serveroproepen](admin/c-server-call-usage/overage-overview.md)
      + [Huidig serveroproepgebruik weergeven](admin/c-server-call-usage/server-call-usage-dashboard.md)
      + [Gebruik van rapportsuite weergeven](admin/c-server-call-usage/report-suite-usage.md)
      + [Gebruikswaarschuwingen voor serveroproepen](admin/c-server-call-usage/scu-alerts.md)
      + [Veelgestelde vragen over servergebruik](admin/c-server-call-usage/overage-faq.md)
   + Gebruiker- en productbeheer (verouderd) {#user-product-management}
      + [Gebruiker- en productbeheer (verouderd)](admin/user-management2/user-management.md)
      + [Oudere gebruikersaccounts, middelen en vervaltijden beheren](admin/user-management2/users-assets.md)
      + Gebruikers migreren naar Adobe Admin Console {#migrate-users}
         + [Analyseer gebruikersmigratie naar de Admin Console](admin/user-management2/user-migration/c-migration-tool.md)
         + [Gebruikersaccounts voor Analyse migreren voor Adobe-id&#39;s](admin/user-management2/user-migration/t-migrate-users.md)
         + [Analytische gebruikersaccounts migreren voor bedrijfs- en federatieve id&#39;s](admin/user-management2/user-migration/migrate-enterprise.md)
         + [Verouderde logins uitschakelen](admin/user-management2/user-migration/t-disable-legacy-login.md)
         + [API&#39;s die door de migratie worden beïnvloed](admin/user-management2/user-migration/developer.md)
+ [Admin-API](c-admin-api/c-admin-api.md)
+ [Adobe Analytics 1.4 API EOL - Veelgestelde vragen](c-admin-api/c-admin-14-api-eol.md)

