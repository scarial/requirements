## Problème lors d'un schema update en **LOCAL**
En local si problèmes liés à des Schema update et des suppressions impossibles de foreign keys
```
php app/console doctrine:schema:update --force --complete --env=dev
```
`--complete` permet de supprimer les champs qui ne sont plus utilisés, et qui sont susceptibles de poser problème
