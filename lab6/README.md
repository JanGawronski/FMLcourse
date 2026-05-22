# Zadanie obowiązkowe [0-10] pkt

- Zapoznaj się z analizą zbioru [twarzy OLivetti](https://scikit-learn.org/stable/auto_examples/decomposition/plot_faces_decomposition.html)
- Zapoznaj się z ze zbiorem [klasyfikacji cyfr](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_digits.html)

1. [0-1 pkt] Załaduj zbiór cyfr, a następnie wyświetl pierwsze 6 (2 wiersze, 3 kolumny) elementów zbioru za pomocą funkcji `plot_gallery()` (zob. pierwszy link)
1. [0-0.5 pkt] Podziel zbiór na treningowy i walidacyjny (czy zbiór jest zbalansowany i wystarczy zwykły podział losowy?). Pamiętaj, że skalowanie cech jak i dostrojenie redukcji wymiarowości (metoda `fit`) przeprowadzamy na zbiorze treningowym!
1. [0-2.5 pkt] Dokonaj transformacji zbioru `digits` przy użyciu (w każdym przypadku wyrysuj kilka przykładowych elementów zbioru):
   1. PCA
   2. [NMF](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.NMF.html) (jaki będzie input?)
   3. [Factor Analysis](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.FactorAnalysis.html)
   4. [Jądrowy PCA](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.KernelPCA.html) (przy użyciu przynajmniej trzech nieliniowych jąder)
1. [0-1.5 pkt] Wytrenuj regresję logistyczną na zbiorze oryginalnym (model *baseline*) oraz przetransformowanym za pomocą technik z punktu 3.
1. [0-1.5 pkt] Sporządź analizę porównawczą wyników zarówno dla zbioru treningowego jak i walidacyjnego. Wyrysuj macierz pomyłek oraz metryki zbiorcze.
1. [0-1 pkt] Wybierz $n=32, 16, 8, 4, 2$ dominujące cechy w każdej metodzie i wykonaj analizę w pkt. 5.
1. [0-1 pkt] Skomentuj uzyskane wyniki. Czy redukcja wymiarowości jest optymalnym rozwiązaniem w przypadku tego zbioru? Jeśli tak, to która? Jeśli żadna, to dlaczego?
1. [0-1 pkt] Zaproponuj usprawnienie metodologii wyżej (np. inną technikę selekcji cech).

# Zadanie dodatkowe [0-4] pkt

1. [0-3 pkt] Dokonaj redukcji wymiarowości za pomocą trzech wybranych metod nieliniowych ze zbioru: t-SNE, UMAP, TriMAP, PaCMAP, a następnie użyj tak przetransformowanego zbioru w naszym problemie klasyfikacji cyfr.
1. [0-1 pkt] Czy użycie tych zaawansowanych technik ma sens w tym przypadku?
