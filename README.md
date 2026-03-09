# Analyse-du-March-Immobilier-Fran-ais
# 🏠 Analyse du Marché Immobilier Français (S1 2020)

## 📋 Présentation du Projet
Ce projet consiste en une analyse exploratoire de données (EDA) sur les transactions immobilières en France au cours du premier semestre 2020. L'objectif est d'extraire des indicateurs clés (KPI) pour comprendre les dynamiques de prix, les volumes de ventes et les disparités régionales.

Le projet utilise quatre sources de données (fichiers CSV) :
- `BienImmobilier.csv` : Détails des transactions.
- `CodeCommune.csv` : Référentiel géographique.
- `CodeTypeBien.csv` : Typologie des biens (Maison, Appartement).
- `CodeTypeVoie.csv` : Nomenclature des voies.

## 🛠️ Stack Technique
- **Langage :** Python 3.x
- **Bibliothèques :** - `Pandas` : Manipulation et nettoyage des données.
  - `Matplotlib` & `Seaborn` : Visualisation de données.
  - `Datetime` : Gestion des séries temporelles.

## 🧹 Nettoyage et Préparation des Données (Data Wrangling)
Une attention particulière a été portée à la qualité des données :
- **Gestion des valeurs manquantes :** Correction manuelle de la commune d'Ajaccio et traitement des IDs de voies inconnus.
- **Filtrage des données :** Exclusion des valeurs aberrantes (biens < 5m² ou < 1000€) pour éviter de fausser les moyennes.
- **Feature Engineering :** Création d'une colonne `surface_utile` (mixant Loi Carrez et Surface réelle) et calcul du `prix_m2`.
- **Conversion de types :** Transformation des colonnes `date_vente` en objets datetime pour l'analyse temporelle.

## 📊 Indicateurs Analysés (Requêtes)
Le notebook répond à 9 problématiques stratégiques, notamment :
1. Volume des ventes d'appartements au S1.
2. Répartition du marché par nombre de pièces.
3. Classement des 10 départements les plus chers.
4. Analyse spécifique du prix moyen en Île-de-France.
5. Évolution des ventes entre le 1er et le 2ème trimestre 2020.
6. Identification des communes en forte croissance (>20%).



## 📈 Visualisations clés
Le projet inclut plusieurs graphiques pour faciliter la lecture des résultats :
- le Top 10 des départements les plus chers (€/m²).
  <img width="1106" height="672" alt="image" src="https://github.com/user-attachments/assets/cce3b64b-f541-415d-ac21-93f25e8ec289" />

- Nombre de ventes par Trimestre (2020).
  <img width="902" height="578" alt="image" src="https://github.com/user-attachments/assets/c144f100-087a-4a7a-86d1-120a99aa972a" />

- la dispersion des prix par type de bien.
<img width="1093" height="643" alt="image" src="https://github.com/user-attachments/assets/236b0514-389a-479f-8419-909bc58dc008" />

