## Démarrage et lancement du serveur

```
# Créé le serveur ipfs et ces ressources
$ ipfs init

# Démarre le serveur ipfs
$ ipfs daemon
```

## Ajouter et partager un fichier

```
# Ajouter un fichier à partager
$ ipfs add coucou.md
added FILE_KEY coucou.md

# Publier le fichier
$ ipfs name publish FILE_KEY
Published to SERVER_KEY: /ipfs/FILE_KEY
```

## Récupérer le lien de partage et accéder au fichier

```
# Récupérer l'id du serveur
$ ipfs id
{
	"ID": SERVER_KEY,
	
}

# Récupère le lien vers le fichier publié avec l'id du serveur
$ ipfs name resolve SERVER_KEY
/ipfs/FILE_KEY

# Affiche le contenu du fichier partagé
$ ipfs cat /ipfs/FILE_KEY
Contenu du fichier coucou
```

## Remarques
* La SERVER_KEY associée au serveur qui permet de récupérer le lien de partage est figée
* Si l'on publie un second fichier, la commande *ipfs name resolve* renvoie le lien de partage du second fichier
* On ne peut donc publier et accéder qu'à un seul fichier à partir de l'extérieur
* Impossible de modifier un fichier, il se supprime au bout d'un timeout
* Possible de "pinner" un document pour forcer son stockage


