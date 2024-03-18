# Reto-7
1. Imprimir un listado con los números del 1 al 100 cada uno con su respectivo cuadrado.
```python
#Se declara la variante del número
n:int=0
#Se hace el loop cuando el número es igual o menor que 100
while n<=100:
#Se saca el cuadrado y se imprime el número con su cuadrado
    c=n**2
    print(str(n)+" al cuadrado es "+str(c))
#Se añade 1 al número y se repite hasta llegar a 100
    n=n+1
```   
2.  Imprimir un listado con los números impares desde 1 hasta 999 y seguidamente otro listado con los números pares desde 2 hasta 1000.
```python
#Se hace la variable de los impares
ni:int=1
#Se hace el loop para los impares, añadiendo de a 2 después de cada loop
while ni<=999:
    print(str(ni))
    ni=ni+2
#Luego lo mismo para los impares, casi se muere mi computador ejecutando el código
np:int=2
while np<=1000:
    print(str(np))
    np=np+2
```   
3.  Imprimir los números pares en forma descendente hasta 2 que son menores o iguales a un número natural n ≥ 2 dado
```python
#Se toma el número
n=int(input("Número? "))
#Se determina si el número es par o impar, si es impar se le resta uno para que se vuelva par
if n%2==1:
    x=n-1
else:
    x=n
#Se imprime el número y se le va restando de a 2, y se repite hasta que llegue a 2
while 2<=x<=n:
    print (str(x))
    x=x-2
```   
4. En 2022 el país A tendrá una población de 25 millones de habitantes y el país B de 18.9 millones. Las tasas de crecimiento anual de la población serán de 2% y 3% respectivamente. Desarrollar un algoritmo para informar en que año la población del país B superará a la de A.
```python
#Se declara la población A, B y un número i que va a contar las iteraciones
a=float(25)
b=float(18.9)
i=0
#Siempre que A sea menor que B, se añade una iteración al número i y se multiplican las poblaciones por sus porcentajes de crecimiento
while a>b:
    a=a*1.002
    b=b*1.003
    i=i+1
#Se imprime el número i final que corresponde a los años
print("La población B superará a la pblación A en "+str(i)+" años")
```
5. Imprimir el factorial de un número natural n dado.
```python
#Se toma el número
n=int(input("Número? "))
#Se determina una variable que nos servirá para multiplicar
f=1
while n>1:
#Se multiplica nuestra variable por el número y se actualiza, mientras que se le resta de a 1 al número
    f=f*n
    n=n-1
print("El factorial del número es "+str(f))
``` 
6. Implementar un algoritmo que permita adivinar un número dado de 1 a 100, preguntando en cada caso si el número es mayor, menor o igual.
```python
#Se toma el 50 como primer intento de acertar, ya que está en la mitad
s=input("50 es el número? ")
#Se establece n como el número que cambia para adivinar el número
n=int(50)
#Cuando el sistema reciba como respuesta "si", se determina que es el número, sino, se hace un loop
if s==str("si"):
    print("El número fue adivinado")
else:
    while s==str("no"):
#Se pregunta qué tan lejano está el número, y si es mayor o menor, dependiendo de esto al número se le va sumando o restando mucho o poco, hasta que de con el número
        m=input("Es el número, o el número es mucho mayor, poco mayor, mucho menor o poco menor? ")
        if m==str("mucho mayor"):
            n=n+10
            print(n)
        elif m==str("poco mayor"):
            n=n+1
            print(n)
        elif m==str("mucho menor"):
            n=n-10
            print(n)
        elif m==str("poco menor"):
            n=n-1
            print(n)
        else:
            print("El número fue adivinado")
            break
```    
7. Implementar un programa que ingrese un número de 2 a 50 y muestre sus divisores.
```python
#Se toma el número
n=int(input("Número? "))
#Se crea una variable que va a actuar como el divisor
e=1
#Como los divisores son siempre más pequeños que el número, siempre que "e" sea menor que el número puesto, el código va a correr, lo que significa que sirve para cualquier número, no solo hasta el 50
while n>e:
#Si la división es exacta se imprime el número y se le añade 1 a "e", sino, solo se añade 1 a "e" 
    if n%e==0:
        f=n/e
        print(f)
        e=e+1
    else:
        e=e+1
```
    
8. Implementar el algoritmo que muestre los números primos del 1 al 100. **Nota:** use funciones
```python
#Se declara la variable para que el código termine en 100 y un número que asciende del 2 al 100
n=100
x=2
#Se hacen funciones para determinar si el número es divisible en 2,3,5 o 7)
def dos(x:int)->int:
    return(x%2)
def tres(x:int)->int:
    return(x%3)
def cinco(x:int)->int:
    return(x%5)
def siete(x:int)->int:
    return(x%7)
#Se hace un loop que evalúa un número dividiendolo entre 2,3,5 y 7, si se divide exactamente en alguno, añade un número, sino, se imprime el número y se sigue el loop
while n>x:
    if dos(x)==0:
        x=x+1
    elif tres(x)==0:
        x=x+1
    elif cinco(x)==0:
        x=x+1
    elif siete(x)==0:
        x=x+1
    else:
        print(x)
        x=x+1

```
    
