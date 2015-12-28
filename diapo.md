# Notes pour la rédaction du diapo
*Rappel: 30 min de présentation en français*

# Introduction

# Présentation du projet CRATE
## Général
* Ici une capture d'écran Google drive et CRATE

## Architecture distribué SPRAY
* Voir le pdf dans le répo

## Écritures simultanés LSEQ
* Voir les personnes ayant se sujet

# Etat de l'art
## Éditeurs collaboratifs
* Captures Google Drive et Overleaf

## Persistance des données
* Images base de données, graphes, etc..

# Recherche sur les liens inter-documents
## Liens de partage
* Schéma avec plusieurs utilisateur pour montrer que pour un document chacun à un lien de partage propre
* Même schéma avec un lien unique est une table qui ressence les liens de partages pour le document donné

## Persistance des données
* Présentation de IPFS

# Contribution au projet CRATE
## Mise en place d'IPFS
* Diagramme de séquence pour expliquer la mécanique (voir avec Anthony pour l'exemple)

## Enregistrement des documents
* Expliquer les limitations

# Conclusion
## Bilan
## Perspectives

# Notes du rapport pour aider 

'''

\section{Introduction}
% Très général sur le besoin de travailler en équipe, en live avec beaucoup
% de personnes en même temps

% Problématique de performance -> décentralisé
% Recherche de solution efficace dans cette voie (cf diapos de pascal)

\section{Présentation du projet CRATE}
\subsection{Architecture distribué}
% La recherche de pascal sur SPRAY

\subsection{Écritures simultanés}
% La recherche de pascal sur LSEQ

\section{État de l'art}

\subsection{Éditeurs collaboratifs}
% Google drive
% Overleaf
% Forces et faiblesses du centralisés
% -> identification, persistance des données
De plus en plus d'éditeurs collaboratifs sont créés de nos jours de par la demande de travailler en collaborations ; le plus connu étant \emph{Google Drive} 

\subsection{Persistance des données}
% IPFS
% Base de données SQL/NoSQL

\section{Recherche sur les liens inter-documents}
\subsection{Liens de partage}
% Une personne donne 1 lien unique vers 1 document
% Si cette autre personne veux partager le même document ce sera un nouveau lien de partage
% -> Le réseau se construit, il ne faut pas que tout le monde soit sur le premier lien

% - Ces liens de partages ont une durée de vie or il nous faut quelque chose de statique
% - Chaque personne ayant une copie du document doit avoir le même lien 
% quelque soit le lien de partage qu'il a reçu pour accéder au document

\subsection{Persistance des données}
% Une personne doit connaître la correspondance entre un lien statique vers un document 
% et tout les liens de partage associé au document

% Problème: ça devient centralisé
% Solution: IPFS permet de partager un document en décentralisé

% Pour être sur que le lien est toujours fonctionnel une personne doit maintenir l'hébergement
% du document. Exemple la dernière personne qui édite un document ayant un lien n'a pas 
% ouvert ce lien et personne d'autre n'édite le document lié donc le lien est mauvais.

% Solution: IPFS sauvegarde le document (mode pin)

\section{Contribution au projet \crate}
\subsection{Mise en place d'IPFS}
% Rappeler qu'il permet d'enregistrer de manière décentralisée
% pour les liens de partage et les documents

\subsubsection{Enregistrement des documents}
% Limitation et utilisation de l'index
% - documents immuables (une fois ajouté à ipfs, on ne peut plus les modifier)
% - si on veut modifier un document, il faut l'ajouter de nouveau mais nouveau hash donc du point de vue ipfs => nouveau fichier
% obligation de créer un index :
% - un noeud ipfs = une seule url "mutable" (on associe à un nœud un document "par défaut", qui est publié sur le nœud)
% - système de "nom de domaine" limité à un document par nœud donc impossible de stocker plus d'un document => choix d'utiliser ce document pour faire un index qu'on utilisera pour référencer des documents simplement "pin" sur le réseau ipfs
% - point partiellement-centralisé :
%		- si grand nombre de serveur ipfs déployé, alors grand nombre d'index donc peu de document différent par index
%		- si un ipfs tombe, seul l'index tombe, les documents sont conservés (possibilité d'ajouter une distribution de l'index)


\subsubsection{Lien unique de partage}
% Dans la theorie...
% Mettre ça dans les perspectives ? un peu gros ça reste une contribution, on y a réfléchi..

% - CRATE basé sur le fait qu'on ait plusieurs liens pour un même document sans "logique" entre les liens (=> système 100% décentralisé)
% - nécessité de créer un lien logique qui masquerait l'ensemble des autres liens (utilisations d'un index ? associé à chaque document une liste de liens équivalents ?)

\subsection{Intégration dans l'interface web}
% Editeur en Markdown
% Faire la différence entre un lien de partage CRATE et les autres
% Ne pas ouvrir plusieurs fois le même document dans la même page

\section{Conclusions}
\subsection{Bilan}
\subsection{Perspectives}
% Changer IPFS par autre chose car pas super dans notre cas
% -> Pas capable de partager plusieurs documents à la fois
% -> Partager un document met plus d'une 1 min donc pas viable

\section{Notes complémentaires pour la rédaction}
% diapos de pascal: https://drive.google.com/open?id=0B35HxQOs5Ma7SmFuaEVINVl0WWs

% Présentation
% Éditeur collaborative
% Algo LSEQ, SPRAY

% ipfs est immuable donc on ne peut pas modifier un fichier enregistré 
% url sur 1 seul document
% 1 ipfs par client
% problème: affichage de tout les fichiers stockés (monde ouvert)
% très lent pour publier un fichier (index vide: jusqu'à 1 min, en fonction de la connexion internet)

% dans IPFS
% un fichier index pour référencer les documents enregistrés
% les documents enregistrés sont des documents CRATE

% Plusieurs liens de partage pour 1 seul document
% et documents qui disparaissent
% -> il faut un lien unique (et valide) vers une version du document qui est maintenue en ligne
% -> au moins une version du document doit être maintenue en ligne
% -> ce lien unique dans ipfs référence des liens de partage pour accéder au document


% Problèmes client
% afficher plusieurs documents partagés dans la même fenêtre
% distinguer lien CRATE et lien externe
% ne pas ouvrir plusieurs fois le même document


'''