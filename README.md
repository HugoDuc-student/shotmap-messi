# ⚽ Shot map xG — Lionel Messi, Liga 2011/2012

![Shot map](figures/messi_shotmap_2011_12_v3.png)

## 🎯 Objectif
Visualiser tous les tirs de Lionel Messi lors de sa saison record en Liga (2011/2012)
et comparer ses buts réels à ses buts attendus (xG).

## 📊 Résultats clés
| Tirs | Buts | xG | Buts − xG |
|---|---|---|---|
| 198 | 50 | 35.7 | +14.3 |

Messi a marqué **XX buts de plus** que ce que la qualité de ses occasions laissait prévoir :
une surperformance exceptionnelle, qui se maintient hors penaltys (npxG : XX).

## 🛠️ Méthode
1. Extraction des événements des 37 matchs via l'API StatsBomb Open Data (`statsbombpy`)
2. Filtrage des tirs de Messi et contrôle qualité (buts retrouvés vs total officiel)
3. Visualisation avec `mplsoccer` : couleur et taille = xG, contour blanc = but,
   densité KDE des zones de tir (hors penaltys)

## 📁 Structure
- `notebooks/02_extraction_tirs.ipynb` : extraction et nettoyage des données
- `notebooks/03_shotmap.ipynb` : visualisations
- `data/` : tirs extraits (CSV)
- `figures/` : figures exportées

## ▶️ Reproduire
    python -m venv .venv
    source .venv/bin/activate
    pip install -r requirements.txt

## 📚 Source
Données : [StatsBomb Open Data](https://github.com/statsbomb/open-data)

---
**Hugo Duchemin** — Data & sciences du sport