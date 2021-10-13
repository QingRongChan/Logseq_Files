- Test Kraft <100N und 2D
	- query-table:: false
	  #+BEGIN_QUERY
	  {:title ""
	   :query [:find (pull ?b [*])
	           :where [?b :block/marker ?marker]
	          	      [(contains? #{"2D" "<100N"} ?marker)]]
	   :breadcrumb-show? false
	   :result-transform (fn [result] (reverse (sort-by (fn [h]) result)))
	   :collapsed? false}
	  #+END_QUERY
- Test Kraft <100N und 3D
	- #+BEGIN_QUERY
	  {:title ""
	   :query [:find (pull ?b [*])
	           :where [?b :block/marker ?marker]
	          	      [(contains? #{"3D" "<100N"} ?marker)]]
	   :breadcrumb-show? false
	   :result-transform (fn [result] (reverse (sort-by (fn [h]) result)))
	   :collapsed? false}
	  #+END_QUERY
- [[Teilfunktion 1]]
- [[Teilfunktion 2]]
- [[Form]]
- [[Lastfall]]
- [[Wirkprinzipien]]
-