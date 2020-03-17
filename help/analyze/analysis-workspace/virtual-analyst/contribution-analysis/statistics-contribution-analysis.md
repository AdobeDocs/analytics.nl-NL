---
description: De analyse van de bijdrage is een intensief machine het leren proces dat wordt ontworpen om contribuanten aan een waargenomen anomalie in de Analytics van Adobe te ontdekken. De bedoeling is de gebruiker te helpen om gebieden van nadruk of mogelijkheden voor extra analyse veel sneller te vinden dan anders mogelijk zou zijn.
title: Statistische technieken voor de analyse van bijdragen
uuid: f77eb4e4-4fd6-4397-b8a8-a063f199b676
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# Statistische technieken voor de analyse van bijdragen

De analyse van de bijdrage is een intensief machine het leren proces dat wordt ontworpen om contribuanten aan een waargenomen anomalie in de Analytics van Adobe te ontdekken. De bedoeling is de gebruiker te helpen om gebieden van nadruk of mogelijkheden voor extra analyse veel sneller te vinden dan anders mogelijk zou zijn.

De Analyse van de bijdrage verwezenlijkt dit door een tweedelige algoritme aan elke enige afmetingsplaats uit te voeren beschikbaar aan het rapport van de Analyse van de Bijdrage van de gebruiker. Het algoritme werkt in deze volgorde:

1. Voor elke dimensie wordt de V-teststatistiek van de Cramer berekend. Neem in het volgende voorbeeld een noodtabel met paginaweergaven van landen over twee tijdsperioden:

   ![](assets/contingency_table.png)

   In tabel 1 kan Cramer&#39;s V worden gebruikt om de koppeling te meten tussen de paginaweergaven per land voor periode 1 (bijvoorbeeld historisch) en periode 2 (bv. de dag waarop de anomalie zich voordeed). Een lage waarde voor Cramer&#39;s V betekent een lage mate van associatie. Cramer&#39;s V loopt van 0 (geen koppeling) tot en met 1 (volledige koppeling). De V-statistiek van Cramer kan worden berekend:

   ![](assets/cramers-v.png)

1. Voor elk afmetingsitem wordt het residu van de persoon (PR) gebruikt om de relatie tussen de afwijkende meting en elk afmetingsitem te meten. PR volgt een standaardnormale distributie, waardoor het algoritme de PR&#39;s van twee willekeurige variabelen kan vergelijken, zelfs als de afwijkingen niet vergelijkbaar zijn. In de praktijk is de fout onbekend en wordt deze geschat met behulp van eindige monstercorrectie.

   In het vorige voorbeeld, tabel 1, wordt de PR, met een eindige monstercorrectie voor land i en periode 2, gegeven door

   ![](assets/persons-residual.png)

   Hier,

   ![](assets/pr-example.png)

   (Een vergelijkbare formule kan worden verkregen voor tijdsperiode 1.)

   Voor eindresultaten wordt de score voor elk afmetingsitem vervolgens gewogen aan de hand van de V-maat van Cramer en opnieuw geschaald naar een getal tussen 0 en 1 om de bijdragescore te leveren.

