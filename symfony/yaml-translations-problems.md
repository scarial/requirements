Pour vérifier les duplicates sur chaque fichier de traduction (mais s'execute sur tous les fichiers, un par un) :

```php bin/console lint:yaml app/Resources/translations/```

Pour vérifier les traductions manquantes, ou inutilisées :

```php bin/console debug:translation fr --domain=form```
