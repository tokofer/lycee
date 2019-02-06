# lycee
# Cour au lycée Elie cartan
# Affichage simulatané
a=2
b=-5
a,b=a+b,a-b
print("Maintenant, a=",a," et b=",b)
# Affichage séparé 
a=2
b=-5
a=a+b
b=a-b
print(a,b)
# Calcul des termes d'une suite 
U=500
N=0
U=0.7*U+300
N=N+1
print(U) # On peut afficher sur la même ligne en faisant print(U,N)
print(N)
# Définition d'une fonction et image
def f(x):
    return x*x-x+41
x=1
print(f(x))
x=2
print(f(x))
# Technique d'iteration
def f(n):
    return n**2-n+41 # n** retourne le carré de n c'est de n c'est la notation puissance
valeursx=[x for x in range(20)] # permet d'iterer pour x de 0 à 19
valeursf=[f(x) for x in range(20)] # on pouvait écrire aussi valeursf=[f(x)for xin valeursx]
print(valeursx)
print(valeursf)
# Calcul du prix ttc à partir du tva
pht=float(input("Donner une valeur"))
pttc= 1.2*pht
print(pttc)
# Calcul d'un pourcentage d'évolution
p=float(input("Donner une valeur"))
t=float(input("Donner une valeur")) # valeur réelle avec float
f= (1+t/100)*p # evolution de t%
print(f)
# Calcul du prix ht à partir du tva et pttc
pttc=float(input("Donner une valeur"))
pht= pttc/1.2
print(pht)
# resolution de ax=b
a=float(input("Donner une valeur"))
b=float(input("Donner une valeur"))
def soleq(a,b):
    if a!=0: # si a est different de 0
       return b/a
       print(b/a)
    else:
        if b==0:
         return "Il y a une infinité de solution"
        else:
         return("pas de solution")
# Triangle de Pascal         
def lignes_pascal(n):
    """
    Génère les n premières lignes du triangle de Pascal.
    Retourne un générateur de liste.
    """
    if (n < 1) | (int(n)!=n):
        raise ValueError('n doit être un entier positif non nul')
    ligne = [1]           # génération de la première ligne
    yield ligne
    for _ in range(n-1): # génération des n-1 lignes restantes
        ligne.append(0)
        for idx in reversed(range(1, len(ligne))):
            ligne[idx] += ligne[idx-1]
        yield ligne
# test
def output_pascal():
    n= int(input("Donner la valeur de l'entier"))
    for p in lignes_pascal(n): print (p)
# Calcul de la distance entre A et B
from math import*
xA= eval(input("Entrer l'abscisse de A:"))
xB= eval(input("Entrer l'abscisse de B:"))
yA= eval(input("Entrer l'ordonnée de A:"))
yB= eval(input("Entrer l'ordonnée de B:"))
d = sqrt((xB-xA)**2+(yB-yA)**2)
print(d)
# Théorème de Pythagore
nbmax=1000
for a in range(1,nbmax):
    for b in range(a,nbmax):
        for c in range(b,nbmax):
            if a**2+b**2==c**2:
               if a<b<c:
                print(a,b,c)

