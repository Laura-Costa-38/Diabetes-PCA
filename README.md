# Analyse des profils biométriques (Diabète) par réduction de dimensionnalité

## 🎯 Problématique
Face à un jeu de données médicales comportant de multiples indicateurs physiologiques (glucose, IMC, insuline, âge, etc.), l'objectif de ce projet est exploratoire. Il cherche à répondre à la question suivante : 
**Peut-on résumer le profil clinique d'un patient en deux indicateurs globaux (composantes) tout en conservant l'essentiel de la variance, et ces axes permettent-ils d'isoler naturellement les patients diabétiques ?**

## ⚙️ Méthodologie
Ce projet met en œuvre une démarche de Machine Learning non supervisé pour analyser les structures cachées des données médicales :
* **Standardisation (`StandardScaler`)** : Mise à l'échelle des variables pour comparer équitablement des métriques hétérogènes (ex: âge vs taux d'insuline).
* **Analyse en Composantes Principales (`PCA`)** : Réduction des 8 dimensions initiales vers un espace 2D pour faciliter la visualisation.
* **Cercle de corrélation** : Étude des poids (loadings) pour comprendre quelles variables cliniques évoluent ensemble et définissent les nouveaux axes.

## 📊 Résultats clés
* **Nuage des individus :** La projection 2D révèle qu'il n'existe pas de frontière stricte isolant parfaitement les patients sains des patients malades avec seulement deux dimensions. Cela confirme la nature multifactorielle complexe de la pathologie.
* **Dynamique des variables :** L'analyse des corrélations permet d'identifier quels biomarqueurs ont le plus de poids dans la variance des profils cliniques étudiés.
