
Balises Personnalisées
--------------------
```
<maBalise></maBalise>
```

**Problème :** IE < 9 ne permet pas d'utiliser de styles sur des balises inconnues; De manière générale, les anciens navigateurs ne connaissent pas les nouvelles balises sémantiques du HTML5.

**Solution :** (forcément dane une balise `<head>`)

    <!--[if lt IE 9]>
    <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->

Balise `<button>`
---------------
**Attention :** Toujours ajouter le type à la balise bug constaté sur du js concernant les balises button sans type.
    
    `<button type="button">`My Button`</button>`

Balise `<video>`
----------------
** voir la doc en ligne **

Attributs
---------
* **autocomplete** : permet au navigateur de conserver en memoire les infos d'un formulaire ou d'un champ
```
<form action="action_page.php" autocomplete="on">...</form>
```
```
First name:<input type="text" name="fname" autocomplete="off">
```
* **autofocus** : le champ de formulaire prend le focus au chargement de la page
```
First name:<input type="text" name="fname" autofocus>
```
* **list** : permet de determiner une liste de valeurs possibles (entrées en autocompletion), pour un input.
```
<input list="browsers">
<datalist id="browsers">
  <option value="Internet Explorer">
  <option value="Firefox">
  <option value="Chrome">
</datalist>
```
localStorage
------------
Rôle de stockage de données sur le navigateur.
**attention:** Name/value pairs are always stored as strings. Remember to convert them to another format when needed!

* contrairement aux cookies, pas d'envoi des localStorage au serveur.
* enregistrement de données sur le client **par domaine**
* https et http on un différent localStorage
* pas de date d'expiration
```
localStorage.setItem("lastname", "Smith");
localStorage.getItem("lastname");
```
ou
```
localStorage.lastname = "Smith";
localStorage.lastname;
```
suppression
```
localStorage.removeItem("lastname");
```
