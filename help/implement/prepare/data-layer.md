---
title: Een gegevenslaag maken
description: Leer wat een gegevenslaag in uw implementatie Analytics is, en hoe het kan worden gebruikt om variabelen in de Analytics van Adobe in kaart te brengen.
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# Een gegevenslaag maken

Een gegevenslaag is een raamwerk van JavaScript-objecten op uw site dat alle variabelenwaarden bevat die in uw implementatie worden gebruikt. Hierdoor kunt u uw implementatie beter beheren en eenvoudiger onderhouden.

## Vereisten

[Maak een document](solution-design.md) voor het ontwerp van een oplossing. Het is belangrijk dat uw organisatie zich uitlijnt op de vereisten voor bijhouden. Zorg ervoor u met een document van het oplossingsontwerp alvorens ontwikkelingsteams in uw organisatie wordt voorbereid te benaderen.

## Workflow

Bij de implementatie van Adobe Analytics met een gegevenslaag worden doorgaans de volgende stappen uitgevoerd:

1. **Werk met uw team van de plaatsontwikkeling om een gegevenslaag** uit te voeren: Uw team van de plaatsontwikkeling is hoofdzakelijk verantwoordelijk voor het ervoor zorgen van het voorwerp van de gegevenslaag bevolkt met correcte waarden. Controleer deze pagina met uw team van de plaatsontwikkeling om ervoor te zorgen de verwachtingen tussen teams worden gericht.
   > [!NOTE] De volgende door Adobe aanbevolen specificaties voor gegevenslagen zijn optioneel. Als u al een gegevenslaag hebt of de Adobe-specificaties op een andere manier niet wilt naleven, moet u controleren of uw organisatie is uitgelijnd op de te volgen specificatie.
2. **Valideer uw gegevenslaag met een browserconsole**: Zodra een gegevenslaag wordt gecreeerd, kunt u bevestigen dat het gebruikend om het even welke browser ontwikkelaarsconsole werkt. U kunt de ontwikkelaarsconsole in de meeste browsers openen gebruikend de `F12` sleutel. Een waarde van een voorbeeldvariabele zou `digitalData.page.pageInfo.pageID`zijn.
3. **Met Adobe Experience Platform Launch kunt u gegevenslaagobjecten toewijzen aan gegevenselementen** starten: Maak gegevenselementen in Launch en wijs deze toe aan de JavaScript-kenmerken die in de gegevenslaag worden beschreven.
4. **Met de extensie Adobe Analytics in Launch kunt u gegevenselementen toewijzen aan analytische variabelen**: Na uw document van het oplossingsontwerp, wijs elk gegevenselement aan de aangewezen variabele Analytics toe.

## Specificaties

Adobe raadt u aan de Digital Data Layer [-laag voor](https://www.w3.org/2013/12/ceddl-201312.pdf) klantervaring op te volgen die door de Digital Data Community Group [voor](https://www.w3.org/community/custexpdata/)Klantenervaring is voorgesteld. Gebruik de volgende secties om te begrijpen hoe de elementen van de gegevenslaag met de Analytics van Adobe communiceren.

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
            subCategory1: "Sub-category example"
        },
        attributes: {
            country: "US",
            language: "en-US"
        }
    },
    product1: {
        productInfo: {
            productID: "4859",
            productName: "Example product",
            description: "Example description",
            productURL: "https://example.com/product.html",
            productImage: "https://example.com/product_image.png",
            productThumbnail: "https://example.com/product_thumbnail.png",
            manufacturer: "Example manufacturer",
            size: "Product size"
        },
        category: {
            primaryCategory: "Example product category",
            subCategory: "Example sub-category"
        }
    },
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
    event1: {
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    },
    component1: {
        componentInfo: {
            componentID: "4921",
            componentName: "Example component"
        },
        category: {
            primaryCategory: "Example event category",
            subCategory: "Example sub-category"
        }
    },
    user1: {
        segment: "Premium membership",
        profile1: {
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
        }
    },
    privacy: {
        accessCategories1: {
            categoryName: "Default",
            domains: "adobedtm.com"
        }
    },
    version: "1.0"
}
```

Gebruik het rapport [Customer Experience Digital Data Layer](https://www.w3.org/2013/12/ceddl-201312.pdf) voor meer informatie over elk object en subobject. Niet alle sites gebruiken alle objecten; als u bijvoorbeeld een nieuwssite host, is het onwaarschijnlijk dat u dit object gebruikt. `digitalData.product`

Gegevenslagen zijn uitbreidbaar; als u specifieke vereisten voor uw organisatie hebt, kunt u voorwerpen in uw gegevenslaag omvatten om die behoeften aan te passen.

## Waarden voor gegevenslagen instellen

Gegevenslagen genereren doorgaans aan de serverzijde, waarbij wordt verwezen naar dezelfde objecten die worden gebruikt om de site-inhoud samen te stellen. Bepaal de de gegevenslaag van de plaats die op het volgen vereisten wordt gebaseerd die in het document [van het de](solution-design.md)oplossingsontwerp van uw organisatie worden geplaatst.

## Volgende stappen

[Gegevenslaagobjecten toewijzen aan gegevenselementen](../launch/layer-to-elements.md): Gebruik de gegevenslaag van uw site in Adobe Experience Platform Launch.
