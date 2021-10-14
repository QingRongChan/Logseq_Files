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
- {{query  (property tl TL4) (property form 3D)}}
  query-table:: false
- query-table:: false
  | [[Teilfunktionen]] | [[Form]] | [[Lastfall]] | [[Dummy_Kriterium1]] | [[Dummy_kriterium2]] | [[Wirkprinzipien]] |
  |--------|-------|---|---|---|---|
  | #Teilfunktion_1 | #2D | #>50N| #DK1_1| #DK2_2 | {{query  (property tl TL4) (property form 3D)}} |
  | #Teilfunktion_2 | #3D | #>70N | #DK1_2 | #DK2_3 | t |
-
-
-
-
-
-
-