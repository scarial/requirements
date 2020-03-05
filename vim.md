### How to comment multiple lines at once in vim (mainly for contrab full commenting usage)

#### For commenting:

`:66,70s/^/#`
#### For uncommenting:

`:66,70s/^#/`

Obviously, here we're commenting lines from 66 to 70 (inclusive).

If you want to comment `//` instead of `#` need to escape them with `\`. `:66,70s/^/\/\/`
