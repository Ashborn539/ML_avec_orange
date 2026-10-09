# Machine Learning avec Orange

Projet d'apprentissage automatique realise avec [Orange Data Mining](https://orangedatamining.com/).
Il contient une analyse de textes et une classification d'images de personnages.

## Contenu

- `hounsa_tylden_fenina_sara_orange1.ows` : workflow d'analyse textuelle.
  Il importe les citations, supprime les mots vides, cree une representation Bag of Words,
  genere des nuages de mots et applique un clustering hierarchique.
- `hounsa_tylden_fenina_sara_orange2.ows` : workflow de classification d'images.
  Il transforme les images en embeddings, compare plusieurs modeles et affiche les resultats
  avec une matrice de confusion et les predictions.
- `hounsa_tylden_fenina_sara_data1.csv` : citations classees par anime.
- `hounsa_tylden_fenina_sara_stopwords1.txt` : liste des mots vides utilises pour le texte.
- `hounsa_tylden_fenina_sara_data2/` : images organisees par personnage, notamment
  `Crocodile`, `Law`, `Nami`, `Rayleigh` et `Test`.

## Installation

1. Installer [Orange Data Mining](https://orangedatamining.com/download/).
2. Installer les extensions **Orange3-Text** et **Orange3-Image Analytics** depuis le gestionnaire d'add-ons d'Orange.

## Utilisation

1. Ouvrir Orange.
2. Ouvrir le fichier `.ows` souhaite.
3. Si Orange demande un fichier, selectionner le CSV, le fichier de stopwords ou le dossier d'images correspondant dans ce projet.
4. Executer les widgets du workflow pour consulter les tableaux, visualisations et resultats.

## Modeles testes

Le workflow d'images compare notamment :

- regression logistique ;
- k plus proches voisins (kNN) ;
- SVM ;
- arbre de decision ;
- foret aleatoire ;
- reseau de neurones.

Les performances sont comparees avec **Test and Score** et analysees dans la **Confusion Matrix**.