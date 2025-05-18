# 💳 SDA_Python - WebApp de Prédiction de Défaut de Crédit


## 👥 Réalisé par :
Jordan Pindoh et Jiwon Yi

---

## 🎯 Objectif du projet

Cette application Web a pour but de prédire si un client de carte de crédit risque de faire défaut sur son paiement le mois suivant.  
Elle permet à une institution financière d’évaluer le **risque client** sur la base de ses caractéristiques personnelles et de son historique de paiements, afin de prendre des décisions plus éclairées lors de l’octroi de crédits.

Le modèle est intégré dans une interface simple et interactive développée avec **Streamlit**.

---

## 📊 Jeu de données utilisé

- **Nom du fichier** : `UCI_Credit_Card.csv`
- **Source officielle** : [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients)
- **Nombre d’observations** : 30 000 clients
- **Variables principales** :
  - Caractéristiques client : `LIMIT_BAL`, `SEX`, `EDUCATION`, `MARRIAGE`, `AGE`
  - Historique de paiements : `PAY_0` à `PAY_6`
  - Montants facturés : `BILL_AMT1` à `BILL_AMT6`
  - Montants payés : `PAY_AMT1` à `PAY_AMT6`
  - Cible : `default.payment.next.month`

---

## 🧠 Modèles testés et sélection

Nous avons comparé plusieurs modèles de classification :

- Régression Logistique
- SVM (Support Vector Machine)
- K-Nearest Neighbors (KNN)
- Random Forest

### 🧪 Métriques utilisées :
- Accuracy
- Précision
- Rappel (Recall)
- F1-score

👉 **Le modèle Random Forest** s’est montré le plus performant et équilibré, et a été sélectionné pour la WebApp.

---

## 💻 Fonctionnement de l'application

L’interface utilisateur a été développée avec **Streamlit**. Sur la **barre latérale**, l’utilisateur peut entrer :

- les données personnelles du client : sexe, âge, statut marital, éducation
- l’historique de paiements (`PAY_0` à `PAY_6`)
- les montants facturés et remboursés (`BILL_AMT` et `PAY_AMT`)

### ▶️ Une fois les données saisies :
- La prédiction est affichée avec un message vert (client fiable) ou rouge (client à risque)
- Une **visualisation circulaire** (pie chart) montre la probabilité de défaut

---

## 🎥 Démonstration vidéo

➡️ Lien Google Drive : [Cliquez ici pour visionner la démonstration](https://drive.google.com/file/d/1Rif2-bcE0ODv066ALckEYCWqqbAxnUv8/view?usp=drive_link)


---

## 📂 Structure du dépôt
```
SDA_Python/
├── app.py # Code principal de l'application Streamlit
├── UCI_Credit_Card.csv # Données utilisé 
├── requirements.txt # Fichier de dépendances Python
├── README.md # Documentation complète du projet
└── superPROJ.ipynb # Notebook de modélisation et d'entraînement
```

