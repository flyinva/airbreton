L'association [AirBreizh publie des données de qualité de l'air](http://www.airbreizh.asso.fr/) sous forme de tableaux HTML mises à jour de temps en temps. Le but de ce script est de télépcharger les données et de les mettre en forme en vue d'une réutilisation par une machine.

Le script télécharge les données du tableau HTML et créée un fichier texte de la forme :

```
timestamp,data1,data2,data3,dataX
```

Le script peut être exécuté via une cron. Il n'ajoutera des lignes au fichier texte uniquement s'il y a de nouvelles données (la mise à jour par AirBreizh n'est pas régulière et il peut y avoir plusieurs heures d'un coup).

C'est écrit en BASH en prenant en compte [quelques bonnes pratiques](https://github.com/progrium/bashstyle/).