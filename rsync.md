Rsync pour copier les données depuis un serveur distant en SSH
--------------------------------------------------------------
```
rsync -ave ssh serveur_ip_ou_nom:/chemin/vers/source /chemin/vers/cible
```
- l’option -a, mode archivage, permet de copier de manière récursive, de préserver les permissions et de ne pas suivre les liens symboliques
- l’option -v, verbose, affiche la liste des fichiers copiés
- l’option -z, compress, permet de compresser les données avant de les transférer
- l’option -e ssh permet d’utiliser ssh pour le transfert de données.
