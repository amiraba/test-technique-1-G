Probl�me 1
Un magasin peut recevoir une note par crit�re (tableau de notation) de 0 � 10(entier, peut �tre vide).  Cette note �tant donn� par un testeur (pas par un utilisateur).

0 signifie que le magasin est tr�s mauvais sur ce crit�re.
5 moyen
10 tr�s bon.

Exemple :
notationShop [0] = {4,3,3,0,5,4,6 } 
notationShop [1] = {0,null,2,1,3,4 } 
notationShop [2] = {null,null,null,null,6,null,9 } 
notationShop [3] = {3,4,3,2,5,1,4}  
notationShop [�] = {�}  

Par exemple le premier crit�re peut �tre la d�coration, le second le service, etc.

Parfois le magasin n�a pas �t� not� (=null). Cela signifie que pour ce crit�re le testeur n�a pas d�avis. ATTENTION Null n�est donc pas �quivalent � 0. 

D�autre part, un utilisateur peut pond�rer ces notations (entier entre 0 et 5, 0 par d�faut). 
Par exemple, un utilisateur va dire que la d�coration est tr�s importante et donner 5 sur ce crit�re, et que le prix l�est moins et donner 2 sur ce crit�re.
0 veut donc dire que ce crit�re n�a aucune importance pour lui (il n�y a pas de null pour les pond�rations).

Cela permet de calculer la note d�un magasin pour un utilisateur donn�.
Ex : 
un utilisateur pense que toutes les notes sont d��gale importance
weightUser [0] = {1,1,1,1,1,1,1}

Ainsi, le magasin 0 pr�c�dent aura une note = 4 + 3 + 3 + 0 + 5 + 4 + 6=25

Un autre utilisateur ne privil�gie que les 3 premiers crit�res, en leur donnant une importance croissante, mais trouve que les autres crit�res ne lui sont pas utiles.
weightUser [1] = {1,2,3,0,0,0,0}

Ainsi, le m�me magasin 0 aura une note = 4*1+3*2+3*3+0*0+5*0+4*0+6*0=19

Ecrire une fonction qui classe, pour un utilisateur, les magasins en fonction de la pond�ration de l'utilisateur et des notations du magasin. 

Expliquez comment vous g�rez les valeurs "null" pour que les notes soient comparables d�un magasin � un autre.

Par exemple, pour l�utilisateur 0, le magasin 2 devrait �tre mieux not� que le 3.
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

 
Probl�me 2
D�finir une fonction qui affiche une note pour chaque magasin et chaque utilisateur. Pr�ciser le calcul de la notation. Elle doit permettre d�avoir des notes comparables aussi bien entre les magasins qu�entre les utilisateurs.

Par exemple,  l�utilisateur  0 a tout pond�r� � 1, alors que l�utilisateur 2 n�a pas tout pond�r�. Si on utilise le calcul pr�c�dent pour le magasin 0, on obtient :
25 pour l�utilisateur 0
13 pour l�utilisateur 1
Ces points ne sont pas vraiment comparables.
Trouvez une formule pour rendre ces scores plus comparables.

Ecrire cette fonction.


