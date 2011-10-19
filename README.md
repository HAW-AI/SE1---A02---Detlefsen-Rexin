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

Abwicklung der Vermietung
-------------------------

Für die Abwicklung einer Vermietung muss im Kern ein Vermietungsobject erzeugt werden, welches dann auf den Mieter und den Strandkorb verweist. Da der Strandkorb selbst über seine position (Strand) bescheid weiß, brauch diese nicht extra aufgeführt zu werden. Aus diesen Informationen, plus Kalenderwoche und Jahr, ergibt sich dann auch die Saison und muss daher nicht explizit ausgewählt werden. 

Einzug der Miete per Lastschrift vom Konto des Mieters
------------------------------------------------------



Erstellen von Übersichten über die vermieteten bzw. noch freien Strandkörbe für einen Tag pro Strand.
-------------------------------------------------------------------------------


Was müssen Sie an Ihrem Modell ändern, um Strandkörbe tagsüber wie üblich und nachts als kostengünstige Übernachtungsmöglichkeit zu vermieten?
----------------------------------------------------------------------------------------------------------------------------------------------

Vermietungen müssten dann tagesgenau angegeben werden, da Übernachtungen am Vorabend für eine Nacht bezahlt werden und nicht mehr für eine Woche vom Konto eingezogen werden. Gleichzeitig hätte eine Vermietung  dann einen Tages- und einen Nachtmieter. Der Preis würde dann zusätzlich noch von Tag oder Nacht abhängen.
