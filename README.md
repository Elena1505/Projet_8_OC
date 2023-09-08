# Projet 8: Déployez un modèle dans le cloud
## Présentation:
Je suis Data Scientist dans une très jeune start-up de l'AgriTech, nommée  "Fruits!", qui cherche à proposer des solutions innovantes pour la récolte des fruits.
La volonté de l’entreprise est de préserver la biodiversité des fruits en permettant des traitements spécifiques pour chaque espèce de fruits en développant des robots cueilleurs intelligents.
Cette start-up souhaite dans un premier temps se faire connaître en mettant à disposition du grand public une application mobile qui permettrait aux utilisateurs de prendre en photo un fruit et d'obtenir des informations sur ce fruit.
Pour l'entreprise', cette application permettrait de sensibiliser le grand public à la biodiversité des fruits et de mettre en place une première version du moteur de classification des images de fruits.
De plus, le développement de l’application mobile permettra de construire une première version de l'architecture Big Data nécessaire.
## Mission:
Je suis donc chargé de vous approprier les travaux réalisés par l’alternant et de compléter la chaîne de traitement.
Il n’est pas nécessaire d’entraîner un modèle pour le moment.
L’important est de mettre en place les premières briques de traitement qui serviront lorsqu’il faudra passer à l’échelle en termes de volume de données !
Lors de son brief initial, Paul vous a averti des points suivants :

- Je dois tenir compte dans mes développements du fait que le volume de données va augmenter très rapidement après la livraison de ce projet. Je continuerai donc à développer des scripts en Pyspark et à utiliser le cloud AWS pour profiter d’une architecture Big Data (EMR, S3, IAM).
- Je dois faire une démonstration de la mise en place d’une instance EMR opérationnelle, ainsi qu’ expliquer pas à pas le script PySpark, que vous aurez complété : 
        - d’un traitement de diffusion des poids du modèle Tensorflow sur les clusters (broadcast des “weights” du modèle) qui avait été oublié par l’alternant. 
        - d’une étape de réduction de dimension de type PCA en PySpark 
- Je respecterais les contraintes du RGPD : dans notre contexte, je veillerais à paramétrer mon installation afin d’utiliser des serveurs situés sur le territoire européen 
- Mon retour critique de cette solution sera également précieuse, avant de décider de la généraliser
## Données:
Mon collègue Paul m'indique l’existence d’un document, formalisé par un alternant qui vient de quitter l’entreprise. 
Il a testé une première approche dans un environnement Big Data AWS EMR, à partir d’un jeu de données (https://www.kaggle.com/moltean/fruits) constitué des images de fruits et des labels associés (en téléchargement direct à ce lien: https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/Data_Scientist_P8/fruits.zip). Le notebook réalisé par l’alternant : https://s3.eu-west-1.amazonaws.com/course.oc-static.com/projects/Data_Scientist_P8/Mode_ope%CC%81ratoire.zip servira de point de départ pour construire une partie de la chaîne de traitement des données.
## Construction:
Dans ce dépôt, vous trouverez un fichier:

- "notebook.ipynb" : notebook  contenant les scripts en Pyspark exécutables (le preprocessing et une étape de réduction de dimension de type PCA).

## Packages:
Différents packages Python ont été utilisés:

- pandas 1.4.4
- numpy 1.23.5
- tensorflow 2.13.0
- pyspark 3.4.1

## Compétences:
- Utiliser les outils du cloud pour manipuler des données dans un environnement Big Data
- Identifier les outils du cloud permettant de mettre en place un environnement Big Data
- Paralléliser des opérations de calcul avec Pyspark