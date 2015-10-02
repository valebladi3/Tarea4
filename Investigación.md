# Tarea4

                                                                                                       Valeria Bladinieres Justo
                                                                                                        150020
                                                          Lenguajes y Paradigmas
                                                          Tarea de Investigación
                                                          
Variables Estáticas

En informática una variable estática es una variable que ha sido ubicada estáticamente y cuyo tiempo de vida se extiende durante toda la ejecución del programa. Normalmente una variable estática tiene un ámbito más amplio que otras variables. Los valores de variables estáticas se pueden establecer una vez (durante el tiempo de ejecución) o se pueden cambiar en múltiples ocasiones durante la ejecución del programa. La terminología "variable estática" se basa en C y C++, pero también se usa en muchos lenguajes de programación derivados. En lenguajes de diferente origen el mismo concepto puede denominarse "variable global".

Ciclos de vida de las variables 

El ciclo de vida de una variable inicia con el momento de la asignación de la zona de memoria, conforme a su definición. La asignación es realizada por el compilador y hay varios tipos de variables:

• Variables de instancia (objeto): 
          •	Se crean cuando se crea el objeto que las contiene.     
          •	Se inicializan por defecto si no se hace de modo explícito:   
            –	0 para números, "false" para booleano, "null" para objetos.  
          •	Se destruyen cuando el recolector de basura de Java no encuentra referencias activas para el objeto.  
• Variables estáticas (clase):  
          •	Se crean cuando la clase se usa por primera vez.  
          •	Se inicializan por defecto si no se hace de modo explícito:  
          –	 0 para números, "false" para booleano, "null" para objetos  
          •	Suelen existir para el resto del programa (salvo que no esté cargado).   
• Variables locales (método): 
          •	Creadas en la sentencia en la que están definidas.  
          •	No se inicializan por defecto. Contienen datos imprevisibles.  
          •	Se destruyen al salir del bloque (en la llave final). 
          
Memoria Dinámica

Es memoria que se reserva en tiempo de ejecución. Su principal ventaja frente a la estática, es que su tamaño puede variar durante la ejecución del programa. (En C, el programador es encargado de liberar esta memoria cuando no la utilice más). El uso de memoria dinámica es necesario cuando no conocemos el número de datos/elementos a tratar. 
Las variables globales y las variables locales declaradas con el especificador static tienen duración estática. Se crean antes de que el programa inicie su ejecución y se destruyen cuando el programa termina. Las variables locales no static tienen duración automática. Se crean al entrar al bloque en el que fueron declaradas y se destruyen al salir de ese bloque. Duración asignada se refiere a los objetos cuya memoria se reserva de forma dinámica. Como se explicó anteriormente, esta memoria se crea y se debe liberar de forma explícita. Los arreglos de longitud variable de C99 son un caso especial. Tienen duración automática, con la particularidad de que son creados a partir de su declaración. 
La biblioteca estándar de C proporciona las funciones malloc, calloc, realloc y free para el manejo de memoria dinámica. Estas funciones están definidas en el archivo de cabecera stdlib.h. 

Clase

Una clase representa un intento de abstraer el mundo real.  Pero desde el punto de vista del programador clásico, lo mejor es considerarlas como "entes" que superceden las estructuras C en el sentido de que, tanto los datos, como los instrumentos para su manipulación (funciones), se encuentran encapsulados en ellos. La idea es empaquetar juntos los datos y la funcionalidad; de ahí que tengan dos tipos de componentes (aquí se prefiere llamarlos miembros). Por un lado las  propiedades, también llamadas variables, campos ("fields") o atributos, y de otro los métodos, también llamados procedimientos o funciones; más formalmente: variables de clase y métodos de clase. 

Se puede considerar una clase como varios tipos de datos cuya única peculiaridad es que pueden ser definidos por el usuario.  Generalmente se trata de tipos complejos, constituidos a su vez por elementos de cualquier tipo (incluso otras clases).  La definición que puede hacerse de ellos no se reduce a diseñar su "contenido"; también pueden definirse su álgebra y su interfaz.  

Es decir:  como se opera con estos tipos y como los ve el usuario (qué puede hacer con ellos). El inventor del lenguaje señala que la principal razón para definir un nuevo tipo es separar los detalles poco relevantes de la implementación de las propiedades que son verdaderamente esenciales para utilizarlos correctamente. Una clase es un grupo de datos y métodos (funciones). Es solo un patrón que será usado para crear una variable que pueda ser manipulada en el programa.  

Objeto

Estos objetos interactúan unos con otros, en contraposición a la visión tradicional en la cual un programa es una colección desubrutinas (funciones o procedimientos), o simplemente una lista de instrucciones para una computadora. Cada objeto es capaz de recibir mensajes, procesar datos y enviar mensajes a otros objetos de manera similar a un servicio (en Windows) o demonio (en Unix y Linux). 

En el mundo de la programación orientada a objetos (POO), un objeto es el resultado de la instanciación de una clase. Una clase es el anteproyecto que ofrece la funcionalidad en ella definida, pero ésta queda implementada sólo al crear una instancia de la clase, en la forma de un objeto. Por ejemplo: dado un plano para construir sillas (una clase de nombreclase_silla), entonces una silla concreta, en la que podemos sentarnos, construida a partir de este plano, sería un objeto declase_silla. Es posible crear (construir) múltiples objetos (sillas) utilizando la definición de la clase (plano) anterior. Los conceptos de clase y objetos son análogos a los de tipo de datos y variable; es decir, definida una clase podemos crear objetos de esa clase, igual que disponiendo de un determinado tipo de dato (por ejemplo el tipo entero). 

Instanciación

Una vez que una clase es escrita en Objective-C, puede ser instanciada. Esto se lleva a cabo primeramente alojando la memoria para el nuevo objeto y luego inicializándolo. Un objeto no es completamente funcional hasta que ambos pasos sean completados. Esos pasos típicamente se logran con una simple línea de código: 

MyObject * o = [[MyObject alloc] init];  

La llamada a alloc aloja la memoria suficiente para mantener todas las variables de instancia para un objeto, y la llamada a init puede ser anulada para establecer las variables de instancia con valores específicos al momento de su creación. El método init es escrito a menudo de la siguiente manera: 

Herencia

No existe un mecanismo de clases derivadas en C, sin embargo esto se puede simular. El método de una clase/estructura, que hereda de otra, puede convertir el puntero de su estructura a una estructura de la clase base y llamar con ello los métodos de esta. Esto corresponde a una herencia privada. Para esto hace falta que la primera parte de la estructura derivada contiene en el inicio los mismos campos como la estructura base. 
Para hacer una herencia pública, el usuario debe convertir el puntero en su llamada. 
MiClaseDerivada miInstancia; 
MiClaseBase_HazAlgo((MiClaseBase) miInstancia); 
Obviamente esta construcción es aún menos práctica ya que es el usuario debe pensar si llama a una función de la clase base o de la clase derivada. 

Sobrecarga

Sobrecarga es la capacidad de un lenguaje de programación, que permite nombrar con el mismo identificador diferentes variables u operaciones. 

En programación orientada a objetos la sobrecarga se refiere a la posibilidad de tener dos o más funciones con el mismo nombre pero funcionalidad diferente. Es decir, dos o más funciones con el mismo nombre realizan acciones diferentes. El compilador usará una u otra dependiendo de los parámetros usados. A esto se llama también sobrecarga de funciones.
También existe la sobrecarga de operadores que al igual que con la sobrecarga de funciones se le da más de una implementación a un operador. El mismo método dentro de una clase permite hacer cosas distintas en función de los parámetros.
Java no permite al programador implementar sus propios operadores sobrecargados, pero sí utilizar los predefinidos como el +. C++, por el contrario si permite hacerlo. 
Algunos métodos en una clase pueden tener el mismo nombre. Estos métodos deben contar con diferentes argumentos. El compilador decide qué método invocar comparando los argumentos. Se generara un error si los métodos tienen definidos los mismos parámetros. 

Ensombrecimiento(shadowing)

El problema de “ensombrecimiento” se produce cuando en un ámbito de validez se define una variable con nombre idéntico a otra válida en un ámbito superior. El siguiente ejemplo ilustra esta situación: 
1 2 3 4 5 6 7 8 9 10 11 12 13 14	#include <stdio.h>  
int numero = 10;   
void funcion()  {       
     int numero;  /* Colisiona con variable global */ 
     numero = 20; /* ¿A qué variable se le asigna el valor? */  
}  
int main(int argc, char *argv[])  { 
     funcion();     /* Imprime el valor de numero */ 
     printf("%d\n", numero); /* ¿Qué valor imprime? */ 
     return 0;  
} 
 
Las declaraciones de las líneas 2 y 5 son idénticas pero están hechas en ámbitos diferentes (global frente a local a la función). El compilador permite esta declaración. Pero cuando se ejecuta la función se produce el ensombrecimiento: la variable global numero no puede ser accedida, pues ese nombre se refiere a la variable local a la función. Al terminar la función, la variable global ya no está “ensombrecida” y vuelve a ser accesible y se imprime su valor (10) en la línea 12.  
 
Referencias  
Juganaru, M. (2014). Introducción a la Programación. México: Grupo Editorial Patria. Retrieved September 16, 2015, from https://goo.gl/YbgPgZ 

Ros, J. (2013). El lenguaje Objective-C. México: Geeky Theory. Retrieved September 16, 2015, from https://goo.gl/cYbYFU 
