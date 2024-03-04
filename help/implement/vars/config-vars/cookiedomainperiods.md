---
title: cookieDomainPeriods
description: Help het AppMeasurement te begrijpen welk domein cookies moeten worden opgeslagen als het domein een punt in het achtervoegsel heeft.
feature: Variables
exl-id: c426d6a7-4521-4d50-bb7d-1664920618d8
role: Admin, Developer
source-git-commit: fe33da47c109adacb8162c7165ad4c63bd65c08d
workflow-type: tm+mt
source-wordcount: '659'
ht-degree: 0%

---


# cookieDomainPeriods

AppMeasurement bepaalt zijn koekjesplaats door het domein en domeinachtervoegsel te bekijken. Voor domeinen zoals `example.com`AppMeasurement stelt cookies in op de juiste locatie. Voor andere domeinen, zoals `example.co.uk`AppMeasurement kan cookies per ongeluk instellen op `co.uk`. De meeste browsers weigeren cookies die op dit ongeldige domein zijn ingesteld, wat problemen met de identificatie van de bezoeker veroorzaakt.

De `cookieDomainPeriods` de variabele helpt AppMeasurement bepalen waar de koekjes van Analytics door te roepen worden geplaatst dat het domeinachtervoegsel een extra periode in het heeft. Met deze variabele kan AppMeasurement de extra periode in het domeinachtervoegsel aanpassen en cookies instellen op de juiste locatie.

* Voor domeinen zoals `example.com` of `www.example.com`hoeft u deze variabele niet in te stellen. Indien nodig, kunt u deze variabele instellen op `"2"`.
* Voor domeinen zoals `example.co.uk` of `www.example.co.jp`stelt u deze variabele in op `"3"`.


>[!IMPORTANT]
>
>Houd geen rekening met subdomeinen voor deze variabele. Niet instellen `cookieDomainPeriods` in de voorbeeld-URL `store.toys.example.com`. AppMeasurement herkent standaard dat cookies moeten worden opgeslagen op `example.com`, zelfs op URL&#39;s met veel subdomeinen.


## Cookie-domeinperiodes, cookies van derden en identificatie van oudere bezoekers

Alleen wanneer u de oudere Adobe Analytics-bezoekersidentificatie gebruikt (in plaats van de aanbevolen Experience Cloud Identity-service), de impliciete of expliciete configuratie van `cookieDomainPeriods` kan gevolgen hebben voor de manier waarop bezoekers worden geïdentificeerd, afhankelijk van het feit of cookies van derden al dan niet worden geblokkeerd.

De volgende tabel illustreert vier mogelijke scenario&#39;s.

| Scenario | `cookieDomainPeriods` configuratie is ... | Cookies van derden worden geblokkeerd? | Resultaat bij gebruik van de oude Adobe Analytics-service voor bezoekersidentificatie |
|:---:|---|---|---|
| 1 | <span style="color:green">Juist</span> | Nee | Bezoekers worden geïdentificeerd met een `s_vi` cookie instellen op de server. |
| 2 | <span style="color:green">Juist</span> | Ja | Bezoekers worden geïdentificeerd met een fallback `s_fid` cookie, client-side instellen (domein van eerste pagina). |
| 3 | <span style="color:red">Onjuist</span> | Nee | De bezoekers worden geïdentificeerd met reserve herkenningsteken dat op combinatie gebruikersagent en IP-adres wordt gebaseerd. <br/>AppMeasurement wordt gedwongen cookies in te stellen als cookies van derden.<br/> De `s_vi` cookie is mogelijk ingesteld wanneer `cookieDomainPeriods` niet correct wordt verzonden. |
| 4 | <span style="color:red">Onjuist</span> | Ja | De bezoekers worden geïdentificeerd met reserve herkenningsteken dat op combinatie gebruikersagent en IP-adres wordt gebaseerd.<br/>AppMeasurement wordt gedwongen cookies in te stellen als cookies van derden die worden geblokkeerd, zodat er geen cookies worden ingesteld. |

>[!CAUTION]
>
>U zou per ongeluk kunnen gevormd hebben `cookieDomainPeriods` <span style="color:red">onjuist</span> (met de standaardwaarde van `"2"`) tijdens het gebruik van domeinen zoals `example.co.uk`. Deze impliciete onjuiste configuratieresultaten die u bezoekers na scenario 3 of 4 identificeert.
>
>AppMeasurement versie 2.26.x of later vormt `cookieDomainPeriods` automatisch met de juiste waarde, zodat alleen scenario 1 of 2 mogelijk zijn. Wanneer u aan versie 2.26.x van het AppMeasurement of recenter, terwijl momenteel het identificeren van bezoekers verkeerd (scenario 3 of 4) bijwerkt, heeft de update belangrijke implicaties.
>
>* Bezoekersidentificatoren worden opnieuw ingesteld en bezoekers worden weergegeven als nieuwe bezoekers. Nieuwe activiteit kan niet worden gekoppeld aan de vorige bezoeker-id.
>* Cookies worden ingesteld (bijvoorbeeld voor het bijhouden van koppelingen of een activiteitenoverzicht, bijvoorbeeld`s_sq` cookie), resulterend in plotselinge verschillen in rapportage.
>
>Tijdens het correct configureren `cookieDomainPeriods` Hiermee verbetert u het AppMeasurement en de analysefunctie. U wordt aangeraden na te gaan of de wijzigingen die u hebt aangebracht als gevolg van de upgrade van uw AppMeasurement.
>
> Zie [Analysecookies](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-analytics.html?lang=en) voor meer informatie over het gebruik van cookies door het AppMeasurement.

## Domeinperioden cookie maken met de SDK van het web

De SDK van het Web kan het correcte domein van de koekjesopslag zonder deze variabele bepalen.

## Domeinperiodes kopiëren met de Adobe Analytics-extensie

Domeinperioden is een veld onder de [!UICONTROL Cookies] accordeon bij het configureren van de Adobe Analytics-extensie.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Ga naar de [!UICONTROL Extensions] en klikt u op de knop **[!UICONTROL Configure]** onder Adobe Analytics.
1. Breid uit [!UICONTROL Cookies] accordion, die de [!UICONTROL Domain Periods] veld.

Stel dit veld in op `3` alleen in domeinen die een punt in zijn achtervoegsel bevatten. Anders kan dit veld leeg blijven.

## De domeinperiodes van het cookie in code AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

U kunt de `cookieDomainPeriods` in de AppMeasurement Javascript bibliotheek of in de redacteur van de douanecode van de uitbreiding van de Analyse.

De `cookieDomainPeriods` variabele is een tekenreeks die doorgaans wordt ingesteld op `"3"`, alleen op domeinen die een punt in het achtervoegsel bevatten. De standaardwaarde is `"2"`, waarin de meeste domeinen kunnen worden opgenomen.

```js
// Manually set cookieDomainPeriods for domains with a period in its suffix, such as www.example.co.uk
s.cookieDomainPeriods = "3";

// Detect if a URL has a domain suffix with an extra period, and set s.cookieDomainPeriods automatically
document.URL.indexOf(".co.") > 0 ? s.cookieDomainPeriods = "3" : s.cookieDomainPeriods = "2";
```
