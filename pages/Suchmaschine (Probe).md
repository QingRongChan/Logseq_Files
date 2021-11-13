Property::
tags:: #p.cards

- Take 1 =Basic Query== Status: ⭕
  collapsed:: true
	- Option 1-> Datomic
	  collapsed:: true
		- Noch in Testphase -> Datomic und Chanpony Query-Funktion
		  collapsed:: true
			- query-table:: true
			  query-sort-by:: block
			  query-sort-desc:: true
			  #+BEGIN_QUERY
			  {:title ""
			   :query [:find (pull ?b [*])
			           :where [?b :block/marker ?marker]
			          	      [(contains? #{"TODO"} ?marker)]]
			   :breadcrumb-show? false
			   :result-transform (fn [result] (reverse (sort-by (fn [h]) result)))
			   :collapsed? false}
			  #+END_QUERY
			-
			-
	- Option 2-> Standalone Query
		- Table structure
		  collapsed:: true
			- | W4 | W3 | W2 | W1 | 
			  |--------|-------|---|---|
			  | Materialkomplexität | Konstruktive Freiheiten | Genutzte AM-Freiheiten| Ausgleichsbewegung| 
			  | ... | TL4 | TRL |  |
		- Query  mit nur einer Stufe
			- {{query  (and [[W2_Technology Readiness Level]] [[TL5]])}}
			  query-table:: true
		- Query mit mehrere Stufen
		  collapsed:: true
			-
			-
			-
			-
	- Option 3-> Tabelle Query
	  collapsed:: true
		- query-table:: false
		  collapsed:: true
		  | [[Teilfunktionen]] | [[Form]] | [[Lastfall]] | [[Dummy_Kriterium1]] | [[Dummy_kriterium2]] | [[Wirkprinzipien]] |
		  |--------|-------|---|---|---|---|
		  | #Teilfunktion_1 | #2D | #>50N| #DK1_1| #DK2_2 | {{query  (property tl TL4) (property form 3D)}} |
		  | #Teilfunktion_2 | #3D | #>70N | #DK1_2 | #DK2_3 | t |
- Take 2 =Query in Org Mode== Status: ❌
  collapsed:: true
	- Trying out Query in org mode
		- Try to include a standout-block using org mdoe in write down editor
- Take 3 ==Test advance query== Status: ✅
  collapsed:: true
	- {{query (and (property konstruktive-freiheiten [[W4_Materialkomplexität]]) (property materialkomplexität [[W5_Kombination von unterschiedlichen Materialien , Hart-Weich Kombination]]) (property formkomplexität Gedruckte Gewinde) (property trl TL3) )}}
	  query-table:: false
	- {{query (and (property konstruktive-freiheiten W4_Materialkomplexität ) (property materialkomplexität W5_Material wird im linearelastischen Bereich deformiert) (property fertigungsverfahren FDM möglich) (property trl TL4) )}}
- Take 4 ==Query Regel== Status: ✅
  collapsed:: true
	- Derzeitige properties der jeweiligen Seite der Wirkprinzipien
		- genutzte-freiheiten-der-am
		- konstruktive-freiheiten
		- materialkomplexität
		- formkomplexität
		- trl
		- quelle
		- fertigungsverfahren
	- Format für Query-Funktion
		- starten mit dem Befehl "/query"
		- "{{query and( (property key value) (property key value) (property key value) (property key value) )}}"
	- Regel für die Eingabe in Query Funktion
		- Eingegebene Property's Schlüssel muss dem dargestellten Schlüssel entsprechen
		- Link zu einer Seite muss nicht als Link in Query Funktion eingegeben werden
		- Es gibt keine Grenze für die Anzahl der Property keys, die eingegeben werden können