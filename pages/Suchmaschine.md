- Take 1
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
-
- Take 2
  collapsed:: true
	- Trying out Query in org mode
		- Try to include a standout-block using org mdoe in write down editor
-
- Take 3
	- ==Test query==
	- {{query (and (property materialkomplexität [[W5_Kombination von unterschiedlichen Materialien , Hart-Weich Kombination]]) (property konstruktive-freiheiten [[W4_Materialkomplexität]]) )}}
	  query-table:: false
	-
	  Genutzte_Freiheiten_der_AM:: [[W3_Konstruktive Freiheiten]]
	  Konstruktive_Freiheiten:: [[W4_Materialkomplexität]] [[W4_Formkomplexität]] 
	  Materialkomplexität:: [[W5_Kombination von unterschiedlichen Materialien , Hart-Weich Kombination]]
	  Formkomplexität::  Gedruckte Gewinde
	  trl:: [[TL3]]
	-
	  Genutzte_Freiheiten_der_AM:: [[W3_Konstruktive Freiheiten]]
	  Konstruktive_Freiheiten:: [[W4_Materialkomplexität]] [[W4_Formkomplexität]] 
	  Materialkomplexität:: [[W5_Kombination von unterschiedlichen Materialien , Hart-Weich Kombination]]
	  Formkomplexität:: Festkörpergelenke
	  TRL:: [[TL5]]
	-
	-
	- {{query (and (property materialkomplexität [[W5_Kombination von unterschiedlichen Materialien , Hart-Weich Kombination]]) (property trl [[TL5]]) (property konstruktive-freiheiten [[W4_Materialkomplexität]]) )}}