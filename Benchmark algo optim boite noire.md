# Benchmark algo optim boite noire 

Pour le poster de la semaine prochaine, j'ai enfin (ça m'a pris 2j presque) comparé les algo d'optim de NLopt. Résultat des courses :

- petit budget de calcul : 100-300 iterations : DIRECT donne les meilleurs résultats, de façon reproductible (déterministe). Il trouve l'optimum global à 1 ou 2% près (en dimensionnement, ça fait plus d'écart)
- moyen budget ~1000-3000 iter : CRS2 meilleur et assez fiable malgé l'aspect stochastique. Il bat DIRECT à tous les coup à partir de 700 iter
- algo local (Nelder Mead ou Subplex) : le multistart est impératif

Condition expérimentales : 

- 3 variantes du même problème d'optim (4 variables : Gen, Batt, PV, Wind) : 3 valeurs différentes du load shed_max autorisé
- 10 runs randomisé (graine aléatoire et initialisation x0)
  - sur les graphs, je trace soit la moyenne sur les 10, ou bien le min/max

Perspectives :

- ajouter le PSO de PREMO (mais je ne l'ai pas sous la main !!)
- ajouter un algo local en multistart

(mais comme il faut que je fasse le poster, je vais m'arrêter là...)