Show project dependences tree with composer :
---------------------------------------------

- Complete tree :
```
composer show --tree --ansi --no-interaction
```

- Specific vendor tree :
```
composer show twig/twig --tree --ansi --no-interaction
```
- Composer use a local repository :

https://stackoverflow.com/questions/17426192/composer-using-a-local-repository

- Bypassing composer memory limit error:
```
php -d memory_limit=-1 /usr/local/bin/composer <..>
```
