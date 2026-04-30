# Zadanie obowiązkowe [0-10] pkt

1. [0-1 pkt] Zaproponuj EDA po skalowaniu cech (tj. analiza macierzy zliczeń)
2. [0-2 pkt] Dostosuj parametry wektoryzacji (np. `ngram_range`, `min_df`, `max_df`) na podstawie analizy wyżej. Zrób wyszukiwanie po parametrach, używając `ROCAUC` jako miary (zob. [roc_auc_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.roc_auc_score.html))
3. [0-1 pkt] Porównaj wyniki z rozkładem Bernoulliego. Zidentyfikuj przykłady, dla których każdy z modeli działa lepiej
4. [0-1.5 pkt] Użyj transformacji [TF-IDF](https://scikit-learn.org/stable/modules/generated/sklearn.feature_extraction.text.TfidfTransformer.html) zaraz po wektoryzacji dla rozkładu wielomianowego i Gaussowskiego. W tym celu użyj funkcjonalności `Pipeline`
   - W przypadku rozkładu Gaussowskiego wymagane będzie użycia transformatora postaci gęstej macierzy (patrz kod niżej)
   - Skomentuj, dlaczego model z rozkładem Gaussa działa gorzej
5. [0-1.5 pkt] Wytrenuj [regresję logistyczną](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html), robiąc przeszukanie po hiperparametrach
6. [0-1 pkt] Porównaj krzywe kalibracyjne (użyj tego [API](https://scikit-learn.org/stable/modules/calibration.html)) dla obu modeli. Skomentuj wyniki
7. [0-2 pkt] Spróbuj znaleźć dwa reprezentatywne n-gramy, które najlepiej separują klasy. Wyrysuj obszary decyzyjne dla obu klasyfikatorów

```python
from sklearn.base import TransformerMixin, BaseEstimator

class DenseTransformer(TransformerMixin, BaseEstimator):
    def fit(self, X, y=None):
        return self
    def transform(self, X, y=None):
        return X.toarray()
```

# Zadanie dodatkowe [0-4] pkt

1. [0-3 pkt] Zaimplementuj [elastyczny naiwny klasyfikator Bayesa](https://arxiv.org/pdf/1302.4964) tj. NBC, w którym wiarygodność p(x_i | y_k) jest modelowana osobno dla każdej klasy k na podstawie [KDE](https://en.wikipedia.org/wiki/Kernel_density_estimation) dla wszystkich punktów treningowych (i = 1…n)
2. [0-1 pkt] Porównaj wyniki uzyskane za pomocą Gaussowskiego KDE dla różnych wartości parametru wygładzania (h, *smoothing*, *bandwidth*) z "globalnym" klasyfikatorem z rozkładem Gaussa (patrz zadanie obowiązkowe)
