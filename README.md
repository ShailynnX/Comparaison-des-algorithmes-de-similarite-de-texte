Le projet vise à explorer les méthodes avancées de TAL pour calculer la similarité entre des ensembles de questions et de réponses à partir de fichier TSV, qui contient trois colonnes principales.
On va utiliser principalement les colonnes 2 et 3, qui contiennent les contenus textuels des questions
et des réponses.
L'objectif principal est d'identifier, pour chaque question, la réponse la plus pertinente dans un
ensemble de données donné, en utilisant des techniques de vectorisation de texte et des mesures de
similarité/distance.

## Comparaison de deux méthodes de représentation de texte :

- Utilisation du modèle de sac de mots pour représenter le texte sous forme d'un ensemble de mots, où chaque mot est représenté par sa fréquence d'apparition. Cela forme un vecteur sparse de grande dimension. Enfin, une normalisation ou un traitement **TF-IDF** est appliqué à ce vecteur.

- Utilisation de l'extraction de caractéristiques **SIF** (Smooth Inverse Frequency), qui utilise des modèles pré-entraînés Word2Vec/GloVe pour représenter le texte sous forme de vecteurs de mots. Généralement, la bibliothèque gensim est utilisée pour charger ces modèles pré-entraînés.

## Comparaison de quatre méthodes de calcul de distance :

- Jaccard  
- Euclidienne  
- De Manhattan  
- Cosinus  

Utilisation de la fonction `pairwise_distances()` de Scikit-learn pour calculer la matrice de distances entre les vecteurs de questions et de réponses vectorisés.

Enfin, l'utilisation de l'algorithme de l'association de correspondance maximale (algorithme hongrois) permet d'obtenir une meilleure précision.
