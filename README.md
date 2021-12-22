# Chiffrement Affine En Python3
Programme de chiffrement et déchiffrement affine d'un message en python3.

# Explication du chiffrement affine avec complexité O(n2)
1. D’abord on donne une liste d’alphabet en minuscule et une liste d’alphabet en majuscule.

2. On parcourt tout l’alphabet et on append l’alphabet en minuscule et l’alphabet en majuscule à 
chaque parcourt.

3. On crée une fonction qui retourne le pgcd de deux nombres a et b, qui change la position de a et 
b à chaque parcourt et effectue le modulo de a et b. 

4. Ensuite on a une fonction de chiffrementAffine qui prend en paramètre a, b et L qui servira plus 
tard pour le chiffrement de notre message, au départ on testera si la lettre est une majuscule ou 
une minuscule après on cherchera l’indice de la lettre qu’on utilisera en appliquant la formule 
Y=(ax+b) mod 26 ou y est l’indice de la lettre chiffre sinon si la lettre n’est pas dans l’alphabet on 
(symbole) on la renverra.

5. Après on a deux fonctions pour calculer l’inverse d’un nombre a, la 1ere n’a pas était vu en cours 
mais elle nécessite moins d’opérations que celle vu en cours et pour cela nous l’avons pris mais 
c ne change pas grande chose puisque la complexité reste la même pour les deux algorithmes. 
Pour le 1ere fonction elle prendra en paramètre a donnera son inverse modulaire 26 d’un 
nombre pour cela on initialise x à 0 et on utilise une boucle tant que a*x%26 n'est pas différent 
de 1, x prend la valeur de x + 1 et finit par retourner la valeur de x à la fin. Et pour la 2eme 
fonction d’Euclide on applique exactement la formule vue en cours pour l’algorithme d’Euclide 
étendu.

6. Par la suite on a une fonction dechiffrementAfiine qui prend les mêmes paramètres de la 
fonction chiffrementAffine et qui fait la même chose que la fonction chiffrementAffine mais la
seule différence est que y prend la valeur de (l’inverse de a)*(x-b) modulo 26.
Au départ on testera si la lettre est une lettre majuscule ou minuscule après on récupéra l’indice 
de la lettre qu’on utilisera pour trouver l’indice de la lettre déchiffre en utilisant la formule 
évoque précédemment sinon si la lettre est un symbole on la renverra.

7. On a deux fonctions l’une crypt et l’autre decrypt, l’une qui sert à crypter notre Jeux d’essais à 
l’aide de la fonction chiffrementAffine et l’autre sert à decrypter notre message, à l’aide de la 
fonction dechiffrementAffine ils vont toute les deux appeler les fonctions chiffrementAffine et 
dechiffrementAffine n fois avec n égale à la taille du message.

8. Finalement on affiche les messages chiffrés et les messages déchiffrés.

# Execution 
`python3 Chiffrement_Affine.py`
