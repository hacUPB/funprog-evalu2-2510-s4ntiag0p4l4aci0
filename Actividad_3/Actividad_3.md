                                                                                                                    

## 📤 Ejercicio 1.

Investiga cuáles son los símbolos que se utilizan para representar cada operación de un algorimo con un diagrama de flujo. Asegúrate de que la fuente es confiable, discute lo que encontraste con tus compañeros y con el profe. Cuando estés seguro/a de tener los símbolos correctos, consigna la información en la bitácora.


![diagrama de flujo 1](./images/img1.png)
![diagrama de flujo 2](./images/img2.png)

## Ejercicio 2

Analicemos el siguiente problema y representemos su solución mediante un algoritmo secuencial.

- Construye un algoritmo que, al recibir como datos **el ID** del empleado y los seis primeros sueldos del año, calcule el ingreso total semestral y el promedio mensual, e imprima el ID del empleado, el ingreso total y el promedio mensual.

![diagrama de flujo 3](./images/img3.png)


### Solución en Diagrama de Flujo


![diagrama de flujo 4](./images/img4.png)

### Solución en Pseudocódigo

```txt:

INICIO

Escribir "Ingrese una letra, si escoge la correcta se lleva un premio mágico"

Leer x

si x =  "y":
    i = 10
    Mientras i>0:

        Escribir "Hola"

        i = i - 1

    Fin Mientras

Si no:
    
    Escribir "Hola

Fin Si

Fin

```
### Solución en C

```c:
#include <stdio.h>

int main(void)
{
    char x;
    int i;
    
    printf("Ingrese una letra, si escoge la correcta se lleva un premio mágico\n");
    
    scanf("%c", &x);
    
    if(x=='y'){
        
        i = 10;
        
        while(i > 0){
            
            printf("Hola\n");
            i = i-1;
        }
    }
    
    else{
        printf("Hola\n");
    }
    return 0;
}


```
### Solución en Python
```python:

x = input("Ingrese una letra, si escoge la correcta se lleva un premio mágico").lower()
if x != "y":
    print("hola")

else:
    z = 0
    while z <= 10:
        print("hola")
        z = z+1

```
## Ejercicios

### Ejercicio 1:

Realice un algoritmo para determinar cuánto se debe pagar por equis cantidad de lápices considerando que si son 1000 o más el costo es de $85 cada uno; de lo contrario, el precio es de $90. Represéntelo con el pseudocódigo y el diagrama de flujo.

![Ejercico 1](./images/img5.jpg)

#### Solución complementaria en Python

```python:
x = int(input("Cantidad de lápices"))

if x  >= 1000:
    y = 85*x
    
else:
    y = 90*x
    
print(y)

```

## Ejercicio 2

Un almacén de ropa tiene una promoción: por compras superiores a $250 000 se les aplicará un descuento de 15%, de caso contrario, sólo se aplicará un 8% de descuento. Realice un algoritmo para determinar el precio final que debe pagar una persona por comprar en dicho almacén y de cuánto es el descuento que obtendrá. Represéntelo mediante el pseudocódigo y el diagrama de flujo.

![Ejercicio 2](./images/img6.jpg)

#### Solución complementaria en Python

```python:

subtotal = int(input("ingrese valor de la compra"))

if subtotal >= 250000:
    descuento = subtotal*0.15
    
else:
    descuento = subtotal*0.08
    
total = subtotal - descuento

print(f"El precio es {total} y el descuanto es {descuento}")

```

### Ejercicio 3

El director de una escuela está organizando un viaje de estudios, y requiere determinar cuánto debe cobrar a cada alumno y cuánto debe pagar a la compañía de viajes por el servicio. La forma de cobrar es la siguiente: si son 100 alumnos o más, el costo por cada alumno es de $65.00; de 50 a 99 alumnos, el costo es de $70.00, de 30 a 49, de $95.00, y si son menos de 30, el costo de la renta del autobús es de $4000.00, sin importar el número de alumnos.

![Ejercicio 3](./images/img7.jpg)
![Ejercicio 3](./images/img8.jpg)

Nota el total puede ser el mismo para todo, ya que para el caso de menos de 30 el costo es 4000/x si tenemos en cuenta total = x*costo, entonces se cancelaría el denominador e igual quedaría como 4000
#### Solución complementaria en Python

```python:
x = int(input("número de estudaintes"))

if x >= 100:
    costo = 65
else:
    if x > 50: 
        costo = 70
    else:
        if x > 30:
            costo = 95
        else:
            costo = 4000/x
total = x*costo

print(f"Dado que el costo por alumno es {costo}, el total sería {total}")
```