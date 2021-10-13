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
-
-
-
-
-
-