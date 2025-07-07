# 🥋🫎 MMAtchMaker

MMAtchMaker est le **premier générateur intelligent de combats de MMA** à destination des **managers** et **matchmakers**. Il vous aide à identifier l’adversaire le plus pertinent pour votre combattant, en équilibrant **challenge sportif** (pour l'audience et la réputation) et **opportunités de progression dans le classement**.

## 🔍 Objectif

Notre outil permet de :

- Trouver automatiquement le meilleur adversaire possible pour un combattant donné
- Analyser les critères clés de performance et de matchmaking
- Générer une **recommandation intelligente** via une interface simple et rapide

## 🧠 Comment ça marche ?

L’utilisateur entre :
- Le **nom du combattant**
- Le **lieu** du prochain combat (qui peut fortement influé sur la cote d'un combat, évidemment!)

MMAtchMaker analyse alors une base de données de plus de 4 000 combattants et sélectionne le meilleur match parmi les adversaires autorisés, en se basant sur les critères suivants :

| Critère                | Pondération | Détail                                                                 |
|------------------------|-------------|------------------------------------------------------------------------|
| Derniers résultats     | 5           | Score basé sur les 3 derniers combats                                 |
| Record professionnel   | 4           | Ratio victoires / total combats                                       |
| Taux de finition       | 4           | Pourcentage de victoires par KO ou soumission                         |
| Lieu du combat         | 3           | Avantage à domicile ou effet public                                   |
| Expérience             | 3           | Nombre total de combats + ancienneté du combattant                    |
| Dernier adversaire     | 3           | Analyse de la difficulté de l'adversaire précédent                    |
| Date du dernier combat| 3           | Plus c’est récent, mieux c’est                                        |

Chaque critère est noté sur 10, puis une note globale est attribuée pour chaque adversaire potentiel.

## 🛠️ Stack technique

- **Python** (traitement des données, moteur de recommandation)
- **Flask** (interface web)
- **Pandas / Numpy** (prétraitement et analyse)
- **HTML** (interface utilisateur)

## 🚀 Lancer le projet en local

### 1. Télécharger les fichiers

Clone le dépôt, assure toi que tu as bien :

```
/mmatchmaker
├── static/
│   └── conor_money.jpg
├── templates/
│   ├── index.html
│   └── message.html
├── prueba2.py
├── rankfeed.xlsx
```

### 2. Installer les dépendances

Dans un terminal ou console Python :

```bash
pip install flask pandas numpy openpyxl
```

### 3. Lancer le serveur

Dans ton environnement Python :

```bash
python prueba2.py
```

Une URL s’affichera (ex. `http://127.0.0.1:5000/`) : **copie-la et colle-la dans ton navigateur.**

## 💡 Exemples de test

- **Fighter**: Mario Bautista  
  **Location**: United States → Avantage local  
  **Location**: France → L’algorithme choisit un adversaire différent

Autres noms de combattants valides :  
`Alexander Volkanovski`, `Ilia Topuria`, `Tim Elliott`, `Emily Ducote`

## 🧩 Aide

- Le pays doit être écrit comme dans les bases de données :  
  - `United States` ✅ (pas `USA`)  
  - `Russian Federation` ✅ (pas `Russia`)  
  - `United Kingdom` ✅ (pas `UK`)

- ⚠️ Ne pas ouvrir le fichier `rankfeed.xlsx` pendant l’exécution du code.

## ⏳ En projet

- Hébergement en ligne (Heroku / Render)
- Système de filtrage personnalisé

## 🤝🤝🤝🤝🤝 Merci à l'équipe finlandaise !

🇫🇷 Charles Brunet 
🇪🇸 Javier Miranda


       🟦🟦
       🟦🟦
       🟦🟦
🟦🟦🟦🟦🟦🟦🟦🟦🟦🟦🟦
🟦🟦🟦🟦🟦🟦🟦🟦🟦🟦🟦
       🟦🟦
       🟦🟦
       🟦🟦
