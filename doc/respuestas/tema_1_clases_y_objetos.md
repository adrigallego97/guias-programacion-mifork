<!--
Posible prompt:
<prompt>
Tengo un cuestionario con preguntas sobre "Clases y Objetos". Debes tener en cuenta que los conocimientos previos que tengo (y por tanto tus respuestas deben ser adaptadas), son:
- C/C++ sin orientación a objetos.
- Temas de Java previos: ninguno.

Cada respuesta debe tener entre 2 - 4 párrafos de longitud (sin contar los trozos de código).

Por favor, escribe en impersonal las respuestas.

</prompt>
----
-->

# TEMA 1. Clases y objetos

## 1. ¿Cuáles son las cuatro características básicas de la programación orientada a objetos? Describe brevemente cada una

### Respuesta
1. Encapsulación: Ocultar los detalles internos de un objeto y proteger sus datos, exponiendo solo una interfaz pública controlada.
2. Abstracción: Representar conceptos simplificándolos a sus características esenciales, ignorando detalles de implementación innecesarios.
3. Herencia: Permitir que una clase hija adquiera atributos y métodos de una clase padre, promoviendo la reutilización de código.
4. Polimorfismo: Capacidad de que diferentes objetos respondan al mismo método de formas distintas según su tipo específico.


## 2. Cita cuatro lenguajes populares que permitan la programación orientada a objetos

### Respuesta
Java
Python
C++
C#

## 3. Los paradigmas anteriores a la POO, ¿Qué es la **programación estructurada**? y, todavía mejor, ¿Qué es la **programación modular**?

### Respuesta
Programación Estructurada
Es un paradigma que organiza el código mediante estructuras de control secuenciales, condicionales (if/else) y repetitivas (bucles), eliminando el uso de sentencias "goto". Se basa en descomponer el programa en bloques lógicos y funciones más pequeñas, siguiendo un flujo de ejecución claro y de arriba hacia abajo. Surgió en los años 60-70 para hacer el código más legible y mantenible. Ejemplos: C, Pascal, ALGOL.
Programación Modular
Es un paradigma que divide un programa en módulos o unidades independientes, cada uno con una función específica y bien definida. Cada módulo tiene su propia interfaz y puede ser desarrollado, probado y mantenido por separado. Los módulos se comunican entre sí a través de interfaces claras, promoviendo la reutilización de código y facilitando el trabajo en equipo. Es una evolución de la programación estructurada que enfatiza la separación de responsabilidades y la organización del código en componentes cohesivos.
La programación modular sentó las bases para la POO, ya que los conceptos de módulos independientes con interfaces definidas evolucionaron hacia las clases y objetos.
## 4. ¿Qué tres elementos definen a un objeto en programación orientada a objetos?

### Respuesta

## 5. ¿Qué es una clase? ¿Es lo mismo que un objeto? ¿Qué es una instancia? ¿Todos los lenguajes orientados a objetos manejan el concepto de clase?

### Respuesta
¿Qué es una clase?
Una clase es una plantilla o molde que define la estructura y comportamiento que tendrán los objetos. Especifica qué atributos (datos) y métodos (funciones) tendrán los objetos creados a partir de ella. Es como un plano arquitectónico que describe cómo será una casa, pero no es la casa en sí.
¿Es lo mismo que un objeto?
No. La clase es la definición abstracta, mientras que el objeto es una instancia concreta creada a partir de esa clase. Si la clase "Coche" define que todo coche tiene color, marca y método acelerar(), un objeto sería un coche específico: un Toyota rojo concreto.
¿Qué es una instancia?
Una instancia es sinónimo de objeto. Es la materialización concreta de una clase en memoria, con valores específicos para sus atributos. Cuando "instancias" una clase, creas un objeto. Por ejemplo, si tienes la clase "Persona", puedes crear múltiples instancias: persona1, persona2, cada una con su propio nombre y edad.
¿Todos los lenguajes orientados a objetos manejan el concepto de clase?
No. Existen dos enfoques principales:

Basados en clases: Java, C++, C#, Python (usan clases como plantillas)
Basados en prototipos: JavaScript (pre-ES6 principalmente), Self (los objetos se crean clonando otros objetos existentes, sin necesidad de clases)

## 6. ¿Dónde se almacenan en memoria los objetos? ¿Es igual en todos los lenguajes? ¿Qué es la **recolección de basura**? 

### Respuesta
¿Dónde se almacenan en memoria los objetos?
Generalmente en el heap (memoria dinámica). Las referencias pueden estar en el stack.
¿Es igual en todos los lenguajes?
No. Java, Python y C# siempre usan el heap. C++ permite objetos tanto en stack como en heap.
¿Qué es la recolección de basura?
Mecanismo automático que libera memoria de objetos que ya no se usan, eliminando referencias sin utilidad.
Lenguajes con recolección de basura: Java, Python, JavaScript, C#
Lenguajes sin recolección de basura: C, C++ (requieren liberación manual)

## 7. ¿Qué es un método? ¿Qué es la **sobrecarga de métodos**? 

### Respuesta
¿Qué es un método?
Es una función definida dentro de una clase que describe el comportamiento o acciones que puede realizar un objeto. Puede acceder y modificar los atributos del objeto.
¿Qué es la sobrecarga de métodos?
Es la capacidad de definir múltiples métodos con el mismo nombre pero con diferentes parámetros (distinto número, tipo u orden). El compilador/intérprete elige cuál ejecutar según los argumentos que se pasen.

## 8. Ejemplo mínimo de clase en Java, que se llame Punto, con dos atributos, x e y, con un método que se llame `calculaDistanciaAOrigen`, que calcule la distancia a la posición 0,0. Por sencillez, los atributos deben tener visibilidad por defecto. Crea además un ejemplo de uso con una instancia y uso del método

### Respuesta
class Punto {
    double x;
    double y;
    
    double calculaDistanciaAOrigen() {
        return Math.sqrt(x * x + y * y);
    }
}

// Ejemplo de uso
public class Main {
    public static void main(String[] args) {
        Punto p1 = new Punto();
        p1.x = 3.0;
        p1.y = 4.0;
        
        double distancia = p1.calculaDistanciaAOrigen();
        System.out.println("Distancia al origen: " + distancia);
        // Salida: Distancia al origen: 5.0
    }
}

## 9. ¿Cuál es el punto de entrada en un programa en Java? ¿Qué es `static` y para qué vale? ¿Sólo se emplea para ese método `main`? ¿Para qué se combina con `final`?

### Respuesta
¿Cuál es el punto de entrada en un programa en Java?
El método public static void main(String[] args). Es donde comienza la ejecución del programa.
¿Qué es static y para qué vale?
static indica que un miembro (método o atributo) pertenece a la clase en sí, no a las instancias. Se puede acceder sin crear objetos: NombreClase.metodoStatic().
¿Sólo se emplea para ese método main?
No. Se usa en:

Métodos estáticos: Utilidades que no necesitan estado del objeto (Math.sqrt())
Atributos estáticos: Variables compartidas por todas las instancias (contadores, constantes)
Bloques estáticos: Inicialización de la clase
Clases internas estáticas: Clases anidadas independientes

¿Para qué se combina con final?
static final crea constantes de clase: valores inmutables compartidos por todas las instancias.

## 10. Intenta ejecutar un poco de Java de forma básica, con los comandos `javac` y `java`. ¿Cómo podemos compilar el programa y ejecutarlo desde linea de comandos? ¿Java es compilado? ¿Qué es la **máquina virtual**? ¿Qué es el *byte-code* y los ficheros `.class`?

### Respuesta
Compilar: javac Punto.java
Genera archivos .class (Punto.class y Main.class)
Ejecutar: java Main
Se ejecuta la clase que contiene el método main
Salida: Distancia al origen: 5.0
¿Java es compilado?
Sí, pero no directamente a código máquina nativo. Java es semi-compilado:
javac compila el código fuente (.java) a byte-code (.class)
El byte-code es interpretado/compilado por la JVM en tiempo de ejecución
La Java Virtual Machine es un programa que ejecuta el byte-code Java. Actúa como capa intermedia entre el código compilado y el hardware, permitiendo que el mismo byte-code funcione en cualquier sistema operativo que tenga una JVM. Principio: "Write Once, Run Anywhere".
¿Qué es el byte-code y los ficheros .class?

Byte-code: Código intermedio en instrucciones de bajo nivel para la JVM (no es código máquina nativo)

## 11. En el código anterior de la clase `Punto` ¿Qué es `new`? ¿Qué es un **constructor**? Pon un ejemplo de constructor en una clase `Empleado` que tenga DNI, nombre y apellidos

### Respuesta
Qué es new?new es un operador que crea una instancia de una clase. Reserva memoria en el heap para el nuevo objeto e invoca su constructor. Devuelve una referencia al objeto creado.
¿Qué es un constructor?
Es un método especial que se ejecuta automáticamente al crear un objeto con new. Su propósito es inicializar el estado del objeto (sus atributos).
class Empleado {
    String dni;
    String nombre;
    String apellidos;
    
    // Constructor
    Empleado(String dni, String nombre, String apellidos) {
        this.dni = dni;
        this.nombre = nombre;
        this.apellidos = apellidos;
    }
    
    void mostrarInfo() {
        System.out.println(nombre + " " + apellidos + " - DNI: " + dni);
    }
}

// Uso
class Main {
    public static void main(String[] args) {
        Empleado emp1 = new Empleado("12345678A", "Juan", "García López");
        emp1.mostrarInfo();
        // Salida: Juan García López - DNI: 12345678A
    }
}

## 12. ¿Qué es la referencia `this`? ¿Se llama igual en todos los lenguajes? Pon un ejemplo del uso de `this` en la clase `Punto`

### Respuesta
¿Qué es la referencia this?
this es una referencia al objeto actual sobre el que se está ejecutando el método. Permite acceder a los atributos y métodos del propio objeto, especialmente útil cuando hay ambigüedad entre parámetros y atributos con el mismo nombre.
¿Se llama igual en todos los lenguajes?
No:
Java, JavaScript, C++, C#: this
Python: self (por convención)
Rust: self
Swift: self
PHP: $this

## 13. Añade ahora otro nuevo método que se llame `distanciaA`, que reciba un `Punto` como parámetro y calcule la distancia entre `this` y el punto proporcionado

### Respuesta

class Punto {
    double x;
    double y;
    
    // Constructor
    Punto(double x, double y) {
        this.x = x;
        this.y = y;
    }
    
    double calculaDistanciaAOrigen() {
        return Math.sqrt(this.x * this.x + this.y * this.y);
    }
    
    // Nuevo método: calcula distancia a otro punto
    double distanciaA(Punto otro) {
        double dx = this.x - otro.x;
        double dy = this.y - otro.y;
        return Math.sqrt(dx * dx + dy * dy);
    }
}

// Ejemplo de uso
class Main {
    public static void main(String[] args) {
        Punto p1 = new Punto(3.0, 4.0);
        Punto p2 = new Punto(6.0, 8.0);
        
        double distOrigen = p1.calculaDistanciaAOrigen();
        double distEntrePuntos = p1.distanciaA(p2);
        
        System.out.println("Distancia de p1 al origen: " + distOrigen);
        System.out.println("Distancia entre p1 y p2: " + distEntrePuntos);
        // Salida:
        // Distancia de p1 al origen: 5.0
        // Distancia entre p1 y p2: 5.0
    }
}
## 14. El paso del `Punto` como parámetro a un método, es **por copia** o **por referencia**, es decir, si se cambia el valor de algún atributo del punto pasado como parámetro, dichos cambios afectan al objeto fuera del método? ¿Qué ocurre si en vez de un `Punto`, se recibiese un entero (`int`) y dicho entero se modificase dentro de la función? 

### Respuesta
En Java, los objetos se pasan por referencia (técnicamente, "por valor de la referencia"). Esto significa que si modificas los atributos del objeto dentro del método, SÍ afectan al objeto original.
Los tipos primitivos (int, double, boolean, etc.) se pasan por copia. Las modificaciones dentro del método NO afectan a la variable original.

## 15. ¿Qué es el método `toString()` en Java? ¿Existe en otros lenguajes? Pon un ejemplo de `toString()` en la clase `Punto` en Java

### Respuesta
## 15. ¿Qué es el método `toString()` en Java? ¿Existe en otros lenguajes? Pon un ejemplo de `toString()` en la clase `Punto` en Java
¿Qué es el método toString() en Java?
Es un método que devuelve una representación en forma de String del objeto. Se hereda de la clase Object (padre de todas las clases en Java) y se puede sobrescribir para personalizar cómo se muestra el objeto.
Se invoca automáticamente cuando:

Se imprime el objeto: System.out.println(objeto)
Se concatena con un String: "Punto: " + objeto
Se convierte explícitamente: objeto.toString()

¿Existe en otros lenguajes?
Sí, con nombres similares:

Python: __str__() y __repr__()
C#: ToString()
JavaScript: toString()
Ruby: to_s
Kotlin: toString()
Swift: description (protocolo CustomStringConvertible)

## 16. Reflexiona: ¿una clase es como un `struct` en C? ¿Qué le falta al `struct` para ser como una clase y las variables de ese tipo ser instancias?
### Respuesta
Reflexión: ¿Una clase es como un struct en C?
Parcialmente. Un struct en C es el ancestro conceptual de una clase, pero mucho más limitado.
Similitudes

Ambos agrupan datos relacionados (atributos/campos)
Definen un tipo de dato personalizado
Permiten crear múltiples variables de ese tipo

Lo que le falta al struct de C para ser una clase
1. Métodos (comportamiento)
struct solo tiene datos
Una clase tiene datos + funciones (métodos) que operan sobre esos datos
2. Encapsulación
struct: todos los campos son públicos por defecto
Clase: puede controlar visibilidad (public, private, protected)
3. Constructores
struct: no tiene inicialización automática
Clase: constructores para inicializar objetos correctamente
4. Herencia
struct: no soporta herencia
Clase: puede heredar de otras clases
5. Polimorfismo
struct: no tiene métodos virtuales ni sobrescritura
Clase: permite polimorfismo y métodos virtuales
6. this/self

struct: no tiene referencia implícita al objeto actual
Clase: tiene this para referenciar la instancia

## 17. Quitemos un poco de magia a todo esto: ¿Como se podría “emular”, con `struct` en C, la clase `Punto`, con su función para calcular la distancia al origen? ¿Qué ha pasado con `this`?
### Respuesta
¿Qué ha pasado con this?
¡Se ha hecho explícito! En C no existe la "magia" de this, así que:
En Java/POO: this es implícito, se pasa automáticamente
p1.calculaDistanciaAOrigen()  // 'this' = p1 (automático)

