# 📊 Analyse de ma recherche d’emploi en Data

## 🚀 Contexte
Après ma formation intensive en **Data Science et Data Engineering (Jedha Bootcamp)**, je me lance dans la recherche de mon premier poste en Data.  
Plutôt que de simplement suivre mes candidatures dans un tableau, j’ai choisi d’en faire un **projet analytique** :  
👉 traiter mes candidatures comme un dataset  
👉 les enrichir avec un modèle de langage (LLM)  
👉 en tirer des visualisations (radars, distributions, tendances).  

L’objectif :  
- Prendre du recul sur mon parcours de recherche,  
- Mettre en avant mes compétences,  
- Partager mes insights 

---

## 🗂 Données
- **Source principale** : export de mon suivi de candidatures (CSV Notion).  
- **Colonnes clés** :  
  - `Entreprise`  
  - `Poste`  
  - `Catégorie Poste (LLM)` (classification via regex + LLM)  
  - `État` (sans réponse, entretien, refus, etc.)  
  - `Compétences (LLM)` (extraites depuis les offres via scraping + LLM).  

---

## ⚙️ Pipeline (Notebook)
1. **Préparation & nettoyage**  
   - Uniformisation du CSV (séparateur, encodage, suppression des caractères spéciaux).  
   - Classification des postes (`Data Analyst`, `Data Scientist`, `Data Engineer`, `Consultant Data`, `Autres`).  

2. **Enrichissement via LLM**  
   - Extraction des compétences clés à partir des descriptions d’offres.  
   - Transformation en format binaire (`1` si présent, `0` sinon).  

3. **Analyses & Visualisations**  
   - 📈 **Distribution temporelle** des candidatures  
   - 📊 **Répartition des postes** par catégorie  
   - 🟦 **Répartition des états** (réponses, sans réponses, etc.)  
   - 🕸 **Radar chart** :  
     - Compétences du marché vs. mon profil  
     - Par catégorie de poste (Data Analyst, Data Scientist, etc.)  

---

## 📊 Résultats clés
- Nombre de candidatures envoyées : **281**  
- Catégorie la plus visée : **Data Analyst**  
- Taux de réponses reçues : **37%** (à compléter)  
- Matching compétences : bonne couverture en **Python, SQL, Machine Learning** mais lacunes sur **Cloud & Big Data** (axe d’amélioration).  

---

## 🛠️ Stack technique
- **Python** : Pandas, Seaborn, Matplotlib  
- **LLM** : Mistral API via LangChain (classification & extraction)  
- **Visualisation** : Radar charts custom + exports images  
- **Outils alternatifs** : Tableau Public, Metabase  

---

## 🔮 Améliorations possibles
- Enrichir la base avec des infos issues de **scraping avancé** (LinkedIn, Indeed, WTTJ).  
- Industrialiser le pipeline (ETL automatisé avec Airflow).  
- Déployer un **dashboard dynamique** (Streamlit ou Metabase).  

---

## 🙌 Remerciements 
Un coup de pouce particulier à **ChatGPT** pour m’avoir aidé à structurer et corriger ces notebook !  
