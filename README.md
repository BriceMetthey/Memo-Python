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
