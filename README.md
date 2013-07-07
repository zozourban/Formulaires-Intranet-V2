Formulaires-Intranet-V2
=======================

Gestion de formulaires en interne

Le système de mises à jour
----------------------------------

Dans la version 1, pour détecter la nouvelle version du logiciel, un fichier version.txt était nécessaire.
Maintenant la version 2, utilise un paramètre en plus dans la base de données :

Table : Parametres

Parametre : version_logiciel

valeur : 3.8.0.0   <- C'est un exemple

Il n'y a plus besoin du version.txt, le logiciel va directement lire la version dans la base de données.
Si la version dans la base est supérieur au client alors le client télécharge la nouvelle version.
Si la version dans la base et inferieur ou égale au client, alors le client ne fera rien :-).

L'Upload
----------------------------------

La fonction Upload a été réecrite afin de cibler plus facilement une erreur. Elle dispose d'une meilleur verification,
d'une barre de progression intégrée, un pourcentage et un descriptif du formulaire sélectionné.

La modification et la suppression
----------------------------------

L'affichage de cette partie a été refaite pour utiliser tout l'espace de l'application et de se concentrer sur le
formulaire sélectionné.
Quand un formulaire est sélectionnée, une description apparait, mais aussi le nom de la personne qui l'a mit et le numéro
du formulaire.
La suppression permet d'effacer le formulaire present sur le réseau et aussi les informations de ce formulaire dans la base
de données.
La modification permet de modifer l'intitulé du formulaire ainsi que le formulaire.
