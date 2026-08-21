# Capitulo 1: Introducción a los algoritmos

En este capitulo:

- Obtienes una base para el resto del libro.
- Usted escribe su primer algoritmo de búsqueda.
- Aprendes a hablar sobre el tiempo de ejecución de un algoritmo (notación Big O).
- Se le presenta una técnica común para el diseño de algoritmos (recursion).

## Introducción

Un algoritmo es un conjunto de instrucciones para realizar una tarea. Cada pieza de código podría llamarse un algoritmo, pero este libro cubre los bits más interesantes. Escogí incluir los algoritmos de este libro porque son rápidos, o resuelven problemas interesantes, o ambos. Aquí hay algunos puntos destacados:

- El capítulo 1 habla de búsqueda binaria y muestra cómo un algoritmo puede acelerar su código. En un ejemplo, el número de pasos necesarios pasa de 4 mil millones a 32!
- Un dispositivo GPS utiliza algoritmos de grafo (como aprenderá en los capítulos 6, 7 y 8) para calcular la ruta más corta a su destino.
- Se puede utilizar la programación dinámica (discutido en el capítulo 9) para escribir un algoritmo de IA que juega a los corredores.

En cada caso, describiré el algoritmo y les daré un ejemplo. Luego hablaré sobre el tiempo de ejecución del algoritmo en notación Big O. Finalmente, exploraré qué otros tipos de problemas podrían resolverse por el mismo algoritmo.

## Lo que aprenderás sobre el rendimiento

La buena noticia es que una implementación de todos los algoritmos en este libro está probablemente disponible en tu idioma favorito, así que no tienes que escribir cada algoritmo tú mismo! Pero esas implementaciones son inútiles si no entiendes las ventajas y desventajas. En este libro, aprenderá a comparar las ventajas y desventajas entre diferentes algoritmos: ¿Debería utilizar la clasificación de fusión o la clasificación rápida? ¿Deberías usar una matriz o una lista? Sólo usar una estructura de datos diferente puede hacer una gran diferencia.

## Lo que aprenderás sobre la resolución de problemas

Aprenderá técnicas para resolver problemas que podrían haber estado fuera de su alcance hasta ahora. Por ejemplo:

- Si te gusta hacer videojuegos, puedes escribir un sistema de IA que sigue al usuario usando algoritmos de grafo.
- Aprenderá a hacer un sistema de recomendaciones utilizando los vecinos más cercanos.
- ¡Algunos problemas no se resuelven a tiempo! La parte de este libro que habla sobre los problemas NP-complete muestra cómo identificar esos problemas y llegar a un algoritmo que le da una respuesta aproximada.

En términos más generales, al final de este libro conocerás algunos de los algoritmos más ampliamente aplicables. Luego puedes usar tu nuevo conocimiento para aprender sobre algoritmos más específicos para IA, bases de datos, etc. O puede enfrentarse a desafíos más grandes en el trabajo.

---

**Lo que necesitas saber**

Tendrás que conocer el álgebra básico antes de comenzar este libro. En particular, tomemos esta función: f(x) \= x × 2. ¿Qué es f(5)? Si has contestado 10, estás listo. Además, este capítulo (y este libro) será más fácil de seguir si está familiarizado con un lenguaje de programación. Todos los ejemplos de este libro están en Python. Si no conoces ningún lenguaje de programación y quieres aprender uno, elige Python - es ideal para principiantes. Si sabes otro lenguaje, como Ruby, estarás bien.

---

## La búsqueda binaria

\[figure-1-1]
\[figure-1-2]

Supongamos que buscas a una persona en la guía telefónica (qué frase anticuada!). Su nombre comienza con K. Podrías empezar desde el principio y seguir volviendo las páginas hasta llegar a los Ks. Pero es más probable que empieces con una página en el medio, porque sabes que los Ks van a estar cerca del centro de la guía telefónica.

O supongamos que estás buscando una palabra en un diccionario, y comienza con O. Una vez más, comenzarás cerca de la mitad.

Ahora supongamos que te conectas a Facebook. Cuando lo hagas, Facebook tiene que verificar que tienes una cuenta en el sitio. Entonces, necesita buscar tu nombre de usuario en su base de datos. Supongamos que su nombre de usuario es Karlmageddon. Facebook podría comenzar con el As y buscar tu nombre, pero tiene más sentido que comience en algún lugar del medio.

Este es un problema de búsqueda. Y todos estos casos utilizan el mismo algoritmo para resolver el problema: _búsqueda binaria_.

La búsqueda binaria es un algoritmo; su entrada es una lista ordenada de elementos (explicaré más adelante por qué debe ser ordenado). Si un elemento que estás buscando está en esa lista, la búsqueda binaria devuelve la posición donde se encuentra. De lo contrario, la búsqueda binaria devuelve `null`.

Por Ejemplo:
\[figure-1-3]

**Buscando empresas en una guía telefónica con búsqueda binaria**

Aquí hay un ejemplo de cómo funciona la búsqueda binaria. Estoy pensando en un número entre 1 y 100.
\[figure-1-4]

Tienes que intentar adivinar mi número en el menor intento posible. Con cada suposición, te diré si tu suposición es demasiado baja, demasiado alta o correcta. Supongamos que empiezas a adivinar así: 1, 2, 3, 4.... Así es como pasaría.
\[figure-1-5]
\[figure-1-6]

**Un mal enfoque para adivinar números**

Esta es una búsqueda simple (tal vez la búsqueda estúpida sería un término mejor). Con cada suposición, estás eliminando sólo un número. Si mi número fuera 99, ¡te llevarían 99 suposiciones llegar allí!

### Una mejor manera de buscar

Aquí hay una mejor técnica. Comienza con 50.
\[figure-1-7]

¡Demasiado bajo, pero acabas de eliminar la mitad de los números! Ahora sabes que 1-50 es demasiado bajo. Siguiente suposición: 75.
\[figure-1-8]

¡Demasiado alto, pero otra vez has reducido la mitad de los números restantes! Con la búsqueda binaria, adivinas el número medio y eliminas la mitad de los números restantes cada vez. Lo siguiente es 63 (medio camino entre 50 y 75).
\[figure-1-9]

Esta es una búsqueda binaria. ¡Acabas de aprender tu primer algoritmo! Aquí tienes cuántos números puedes eliminar cada vez.
\[figure-1-10]

**Elimina la mitad de los números cada vez con búsqueda binaria.**

Cualquiera que sea el número en que estoy pensando, puedes adivinar en un máximo de siete suposiciones - porque eliminas tantos números con cada suposición!

Supongamos que estás buscando una palabra en el diccionario. El diccionario tiene 240.000 palabras. En el peor de los casos, ¿cuántos pasos crees que llevará cada búsqueda?
\[figure-1-11]

Una simple búsqueda podría tomar 240.000 pasos si la palabra que buscas es la última en el libro. Con cada paso de búsqueda binaria, se reduce el número de palabras a la mitad hasta que sólo queda una palabra.
\[figure-1-12]

Así que la búsqueda binaria tomará 18 pasos - ¡una gran diferencia! En general, para cualquier lista de n, la búsqueda binaria tomará log2n pasos para ejecutarse en el peor de los casos, mientras que una simple búsqueda tomará n pasos.

---

**Logaritmos**

Puede que no recuerdes qué son los logaritmos, pero probablemente sepas lo que son los exponenciales. log10 100 es como preguntar, ¿Cuántos 10 multiplicamos juntos para obtener 100? La respuesta es 2: 10 × 10. Así que log10 100 es igual a 2. Los registros son el cambio de exponenciales.
\[figure-1-13]

Los registros son el cambio de exponenciales.

En este libro, cuando hablo del tiempo de ejecución en la notación Big O (explicado un poco más tarde), log siempre significa log2. Cuando buscas un elemento usando una búsqueda simple, en el peor de los casos podrías tener que mirar cada elemento. Así que para una lista de 8 números, usted tendría que comprobar 8 números como máximo.

Para la búsqueda binaria, tienes que comprobar los elementos de registro en el peor de los casos. Para una lista de 8 elementos, registro 8 \=\= 3, porque 23 \=\= 8. Así que para una lista de 8 números, usted tendría que comprobar 3 números como máximo. Para una lista de 1.024 elementos, registro 1,024 \= 10, porque 210 \=\= 1,024. Así que para una lista de 1.024 números, usted tendría que comprobar 10 números como máximo.

---

---

**Nota**

Hablaré mucho del tiempo logarítmico en este libro, así que deberías entender el concepto de los logaritmos. Si no lo hace, Khan Academy (khanacademy.org) tiene un buen video que lo deja claro.

---

---

**Nota**

La búsqueda binaria sólo funciona cuando la lista está ordenada. Por ejemplo, los nombres en una guía telefónica están ordenados por orden alfabético, así que puedes usar la búsqueda binaria para buscar un nombre. ¿Qué pasaría si los nombres no fueran ordenados?

---

Veamos cómo escribir búsqueda binaria en Python. La muestra de código aquí utiliza matrices. Si usted no sabe cómo funcionan las matrículas, no se preocupe; están cubiertas en el siguiente capítulo. Solo necesitas saber que puedes almacenar una secuencia de elementos en una fila de cubos consecutivos llamados array.

Los baldes están numerados a partir de 0: el primer balde está en la posición #0, el segundo es #1, el tercero es #2, y así sucesivamente.

La función de búsqueda binaria `binary_search` toma una matriz ordenada y un elemento. Si el elemento está en la matriz, la función devuelve su posición. Mantendrá un registro de qué parte del matriz tiene que buscar. Al principio, esta es toda la matriz:
[figure-1-14]
