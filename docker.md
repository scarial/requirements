Use interactively docker container 
----------------------------------

```
docker run --tty --interactive IMAGE_NAME(:image_tag)
```

or 

```
docker run IMAGE_NAME(:image_tag) echo Docker is fun
```

Un container est l'équivalent d'un Filesystem
---------------------------------------------
Notion à garder en tête

docker run
----------
Execute 2 autres commandes docker create et docker start

docker create
-------------
Permet de convertir une image en container, auquel on passe des paramètres
ex de params:
mapping des ports, partage des dossiers...(cf doc de docker create)
ex en renommant le container en 'wonderful_mobidock' :
```
docker create --tty --interactive --name="wonderful_mobidock" IMAGE_NAME(:image_tag)
```

docker start
------------
Une fois un container créé et configuré à partir d'une image, on peut le lancer quand on veut
```
docker start wonderful_mobidock
```
Par défaut, "docker start" ne vous attache pas la console, mais vous pouvez le spécifier avec l'option --attach.
```
docker start --attach wonderful_mobidock
```
docker stop
-----------
Arrêter proprement l'utilisation d'un container.

TIPS:
-----
 - Une BDD sera utilisée dans un Volume


