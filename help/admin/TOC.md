---
product: analytics
audience: admin
user-guide-title: Analytics Admin-handleiding
breadcrumb-title: Beheerdershandleiding
user-guide-description: Leer over Analytics beleidstaken, zoals het leiden van gebruikers en producten in de Admin Console van de Experience Cloud, het vormen rapportreeksen, en meer.
source-git-commit: 10a325b5479b6852fc98ed780f59ee525ec6f51b
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 86%

---


# Adobe Analytics Admin Guide {#admin}

+ [Analytics Admin-handleiding](home.md)
+ [Opmerkingen bij de release Analytics](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
+ Overzicht van Analytics Admin {#admin-overview}
   + [Welke Adobe Analytics-tool moet ik gebruiken?](c-analytics-product-comparison/which-analytics-tool.md)
   + [Analytics-productvergelijking en -vereisten](c-analytics-product-comparison/analytics-product-comparison.md)
+ [Systeemvereisten](sys-reqs.md)
+ Admin Tools {#admin-tools}
   + [Admin Tools](admin/c-admin-tools.md)
   + [Facturering](admin/billing-admin.md)
   + Bot verwijderen {#bot-removal}
      + [Bot verwijderen](admin/bot-removal/bot-removal.md)
      + [Overzicht van regels voor bots](admin/bot-removal/bot-rules.md)
      + [Handtekeningen van gewone bot](admin/bot-removal/bot-signatures.md)
      + [Methoden voor botteling](admin/bot-removal/bot-exclusion-methods.md)
   + [Code Manager](admin/code-manager-admin.md)
   + Conversievariabelen {#conversion-variables}
      + [Conversievariabelen (eVars)](admin/conversion-var-admin/conversion-var-admin.md)
      + [Conversievariabelen bewerken](admin/conversion-var-admin/t-conversion-variables-admin.md)
      + [Conversieclassificaties](admin/conversion-var-admin/conversion-classifications.md)
      + [Classificatiehiërarchieën](admin/conversion-var-admin/classification-hierarchies.md)
      + [Lijstvariabelen](admin/conversion-var-admin/list-var-admin.md)
      + [Merchandising-eVars](admin/conversion-var-admin/merchandising-evars.md)
   + [Valutacodes](admin/currency.md)
   + [Aangepaste rapportbeschrijvingen](admin/custom-desc-admin.md)
   + [Kalender aanpassen](admin/custom-calendar.md)
   + [Databronnen](admin/data-sources.md)
   + [Standaardcijfers](admin/default-metrics.md)
   + [Uitsluiten op IP-adres](admin/exclude-ip.md)
   + [Methoden zoeken](admin/finding-methods.md)
   + [Algemene accountinstellingen](admin/general-acct-settings-admin.md)
   + [Interne URL-filters](admin/internal-url-filter-admin.md)
   + [Logboeken](admin/logs.md)
   + [Marketingkanalen](admin/marketing-channels-admin.md)
   + [Menuaanpassing](admin/customize-menus.md)
   + [Metrische zichtbaarheid](admin/metric-visibility.md)
   + [Toepassingsbeheer](admin/mobile-management.md)
   + Paid search-detectie {#paid-search-detection}
      + [Overzicht van paid search-detectie](admin/paid-search-detection/paid-search-detection.md)
      + [Paid search-detectie configureren](admin/paid-search-detection/t-paid-search-detection.md)
   + [Lijsten publiceren](admin/publishing-list.md)
   + [Widget publiceren](admin/publishing-widgets-admin.md)
   + [Voorkeurenbeheer](admin/preferences-manager.md)
   + [Privacy-instellingen](admin/privacy-settings.md)
   + [Privacy-rapportage](admin/privacy-reporting.md)
   + Verwerkingsregels {#processing-rules}
      + [Overzicht van verwerkingsregels](admin/c-processing-rules/processing-rules.md)
      + Configuratie van verwerkingsregels {#processing-rules-configuration}
         + [De werking van verwerkingsregels](admin/c-processing-rules/c-processing-rules-configuration/processing-rules-about.md)
         + [Verwerkingsregels maken](admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules.md)
         + [Actieve verwerkingsregels weergeven](admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules-view.md)
         + [Verwerkingsregelgeschiedenis weergeven](admin/c-processing-rules/c-processing-rules-configuration/t-processing-rule-view-history.md)
         + [Verwerkingsregels herstellen](admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules-restore.md)
         + [Verwerkingsregels kopiëren naar een andere rapportsuite](admin/c-processing-rules/c-processing-rules-configuration/t-processing-rules-copy-to-rs.md)
      + [Beschikbare dimensies voor verwerkingsregels](admin/c-processing-rules/processing-rule-dimensions.md)
      + Voorbeelden van verwerkingsregels {#processing-rules-examples}
         + [Voorbeelden van verwerkingsregels](admin/c-processing-rules/processing-rules-examples/processing-rules-examples.md)
         + [Een campagne-id invullen op basis van een queryreeksparameter](admin/c-processing-rules/processing-rules-examples/processing-rules-populate-campaign-id.md)
         + [Productweergavegebeurtenis instellen op basis van de productoverzichtspagina](admin/c-processing-rules/processing-rules-examples/setting-the-product-view-event.md)
         + [Een subcategorie toevoegen door de categorie- en paginanaam samen te voegen](admin/c-processing-rules/processing-rules-examples/subcategory-concatenating.md)
         + [Een pad bepalen door een eVar-waarde naar een prop te kopiëren](admin/c-processing-rules/processing-rules-examples/processing-rules-determining-path.md)
         + [Waarden in een rapport opschonen](admin/c-processing-rules/processing-rules-examples/clean-up-values-in-a-report.md)
         + [Interne zoektermen invullen op basis van een queryreeksparameter](admin/c-processing-rules/processing-rules-examples/processing-rules-populating-internal-search.md)
         + [Een contextdatavariabele kopiëren naar een eVar](admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data.md)
         + [Een gebeurtenis instellen met een contextdatavariabele](admin/c-processing-rules/processing-rules-examples/processing-rules-copy-context-data-event.md)
         + [Een gebeurtenis verwijderen uit een treffer](admin/c-processing-rules/processing-rules-examples/processing-rules-remove-event.md)
      + [Tips en trucs voor verwerkingsregels](admin/c-processing-rules/processing-rules-tips.md)
   + Realtimerapporten {#real-time-reports}
      + [Overzicht van realtimerapporten](admin/realtime/realtime.md)
      + [Configuratie van realtimerapporten](admin/realtime/t-realtime-admin.md)
      + [Ondersteunde cijfers en en dimensies in real time](admin/realtime/realtime-metrics.md)
   + [Activity Manager rapporteren](admin/reporting-activity.md)
   + [Wachtrij voor geplande rapporten](admin/scheduled-reports-admin.md)
   + Server-side doorsturen {#server-side-forwarding}
      + [Overzicht van server-side doorsturen](admin/c-server-side-forwarding/ssf.md)
      + [GDPR/ePrivacy-compliance en server-side doorsturen](admin/c-server-side-forwarding/ssf-gdpr.md)
      + [Vereisten voor server-side doorsturen](admin/c-server-side-forwarding/ssf-requirements.md)
      + [Data- en codereferentie server-side doorsturen](admin/c-server-side-forwarding/ssf-reference.md)
      + [Implementatie van server-side doorsturen controleren](admin/c-server-side-forwarding/ssf-verify.md)
      + [Veelgestelde vragen over server-side doorsturen](admin/c-server-side-forwarding/ssf-faq.md)
   + [Menu Vereenvoudigde rapporten](admin/t-simplified-menu.md)
   + [Social Management](admin/social-management.md)
   + Succesgebeurtenissen {#success-events}
      + [Overzicht van succesgebeurtenissen](admin/c-success-events/success-event.md)
      + [Succesgebeurtenissen configureren](admin/c-success-events/t-success-events.md)
      + [Het gebeurtenistype wijzigen](admin/c-success-events/event-type.md)
   + [Tijdstempels optioneel](admin/timestamp-optional.md)
   + Traffic variabelen {#traffic-variables}
      + [Overzicht traffic variabele (prop)](admin/c-traffic-variables/traffic-var.md)
      + [Rapporten voor traffic variabelen inschakelen](admin/c-traffic-variables/t-traffic-variable.md)
      + [Traffic-classificaties](admin/c-traffic-variables/traffic-classifications.md)
   + Variabele Unique Visitor {#unique-visitor-variable}
      + [De variabele Unique Visitor opgeven](admin/unique-visitor-variable-admin/t-unique-visitor-variable.md)
      + [Gebruiksscenario - Bezoekers-id&#39;s](admin/unique-visitor-variable-admin/extract-visitorids-usecase.md)
   + [Videobeheer](admin/video-management.md)
+ Analyses in de Adobe Admin Console {#admin-console}
   + [Analyses in de Adobe Admin Console](admin-console/home.md)
   + Toestemmingen {#permissions}
      + [Machtigingen voor Analytics in Admin Console](admin-console/permissions/summary-tables.md)
      + [Productprofielen voor Adobe Analytics](admin-console/permissions/product-profile.md)
      + [Machtigingen voor productprofielen voor rapportsuite](admin-console/permissions/report-suite-tools.md)
      + [Machtigingen voor productprofielen voor Analytics Tools](admin-console/permissions/analytics-tools.md)
   + [Eerste Adobe Analytics-beheerdershandleiding](admin-console/first-admin-guide.md)
+ Bedrijfsinstellingen {#company-settings}
   + [Overzicht van bedrijfsinstellingen](company/c-company-settings.md)
   + [Toegangsniveaus voor functies](company/feature-access-levels.md)
   + [Webservices](company/web-services-admin.md)
   + [Report Builder-rapporten](company/report-builder-reports-admin.md)
   + [Eenmalige aanmelding](company/single-signon-admin.md)
   + [In behandeling zijnde handelingen](company/pending-actions-admin.md)
   + [Co-branding](company/co-branding-admin.md)
   + [Rapportsuites verbergen](company/c-hide-report-suites.md)
   + [Security Manager](company/security-manager.md)
+ Rapportsuites beheren {#manage-report-suites}
   + [Rapportsuitebeheer](c-manage-report-suites/report-suites-admin.md)
   + [Samenvatting en global report suites](c-manage-report-suites/rollup-report-suite.md)
   + [Een overzichtsrapportsuite maken](c-manage-report-suites/t-rollups.md)
   + Sjablonen voor rapportsuites {#report-suite-templates}
      + [Overzicht van sjablonen voor rapportsuites](c-manage-report-suites/c-report-suite-templates/report-suite-templates.md)
      + [Verzamel-portal](c-manage-report-suites/c-report-suite-templates/aggregator-portal.md)
      + [Commerce](c-manage-report-suites/c-report-suite-templates/commerce-admin.md)
      + [Content en media](c-manage-report-suites/c-report-suite-templates/content-media.md)
      + [Standaardsjabloon](c-manage-report-suites/c-report-suite-templates/default-rs-template.md)
      + [Financiële diensten](c-manage-report-suites/c-report-suite-templates/financial-services.md)
      + [Vacatureportal](c-manage-report-suites/c-report-suite-templates/job-portal.md)
      + [Lead generation](c-manage-report-suites/c-report-suite-templates/lead-generation.md)
      + [Ondersteuningsmedia](c-manage-report-suites/c-report-suite-templates/support-media.md)
   + [Een zoekopdracht in een rapportsuite opslaan](c-manage-report-suites/t-report-suite-saved-search.md)
   + [Instellingen voor afzonderlijke rapportsuites](c-manage-report-suites/individual-rs-settings.md)
   + [Instellingen voor rapportsuites downloaden](c-manage-report-suites/t-download-rs-settings.md)
   + Nieuwe rapportsuite {#new-report-suite}
      + [Een rapportsuite maken](c-manage-report-suites/c-new-report-suite/t-create-a-report-suite.md)
      + [Nieuwe rapportsuite - instellingen](c-manage-report-suites/c-new-report-suite/new-report-suite.md)
      + [Instellingen die niet uit een bronrapportsuite zijn gekopieerd](c-manage-report-suites/c-new-report-suite/settings-not-copied-from-rs.md)
   + [Een rapportsuitegroep maken](c-manage-report-suites/t-create-rs-group.md)
+ User en Product Management (verouderd) {#user-product-management}
   + [User en Product Management](user-management2/user-management.md)
   + Gebruikers migreren naar Adobe Admin Console {#migrate-users}
      + [Analytics-gebruikersmigratie naar de Admin Console](user-management2/user-migration/c-migration-tool.md)
      + [Analytics-gebruikersaccounts voor Adobe ID’s migreren](user-management2/user-migration/t-migrate-users.md)
      + [Analytics-gebruikersaccounts voor Enterprise en Federated ID’s migreren](user-management2/user-migration/migrate-enterprise.md)
      + [Verouderde logins uitschakelen](user-management2/user-migration/t-disable-legacy-login.md)
      + [API&#39;s die door de migratie worden beïnvloed](user-management2/user-migration/developer.md)
+ Data Governance {#data-governance}
   + [Adobe Analytics en GDPR](c-data-governance/an-gdpr-overview.md)
   + [Adobe Analytics en CCPA](c-data-governance/an-ccpa-overview.md)
   + [Vrijstelling van CNIL-toestemming](c-data-governance/cnil-consent-exemption.md)
   + [Veelgestelde vragen](c-data-governance/gdpr-faq.md)
   + [Adobe Analytics Data Privacy-workflow](c-data-governance/an-gdpr-workflow.md)
   + [Data Governance-instellingen van rapportsuites weergeven/beheren](c-data-governance/gdpr-view-settings.md)
   + [Rapportsuitedata labelen](c-data-governance/gdpr-setup-reportsuite.md)
   + [Aanvragen voor toegang en verwijdering verzenden](c-data-governance/gdpr-submit-access-delete.md)
   + [Data Privacy-labels voor Analytics-variabelen](c-data-governance/gdpr-labels.md)
   + [Naamruimten](c-data-governance/gdpr-namespaces.md)
   + [Id-uitbreiding](c-data-governance/gdpr-id-expansion.md)
   + [Best practices voor labelen](c-data-governance/gdpr-analytics-ids.md)
   + [Voorbeeld van labeling](c-data-governance/gdpr-labeling-example.md)
   + [Data Privacy en Data Connectors (Genesis)](c-data-governance/data-connectors-gdpr.md)
   + [Data Privacy-terminologie](c-data-governance/gdpr-terminology.md)
   + [Variabelen voor privacyrapportage](c-data-governance/consent-variables.md)
+ Gebruik van server calls {#server-call-usage}
   + [Overzicht van het gebruik van server calls](c-server-call-usage/overage-overview.md)
   + [Huidig gebruik van server calls weergeven](c-server-call-usage/server-call-usage-dashboard.md)
   + [Gebruik van rapportsuites weergeven](c-server-call-usage/report-suite-usage.md)
   + [Waarschuwingen over het gebruik van server calls](c-server-call-usage/scu-alerts.md)
   + [Veelgestelde vragen over het gebruik van server calls](c-server-call-usage/overage-faq.md)
+ Traffic-beheer {#traffic-management}
   + [Traffic beheren](c-traffic-management/traffic-management.md)
   + [Een traffic-piek plannen](c-traffic-management/t-traffic-schedule-spike.md)
   + [Vroegere server calls beoordelen en een traffic-piek plannen](c-traffic-management/traffic-spike-estimate-past-server-calls.md)
   + [Permanente traffic-toename opgeven](c-traffic-management/t-traffic-permanent.md)
   + [Vereiste aanlooptijd voor traffic-toename](c-traffic-management/traffic-lead-time.md)
+ [Admin-API](c-admin-api/c-admin-api.md)
