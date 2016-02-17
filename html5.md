
Balise Personnalisée
--------------------
```
<maBalise></maBalise>
```

**Problème :** IE < 9 ne permet pas d'utiliser de styles sur des balises inconnues.

**Solution :** (forcément dane une balise <head>)

    <!--[if lt IE 9]>
    <script src="http://html5shiv.googlecode.com/svn/trunk/html5.js"></script>
    <![endif]-->

