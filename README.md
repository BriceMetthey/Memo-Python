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

## xxx

La valeur d’un élément du tuple est obtenue en utilisant la même syntaxe que pour une liste.

```python
print("Variable Tuple :",tuple[0])
print("Variable Tuple :",tuple[1])
print("Variable Tuple :",tuple[2])
```

