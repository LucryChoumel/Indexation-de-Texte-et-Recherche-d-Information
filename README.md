# Indexation de Texte et Recherche d'Information

Bienvenue dans ce projet ambitieux d’indexation de texte et de recherche d’information. Le projet explore différentes techniques d’indexation et de recherche, en utilisant des méthodes avancées pour améliorer la précision et l’efficacité des recherches dans de grands corpus de texte.

Table des Matières

	•	Aperçu
	•	Prérequis
	•	Installation
	•	Utilisation
	•	Fonctionnalités Principales
	•	Construction de l’Index
	•	Chargement et Vérification de l’Index
	•	Requête et Affichage des Résultats
	•	Affichage des Contextes
	•	Calcul TF-IDF
	•	Seuil de Similarité Cosinus
	•	Classement par Pertinence
	•	Structuration de l’Espace de Recherche
	•	Analyse des Résultats
	•	Contributions
	•	Auteur
	•	Licence

Aperçu

Ce projet a été réalisé par Lucry CHOUMELE (choumelelucry@gmail.com). Il vise à construire un système complet d’indexation et de recherche de texte en utilisant différentes techniques pour évaluer et améliorer la précision et l’efficacité des recherches. Le projet couvre plusieurs aspects allant de la construction de l’index à la structuration de l’espace de recherche, en passant par des méthodes avancées telles que le KD-Tree, K-Means et Locality-Sensitive Hashing (LSH).
![ảnh](https://github.com/user-attachments/assets/1f6433f4-bea8-4a05-a8a8-bd3e781dacbf)
![ảnh](https://github.com/user-attachments/assets/fcbc05d1-4eff-4b58-9f46-3bd49912ae33)
![ảnh](https://github.com/user-attachments/assets/88ae6bc4-d8b6-43e2-9981-85da2b0dbdfe)

Prérequis

Avant de commencer, assurez-vous d’avoir les éléments suivants installés sur votre machine :

	•	Python 3.x
	•	Jupyter Notebook
	•	Bibliothèques Python : numpy, pandas, scikit-learn, json, glob, re

Installation

	1.	Clonez ce dépôt pour obtenir tous les fichiers nécessaires 
 git clone https://github.com/votre-utilisateur/projet-indexation-recherche.git
cd projet-indexation-recherche
2.	Installez les dépendances pour garantir que tous les scripts s’exécutent correctement :
pip install numpy pandas scikit-learn

2.	Suivez les étapes détaillées dans le notebook pour découvrir les différentes fonctionnalités et méthodes que nous avons développées.

Fonctionnalités Principales

Construction de l’Index

Cette section couvre la construction de l’index sur l’ensemble du corpus :

	•	Lecture et découpage des fichiers : Utilisation de fonctions pour lire et découper les textes en mots.
	•	Création de l’index : Stockage des occurrences des mots dans un index pour une recherche efficace.

Chargement et Vérification de l’Index

Ici, nous abordons le chargement de l’index précédemment créé et la vérification de la présence de mots spécifiques :

	•	Chargement de l’index : Utilisation de JSON pour stocker et charger l’index.
	•	Vérification des mots : Vérification de la présence de mots spécifiques dans l’index.

Requête et Affichage des Résultats

Cette section montre comment requêter l’index et afficher les résultats correspondants :

	•	Traitement des requêtes : Découpage et traitement des requêtes utilisateur.
	•	Affichage des résultats : Affichage des documents contenant les mots de la requête.
![ảnh](https://github.com/user-attachments/assets/8174bc53-9550-4f15-8c93-3c2b525a1609)

Affichage des Contextes

Intégration de la fonction pour afficher les contextes des mots recherchés dans les documents.
![ảnh](https://github.com/user-attachments/assets/4b390353-3b40-4400-bdb3-1512a4f6da5b)

Calcul TF-IDF

Calcul des valeurs TF-IDF pour les termes du corpus pour évaluer leur importance relative dans les documents.

Seuil de Similarité Cosinus

Application d’un seuil de similarité cosinus pour filtrer les résultats de recherche :

	•	Calcul de la similarité cosinus : Utilisation de cette mesure pour évaluer la similarité entre documents.

Classement par Pertinence

Classement des résultats de recherche par pertinence basée sur les scores de similarité.
![ảnh](https://github.com/user-attachments/assets/9f9c4875-2756-48f2-b835-8665804a0910)

Structuration de l’Espace de Recherche

Exploration de différentes méthodes pour structurer l’espace de recherche :

	•	KD-Tree
	•	K-Means
	•	Locality-Sensitive Hashing (LSH)

Analyse des Résultats
![ảnh](https://github.com/user-attachments/assets/4cc36180-f51b-46cc-b4ac-cba8951a806b)

Analyse comparative des résultats obtenus avec différentes méthodes :

	•	KD-Tree : Bon compromis entre temps de construction et précision.
	•	K-Means : Temps de construction long mais recherche rapide, avec une précision légèrement inférieure.
	•	LSH : Temps de recherche plus long avec une précision moindre comparée à KD-Tree.

Conclusion
## Comparaison des Résultats



### Analyse des Résultats

1. **KD-Tree** :
   - Le temps de construction est moyen (5.4462 secondes).
   - Le temps de recherche est très rapide (0.0338 secondes).
   - Les scores de similarité sont les plus élevés comparés aux autres méthodes, ce qui suggère une bonne précision.

2. **K-Means** :
   - Le temps de construction est le plus long (10.1078 secondes).
   - Le temps de recherche est très rapide (0.0136 secondes).
   - Les scores de similarité sont plus bas que ceux obtenus avec KD-Tree, ce qui pourrait indiquer une précision légèrement moindre.

3. **LSH** :
   - Le temps de construction est similaire à celui du KD-Tree (5.4510 secondes).
   - Le temps de recherche est le plus long parmi les trois méthodes (0.0649 secondes).
   - Les scores de similarité sont également plus bas, ce qui pourrait indiquer une précision moindre comparée à KD-Tree.

### Conclusion

- **KD-Tree** semble offrir un bon compromis entre le temps de construction et la précision des résultats. C'est une méthode efficace pour des bases de données de taille modérée.
- **K-Means** a le temps de construction le plus long, mais offre un temps de recherche très rapide. Cependant, la précision semble légèrement inférieure à celle du KD-Tree.
- **LSH** a un temps de construction comparable à KD-Tree, mais un temps de recherche plus long et une précision légèrement inférieure.
	•	KD-Tree offre un bon équilibre entre temps de construction et précision des résultats.
	•	K-Means a un temps de construction long mais un temps de recherche rapide, avec une précision légèrement inférieure.
	•	LSH a un temps de recherche plus long et une précision inférieure.

Contributions

Nous accueillons chaleureusement toutes les contributions. Que vous souhaitiez corriger des bugs, améliorer les modèles ou ajouter de nouvelles fonctionnalités, vos efforts sont les bienvenus. Veuillez soumettre une pull request ou ouvrir une issue pour discuter de vos propositions.

Auteur

Ce projet a été développé par CHOUMELE Lucry. Si vous avez des questions ou des suggestions, n’hésitez pas à le contacter.(choumelelucry@gmail.com)

