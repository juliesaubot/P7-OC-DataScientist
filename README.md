# P7-OC-DataScientist

## Projet : Implémentez un modèle de scoring
Projet 7 de la formation OpenClassrooms du parcours data scientist

## Objectifs du projet
Une société financière, nommée "Prêt à dépenser", qui propose des crédits à la consommation pour des personnes ayant peu ou pas du tout d'historique de prêt souhaite mettre en œuvre un outil de “scoring crédit” pour calculer la probabilité qu’un client rembourse son crédit, puis classifie la demande en crédit accordé ou refusé.

Elle souhaite donc développer un algorithme de classification en s’appuyant sur des sources de données variées (données comportementales, données provenant d'autres institutions financières, etc.). De plus, les chargés de relation client ont fait remonter le fait que les clients sont de plus en plus demandeurs de transparence vis-à-vis des décisions d’octroi de crédit. Cette demande de transparence des clients va tout à fait dans le sens des valeurs que l’entreprise veut incarner.

Ce projet a donc pour but de déployer le modèle via une API (FAST API) dans le Web via Heroku en utilisant un dashboard interactif (Streamlit) pour présenter le travail de modélisation. Il comporte aussi un test unitaire à l'aide de Pytest. Le code source de l'API contient entre autres un calculateur de score pour une demande de crédit bancaire qui retourne au Dashboard la probabilité que le client puisse le rembourser, et qui indique donc si le crédit est accordé ou non.

Le projet est composé en deux parties : 
- La partie Dashboard qui correspond au repository : P7-OC-DataScientist-streamlit
- La partie API qui correspond au repository : P7-OC-DataScientist-FASTAPI

### Données à disposition : 
Le jeu de données mis à disposition est composé de plusieurs datasets :
- application_{train|test}.csv : Il s'agit des données des informations clients où une ligne représente un prêt, divisé en deux fichiers pour Train (avec TARGET) et Test (sans TARGET). 
- bureau.csv : Tous les crédits antérieurs du client fournis par d'autres institutions financières qui ont été signalés au bureau de crédit
- bureau_balance.csv : Soldes mensuels des crédits antérieurs dans le bureau de crédit.
- POS_CASH_balance.csv : Instantanés mensuels des soldes des crédits POS (point de vente) et des crédits de trésorerie antérieurs que le demandeur a contractés auprès de Home Credit.
- credit_card_balance.csv : Instantanés mensuels des soldes des cartes de crédit antérieures que le demandeur possède auprès de Home Credit.


### Missions : 

- Élaborer un modèle de scoring visant à automatiser la prédiction de la probabilité de faillite d'un client.
- Développer un dashboard interactif destiné aux gestionnaires de la relation client, permettant une interprétation des prédictions du modèle et contribuant à enrichir la connaissance client des chargés de relation client.
- Déployer en production le modèle de scoring de prédiction à l’aide d'une API, accompagné du dashboard interactif qui appelle l'API pour obtenir les prédictions.

## Compétences évaluées :

- Déployer un modèle via une API dans le Web
- Réaliser un dashboard pour présenter son travail de modélisation
- Rédiger une note méthodologique afin de communiquer sa démarche de modélisation
- Utiliser un logiciel de version de code pour assurer l’intégration du modèle
- Présenter son travail de modélisation à l'oral
- Définir et mettre en œuvre une stratégie de suivi de la performance d’un modèle
- Définir et mettre en œuvre un pipeline d’entraînement des modèles
- Définir la stratégie d’élaboration d’un modèle d’apprentissage supervisé
- Évaluer les performances des modèles d’apprentissage supervisé

## Découpage des dossiers

- Julie_Saubot_note_méthodologique_102023.pdf : Note méthodologique pour de communiquer la démarche de modélisation
- Dossier Saubot_Julie_2_dossier_code_102023 :
  - data_drift.ipynb : notebook de l'analyse du Data Drift
  - data_drift.html : fichier htlm du tableau résultat du Data Drift
  - notebook_modelisation.ipynb : code de la modélisation du prétraitement à la prédiction
- Saubot_Julie_4_presentation_022023.pptx : support de présentation pour la soutenance


## Lien utiles

- Données utilisées : https://www.kaggle.com/c/home-credit-default-risk/data
- URL github du code du dashboard Streamlit : https://github.com/juliesaubot/Saubot_Julie_streamlit_102023
- URL github du code de l'API : https://github.com/juliesaubot/Saubot_Julie_FASTAPI_102023
- URL API déployé dans le Cloud : https://saubot-julie-fastapi-102023-5cca48d2a8d1.herokuapp.com/
- URL dashboard déployé dans le Cloud : https://saubot-julie-dashboard-102023-00ee4bc4d00a.herokuapp.com/ 
