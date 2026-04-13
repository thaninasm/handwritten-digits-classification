# 🧠 Handwritten Digits Classification — Deep Learning

<div align="center">

![Python](https://img.shields.io/badge/Python-3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Status](https://img.shields.io/badge/Accuracy-91.6%25-27ae60?style=for-the-badge)

**Classification de chiffres manuscrits avec un réseau de neurones MLP**

*Introduction pratique au Deep Learning · EMLV MSID · 2025-26*

</div>

---

## 🎯 Objectif

Créer, entraîner et évaluer un **réseau de neurones** capable de reconnaître des chiffres manuscrits (0 à 9) à partir d'images 8x8 pixels — et atteindre une précision comparable à celle d'un humain.

---

## 🗂️ Dataset — Handwritten Digits (scikit-learn)

| Propriété | Valeur |
|---|---|
| Source | `sklearn.datasets.load_digits()` |
| Nombre d'images | 1 797 |
| Résolution | 8 × 8 pixels (64 features) |
| Classes | 10 (chiffres 0 → 9) |
| Split Train / Test | 1 000 / 797 |

---

## 🏗️ Architecture du réseau

```
Couche d'entrée   →   64 neurones  (1 par pixel)
Couche cachée     →   15 neurones  (activation sigmoïde)
Couche de sortie  →   10 neurones  (1 par classe 0-9)
```

Réseau **dense** (fully connected) — chaque neurone connecté à tous ceux de la couche suivante.

---

## ⚙️ Paramètres du modèle

| Paramètre | Valeur | Rôle |
|---|---|---|
| `hidden_layer_sizes` | `(15,)` | Architecture : 1 couche cachée, 15 neurones |
| `activation` | `logistic` | Fonction sigmoïde → sortie en [0,1] |
| `solver` | `sgd` | Descente de gradient stochastique |
| `alpha` | `1e-4` | Régularisation L2 (anti-overfitting) |
| `learning_rate_init` | `0.1` | Taille des pas d'optimisation |
| `tol` | `1e-4` | Seuil d'arrêt de l'entraînement |

---

## 📈 Résultat

> **Accuracy : 91.6%** sur les données de test (jamais vues pendant l'entraînement)

Dans 91.6% des cas, le réseau identifie correctement le chiffre manuscrit.

---

## 🧪 Contenu du notebook

1. **Chargement & exploration** des données — visualisation des images et étiquettes
2. **Préparation** — reshape des images 8×8 en vecteurs de 64 valeurs
3. **Split Train/Test** — 1000 images d'entraînement, 797 de test
4. **Création & entraînement** du réseau MLP avec scikit-learn
5. **Prédiction** sur les données de test
6. **Évaluation** — accuracy score à 91.6%

---

## 🚀 Lancement

```bash
# Cloner le repo
git clone https://github.com/thaninaflow/handwritten-digits-classification

# Installer les dépendances
pip install scikit-learn matplotlib numpy

# Lancer le script
python handwritten_digits_sklearn_fr.py
```

---

## 📁 Structure

```
handwritten-digits-classification/
│
├── 🐍 handwritten_digits_sklearn_fr.py   # Script principal
└── 📄 README.md
```

---

## 👤 Auteur

<div align="center">

**Thanina** · [@thaninaflow](https://github.com/thaninaflow)

*Étudiante en Data & IA · EMLV MSID · Passionnée de Machine Learning*

</div>
