Strace
------
Permet de savoir ce que fait un processus. Utile pour savoir où un problème survient, ou quelle ressource est le plus consommée par le processus.

    strace -o strace.out rm -f /etc/yp.conf
Ou pour voir ce que fait un processus en particulier
```
strace -c -p mypid
```
Suivi de CTRL+C pour voir l'output.

