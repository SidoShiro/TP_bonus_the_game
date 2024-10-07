# NO-HOLIDAYS

## README

Exercices for 2nd year students in IT, on the C language, made by a sleepful TA... mixing FR/EN wirting, incomplete exercices, stupid jokes, syntax mistakes, etc ... and a **will** to help you guys !

## AUTHORS

sidore\_m

## Table of Contents

 [I Basiques](#basiques)
 
 [II La force est puissante en toi ...](#force)
 
 [III Matrix in Matrix in MATRIX](#matrix)
 
 [IV Sorts ... Sortilièges !!!](#sorts)
 
 [V Lord of the Lakes !](#lord)
 
 [VI Histogramme](#histo)
 
 [VI Rotation 360](#rotate)
 
 [VII Et l'imprimerie fut !](#print)

## Rules

```
Try hard ! Play hard !
```

__Pointers only__ __!__

Vous rendez un fichier exo.c **SANS fonction main()** !!!
Commentez votre main() ou utilisez des directives.

Vous pouvez faire des fonctions supplémentaires (si nécessaire) -- ajouter juste *static* devant.
```c
// Ex:
static int my_secondary_fun(...)
```

*Questions* sur ces exercices:
* ---------->:  marc.sidorenko@epita.fr
* Balise mail: \[ASM\]\[NO-HOLIDAYS\]

```c
// Avec Commentaires

/* My main

int main(void)
{

  ... code here ...

  return 0;
}
*/

// Avec directives if et endif

#if 0
int main(void)
{

  ... code here ...

  return 0;
}
#endif
```


## I  Basiques  <a name="basiques"></a>

### Fibo Rec

Faire fibonacci en récursif.

```c

unsigned fibo_rec(unsigned n);

```

### Fibo Itératif

Et en itératif...

```c

unsigned fibo_ite(unsigned n);

```

### Crible d'Eratosthène

Faire l'algorithme d'érathostène.
Votre fonction doit afficher les nombres premiers compris entre 2 et n (inclus)
Checker que n >= 2 !

```c
void eratosthene(unsigned n);
```

Output for n = 9

```
2
3
5
7
```

Output for n = 5

```
2
3
5
```
### Factorielle Récursive

Faire la factorielle récursive

```c
unsigned fac_rec(unsigned n);
```

### Factorielle Itérative

Faire la factorielle itérative

```c
unsigned fac_ite(unsigned n);
```

## II La force est puissante en toi ... <a name="force"></a>

### PowerOF

Faire une fonction qui calcule la puissance de a par b.
Vous devez gérer les puissances, nulle, positives et **négatives** !

```c
long double power_of(short a, char b);
```

### Solve This ... !

Faire une fonction qui calcule la solution pour une équation du second degré.
Les arguments sont a, b et c, des coeffs tel que : ax² + bx + c
Renvoyez les racines x1 et/ou x2 tel que ax² + bx + c = 0 ou *NO ROOTS* si pas de solution.

Output (print) : dans l'ordre croissant

Retournez le nombre de racines

```c
size_t solve_sec(float a, float b, float c)
```

Output : Pour x² ; a = 1.0f, b = 0.0f, c = 0.0f

```
0
```

Output : Pour x² + 1 ; a = 1.0f, b = 0.0f, c = 1.0f

```
NO ROOTS
```

Output : Pour x² - 1 ; a = 1.0f, b = 0.0f, c = -1ty.0f

```
-1
1
```


## III Matrix in Matrix in MATRIX  <a name="matrix"></a>

Fonctions sur les matrices de taille NxN !

```
Matrice avec N = 3 d'où 3x3
// En mémoire :
0|1|2|3|4|5|6|7|8

// Traité tel que :
0|1|2
3|4|5
6|7|8
```

Somme de A et B.
Le retour de la fonction est une matrice NxN allouée via (malloc/calloc/realloc)

```c
int *sum_matrix(int *A, int *B, size_t N);
```

Soustraction de A par B
Le retour de la fonction est une matrice NxN allouée via (malloc/calloc/realloc)

```c
int *sub_matrix(int *A, int *B, size_t N);
```

Produit de matrice A par B (c-a-d A * B = C)
Le retour de la fonction est une matrice NxN allouée via (malloc/calloc/realloc)

```c
int *prod_matrix(int *A, int *B, size_t N);
```

Transpose une matrice de taille NxN

```c
void transpose(int *A, size_t N);
```

## IV Sorts ... Sortilièges !!!  <a name="sorts"></a>

Les *sorts* seront appliqué a des tableaux \*t de n valeurs de type (int).

### Bubble sort

```c
void bubble_sort(int *t, size_t n);
```

### Insert sort

```c
void insert_sort(int *t, size_t n);
```

### Quick sort

```c
void quick_sort(int *t, size_t n);
```

### Insert sort avec recherche dichotomique

```c
void insert_sort_bin(int *t, size_t n);
```

### Insert sort avec interpolation linéaire

Pour votre culture :)

```c
void insert_sort_inter(int *t, size_t n);
```

## V Lord of the Lakes !  <a name="lord"></a>

### 1, 2 ou 3 lacs un truc comme ça

Vous devez calculer le nombre de lacs contenu dans une carte donnée en
paramètre.

Exemple de carte :

```
MAP =

    j_len
   ________
  |00000000
i |01000100
_ |00011100
l |00110000
e |00000100
n |00000000
  |11111000

```

```c
size_t nb_lakes(int **map, size_t i_len, size_t j_len);
```

Output for MAP

```
4
```

## VI Histogramme  <a name="histo"></a>

**/!\ malloc(3), realloc(3), calloc(3) interdit !!!**

> Protip : Faire un histogramme, représentant la fréquence de chaque caractère, avec la chaîne donné en paramètre.

Afficher le charactère avec la plus grosse fréquence (et sa fréquence) puis celui avec la plus basse.

```c
void best_and_worst_freq(const char* str);
```

Output : pour la chaîne "bbaaac"

```
a : 3
c : 1
```

Output : pour la chaîne "??aaaabb"

```
a : 4
? : 2
c : 2
```

Output : pour la chaîne "aaaa"

```
a : 4
```

Output : pour la chaîne "Abcd"

```
A : 1
b : 1
c : 1
d : 1
```

## VII Rotatation 360 <a name="rotate"></a>

### Rotation d'une lettre

Faites varier votre lettre ascii de 'n', vers *l'avant* quand n > 0 et vers *l'arrière* quand n < 0, travaillez dans l'intervale [0;25].
Vous devez gérer les minuscules et majuscules.

```c
void rotchar(char x, size_t n);
```

### Rotatation d'une chaîne de caractères

Appliquez **rotchar()** sur un tableau de charactères. Si le caractère n'est ni une majuscule, ni une minuscule, ne pas la modifier.

char* str finira toujours par un **'\0'**

```c
void rotchar_array(char* str, size_t n); 
```

Output pour str = "Ah ? CouCou!!!" n = 2

```
Cj ? EqwEqw!!!
```

### Rotatation tableau d'entiers 

**TODO**

## Et l'imprimerie fut ! <a name="print"></a>

### Le sapin

Vous devez afficher un sapin, exactement comme dans l'example.

Output (les **$** représentent des **\n**, testez avec :

```shell
cat -e
```

```
  *$
 ***$
*****$
  *$
```

```c
void print_pine();
```

### Le sapin de taille n

Même chose, mais votre sapin peut avoir une taille différente, la taille n doit être minimum de 3, sinon n'afficher rien.

Le tronc sera toujours de 1.

```c
void print_variadic_pine(unsigned n);
```

Output : pour n = 5

```
    *$
   ***$
  *****$
 *******$
*********$
    *$
```

Output : pour n = 4

```
   *$
  ***$
 *****$
*******$
   *$
```

### Affichage de tableau qui ont du style !

**/!\ Respectez à au caractère près l'affichage. (Toujours en générale)**

Pour un tableau de n entier afficher chaque entier avec un *padding* équivalent a la taille du plus grand entier.

> Utilisez \%\*u dans printf (lisez le **man**)

Pour faire simple vous gérer que les tableaux avec des entiers positif.

```c
void print_with_style(unsigned* tab, unsigned size);
```

Output pour tab = { 0, 34 35, 100, 56, 207 };

```
+-----+-----+-----+-----+-----+-----+
|   0 |  34 |  35 | 100 |  56 | 207 |
+-----+-----+-----+-----+-----+-----+
```

Output pour tab = { 0, 3 5 };

```
+---+---+---+
| 0 | 3 | 5 |
+---+---+---+
```

Output pour tab = { 100500, 1 };

```
+--------+--------+
| 100500 |      1 |
+--------+--------+
```
