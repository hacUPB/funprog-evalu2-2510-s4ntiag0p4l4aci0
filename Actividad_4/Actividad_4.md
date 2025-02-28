## 1. Introducción

¿Alguna vez te has preguntado cómo convertir un conjunto de pasos lógicos (pseudocódigo) en un programa funcional en C?

Este tutorial te guiará a través del proceso de:

1. Interpretar tu pseudocódigo.
2. Traducirlo a sintaxis C.
3. Añadir detalles específicos (tipos de datos, prototipos de funciones, etc.).

Pregunta orientadora:
 - ¿Por qué crees que el pseudocódigo es útil antes de escribir un programa en C?

    - Al escribir un pseudocódigo, o bien un diagrama de flujo, se plasma la solución en un conjunto de pasos en un orden lógico y conciso,


---

## 2. Estructura básica del pseudocódigo

Generalmente, el pseudocódigo se escribe en un lenguaje “amigable” que describe el **orden de las operaciones**. Por ejemplo:

```
INICIO
    Leer valor1
    Leer valor2
    suma = valor1 + valor2
    Mostrar suma
FIN
```

> Actividad
> 
> - Toma un pseudocódigo de un ejercicio anterior o escribe tu propio pseudocódigo, similar al mostrado en el ejemplo de arriba.

**Retos**:

1. **Claridad**: Asegúrate de que cada paso esté claro y sea fácil de entender.
2. **Secuencia**: Verifica que tu pseudocódigo siga el orden lógico (entrada → procesamiento → salida).

---

## 3. Traduciendo el pseudocódigo a C

Cuando traducimos un pseudocódigo a C, debemos prestar atención a:

- **Declaración de variables**: En C, es **obligatorio** especificar el tipo de cada variable (int, float, etc.).
- **Funciones de entrada/salida**: `scanf` para leer datos, `printf` para mostrar resultados.
- **Estructuras de control**: `if`, `while`, `for`, etc.

### Ejemplo de pseudocódigo a C

Pseudocódigo:

```
INICIO
    Leer valor1
    Leer valor2
    suma = valor1 + valor2
    Mostrar suma
FIN
```

Versión en C (programa completo):

```c
#include <stdio.h>

int main() {
    float valor1, valor2, suma;

    printf("Ingresa el primer número: ");
    scanf("%f", &valor1);

    printf("Ingresa el segundo número: ");
    scanf("%f", &valor2);

    suma = valor1 + valor2;
    printf("La suma es: %.2f\n", suma);

    return 0;
}
```

> Pregunta orientadora
> 
> - ¿Por qué es importante declarar el tipo de variable (int, float, etc.) antes de usarla en C?

---

## 4. Ejemplos adicionales de pseudocódigo y su traducción

**¡Importante!**

Estos ejemplos te ayudarán a ver la correspondencia entre el lenguaje natural del pseudocódigo y las instrucciones del lenguaje C. No te preocupes si no dominas todos los aspectos aún o si aún no conoces la sintaxis de C; lo importante es que veas cómo se transforman los pasos lógicos en sintaxis.

### Ejemplo 1: Encontrar el mayor de dos números

**Pseudocódigo**:

```
INICIO
    Leer num1
    Leer num2
    Si num1 > num2 Entonces
        Mostrar "El número 1 es mayor"
    Sino
        Mostrar "El número 2 es mayor"
FIN
```

**Lenguaje C**:

```c
#include <stdio.h>

int main() {
    float num1, num2;

    printf("Ingresa el primer número: ");
    scanf("%f", &num1);
    printf("Ingresa el segundo número: ");
    scanf("%f", &num2);

    if (num1 > num2) {
        printf("El número 1 es mayor\n");
    } else {
        printf("El número 2 es mayor\n");
    }

    return 0;
}
```

### Ejemplo 2: Calcular factorial de un número

**Pseudocódigo**:

```
INICIO
    Leer n
    factorial = 1
    Para i desde 1 hasta n
        factorial = factorial * i
    Mostrar factorial
FIN
```

**Lenguaje C**:

```c
#include <stdio.h>

int main() {
    int n;
    long factorial = 1;

    printf("Ingresa un número entero: ");
    scanf("%d", &n);

    for(int i = 1; i <= n; i++) {
        factorial *= i;
    }

    printf("El factorial es: %ld\n", factorial);

    return 0;
}
```

> Actividad
> 
> - Escribe tu propio pseudocódigo para calcular el promedio de una lista de calificaciones y tradúcelo a C.

---

## 5. Buenas prácticas

1. **Comentarios**: Utiliza `/* comentario */` o `// comentario` para describir líneas clave.
2. **Funciones**: Divide tu código en funciones para mantenerlo ordenado.
3. **Convenciones de nombres**: Utiliza nombres descriptivos para variables y funciones.

> Pregunta orientadora
> 
> - ¿Por qué es importante comentar el código, aunque sea breve y conciso?

---

## 6. Reto final

### Reto: toma el pseudocódigo de los 5 primeros ejercicios del Reto y realiza la traducción a C:

1. Revisa el pseudocódigo y verifica que no contenga errores.
2. **Traduce** ese pseudocódigo a C.
3. **Comenta** tu código para explicar los pasos principales.

---

<aside>
💡

**Mensaje final**:
Traducir pseudocódigo a C implica **comprender la lógica** descrita en un lenguaje simple y llevarla a un **código C** con una estructura clara. Desarrollar esta habilidad te permitirá planificar proyectos, depurar problemas y comunicar ideas de programación de manera efectiva.

</aside>

> Pregunta final
> 
> - Después de este tutorial, ¿qué puntos crees que deberías reforzar para sentirte más seguro al traducir pseudocódigo a C?