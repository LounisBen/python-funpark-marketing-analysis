# FunPark International — Analyse d'une campagne commerciale avec Python

## Présentation du projet

Ce projet analyse les performances commerciales de FunPark International
sur le premier semestre 2025.

L'objectif est d'exploiter les données de fréquentation et de dépenses
afin de :

- fiabiliser les données ;
- analyser les profils des visiteurs ;
- identifier les offres générant le plus de revenus ;
- mesurer l'impact d'une campagne promotionnelle ;
- formuler des recommandations commerciales.

> Projet pédagogique réalisé dans le cadre de ma formation Data Analyst.
> Les données utilisées sont fictives et servent uniquement à des fins d'apprentissage.

---

## Problématique

FunPark International a mis en place plusieurs initiatives commerciales,
notamment :

- le lancement d'une offre VIP ;
- une promotion « 2e entrée à -50 % » ;
- le développement de nouvelles offres de restauration.

L'analyse vise notamment à répondre aux questions suivantes :

- Quels sont les principaux profils de visiteurs ?
- Quels billets génèrent le plus de revenu ?
- Quels marchés sont les plus importants ?
- La campagne promotionnelle a-t-elle eu un impact mesurable sur le revenu moyen ?
- Quelles actions commerciales pourraient être prioritaires ?

---

## Technologies utilisées

- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- SciPy
- Jupyter Notebook

---

## Méthodologie

### 1. Exploration des données

Analyse initiale du dataset :

- structure des données ;
- types de variables ;
- valeurs manquantes ;
- statistiques descriptives.

Le dataset initial contient **2 505 observations et 10 variables**.

---

### 2. Nettoyage et fiabilisation

Plusieurs traitements ont été réalisés :

- uniformisation des valeurs textuelles ;
- conversion des types de données ;
- traitement des valeurs manquantes ;
- détection des valeurs aberrantes avec la méthode IQR ;
- suppression des outliers ;
- contrôle des doublons.

Après nettoyage, le dataset contient **2 390 observations** sans valeurs manquantes.

---

### 3. Analyse des visiteurs

L'analyse porte notamment sur :

- la répartition des visiteurs par pays ;
- les types de billets ;
- les classes d'âge ;
- les dépenses moyennes ;
- les produits les plus vendus ;
- les revenus générés par visiteur.

Une variable `Revenue_Total` a été créée afin de regrouper :

- le prix du billet ;
- les dépenses de restauration.

Les visiteurs ont également été segmentés en quatre groupes de revenus
à l'aide de `pandas.qcut()` :

- Faible
- Moyen
- Élevé
- Très élevé

---

## Principaux résultats

### Répartition géographique

La France constitue le premier marché avec environ **40,9 % des visites**.

Elle est suivie par :

- l'Espagne ;
- l'Allemagne ;
- le Maroc.

---

### Performance des offres

Le billet **Famille** génère le revenu moyen par visite le plus élevé :

**137,45 €**

Le billet **VIP** arrive ensuite avec :

**110,56 €**

Ces deux offres représentent donc des leviers importants pour augmenter
le revenu moyen par visiteur.

---

### Profil des visiteurs

Les adultes et jeunes adultes représentent environ **82,4 % des visiteurs**.

Ce résultat permet d'identifier les segments de clientèle les plus
importants pour les futures campagnes marketing.

---

## Analyse de la campagne promotionnelle

Le revenu moyen par visite est comparé avant et après la promotion.

| Période | Revenu moyen |
|---|---:|
| Avant promotion | 73,72 € |
| Après promotion | 76,76 € |

L'écart observé est donc d'environ :

**+3,04 € par visite**

Afin de vérifier si cette différence peut être considérée comme
statistiquement significative, un **test de Student** a été réalisé.

Résultat :

- T-statistique : **-2,07**
- p-value : **0,0383**

La p-value étant inférieure au seuil de 5 %, la différence observée
entre les deux périodes est statistiquement significative.

La campagne promotionnelle semble donc avoir contribué à une légère
augmentation du revenu moyen par visite.

---

## Recommandations

L'analyse permet de dégager plusieurs pistes d'action :

1. **Renforcer l'offre VIP**

   Développer sa visibilité dans les campagnes marketing et valoriser
   les avantages associés à l'expérience premium.

2. **Développer l'offre Famille**

   Le billet Famille génère le revenu moyen le plus élevé et pourrait
   être associé à des offres complémentaires : restauration, souvenirs
   ou services.

3. **Optimiser les promotions**

   Tester différentes offres et mesurer systématiquement leurs effets
   sur le revenu et la fréquentation.

4. **Adapter les campagnes aux principaux segments**

   Les adultes et jeunes adultes représentent la majorité des visiteurs
   et constituent une cible prioritaire.

5. **Développer les marchés moins représentés**

   Certains marchés comme le Maroc pourraient faire l'objet de campagnes
   ou partenariats spécifiques.

---

## Compétences mobilisées

Ce projet m'a permis de travailler sur :

- le nettoyage et la préparation des données ;
- l'analyse exploratoire ;
- la détection des valeurs aberrantes ;
- la création de variables métier ;
- la segmentation de données ;
- la visualisation ;
- les statistiques descriptives ;
- les tests statistiques ;
- l'interprétation des résultats ;
- la formulation de recommandations métier.

---

## Auteur

Projet réalisé dans le cadre de ma montée en compétences en Data Analyse.
