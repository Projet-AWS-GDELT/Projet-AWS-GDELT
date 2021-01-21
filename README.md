# Projet-AWS-GDELT
Projet réalisé dans le cadre du MS BigData 2020/2021 à Télécom Paris par :
  - Elliot CANDALE
  - Sully DILOU
  - Rémi GENET
  - Vincent POQUET
  - Adrien SENET
 
 ![](http://andreiarion.github.io/images/gdelt-linguistic-geography.png)
 Locations mentioned in global news coverage monitored by GDELT 2015-2018, colored by the primary language of coverage mentioning each location ([Seeing The World Through The Eyes Of Others: Mass Machine Translation, KALEV LEETARU](https://www.forbes.com/sites/kalevleetaru/2018/11/24/seeing-the-world-through-the-eyes-of-others-mass-machine-translation/?sh=280c83702c8a))
 
 
### Introduction:
  La base de données mondiale sur les événements, les langues et les tonalités ([GDELT](https://www.gdeltproject.org/)) surveille les informations diffusées dans le monde entier, dans la presse écrite et sur le web, en provenance de presque tous les coins de chaque pays et dans plus de 100 langues. Elle identifie les personnes, les lieux, les organisations, les thèmes, les sources, les émotions, les comptes, les citations, les images et les événements qui animent notre société mondiale à chaque seconde de chaque jour, créant ainsi une plate-forme ouverte et gratuite pour l'informatique sur le monde entier.


### Objectif:
  L’objectif de ce projet est de proposer un système de stockage distribué, résilient et performant sur AWS pour repondre aux question suivantes:

   a. Afficher le nombre d’articles/évènements qui parlent de COVID qu’il y a eu pour chaque triplet (jour, pays de l’évènement, langue de l’article)

   b. Pour un pays donné en paramètre, affichez les évènements qui y ont eu place triées par le nombre de mentions (tri décroissant); permettez une agrégation par jour/mois/année

   c. Pour une source de donnés passée en paramètre (gkg.SourceCommonName) affichez les thèmes, personnes, lieux dont les articles de cette sources parlent ainsi que le le nombre  d’articles et le ton moyen des articles (pour chaque thème/personne/lieu); permettez une agrégation par jour/mois/année.

   d. Est-ce qu’on observe des patterns dans l’evolution qui pourraient nous permettre d’identifier la prochaine vague/pandemie
    
    
### Architecture


### Outils et logiciels utilisés
Le processus ETL des fichiers GDELT a été réalisé dans un notebook Zeppelin, en utilisant Spark (Scala) connecté à AWS.
Le système de gestion de base de donnée utilisé est Mongodb.
