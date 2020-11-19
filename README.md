# Memo-Python

## Les calculs simples

La priorité des opérations mathématiques sont respectés
Les multiplications et les divisions sont prioritaires

```python
calcul = 5 + 2 * 3
print("Calcul : " + str(calcul))
```

```python
calcul = (6 + 3) * 2
print("Calcul : " + str(calcul))
```

Pour calculer une puissance, on utilise **
```python
calcul = 5**2
print("Calcul : " + str(calcul))
```


Division euclidienne ou division entière (c’est-à-dire une division dont le résultat est un entier).

Pour réaliser une division entière, il faut utiliser // 
```python
calcul = 7 // 2
print("Calcul : " + str(calcul))
```

Pour une vraie division
```python
calcul = 7 / 2
print("Calcul vrai division : " + str(calcul))
```


L’opérateur % (appelé opérateur modulo) fournit le reste de la division entière d’un nombre par un autre.
```python
calcul = 7 % 2
print("Calcul : " + str(calcul))
calcul = 6 % 2
print("Calcul : " + str(calcul))
```


## Les conditions

```python
x = -2
if x > 0:
    print(x, "est positif")
else:
    print(x, "est négatif ou nul")
print("Fin")
```

Le mot clé `elif` Si la condition précedente n'est pas vraie, alors essaye cette condition :
```python
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

```python
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```

Notations racourcies :

`if a > b: print("a is greater than b")`

ou

`print("A") if a > b else print("B")`

## Les boucles

```python
for i in range(4):
    print("i a pour valeur", i)
```
resultat =>

i a pour valeur 0

i a pour valeur 1

i a pour valeur 2

i a pour valeur 3

` range(start, stop[, step]) -> range object`
Return an object that produces a sequence of integers from start (inclusive)
to stop (exclusive) by step.  range(i, j) produces i, i+1, i+2, ..., j-1.
start defaults to 0, and stop is omitted!

```python
for k in range(18, 24, 1):
    print("k a pour valeur", k)


c = ["Marc", "est", "dans", "le", "jardin"]
for i in range(len(c)):
    print("i vaut", i, "et c[i] vaut", c[i])


z = 1
while z < 10:
    print("z a pour valeur", z)
    z = z * 2
print("Fin")
```


break: fait sortir de la boucle et passer à l’instruction suivante
```python
for u in range(10):
    print("debut iteration", u)
    print("bonjour")
    if u == 2:
        break
    print("fin iteration", u)
print("apres la boucle")
```


continue : permet de passer prématurément au tour de boucle suivant
```python
for g in range(4):
    print("debut iteration", g)
    print("bonjour")
    if g < 2:
        continue
    print("fin iteration", g)
print("apres la boucle")
```

## Les Tuples

A partir des types de base, il est possible d’en élaborer de nouveaux. On les appelle des types construits.

Un exemple de type construit est le tuple. Il permet de créer une **collection ordonnée de plusieurs éléments**.

```python
a = (3, 4, 7)
print(type(a))
=> <class 'tuple'>


b, c = 5, 6


(d, e) = (7, 8)


f = (99, 204)
u, v = f


def test():
     return (456, 789)

s,t = test()
```


Comment itérer sur les éléments d’un tuple ?
Comme une liste, il est possible de parcourir un tuple avec une boucle for.

```python
tuple = (5, 6, 7)

for i in tuple:
    print(i)
```

La valeur d’un élément du tuple est obtenue en utilisant la même syntaxe que pour une liste.

```python
print("Variable Tuple :",tuple[0])
print("Variable Tuple :",tuple[1])
print("Variable Tuple :",tuple[2])
```

## Les dictionnaires


Un dictionnaire en Python va permettre de rassembler des éléments mais ceux-ci seront identifiés par une clé.

`mon_dictionnaire = {"voiture": "véhicule à quatre roues", "vélo": "véhicule à deux roues"}`

On accède à une valeur du dictionnaire en utilisant la clé entourée par des crochets avec la syntaxe suivante :

`print(mon_dictionnaire["voiture"])`


Ajouter un élément à un dictionnaire. Il suffit d’affecter une valeur pour la nouvelle clé.

```python
mon_dictionnaire["tricycle"] = "véhicule à trois roues"
print(mon_dictionnaire["tricycle"])
```

Comment créer un dictionnaire ?

```python
nombre_de_pneus = {}
nombre_de_pneus["voiture"] = 4
nombre_de_pneus["vélo"] = 2
nombre_de_pneus["tricycle"] = 3

print(nombre_de_pneus)
```

Exemple boucles for avec un indice i

```python
for i in nombre_de_pneus.items():
    print(i)

for cle, valeur in nombre_de_pneus.items():
    print("l'élément de clé", cle, "vaut", valeur)
```

## Les différents scopes

```python
def scope_test():
    
    def do_local():
        spam = "local spam"

    def do_nonlocal():
        nonlocal spam
        spam = "nonlocal spam"

    def do_global():
        global spam
        spam = "global spam"

    spam = "test spam"
    do_local()
    print("After local assignment:", spam)
    
    do_nonlocal()
    print("After nonlocal assignment:", spam)
    
    do_global()
    print("After global assignment:", spam)

scope_test()
print("In global scope:", spam)
```

Ce qui donne :

After local assignment: test spam

After nonlocal assignment: nonlocal spam

After global assignment: nonlocal spam

In global scope: global spam


Le mot clé nonlocal est utilisé pour travailler avec des variables à l'intérieur de fonctions imbriquées, où la variable ne doit pas appartenir à la fonction interne. 
Utilisez le mot clé nonlocal pour déclarer que la variable n'est pas locale.

## Héritage


```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)


class Student(Person):
  
    def __init__(self, fname, lname, year):
        super().__init__(fname, lname)
        self.graduationyear = year
    
    def welcome(self):
        print("Welcome", self.firstname, self.lastname, "to the class of", self.graduationyear)



x = Person("John", "Doe")
x.printname()

y = Student("Mike", "Olsen", 2019)
y.printname()
y.welcome()

```
