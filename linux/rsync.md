Installer Rsync
---------------
```
sudo apt-get install rsync
```

Utilisation basique
-------------------

```
rsync chemin/vers/source chemin/vers/cible
```

Utiliser rsync pour transférer des données d’un serveur à un autre
------------------------------------------------------------------
```
rsync -e ssh -avz /chemin/vers/source serveur_ip_ou_nom:/chemin/vers/cible
```

Rsync pour copier les données en local depuis un serveur distant en SSH
-----------------------------------------------------------------------
```
rsync -ave ssh serveur_ip_ou_nom:/chemin/vers/source /chemin/vers/cible
```
- l’option -a, mode archivage, permet de copier de manière récursive, de préserver les permissions et de ne pas suivre les liens symboliques
- l’option -v, verbose, affiche la liste des fichiers copiés
- l’option -z, compress, permet de compresser les données avant de les transférer
- l’option -e ssh permet d’utiliser ssh pour le transfert de données.
