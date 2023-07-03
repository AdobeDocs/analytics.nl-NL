---
title: Veldgebaseerde stitching
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend op gebied-gebaseerde stitching.
exl-id: 81f2768c-53c2-40b4-8d3b-8d3b94cd7318
feature: CDA
source-git-commit: 811e321ce96aaefaeff691ed5969981a048d2c31
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Veldgebaseerde stitching

Cross-Device Analytics biedt twee verschillende methoden om gegevens aan elkaar te koppelen. Deze methode is gebaseerd op een variabele Analytics, zoals een [prop](/help/implement/vars/page-vars/prop.md) of [eVar](/help/implement/vars/page-vars/evar.md), om een persoon-id te bevatten. Het gebruikt die variabele als basis om apparaten samen te verbinden. Adobe raadt deze optie aan voor meer transparantie en voorspelbaarheid bij het bijhouden van bezoekers.

## Vereisten die specifiek zijn voor veldomstandigheden

Als u Cross-Device Analytics wilt implementeren met behulp van op het veld gebaseerde stitching, is het volgende vereist. Werk met teams binnen uw organisatie en uw Adobe Account Team om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!WARNING]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* Alle voorwaarden die op de [overzichtspagina](overview.md).
* Uw implementatie moet een proxy of eVar instellen die een individu waar mogelijk op unieke wijze identificeert, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Wijs geen standaardwaarde aan de eigenschap of de eVar toe.
* Deel de gewenste identificerende variabele aan uw Team van de Rekening van Adobe mee wanneer provisioned voor op gebied-gebaseerd het stitching.

## Beperkingen die specifiek zijn voor stitching in het veld

* Op veld gebaseerde stitching werkt het beste bij rapportsuites met een hoog gebruikersidentificatie-/verificatiepercentage.
* Hoewel props en eVars elk regels bevatten voor de manier waarop hoofdletters en kleine letters worden verwerkt voor rapportagedoeleinden, wordt door het stitching op basis van velden op geen enkele manier de eigenschap of eVar die voor stitching wordt gebruikt, getransformeerd. Op velden gebaseerde stitching gebruikt de waarde in het opgegeven veld omdat deze regels voor post VISTA en nabewerkingsregels bevat. Het stitching proces is case-sensitive. Als bijvoorbeeld soms het woord &#39;Bob&#39; voorkomt in de pop/eVar en soms het woord &#39;BOB&#39; wordt weergegeven, worden deze door het stitching-proces als twee aparte personen behandeld.
* Aangezien veldoverstikken hoofdlettergevoelig is, raadt Adobe aan om alle VISTA-regels of verwerkingsregels te herzien die van toepassing zijn op de eigenschap of eVar die wordt gebruikt voor veldoverstikken. Zij moeten worden herzien om ervoor te zorgen dat geen van deze regels nieuwe vormen van zelfde identiteitskaart introduceert. U moet er bijvoorbeeld voor zorgen dat er geen VISTA- of verwerkingsregels zijn die alleen voor een deel van de treffers een lagere waarde aan de proxy of eVar toevoegen.
* Op velden gebaseerde stitching ondersteunt het gebruik van meer dan één prop of eVar voor stitching doeleinden niet. Als eVar12 bijvoorbeeld een aanmeldings-id bevat en eVar20 een e-mailadres bevat, moet u een van deze id&#39;s kiezen.
* Veldgebaseerde stitching combineert of voegt geen velden samen (bijvoorbeeld eVar10 + prop5).
* De eigenschap of eVar moet één type id bevatten. De proxy of eVar mag bijvoorbeeld geen combinatie bevatten van aanmeldings-id&#39;s en e-mailid&#39;s.
* Als meerdere treffers voorkomen met dezelfde tijdstempel voor dezelfde bezoeker, maar met verschillende waarden in de tekenreekscode of eVar, kiest CDA op basis van alfabetische volgorde. Dus als bezoeker A twee hits heeft met dezelfde tijdstempel en een van de hits Bob opgeeft en de andere gebruiker Ann opgeeft, kiest CDA Ann.


## Volgende stappen

Zodra uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u beginnen [Apparaatanalyse instellen](setup.md).
