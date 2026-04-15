# Zadanie obowiązkowe [0-10] pkt

Użyj zbioru danych [Yeast](https://archive.ics.uci.edu/dataset/110/yeast) i powtórz kroki z ćwiczeń.

1. [0-2 pkt] Używając [GridSearchCV](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html), dokonaj przeszukania przestrzeni hiperparametrów kNN, zmieniając (uargumentuj wybór zakresów):
   1. liczbę sąsiadów
   1. wagę dla sąsiadów
   1. metrykę
1. [0-1.5 pkt] Do wyszukiwania dodaj miary skuteczności m.in. dokładność (*accuracy*) precyzję (*precision*), czułość (*recall*, *sensitivity*), czy też współczynnik korelacji Matthewsa (MCC). Gdzie to możliwe, dostosuj opcje miar, żeby uwzględniały niezbalansowanie zbioru
1. [0-0.5 pkt] Skomentuj wyniki uzyskane w punktach 1 i 2. Spróbuj zinterpretować wyniki
1. [0-2 pkt] Dokonaj selekcji cech, używając [SequentialFeatureSelector](https://scikit-learn.org/stable/modules/generated/sklearn.feature_selection.SequentialFeatureSelector.html). Zmieniaj parametr `n_features_to_select` od dwóch do pięciu. Ile cech uzyskujemy przy opcji `auto`?
1. [0-0.5 pkt] Używając [Pipeline](https://scikit-learn.org/stable/modules/generated/sklearn.pipeline.Pipeline.html), sprawdź wpływ skalowania / normalizacji na wyniki (użyj m.in. `MinMaxScaler` oraz `RobustScaler`)
1. [0-1 pkt] Skomentuj wyniki uzyskane w punktach 4 i 5
1. [0-1.5 pkt] Dla najlepszej pary `n_features_to_select=2` wyrysuj obszary decyzyjne. Skomentuj wyniki
2. [0-1 pkt] Czy w świetle uzyskanych wyników, kNN jest odpowiednim klasyfikatorem do tego problemu? Uzasadnij odpowiedź
