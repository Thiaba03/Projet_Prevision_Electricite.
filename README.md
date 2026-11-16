# Projet_Prevision_Electricite.
# ⚡ Analyse et prévision de la consommation électrique en France

Projet data réalisé avec Python et Jupyter à partir des données **éCO2mix** publiées par RTE (Réseau de transport d'électricité).

**Objectif :** explorer la consommation électrique française, comprendre ses grandes tendances (saisonnalité, mix énergétique, émissions de CO₂), puis construire un modèle de prévision.

> 🚧 **Projet en cours.** Pour l'instant, seule la phase de mise en place de l'environnement est terminée.

---

## 📊 Les données

| Élément | Détail |
|---|---|
| Source | RTE, jeu de données éCO2mix national (données consolidées et définitives) |
| Fichier | `eco2mix-national-cons-def.csv` |
| Période | du 01/01/2012 au 31/08/2026 |
| Taille | environ 514 000 lignes, 37 colonnes, environ 86 Mo |
| Format | séparateur `;`, encodage UTF-8 avec BOM |

**Principales variables :**

- consommation, prévision J-1 et prévision J (MW) ;
- production par filière : nucléaire, éolien, solaire, hydraulique, gaz, fioul, charbon, bioénergies ;
- échanges physiques et commerciaux avec les pays voisins ;
- taux de CO₂ (g/kWh).

**Points d'attention repérés :**

- la consommation n'est renseignée qu'une ligne sur deux (pas de 30 minutes sur des données au pas de 15 minutes) ;
- les colonnes de détail par sous-filière sont vides à environ 53 % ;
- deux colonnes contiennent des types mixtes et devront être converties en numérique.

> Le fichier CSV **n'est pas versionné** dans ce dépôt (trop volumineux). Il est exclu par le `.gitignore`. Télécharge-le depuis le site Open Data de RTE (éCO2mix) et place-le dans le dossier du projet ou dans `data/`.

---

## 🗂️ Structure du dépôt

```
.
├── analyse_exploratoire.ipynb   # notebook d'exploration des données
├── .gitignore                   # exclut .venv, les CSV et les fichiers temporaires
└── README.md
```

Structure cible prévue pour la suite :

```
Projet_Prevision_Electricite/
├── data/          # données brutes (non versionnées)
├── notebooks/     # analyses Jupyter
└── outputs/       # graphiques et résultats
```

---

## 🛠️ Installation

**Prérequis :** Python 3.9 ou plus récent.

```bash
# 1. Cloner le dépôt
git clone https://github.com/Thiaba03/Projet_Prevision_Electricite.git
cd Projet_Prevision_Electricite

# 2. Créer et activer un environnement virtuel
python3 -m venv .venv
source .venv/bin/activate

# 3. Installer les bibliothèques
pip install pandas numpy matplotlib seaborn jupyter

# 4. Lancer Jupyter
jupyter notebook
```

**Bibliothèques utilisées :**

- `pandas` : manipulation des tableaux de données
- `numpy` : calcul numérique
- `matplotlib` et `seaborn` : visualisation

---

## ✅ Avancement

**Fait**

- [x] Mise en place de l'environnement Python (`.venv`)
- [x] Installation et test de pandas, numpy, matplotlib et seaborn
- [x] Localisation du fichier de données
- [x] Initialisation du dépôt Git et du `.gitignore`

**À venir**

- [ ] Chargement du CSV avec pandas
- [ ] Nettoyage des données (dates, types, valeurs manquantes)
- [ ] Analyse exploratoire : évolution de la consommation, saisonnalité, mix énergétique, CO₂
- [ ] Visualisations
- [ ] Modèle de prévision de la consommation
- [ ] Évaluation du modèle et conclusions

---

## 👤 Auteure

**Thiaba** : étudiante en master data .
