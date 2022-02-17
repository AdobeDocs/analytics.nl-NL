---
title: Een datalaag maken
description: Leer wat een gegevenslaag in uw implementatie Analytics is, en hoe het kan worden gebruikt om variabelen in Adobe Analytics in kaart te brengen.
feature: Implementation Basics
exl-id: 271dd8fa-3ba1-4a7f-b16a-c48a736a5bb5
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%

---

# Een datalaag maken

Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.

Hier volgt een video over het gebruik van gegevenslagen:

>[!VIDEO](https://video.tv.adobe.com/v/28775/?quality=12)

## Vereisten

[Een document voor het ontwerp van een oplossing maken](solution-design.md) - Het is belangrijk dat uw organisatie zich aanpast aan de traceervereisten. Zorg ervoor dat u met een document van het oplossingsontwerp alvorens ontwikkelingsteams in uw organisatie wordt voorbereid te benaderen.

## Workflow

Bij het implementeren van Adobe Analytics met een gegevenslaag worden doorgaans de volgende stappen uitgevoerd:

1. **Werk met uw team van de plaatsontwikkeling om een gegevenslaag uit te voeren**: Uw team van de plaatsontwikkeling is hoofdzakelijk verantwoordelijk voor het ervoor zorgen van het voorwerp van de gegevenslaag bevolkt met correcte waarden. Controleer deze pagina met uw team van de plaatsontwikkeling om ervoor te zorgen de verwachtingen tussen teams worden gericht.

   >[!NOTE]
   >
   >De volgende Adobe aanbevolen gegevenslaagspecificaties is optioneel. Als u reeds een gegevenslaag hebt, of anders verkiest om Adobe geen specificaties te volgen, zorg ervoor dat uw organisatie zich op welke specificatie richt te volgen.
1. **Valideer uw gegevenslaag met een browserconsole**: Zodra een gegevenslaag wordt gecreeerd, kunt u bevestigen dat het gebruikend om het even welke browser ontwikkelaarsconsole werkt. U kunt de ontwikkelaarsconsole in de meeste browsers openen gebruikend `F12` toets. Een waarde van een voorbeeldvariabele zou `digitalData.page.pageInfo.pageID`.
1. **Adobe Experience Platform-tags gebruiken om gegevenslaagobjecten toe te wijzen aan gegevenselementen**: Maak gegevenselementen in de gebruikersinterface voor gegevensverzameling in Adobe Experience Platform en wijs deze toe aan de JavaScript-kenmerken die in de gegevenslaag worden beschreven.
1. **De Adobe Analytics-tagextensie gebruiken om gegevenselementen toe te wijzen aan analytische variabelen**: Na uw document van het oplossingsontwerp, wijs elk gegevenselement aan de aangewezen variabele Analytics toe.

## Specificaties

Adobe beveelt aan de [Klantenervaring met digitale gegevenslaag](https://www.w3.org/2013/12/ceddl-201312.pdf) door de [Klantervaring met Digital Data Community Group](https://www.w3.org/community/custexpdata/). Gebruik de volgende secties om te begrijpen hoe de elementen van de gegevenslaag met Adobe Analytics in wisselwerking staan.

Het aanbevolen overkoepelende gegevenslaagobject is `digitalData`. In het volgende voorbeeld wordt een enigszins uitgebreid JSON-gegevenslaagobject met voorbeeldwaarden weergegeven:

```js
digitalData = {
    pageInstanceID: "Example page - production",
    page: {
        pageInfo: {
            pageID: "5093",
            pageName: "Example page",
            destinationURL: "https://example.com/index.html",
            referringURL: "https://example.com/referrer.html",
            sysEnv: "desktop",
            variant: "2",
            version: "1.14",
            breadCrumbs: ["Home","Example group","Example page"],
            author: "J Smith",
            issueDate: "Example date",
            effectiveDate: "Example date",
            expiryData: "Example date",
            language: "en-US",
            geoRegion: "US",
            industryCodes: "Example industry codes",
            publisher: "Example publisher"
        },
        category: {
            primaryCategory: "Example page category",
            subCategory: "Sub-category example"
        },
        attributes: {
            country: "US",
            language: "en-US"
        }
    },
    product: [{
        productInfo: {
            productID: "4859",
            productName: "Example product",
            description: "Example description",
            productURL: "https://example.com/product.html",
            productImage: "https://example.com/product_image.png",
            productThumbnail: "https://example.com/product_thumbnail.png",
            manufacturer: "Example manufacturer",
            quantity: 1,
            size: "Product size"
        },
        category: {
            primaryCategory: "Example product category",
            subCategory: "Example sub-category"
        }
    }],
    cart: {
        cartID: "934856",
        price: {
            basePrice: 200.00,
            voucherCode: "EXAMPLEVOUCHER1",
            voucherDiscount: 0.50,
            currency: "USD",
            taxRate: 0.20,
            shipping: 5.00,
            shippingMethod: "UPS",
            priceWithTax: 120,
            cartTotal: 125
        }
    },
    transaction: {
        transactionID: "694025",
        profile: {
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com"
            },
            address: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            },
            shippingAddress: {
                line1: "123 Vague Street",
                line2: "Apt 1",
                city: "Austin",
                stateProvince: "TX",
                postalCode: "78610",
                country: "USA"
            }
        }
    },
    event: [{
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    }],
    component: [{
        componentInfo: {
            componentID: "4921",
            componentName: "Example component"
        },
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    }],
    user: [{
        segment: "Premium membership",
        profile: [{
            profileInfo: {
                profileID: "exampleprofile",
                userName: "exampleusername",
                email: "user@example.com",
                language: "en-US",
                returningStatus: "New"
            },
            social: {
                facebook: "examplefacebookid",
                twitter: "exampletwitterhandle"
            }
        }]
    }],
    privacy: {
        accessCategories: [{
            categoryName: "Default",
            domains: "adobedtm.com"
        }]
    },
    version: "1.0"
}
```

Gebruik de [Klantenervaring met digitale gegevenslaag](https://www.w3.org/2013/12/ceddl-201312.pdf) rapporteren voor details over elk object en subobject. Niet alle sites gebruiken alle objecten; als u bijvoorbeeld een nieuwssite host, is het onwaarschijnlijk dat u het programma `digitalData.product` objectarray.

Gegevenslagen zijn uitbreidbaar; als u specifieke vereisten voor uw organisatie hebt, kunt u voorwerpen in uw gegevenslaag omvatten om die behoeften aan te passen.

## Waarden voor gegevenslagen instellen

Gegevenslagen genereren doorgaans aan de serverzijde, waarbij wordt verwezen naar dezelfde objecten die worden gebruikt om de site-inhoud samen te stellen. Stel de gegevenslaag van de site in op basis van de traceervereisten die zijn ingesteld in de [document ontwerp oplossing](solution-design.md).

## Volgende stappen

[Gegevenslaagobjecten toewijzen aan gegevenselementen](../launch/layer-to-elements.md): Gebruik de gegevenslaag van uw site in Adobe Experience Platform.
