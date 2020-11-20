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

Les puissances

```python
def carre(valeur):
    resultat = valeur**2
    return resultat

def cube(valeur):
    resultat = valeur**3
    return resultat
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


c = ["Prénom1", "Prénom2", "Prénom3"]
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

## Les listes

```python
thislist = ["el1", "el2", "el3"]
for x in thislist:
  print(x)
```

```python
thislist = ["el1", "el2", "el3"]
for i in range(len(thislist)):
  print(thislist[i])
```

```python
thislist = ["el1", "el2", "el3"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1
```

### Modification de listes

```python
thislist = ["el1", "el2"]
thislist[1] = "blackcurrant"
print(thislist)
```

```python
thislist = ["el1", "el2", "el3"]
thislist[1] = ["el2-1", "el2-2"]
print(thislist)

=> ['el1', ['el2-1', 'el2-2'], 'el3']
```

```python
thislist = ["el1", "el2", "el3", "el4"]
thislist[1:3] = ["nouveau-2", "nouveau-3"]
print(thislist)

=> ['el1', 'nouveau-2', 'nouveau-3', 'el4']
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


## Gestion des exceptions

```python
try:
  print(x)
except:
  print("An exception occurred")
  
  
try:
  print(x)
except NameError:
  print("Variable x is not defined")
except:
  print("Something else went wrong")
  
  
# Si aucune exception est levé
try:
  print("Hello")
except:
  print("Something went wrong")
else:
  print("Nothing went wrong")
  
  
try:
  print(x)
except:
  print("Something went wrong")
finally:
  print("The 'try except' is finished")
  
  
  
x = -1

if x < 0:
  raise Exception("Sorry, no numbers below zero")
  
  
  
try:
  f = open("demofile.txt")
  f.write("Lorum Ipsum")
except:
  print("Something went wrong when writing to the file")
finally:
  f.close()
  
  
x = "hello"

if not type(x) is int:
  raise TypeError("Only integers are allowed")
  
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


## Classe



Par convention en Python, le nom identifiant une classe (qu’on appelle aussi son identifiant) débute par une majuscule

```python
class Point:
    # Exemple Doc sur une seule ligne ->  "Definition d'un point geometrique"

    """
        Presentation de la classe avec plusieurs lignes\n
        Super youpi!!!
    """
    
    # Constructeur sans parametre
    #def __init__(self):
    #    self.x = 0
    #    self.y = 0

    # Constructeur avec parametre
    def __init__(self, x, y):
        self.x = x
        self.y = y
    

    def deplace(self, dx, dy):
        self.x = self.x + dx
        self.y = self.y + dy
```

Note : ici les attributs de classe sont publiques


### Définition d’attributs privés
On réalise la protection des attributs de notre classe Point grâce à l’utilisation d’attributs privées.
Pour avoir des attributs privés, leur nom doit débuter par __ 

```python

class Point:
    def __init__(self, x, y):
        self.__x = x
        self.__y = y

    def deplace(self, dx, dy):
        self.__x = self.__x + dx
        self.__y = self.__y + dy

    def affiche(self):
        print("abscisse =", self.__x, "ordonnee =", self.__y)
```

```python
class Point:
    def __init__(self, x, y):
        self.__x = x
        self.__y = y

    def get_x(self):
        return self.__x

    def get_y(self):
        return self.__y

    def set_x(self, x):
        self.__x = x

    def set_y(self, y):
        self.__y = y
```

### Les attributs de classe

```python
class A:
    nb = 0

    def __init__(self, x):
        print("creation objet de type A")
        self.x = x
        A.nb = A.nb + 1
        
print("A : nb = ", A.nb)
print("Partie 1")
a = A(3)
print("A : nb = ", A.nb)
print("a : x = ", a.x, " nb = ", a.nb)
print("Partie 2")
b = A(6)
print("A : nb = ", A.nb)
print("a : x = ", a.x, " nb = ", a.nb)
print("b : x = ", b.x, " nb = ", b.nb)
c = A(8)
print("Partie 3")
print("A : nb = ", A.nb)
print("a : x = ", a.x, " nb = ", a.nb)
print("b : x = ", b.x, " nb = ", b.nb)
print("c : x = ", c.x, " nb = ", c.nb)
```

A : nb =  0

Partie 1

creation objet de type A

A : nb =  1

a : x =  3  nb =  1     

Partie 2

creation objet de type A

A : nb =  2

a : x =  3  nb =  2     

b : x =  6  nb =  2     

creation objet de type A

Partie 3

A : nb =  3

a : x =  3  nb =  3     

b : x =  6  nb =  3     

c : x =  8  nb =  3     



### Les méthodes de classe

Pour créer une méthode de classe, il faut la faire précéder d’un « décorateur » : `@classmethod`

Le premier argument de la méthode de classe doit être `cls`.

```python
class A:
    nb = 0

    def __init__(self):
        print("creation objet de type A")
        A.nb = A.nb + 1
        print("il y en a maintenant ", A.nb)

    @classmethod
    def get_nb(cls):
        return A.nb

print("Partie 1 : nb objets = ", A.get_nb())
a = A()
print("Partie 2 : nb objets = ", A.get_nb())
b = A()
print("Partie 3 : nb objets = ", A.get_nb())
```

- Une méthode de classe est une méthode liée à la classe et non à l'objet de la classe.

- Ils ont accès à l'état de la classe car il prend un paramètre de classe qui pointe vers la classe et non l'instance d'objet.

- Il peut modifier un état de classe qui s'appliquerait à toutes les instances de la classe. Par exemple, il peut modifier une variable de classe qui sera applicable à toutes les instances.


```python
class Student(object):

    @classmethod
    def from_string(cls, name_str):
        first_name, last_name = map(str, name_str.split(' '))
        student = cls(first_name, last_name)
        return student

scott = Student.from_string('Scott Robinson')
```

We generally use **class method** to create factory methods. Factory methods return class object ( similar to a constructor ) for different use cases.

We generally use **static methods** to create utility functions.

### Méthode statique

```python
class C:
    
    @staticmethod
    def maMethode(arg1, arg2, ...):
        ...
```

Une méthode statique ne reçoit pas de premier argument implicite.

- Une méthode statique est également une méthode liée à la classe et non à l'objet de la classe.

- Une méthode statique ne peut pas accéder ou modifier l'état de la classe.

- Il est présent dans une classe car il est logique que la méthode soit présente dans la classe.


Ces types de méthodes ne sont généralement pas destinés à créer / instancier des objets,
mais ils peuvent contenir un type de logique appartenant à la classe elle-même, comme une méthode d'assistance ou d'utilitaire.


### Exemple plus long

```python
class ClassGrades:

    def __init__(self, grades):
        self.grades = grades

    @classmethod
    def from_csv(cls, grade_csv_str):
        grades = map(int, grade_csv_str.split(', '))
        cls.validate(grades)
        return cls(grades)


    @staticmethod
    def validate(grades):
        for g in grades:
            if g < 0 or g > 100:
                raise Exception()

try:
    # Try out some valid grades
    class_grades_valid = ClassGrades.from_csv('90, 80, 85, 94, 70')
    print 'Got grades:', class_grades_valid.grades

    # Should fail with invalid grades
    class_grades_invalid = ClassGrades.from_csv('92, -15, 99, 101, 77, 65, 100')
    print class_grades_invalid.grades
except:
    print 'Invalid!'
    
```

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


## Ecrire dans un fichier

```python
try:
  f = open("demofile.txt")
  f.write("Lorum Ipsum")
except:
  print("Something went wrong when writing to the file")
finally:
  f.close()
```
