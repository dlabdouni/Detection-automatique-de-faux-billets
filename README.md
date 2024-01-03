# Projet Détection Automatique de Faux Billets

Bienvenue dans ce projet visant à développer un algorithme de détection automatique de faux billets. Ce projet a pour objectif de mettre en place des méthodes efficaces d'identification des contrefaçons des billets en euros.

# Contexte du Projet

Il a été constaté des différences de dimensions entre les vrais et les faux billets, difficiles à détecter à l'œil nu. Afin de renforcer la lutte contre le faux-monnayage, nous souhaitons mettre en place un algorithme capable de différencier automatiquement les vrais des faux billets en se basant sur leurs caractéristiques géométriques.

# Objectifs

L'objectif principal est de construire un algorithme performant qui, à partir des dimensions géométriques d'un billet, peut déterminer s'il s'agit d'un vrai ou d'un faux billet.

# Modèle de Données
Dimensions Géométriques

    length: Longueur du billet (en mm)
    height_left: Hauteur du billet (côté gauche, en mm)
    height_right: Hauteur du billet (côté droit, en mm)
    margin_up: Marge entre le bord supérieur du billet et son image (en mm)
    margin_low: Marge entre le bord inférieur du billet et son image (en mm)
    diagonal: Diagonale du billet (en mm)

# Fichier pour Paramétrisation

Un fichier d'exemple contenant 1 500 billets (1 000 vrais et 500 faux) est fourni pour la paramétrisation de l'algorithme.

# Fonctionnement Général

L'algorithme prend en entrée un fichier contenant les dimensions de plusieurs billets et détermine le type de chacun (vrai ou faux) en se basant uniquement sur les dimensions. Deux méthodes de prédiction seront mise en concurrence :

    --> la Régression logistique
    --> le K-means (clustering) avec utilisation des centroïdes pour la prédiction

L'évaluation des modèles se fera entre autre à travers une matrice de confusion, analysant les faux positifs et faux négatifs.




