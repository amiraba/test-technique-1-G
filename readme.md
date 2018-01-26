Problème 1
Un magasin peut recevoir une note par critère (tableau de notation) de 0 à 10(entier, peut être vide).  Cette note étant donné par un testeur (pas par un utilisateur).

0 signifie que le magasin est très mauvais sur ce critère.
5 moyen
10 très bon.

Exemple :
notationShop [0] = {4,3,3,0,5,4,6 } 
notationShop [1] = {0,null,2,1,3,4 } 
notationShop [2] = {null,null,null,null,6,null,9 } 
notationShop [3] = {3,4,3,2,5,1,4}  
notationShop […] = {…}  

Par exemple le premier critère peut être la décoration, le second le service, etc.

Parfois le magasin n’a pas été noté (=null). Cela signifie que pour ce critère le testeur n’a pas d’avis. ATTENTION Null n’est donc pas équivalent à 0. 

D’autre part, un utilisateur peut pondérer ces notations (entier entre 0 et 5, 0 par défaut). 
Par exemple, un utilisateur va dire que la décoration est très importante et donner 5 sur ce critère, et que le prix l’est moins et donner 2 sur ce critère.
0 veut donc dire que ce critère n’a aucune importance pour lui (il n’y a pas de null pour les pondérations).

Cela permet de calculer la note d’un magasin pour un utilisateur donné.
Ex : 
un utilisateur pense que toutes les notes sont d’égale importance
weightUser [0] = {1,1,1,1,1,1,1}

Ainsi, le magasin 0 précédent aura une note = 4 + 3 + 3 + 0 + 5 + 4 + 6=25

Un autre utilisateur ne privilégie que les 3 premiers critères, en leur donnant une importance croissante, mais trouve que les autres critères ne lui sont pas utiles.
weightUser [1] = {1,2,3,0,0,0,0}

Ainsi, le même magasin 0 aura une note = 4*1+3*2+3*3+0*0+5*0+4*0+6*0=19

Ecrire une fonction qui classe, pour un utilisateur, les magasins en fonction de la pondération de l'utilisateur et des notations du magasin. 

Expliquez comment vous gérez les valeurs "null" pour que les notes soient comparables d’un magasin à un autre.

Par exemple, pour l’utilisateur 0, le magasin 2 devrait être mieux noté que le 3.
Lots de tests
notationShop [0] = {4,3,3,0,5,4,6 } 
notationShop [1] = {0,null,2,1,3,4,null} 
notationShop [2] = {null,null,null,null,6,null,9} 
notationShop [3] = {3,4,3,2,5,1,4}  
notationShop [4] = {null,4,3,null,5,0,1}  
notationShop [5] = {2,2,3,5,5,9,null}  



weightUser [0] = {1,1,1,1,1,1,1}
weightUser [1] = {1,1,2,0,0,0,0}
weightUser [2] = {1,0,1,0,1,0,0}
weightUser [3] = {0,0,1,1,1,0,4}

 
Problème 2
Définir une fonction qui affiche une note pour chaque magasin et chaque utilisateur. Préciser le calcul de la notation. Elle doit permettre d’avoir des notes comparables aussi bien entre les magasins qu’entre les utilisateurs.

Par exemple,  l’utilisateur  0 a tout pondéré à 1, alors que l’utilisateur 2 n’a pas tout pondéré. Si on utilise le calcul précédent pour le magasin 0, on obtient :
25 pour l’utilisateur 0
13 pour l’utilisateur 1
Ces points ne sont pas vraiment comparables.
Trouvez une formule pour rendre ces scores plus comparables.

Ecrire cette fonction.


