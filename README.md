# 210---Creaci-n-y-uso-de-paquetes-o-librer-as-Propias

# Actividad: Creación de Paquetes Reutilizables

## Objetivo

Crear paquetes reutilizables para organizar código, facilitar su mantenimiento y permitir el uso de funciones y clases desde diferentes archivos.

## 1. Actividad Python

### Estructura del proyecto

```text
proyecto/
├── libreria/
│   ├── __init__.py
│   └── operaciones.py
└── main.py
```

### Archivo operaciones.py

Contiene una función que calcula el área de un círculo a partir de su radio.

```python
def area_circulo(r):
    return 3.1416 * r * r
```

### Archivo __init__.py

Identifica explícitamente la carpeta `libreria` como un paquete de Python.

### Archivo main.py

Importa la función `area_circulo()` desde el paquete `libreria` y la ejecuta.

```python
from libreria.operaciones import area_circulo

print(area_circulo(5))
```

### Ejecución

Desde la carpeta `Python`, ejecutar:

```bash
python proyecto/main.py
```

### Resultado

```text
78.54
```

### Explicación

El programa importa la función `area_circulo()` desde el módulo `operaciones.py`.

La función recibe un radio de 5 y aplica la fórmula:

A = π × r²

A = 3.1416 × 5²

A = 78.54

De esta manera, se demuestra cómo reutilizar una función almacenada en otro archivo mediante un paquete.

---

## 2. Actividad Java

### Estructura del proyecto

```text
src/
├── utilidades/
│   └── Operaciones.java
└── app/
    └── Main.java
```

### Archivo Operaciones.java

Contiene una clase con un método estático que calcula el cuadrado de un número entero.

```java
package utilidades;

public class Operaciones {

    public static int cuadrado(int n) {
        return n * n;
    }

}
```

### Archivo Main.java

Importa la clase `Operaciones` y utiliza su método `cuadrado()`.

```java
package app;

import utilidades.Operaciones;

public class Main {

    public static void main(String[] args) {

        System.out.println(Operaciones.cuadrado(5));

    }

}
```

### Compilación y ejecución

Desde la carpeta `Java`, compilar con:

```bash
javac -d out src/utilidades/Operaciones.java src/app/Main.java
```

Posteriormente, ejecutar:

```bash
java -cp out app.Main
```

### Resultado

```text
25
```

### Explicación

El programa utiliza la clase `Operaciones`, ubicada en el paquete `utilidades`.

Mediante la instrucción `import`, la clase `Main` puede acceder al método estático `cuadrado()`.

Se envía el número 5 como argumento y se realiza la operación:

5 × 5 = 25

El resultado se muestra en la consola.

---

## 3. Diferencias entre Python y Java

| Característica | Python | Java |
|---|---|---|
| Organización | Módulos y paquetes | Clases y paquetes |
| Importación | from ... import | import |
| Archivo principal | main.py | Main.java |
| Función o método | area_circulo() | cuadrado() |
| Resultado | 78.54 | 25 |

## 4. Conclusión

La actividad permitió comprender la importancia de organizar el código mediante paquetes reutilizables en Python y Java.

En Python se implementó un paquete llamado `libreria`, que contiene una función para calcular el área de un círculo. Posteriormente, dicha función se importó y ejecutó desde el archivo principal.

En Java se utilizó el paquete `utilidades`, que contiene una clase con un método para calcular el cuadrado de un número. Este método se utilizó desde otra clase mediante una importación.

Ambos ejercicios permitieron comprobar que los paquetes facilitan la reutilización del código, mejoran su organización y evitan repetir funciones o métodos en diferentes partes de un programa.
