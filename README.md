Schema
======
```
Strandkorb
+ Farbe Korb
+ Farbe Bezug

Strand
* Strandkorb[]
* Preis[]

Preis
* Strand
* Saison
+ Wert

Saison
* Preis[]
+ Begin
+ Ende

Mieter
* Vermietung[]
+ Kontodaten


Vermietung
* Strandkorb
* Mieter
+ Kalenderwoche
+ Jahr

=== Legende
Model
* Referenz
+ Attribut
```

Lösungen
========
Was müssen Sie an Ihrem Modell ändern, um Strandkörbe tagsüber wie üblich und nachts als kostengünstige Übernachtungsmöglichkeit zu vermieten?
---------------------------------------------------------------------------------------------------------------------------------------------- 

Vermietungen müssten dann tagesgenau angegeben werden, da Übernachtungen am Vorabend für eine Nacht bezahlt werden und nicht mehr für eine Woche vom Konto eingezogen werden. Gleichzeitig hätte eine Vermietung  dann einen Tages- und einen Nachtmieter. Der Preis würde dann zusätzlich noch von Tag oder Nacht abhängen.
