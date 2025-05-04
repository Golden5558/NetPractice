# NetPractice
My NetPractice experience

- Tableau magique des masques utiles :

CIDR	Masque	Saut	IP de début typique	IP de fin typique

/24   255.255.255.0	    256	  .0	.255

/25  	255.255.255.128 	 128	  .0, .128	.127, .255

/26  	255.255.255.192	  64	   .0, .64, .128, .192	.63, .127, .191, .255

/27	  255.255.255.224	  32	   .0, .32, .64, .96, etc.	.31, .63, .95, .127, etc.

/28	  255.255.255.240	  16	   .0, .16, .32, .48, etc.	.15, .31, .47, .63, etc.

/29	  255.255.255.248	  8	    .0, .8, .16, .24, etc.	.7, .15, .23, .31, etc.

/30	  255.255.255.252	  4	    .0, .4, .8, .12, etc.	.3, .7, .11, .15, etc.

— Comment Calculer les Plages IP Manuellement
Étapes pour n'importe quelle IP et masque :
Écris le masque en /XX (par exemple /26).

Déduis la taille d'un bloc :

Taille du bloc
=
2
(
32
−
CIDR
)
Taille du bloc=2 
(32−CIDR)
 
Exemple : /26 → 32-26 = 6 bits → 
2
6
=
64
2 
6
 =64 IP.

Calcule les plages :

Départ = multiple de la taille du bloc.

Exemple pour /26 → plages 0-63, 64-127, 128-191, 192-255 sur le dernier octet.

Détermine :

Adresse réseau (début de la plage)

Adresse broadcast (fin de la plage)

Plage utilisable = adresse réseau +1 → adresse broadcast -1
