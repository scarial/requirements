# Sublime Text Tips





### Effective research using CTRL+SHIFT+F

#### Exclude a directory from search results
prefix pattern with a dash `-` in the `Where` field.

Ex: I search in all .php files, but exclude results from directories having '/vendor/' inside their path :

```
*.php,-*/vendor/*
```

#### Show more line context in the serarch results
The idea is to use a regexp to extend the context displayed, adapting the following pattern inside the `Find` field :

```
(.*\n){0,2}.*search_string.*(\n.*){0,2}
```
where `search_string` is to replace with your actual searched string
