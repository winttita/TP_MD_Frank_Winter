# TP_MD_Frank_Winter

Trabajos Prácticos de **Minería de Datos** (TUIA, UNR — 2026).

**Integrantes:** Maximiliano Frank y Federico Winter

---

## TP1 — Reducción de dimensionalidad y clustering (Palmer Penguins) ✅

**Estado: completo**

Dataset: [`penguins_size.csv`](TP1/Data/penguins_size.csv) — variable objetivo: `Especie` (Adelie, Chinstrap, Gentoo).

Enunciado: [`TP1/Docs/TP1.pdf`](TP1/Docs/TP1.pdf) · Notebook: [`TP1/TP1_MD_Frank_Winter.ipynb`](TP1/TP1_MD_Frank_Winter.ipynb)

| Punto | Contenido |
|---|---|
| 1 | Análisis exploratorio, limpieza, codificación y estandarización |
| 2 | PCA (varianza acumulada, criterio de Kaiser, gráfico del codo) |
| 3 | Isomap (variando `n_neighbors` y `n_components`) |
| 4 | t-SNE (variando iteraciones, componentes y perplejidad) |
| 5 | K-means (número óptimo con GAP y Silhouette, gráfico 3D por cluster) |
| 6 | Clustering jerárquico (Ward, número óptimo con GAP y Silhouette) |
| — | Conclusiones generales |

---

## TP2 — Árboles de decisión, Naive Bayes y k-NN 🔲

**Estado: pendiente**

Enunciado: [`TP2/TP2.pdf`](TP2/TP2.pdf)

**Parte A — Regresión** (dataset [`1000_Companies.csv`](TP2/1000_Companies.csv), variable objetivo: `Profit`)
- [ ] Preparación de datos (EDA, limpieza, codificación, normalización, splits 80/20 y 70/30, `random_state=63`)
- [ ] Árboles de decisión para regresión (`DecisionTreeRegressor`), tuning de `max_depth`, `min_samples_leaf`, `min_samples_split`
- [ ] Métricas: MAE, MSE, RMSE sobre ambos splits

**Parte B — Clasificación** (dataset [`drugType.csv`](TP2/drugType.csv), variable objetivo: `Droga`)
- [ ] Preparación de datos (EDA, balance de clases, splits estratificados 80/20 y 70/30, `random_state=63`)
- [ ] Árboles de decisión para clasificación (`DecisionTreeClassifier`), tuning + post-poda (`ccp_alpha`)
- [ ] Naive Bayes (discretización equal-frequency + `CategoricalNB`/`MultinomialNB`, o `GaussianNB`)
- [ ] k-NN (`KNeighborsClassifier`), tuning de `n_neighbors` y `metric`
- [ ] Tabla comparativa de los tres modelos de clasificación + selección justificada

---

## TP3 — SVM y Random Forest (recomendación de cultivos) 🔲

**Estado: pendiente**

Dataset: [`dxCropRecommendation.csv`](TP3/dxCropRecommendation.csv) — variable objetivo: `Cultivo` (12 clases). Enunciado: [`TP3/TP3.pdf`](TP3/TP3.pdf)

- [ ] Preparación de datos (EDA, nulos, duplicados, outliers, `StandardScaler`, `LabelEncoder`, `random_state=13`)
- [ ] SVM kernel lineal (`SVC(kernel='linear')`), tuning de `C`, validación cruzada estratificada k=5
- [ ] SVM kernel RBF (`SVC(kernel='rbf')`), tuning de `C` y `gamma`, tabla o heatmap de resultados
- [ ] Random Forest (`RandomForestClassifier`), tuning de `n_estimators` y `max_depth`, `feature_importances_`
- [ ] Tabla comparativa de los tres modelos + matrices de confusión + selección justificada

---

## Estructura del repositorio

```
TP_MD_Frank_Winter/
├── TP1/
│   ├── Data/                          # penguins_size.csv
│   ├── Docs/                          # enunciado (TP1.pdf)
│   └── TP1_MD_Frank_Winter.ipynb
├── TP2/
│   ├── 1000_Companies.csv
│   ├── drugType.csv
│   └── TP2.pdf
└── TP3/
    ├── dxCropRecommendation.csv
    └── TP3.pdf
```

## Notas generales de formato (todos los TPs)

- Informe en formato `.ipynb`, con cabecera de año, materia e integrantes, y sección de conclusiones al final.
- Sin definiciones teóricas ni explicación de parámetros en el informe — foco en resultados e interpretación.
- Gráficas acotadas y representativas, cada una con su interpretación y contraste con la hipótesis previa.
