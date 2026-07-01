# Zadanie obowiązkowe [0-10] pkt

1. [0-1.5 pkt] Porównaj wyniki k-means z k-medoids, testując przynajmniej trzy różne metryki (użyj [tego API](https://scikit-learn-extra.readthedocs.io/en/stable/generated/sklearn_extra.cluster.KMedoids.html)). Jako miar porównania metod, użyj [ARI](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.adjusted_rand_score.html) oraz [Silhouette](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.silhouette_score.html) (dotyczy to też punktów niżej). Wyrysuj klastry i omów wyniki.
1. [0-2 pkt] Użyj DSBSCAN i wyrysuj klastry dla różnych kombinacji wartości `eps`, `min_samples` i `metric`. Porównaj wyniki z metodami wyżej.
2. [0-2 pkt] Użyj HDBSCAN, testując różne kombinacje parametrów. Czy wyniki różnią się od DBSCAN?
3. [0-2.5 pkt] Uzyj [klastrowania aglomeracyjnego](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.AgglomerativeClustering.html). Dla każdej wartości parametru `linkage`, wyrysuj [dendrogram](https://scikit-learn.org/stable/auto_examples/cluster/plot_agglomerative_dendrogram.html). Na podstawie dendrogramów, dobierz, w Twojej ocenie, optymalne parametry `n_clusters` albo `distance_threshold` (chodzi o określenie, czy w dendrogramie, na pewnym poziomie odcięcia, widać ewidentne klastry). Wyrysuj klastry i skomentuj wyniki.  
1. [0-1 pkt] Sprawdź wyniki poszczególnych metod klastrowania bez skalowania cech. Zinterpretuj wyniki.
1. [0-1 pkt] Który z algorytmów działa najlepiej dla tego problemu? Skomentuj wyniki.

# Zadanie dodatkowe [0-10] pkt

1. [0-7 pkt] Wytrenuj sieć konwolucyjną (CNN) na macierzach podobieństwa, przewidując klasy CATH (problem klasyfikacji). Pamiętaj o ewaluacji na zbiorze walidacyjnym.
2. [0-1 pkt] Uruchom wytrenowany model na wszystkich białkach. Użyj wag z ostatniej warstwy jako wektora cech.
3. [0-1 pkt] Dokonaj redukcji wymiarowości wektora cech do dwóch wymiarów np. za pomocą PCA.
4. [0-1 pkt] Czy tak skonstruowane cechy korelują z klasą białek?
