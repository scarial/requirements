same as
-------
Comparaison stricte d'une variable twig (équivalent de === en php)

Ex:
```
{% if foo.attribute is same as(false) %}
    the foo attribute really is the 'false' PHP value
{% endif %}
```


default
-------
Permet de tester l'existance d'une variable et qu'elle ne vaut pas `null`

Ex:
```
{% if var is defined and var is not null %}

one can instead simply do this:

{% if var|default is not empty %}

or even more simply:

{% if var|default %}
```
