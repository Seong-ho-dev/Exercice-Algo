Exercice de tri et de recherche 

Exercice 3 : Trier Puis chercher 

On consideère le tableau : [45, 12, 89, 23, 67, 34, 5, 78]
FONCTION triABulles(tableau) 
n ← longueur(tableau) 
 POUR i de 0 à n - 2   
 POUR j de 0 à n - 2 - i 
  SI tableau[j] > tableau[j + 1] 

temp ← tableau[j] 
  tableau[j] ← tableau[j + 1] 
 tableau[j + 1] ← temp 
FIN SI 

     FIN POUR 
FIN POUR

FIN FONCTION

[5, 12, 23, 34, 45, 67, 78, 89]

Exercice 
FONCTION rechercheDichotomique(tableau, element)
 debut ← 0
   fin ← longueur(tableau) – 1
    TANT QUE debut ≤ fin
   milieu ← (debut + fin) / 2
 SI tableau[milieu] = element
 RETOURNER milieu
 SINON SI tableau[milieu] < element
 debut ← milieu + 1
 SINON
 fin ← milieu - 1 
 FIN SI
  FIN TANT QUE
 RETOURNER -1 
   FIN FONCTION
 
Etape 1 : 
debut = 0, fin = 7
milieu = (0 + 7) / 2 = 4
tableau[4] = 45

Exercice 2 :
 FONCTION rechercherToutesOccurrences(tableau, element)
 positions ← [] 
 POUR i de 0 à longueur(tableau) – 1
 SI tableau[i] = element
 ajouter i dans positions
 FIN SI

 FIN POUR
 
 RETOURNER positions

FIN FONCTION

 nombres ← [3, 7, 2, 7, 5, 7, 2, 9, 3, 7]
 positions ← rechercherToutesOccurrences(nombres, 7)
 → positions = [1, 3, 5, 9]



 Exercice 3 :

 Soit le tableau trié : [2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78]
Écrire l'algorithme de recherche dichotomique complet,
Tracer l'exécution pour rechercher le nombre 5,
Indiquer les valeurs de debut, fin et milieu à chaque étape

On consideère le tableau : [2, 5, 8, 12, 16, 23, 38, 45, 56, 67, 78]

FONCTION rechercheDichotomique(tableau, element)
 debut ← 0
   fin ← longueur(tableau) – 1
    TANT QUE debut ≤ fin
   milieu ← (0 + 2) / 2
 SI tableau[1] = element
 RETOURNER milieu
 SINON SI tableau[1] < element
 debut ← milieu + 1
 SINON
 fin ← 1 - 1 
 FIN SI
  FIN TANT QUE
 RETOURNER -1 
   FIN FONCTION
   
   Etape 1 : 
   debut = 1, fin = 10
milieu = (1 + 10) / 2 = 6
tableau[1] = 5
5 < 23 → chercher à droite
debut = 2
 
 Etape 2 : 
 debut = 2, fin = 10
milieu = ( 1+ 10) / 2 = 5
tableau[1] = 5
5 < 23 → chercher à droite
debut = 3
