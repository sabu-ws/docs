# Versionning

## VERSIONNING DE RELEASE

### MAJEUR: Quand il y a des changements non rétrocompatibles
Imaginez un champ unique "name". Si la nouvelle version sépare en "first name" et "last name" et ne prévoit plus un champ "name", il faudra établir comment les données disponibles seront départagées entre les nouveaux champs.
Imaginez une bibliothèque de dessin qui présente les fonctions drawCircle() et drawSquare(). Par souci d'uniformité, les concepteurs décident de créer un objet draw avec la méthode circle(), square(), rectangle(), elipse(), etc. Les deux fonctions disparaissent et sont remplacées par draw.circle() et draw.square().

### MINEUR : Quand il y a des ajouts de fonctionnalités rétrocompatibles
 
Ajouter un nouveau champ "surname" dans une table, tout en gardant "first name" et "last  name" intacts
Pouvoir imprimer un document en modalité horizontale, tout en gardant la version verticale intacte et comme choix prédéfini

### CORRECTIF: Quand il y a des corrections d’anomalies rétrocompatibles.
Des petits bugs
Des problèmes de sécurité
Amélioration du code
Réduction du temps d'exécution