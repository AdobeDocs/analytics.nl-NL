---
product: analytics
audience: admin
user-guide-title: Analytics Admin-handleiding
breadcrumb-title: Beheerdershandleiding
user-guide-description: Leer over Analytics beheerderstaken, zoals het beheren van gebruikers en producten in de Admin Console van Experience Cloud, het configureren van rapportreeksen, en meer.
source-git-commit: 5b4017bf7ce3f61b365829d058f820b48622d482
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 14%

---


# Beheerhandleiding voor Adobe Analytics {#admin}

+ [Analytics Admin-handleiding](home.md)
+ [Opmerkingen bij de release van Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
+ Adobe-beheerconsole {#admin-console}
   + [Overzicht](admin-console/home.md)
   + [Adobe Analytics eerste beheerdershandleiding](admin-console/first-admin-guide.md)
   + [Beheerdersrollen in Adobe Analytics](admin-console/admin-roles-in-analytics.md)
   + Overzicht van machtigingen voor analysetools {#permissions}
      + [Productprofielen voor Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Machtigingen voor productprofielen voor Report Suite-tools](admin-console/permissions/report-suite-tools.md)
      + [Rechten voor productprofielen voor Analytics-tools](admin-console/permissions/analytics-tools.md)
+ Beheertools voor analyse {#admin-tools}
   + [Overzicht van beheertools](admin/c-admin-tools.md)
   + [Code Manager](admin/code-manager-admin.md)
   + [Analytics-inventarisatie](admin/analytics-inventory.md)
   + [Databronnen](admin/data-sources.md)
   + [Uitsluiten op IP-adres](admin/exclude-ip.md)
   + [Logs](admin/logs.md)
   + Activiteitenbeheer voor rapportage {#reporting-activity-manager}
      + [Overzicht](admin/reporting-activity-manager/reporting-activity-overview.md)
      + [Rapportageactiviteit weergeven](admin//reporting-activity-manager/reporting-activity.md)
      + [Meldingsverzoeken annuleren](admin/reporting-activity-manager/reporting-activity-cancel-requests.md)
   + Migratie van componenten {#component-migration}
      + [Bereid je voor op migratie](admin/component-migration/prepare-component-migration.md)
      + [Migratie werkstroom](admin/component-migration/component-migration.md)
   + Beheer van Report Suite {#manage-report-suites}
      + Instellingen van een rapportsuite bewerken {#edit-report-suite}
         + Algemeen {#report-suite-general}
            + [Algemene accountinstellingen](admin/c-manage-report-suites/c-edit-report-suites/general/general-acct-settings-admin.md)
            + [Interne URL-filters](admin/c-manage-report-suites/c-edit-report-suites/general/internal-url-filter-admin.md)
            + [Agenda aanpassen](admin/c-manage-report-suites/c-edit-report-suites/general/custom-calendar.md)
            + Detectie van betaalde zoekopdrachten {#paid-search-detection}
               + [Overzicht van detectie van betaalde zoekopdrachten](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/paid-search-detection.md)
               + [Detectie van betaalde zoekopdrachten configureren](admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md)
            + Regels voor verwerking {#c-processing-rules}
               + [Overzicht van verwerkingsregels](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules.md)
               + Regels voor verwerking {#c-processing-rules-configuration}
                  + [Hoe verwerkingsregels werken](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/processing-rules-about.md)
                  + [Verwerkingsregels maken](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)
                  + [Actieve verwerkingsregels weergeven](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-view.md)
                  + [Geschiedenis van verwerkingsregels weergeven](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rule-view-history.md)
                  + [Verwerkingsregels herstellen](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-restore.md)
                  + [Verwerkingsregels kopiëren naar een andere rapportsuite](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md)
                  + [Afmetingen beschikbaar voor verwerkingsregels](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rule-dimensions.md)
               + Voorbeelden van verwerkingsregels {#processing-rules-examples}
                  + [Voorbeelden van verwerkingsregels](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-examples.md)
                  + [Vul een campagne-ID in op basis van een queryreeksparameter](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-populate-campaign-id.md)
                  + [Stel de gebeurtenis in op de productweergave vanaf de pagina met het productoverzicht](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/setting-the-product-view-event.md)
                  + [Voeg een subcategorie toe door de categorie- en paginanaam samen te voegen](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/subcategory-concatenating.md)
                  + [Waarden in een rapport opschonen](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md)
                  + [Vul interne zoektermen in met behulp van een query string-parameter](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-populating-internal-search.md)
                  + [Kopieer een contextgegevensvariabele naar een eVar](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md)
                  + [Een gebeurtenis instellen met behulp van een contextgegevensvariabele](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md)
                  + [Een gebeurtenis uit een treffer verwijderen](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-examples/processing-rules-remove-event.md)
               + [Regels verwerken: tips en trucs](admin/c-manage-report-suites/c-edit-report-suites/general/c-processing-rules/processing-rules-tips.md)
            + Bot-regels {#bot-removal}
               + [Bot verwijderen](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-removal.md)
               + [Botregels begrijpen en configureren](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-rules.md)
               + [Veelvoorkomende bothandtekeningen](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-signatures.md)
               + [Methoden voor het uitsluiten van bots](admin/c-manage-report-suites/c-edit-report-suites/general/bot-removal/bot-exclusion-methods.md)
            + [Privacy-instellingen](admin/c-manage-report-suites/c-edit-report-suites/general/privacy-settings.md)
            + [Configuratie van tijdstempels](admin/c-manage-report-suites/c-edit-report-suites/general/timestamp-optional.md)
            + Doorsturen aan de serverzijde {#server-side-forwarding}
               + [Overzicht van doorsturen aan de serverzijde](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf.md)
               + [Naleving van de AVG/ePrivacy en doorsturen aan de serverzijde](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-gdpr.md)
               + [Vereisten voor doorsturen aan de serverzijde](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-requirements.md)
               + [Server-side doorsturen van gegevens en codereferentie](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-reference.md)
               + [Hoe u uw implementatie van server-side forwarding kunt verifiëren](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-verify.md)
               + [Veelgestelde vragen over doorsturen aan de serverzijde](admin/c-manage-report-suites/c-edit-report-suites/general/c-server-side-forwarding/ssf-faq.md)
         + Verkeer {#traffic-variables}
            + [Verkeer variabelen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md)
            + [Verkeer classificaties](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-classifications.md)
            + [Aangepaste rapportbeschrijvingen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/custom-desc-admin.md)
         + Conversie {#conversion-variables}
            + [Conversie variabelen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-var-admin.md)
            + [Methoden vinden](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/finding-methods.md)
            + [Conversie classificaties](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/conversion-classifications.md)
            + Unieke bezoekersvariabele {#unique-visitor-variable}
               + [Geef de variabele Unieke bezoeker op](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
               + [Use case - Bezoekers-ID&#39;s extraheren](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
            + [Succes evenementen](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md)
            + [Classificatie hiërarchieën](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/classification-hierarchies.md)
            + [Variabelen weergeven](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md)
            + [Merchandising-eVars](admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/merchandising-evars.md)
         + Marketingkanalen {#marketing-channels}
            + [Marketing Channel Manager](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-channels.md)
            + [Regels voor de verwerking van marketingkanalen](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)
            + [Classificaties van marketingkanalen](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md)
            + [Vervaldatum marketingkanaal](admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/visitor-engagement.md)
         + Traffic-beheer {#traffic-management}
            + [Overzicht](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/traffic-management.md)
            + [Piek plannen](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-schedule-spike.md)
            + [Permanent verkeer](admin/c-manage-report-suites/c-edit-report-suites/c-traffic-management/t-traffic-permanent.md)
         + [Standaard metrische gegevens](admin/c-manage-report-suites/c-edit-report-suites/default-metrics.md)
         + App-beheer {#app-management}
            + [App-rapportage](admin/c-manage-report-suites/c-edit-report-suites/app-reporting.md)
            + [App-classificaties](admin/c-manage-report-suites/c-edit-report-suites/app-classifications.md)
         + [Mediabeheer](admin/c-manage-report-suites/c-edit-report-suites/media-management.md)
         + [Activiteitenkaart](admin/c-manage-report-suites/c-edit-report-suites/activity-map.md)
         + [AEM](admin/c-manage-report-suites/c-edit-report-suites/adobe-experience-manager.md)
         + [Adobe Campagne](admin/c-manage-report-suites/c-edit-report-suites/adobe-campaign.md)
         + [Privacy Rapportage](admin/c-manage-report-suites/c-edit-report-suites/privacy-reporting.md)
         + Document Cloud-beheer {#doc-cloud-mgt}
            + [Document Cloud configureren met Adobe Analytics](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-mgt.md)
            + [Document Cloud-rapportage configureren](admin/c-manage-report-suites/c-edit-report-suites/document-cloud-config.md)
         + [Advertising Analytics-configuratie](admin/c-manage-report-suites/c-edit-report-suites/advertising-analytics-config.md)
         + Real-time {#real-time-reports}
            + [Overzicht van real-time rapporten](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime.md)
            + [Configuratie van realtime rapporten](admin/c-manage-report-suites/c-edit-report-suites/realtime/t-realtime-admin.md)
            + [Ondersteunde realtime metrische gegevens en dimensies](admin/c-manage-report-suites/c-edit-report-suites/realtime/realtime-metrics.md)
      + [Rapportsuites beheren](admin/c-manage-report-suites/report-suites-admin.md)
      + [Wereldwijde rapportsuites](admin/c-manage-report-suites/rollup-report-suite.md)
      + [Een zoekopdracht in een rapportsuite opslaan](admin/c-manage-report-suites/t-report-suite-saved-search.md)
      + [Instellingen voor rapportsuite downloaden](admin/c-manage-report-suites/t-download-rs-settings.md)
      + Nieuwe rapportsuite {#c-new-report-suite}
         + [Een rapportsuite maken](admin/c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md)
         + [Een rapportgroepgroep maken](admin/c-manage-report-suites/c-new-report-suite/t-create-rs-group.md)
         + [Nieuwe rapportsuite - instellingen](admin/c-manage-report-suites/c-new-report-suite/new-report-suite.md)
         + [Instellingen die niet zijn gekopieerd uit een suite met bronrapporten](admin/c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md)
      + Sjablonen voor rapportsuites {#report-suite-templates}
         + [Overzicht van sjablonen voor rapportsuite](admin/c-manage-report-suites/c-report-suite-templates/report-suite-templates.md)
         + [Aggregator portaal](admin/c-manage-report-suites/c-report-suite-templates/aggregator-portal.md)
         + [Commerce](admin/c-manage-report-suites/c-report-suite-templates/commerce-admin.md)
         + [Inhoud en media](admin/c-manage-report-suites/c-report-suite-templates/content-media.md)
         + [Standaard sjabloon](admin/c-manage-report-suites/c-report-suite-templates/default-rs-template.md)
         + [Financiële dienstverlening](admin/c-manage-report-suites/c-report-suite-templates/financial-services.md)
         + [Vacatureportaal](admin/c-manage-report-suites/c-report-suite-templates/job-portal.md)
         + [Leads genereren](admin/c-manage-report-suites/c-report-suite-templates/lead-generation.md)
         + [Ondersteuning Media](admin/c-manage-report-suites/c-report-suite-templates/support-media.md)
   + Bedrijfsinstellingen {#company-settings}
      + [Overzicht van bedrijfsinstellingen](admin/company/c-company-settings.md)
      + [Beveiligingsmanager](admin/company/security-manager.md)
      + [Webservices](admin/company/web-services-admin.md)
      + [Rapporten van Report Builder](admin/company/report-builder-reports-admin.md)
      + [Eenmalige aanmelding](admin/company/single-signon-admin.md)
      + [Rapportsuites verbergen](admin/company/c-hide-report-suites.md)
      + [Voorkeuren beheer](admin/company/preferences-manager.md)
      + [Hangende acties](admin/company/pending-actions-admin.md)
      + [Toegangsniveaus voor functies](admin/company/feature-access-levels.md)
   + Privacylabeling voor gegevensbeheer {#data-governance}
      + [Workflow voor gegevensprivacy van Adobe Analytics](admin/c-data-governance/an-gdpr-workflow.md)
      + [Veelgestelde vragen](admin/c-data-governance/gdpr-faq.md)
      + Gegevens labelen {#data-labels}
         + [Privacylabels voor gegevens voor Analytics-onderdelen](admin/c-data-governance/data-labeling/gdpr-labels.md)
         + [Rapportsuitedata labelen](admin/c-data-governance/data-labeling/gdpr-setup-reportsuite.md)
         + [De privacylabels van Report Suite bekijken/beheren](admin/c-data-governance/data-labeling/gdpr-view-settings.md)
         + [Best practices voor labelen](admin/c-data-governance/data-labeling/gdpr-analytics-ids.md)
         + [Voorbeeld van etikettering](admin/c-data-governance/data-labeling/gdpr-labeling-example.md)
         + [Naamruimten](admin/c-data-governance/data-labeling/gdpr-namespaces.md)
      + [Vrijstelling van toestemming van de CNIL](admin/c-data-governance/cnil-consent-exemption.md)
   + Gebruik van server calls {#server-call-usage}
      + [Overzicht van het gebruik van servergesprekken](admin/c-server-call-usage/overage-overview.md)
      + [Bekijk het huidige gebruik van serveroproepen](admin/c-server-call-usage/server-call-usage-dashboard.md)
      + [Gebruik van rapportsuite weergeven](admin/c-server-call-usage/report-suite-usage.md)
      + [Waarschuwingen voor het gebruik van serveroproepen](admin/c-server-call-usage/scu-alerts.md)
      + [Veelgestelde vragen over het gebruik van serveroproepen](admin/c-server-call-usage/overage-faq.md)
   + User en Product Management (verouderd) {#user-product-management}
      + [Gebruikers- en productbeheer (verouderd)](admin/user-management2/user-management.md)
      + [Verouderde gebruikersaccounts, activa en vervaldatums beheren](admin/user-management2/users-assets.md)
      + Gebruikers migreren naar Adobe Admin Console {#migrate-users}
         + [Analytics-gebruikersmigratie naar de Admin Console](admin/user-management2/user-migration/c-migration-tool.md)
         + [Analytics-gebruikersaccounts migreren voor Adobe ID&#39;s](admin/user-management2/user-migration/t-migrate-users.md)
         + [Analytics-gebruikersaccounts migreren voor Enterprise- en Federated ID&#39;s](admin/user-management2/user-migration/migrate-enterprise.md)
         + [Verouderde aanmeldingen uitschakelen](admin/user-management2/user-migration/t-disable-legacy-login.md)
         + [API&#39;s die door de migratie worden beïnvloed](admin/user-management2/user-migration/developer.md)
+ [API voor beheerders](c-admin-api/c-admin-api.md)
+ [Veelgestelde vragen over Adobe Analytics 1.4 API EOL](c-admin-api/c-admin-14-api-eol.md)

