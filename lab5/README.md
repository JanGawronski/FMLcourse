# Zadanie obowiązkowe [0-10] pkt

1. [0-0.5 pkt] Użyj zbalansowania klas w regresji logistycznej (parametr `class_weight`). Porównaj z modelem podstawowym.
2. [0-1 pkt] Porównaj różne techniki podpróbkownia (*undersampling*). W szczególności (weź pod uwagę hiperparametry każdego podejścia!):
   1. Podpróbkowanie losowe
   2. [Cluster Centroids](https://imbalanced-learn.org/stable/references/generated/imblearn.under_sampling.ClusterCentroids.html#clustercentroids)
   3. *Edited Nearest Neighbours* (patrz ćwiczenia)
3. [0-2 pkt] Porównaj różne techniki nadpróbkowania (*oversampling*). W szczególności (weź pod uwagę hiperparametry każdego podejścia!):
   1. Nadpróbkowanie losowe
   2. [SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.SMOTE.html)
   3. [Borderline SMOTE](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.BorderlineSMOTE.html#)
   4. [ADASYN](https://imbalanced-learn.org/stable/references/generated/imblearn.over_sampling.ADASYN.html)
4. [0-1 pkt] Przeprowadź dostrajanie progu (*threshold tuning*) tj. użyj innych progów odcięcia klasy pozytywnej w regresji logistycznej. Możesz wykorzystać np. metody opisane [tutaj](https://scikit-learn.org/stable/modules/classification_threshold.html). Optymalizuj względem AUPRC.
5. [0-1 pkt] Użyj przynajmniej jednego innego klasyfikatora poznanego na zajęciach i porównaj jego wyniki z regresją logistyczną.
6. [0-1.5 pkt] Zaimplementuj fokalną funkcję kosztu (*focal loss*) w `scikit-learn`. W tym celu, wyjątkowo, **możesz skorzystać z narzędzi generatywnej sztucznej inteligencji**.
7. [0-2 pkt] Sporządź analizę porównawczą technik / modeli wyżej, uwzględniając podejścia podstawowe (*baseline*). Zwizualizuj krzywe ROC i PRC.
8. [0-1 pkt] Skomentuj uzyskane wyniki.

## Środowisko (uv + systemowy Jupyter)

W katalogu `lab5`:

```bash
uv venv .venv
uv pip install --python .venv/bin/python numpy pandas matplotlib seaborn scikit-learn imbalanced-learn scipy ipykernel ucimlrepo
.venv/bin/python -m ipykernel install --user --name fml-lab5 --display-name "Python (fml-lab5)"
```

Następnie uruchom systemowy Jupyter:

```bash
jupyter notebook
```

I wybierz kernel **Python (fml-lab5)** dla `homework.ipynb`.
