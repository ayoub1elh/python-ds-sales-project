# Projet d'Analyse des Ventes avec Python

## Description
Ce projet utilise Python et diverses bibliothèques d'analyse de données pour étudier un jeu de données de ventes, calculer des indicateurs clés de performance (KPI) et créer des visualisations pertinentes pour les décideurs.

## Structure du Projet
Le projet est organisé en plusieurs notebooks Jupyter qui traitent différents aspects de l'analyse :

- **[python_f4ds.ipynb](python_f4ds.ipynb)** - Chargement et nettoyage des données initiales
- **[Calcul_KPI.ipynb](Calcul_KPI.ipynb)** - Calcul des indicateurs clés de performance (KPI)
- **[Visualisation.ipynb](Visualisation.ipynb)** - Création de visualisations diverses pour l'analyse
- **[Afficher_principales_villes.ipynb](Afficher_principales_villes.ipynb)** - Analyse détaillée des 5 principales villes/régions
- **[sales.xlsx](sales.xlsx)** - Fichier de données source
- **Projet_Python_DS_Rapport.docx.pdf** - Rapport détaillé du projet
- **Projet_Python_DS_Presentation.pptx** - Présentation PowerPoint du projet

## À propos des Données
Le fichier de données `sales.xlsx` contient des informations sur les commandes avec les colonnes suivantes :
- OrderNumber, OrderDate, Ship Date
- Customer Name Index
- Channel (Distributor, Export, Wholesale)
- Currency Code, Warehouse Code
- Delivery Region Index
- Product Description Index
- Order Quantity
- Unit Selling Price, Unit Cost

## Fonctionnalités Principales

### 1. Préparation des Données
- Chargement des données depuis le fichier Excel
- Création de colonnes calculées :
  ```python
  df["Sales"] = df["Order Quantity"] * df["Unit Selling Price"]
  df["Cost"] = df["Order Quantity"] * df["Unit Cost"]
  df["Profit"] = df["Sales"] - df["Cost"]
  ```
- Création d'une table de dates pour faciliter les analyses temporelles

### 2. Calcul des KPI
- Indicateurs globaux (ventes totales, profit, marge, etc.)
- Analyse Year-Over-Year (YOY) pour comparer avec l'année précédente
- Calcul des variations en valeur absolue et en pourcentage

### 3. Visualisations
- Ventes par mois avec comparaison année précédente
- Top 5 des régions/villes par ventes
- Comparaison des bénéfices par canal de vente
- Top 5 et derniers 5 clients par année
- Ventes par produit et par année

## Comment Utiliser ce Projet

1. Assurez-vous d'avoir installé les bibliothèques requises :
   ```bash
   pip install pandas numpy matplotlib seaborn
   ```

2. Exécutez les notebooks dans l'ordre suivant :
   - python_f4ds.ipynb (préparation des données)
   - Calcul_KPI.ipynb (calcul des indicateurs)
   - Visualisation.ipynb et Afficher_principales_villes.ipynb (visualisations)

3. Consultez le rapport et la présentation pour une analyse complète et des conclusions.

## Aperçu des Résultats

- Indicateurs globaux :
  - Total des ventes : 154,573,140.60
  - Profit total : 57,789,142.91
  - Marge bénéficiaire : 37.39%

- Les visualisations montrent les tendances des ventes par année, mois, canal de vente et région, permettant d'identifier les opportunités et les défis.

- Analyse comparative par année permettant de voir l'évolution des performances.

## Auteur et Contact

Projet réalisé par Ayoub el hallaoui
GitHub: [@Ayoub1elh](https://github.com/Ayoub1elh)

---
