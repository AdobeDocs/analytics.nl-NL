---
title: Veldgebaseerde stitching
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend op gebied-gebaseerde stitching.
exl-id: 81f2768c-53c2-40b4-8d3b-8d3b94cd7318
feature: CDA
role: Admin
source-git-commit: cfa5cc02ba3a7349b51a904f29bab533c0f1c603
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Veldgebaseerde stitching

{{available-existing-customers}}

Cross-Device Analytics biedt twee verschillende methoden om gegevens aan elkaar te koppelen. Deze methode baseert zich op een variabele Analytics, zoals a [ pro ](/help/implement/vars/page-vars/prop.md) of [ eVar ](/help/implement/vars/page-vars/evar.md), om een persoonsidentificatie te bevatten. Het gebruikt die variabele als basis om apparaten samen te verbinden. De Adobe beveelt deze optie aan om bezoekers transparanter en voorspelbaarder te maken.

## Vereisten die specifiek zijn voor veldomstandigheden

Als u Cross-Device Analytics wilt implementeren met behulp van op het veld gebaseerde stitching, is het volgende vereist. Werk met teams binnen uw organisatie en uw Team van de Rekening van de Adobe om ervoor te zorgen dat u aan elk van het volgende voldoet.

>[!WARNING]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* Alle eerste vereisten die op de [ overzichtspagina ](overview.md) worden vermeld.
* In uw implementatie moet een proxy of eVar worden ingesteld die een individu waar mogelijk op unieke wijze identificeert, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Wijs geen standaardwaarde toe aan de proxy of eVar.
* Deel de gewenste identificerende variabele aan uw Team van de Rekening van de Adobe mee wanneer provisioned voor op gebied-gebaseerd het stitching.

## Beperkingen die specifiek zijn voor stitching in het veld

* Op veld gebaseerde stitching werkt het beste bij rapportsuites met een hoog gebruikersidentificatie-/verificatiepercentage.
* Hoewel props en eVars elk regels bevatten voor de manier waarop hoofdletters en kleine letters worden verwerkt voor rapportagedoeleinden, wordt door veldobjecten de voor stitching gebruikte eigenschap of eVar op geen enkele manier getransformeerd. Op velden gebaseerde stitching gebruikt de waarde in het opgegeven veld omdat deze regels voor post VISTA en nabewerkingsregels bevat. Het stitching proces is case-sensitive. Als bijvoorbeeld soms het woord &#39;Bob&#39; voorkomt in de pop/eVar en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze door het stitching-proces als twee aparte personen behandeld.
* Aangezien veldoverstikken hoofdlettergevoelig is, beveelt de Adobe aan om alle VISTA-regels of verwerkingsregels te herzien die van toepassing zijn op de prop of eVar die wordt gebruikt voor veldoverstikken. Zij moeten worden herzien om ervoor te zorgen dat geen van deze regels nieuwe vormen van zelfde identiteitskaart introduceert. U moet er bijvoorbeeld voor zorgen dat er geen VISTA- of verwerkingsregels zijn die alleen voor een deel van de treffers een lagere waarde aan de proxy of eVar toevoegen.
* Op velden gebaseerde stitching ondersteunt het gebruik van meer dan één prop of eVar voor stitching doeleinden niet. Bijvoorbeeld, als eVar12 login identiteitskaart bevat en eVar20 e-mailidentiteitskaart bevat, moet u één van hen kiezen.
* Veldgebaseerde stitching combineert of voegt geen velden samen (bijvoorbeeld eVar10 + prop5).
* De eigenschap of eVar moet één type id bevatten. De proxy of eVar mag bijvoorbeeld geen combinatie van aanmeldings-id&#39;s en e-mailadressen bevatten.
* Als meerdere treffers voorkomen met dezelfde tijdstempel voor dezelfde bezoeker, maar met verschillende waarden in de tekenreekscode of eVar, kiest CDA op basis van alfabetische volgorde. Dus als bezoeker A twee hits heeft met dezelfde tijdstempel en een van de hits Bob opgeeft en de andere gebruiker Ann opgeeft, kiest CDA Ann.


## Volgende stappen

Zodra uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u [ Opstelling Analytics van het Apparaat ](setup.md) beginnen.
