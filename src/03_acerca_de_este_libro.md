# Acerca de este libro

Este libro está diseñado para que sea fácil de seguir. Evito los grandes saltos de pensamiento.

Cada vez que se introduce un nuevo concepto, lo explico de inmediato o te digo cuándo lo explicaré. Los conceptos básicos se refuerzan con ejercicios y múltiples explicaciones para que puedas comprobar tus suposiciones y asegurarte de seguir adelante.

Lo hago con ejemplos. En lugar de escribir sopa de símbolos, mi objetivo es que sea fácil para ti visualizar estos conceptos. También creo que aprendemos mejor si somos capaces de recordar algo que ya sabemos, y los ejemplos nos hacen recordar más fácilmente. Así que cuando estás tratando de recordar la diferencia entre matrices y listas vinculadas (explicado en el capítulo 2), puedes pensar en sentarte para una película. Además, a riesgo de decir lo obvio, soy un aprendiz visual. Este libro está lleno de imágenes.

El contenido del libro está cuidadosamente seleccionado. No es necesario escribir un libro que cubra todos los algoritmos de clasificación por eso tenemos Wikipedia y Khan Academy. Todos los algoritmos incluidos son prácticos. Los he encontrado útiles en mi trabajo como ingeniero de software, y proporcionan una buena base para temas más complejos.

¡Feliz lectura!

## Mapa de ruta

Los tres primeros capítulos de este libro ponen los cimientos:

- **En el capítulo 1** Aprenderá su primer algoritmo práctico: búsqueda binaria. También aprendes a analizar la velocidad de un algoritmo usando la notación Big O. La notación Big O se utiliza a lo largo del libro para analizar cuán lento o rápido es un algoritmo.

- **En el capítulo 2** aprenderás sobre dos estructuras de datos fundamentales: matrices y listas vinculadas. Estas estructuras de datos se utilizan a lo largo del libro, y se utilizan para hacer estructuras de datos más avanzadas como tablas hash (capítulo 5).

- **En el capítulo 3** aprenderás acerca de la recursion, una técnica práctica utilizada por muchos algoritmos (como el quicksort, cubierto en el capítulo 4).

En mi experiencia, la notación de Big O y la recursion son temas desafiantes para los principiantes. Así que fui más despacio y pasé más tiempo en estas secciones.

El resto del libro presenta algoritmos con amplias aplicaciones:

- **Técnicas de resolución de problemas**: Cubiertas en los capítulos 4, 8 y 9. Si se encuentra con un problema y no está seguro de cómo resolverlo eficientemente, intente dividir y conquistar (capítulo 4) o la programación dinámica (capítulo 9). O puede darse cuenta de que no hay una solución eficiente, y obtener una respuesta aproximada utilizando un algoritmo codicioso en su lugar (capítulo 8).

- **Tablas de Hash**: cubiertas en el capítulo 5. Una tabla de hash es una estructura de datos muy útil. Contiene conjuntos de pares de claves y valores, como el nombre de una persona y su dirección de correo electrónico, o un nombre de usuario y la contraseña asociada. Es difícil exagerar la utilidad de las tablas hash. Cuando quiero resolver un problema, los dos planes de ataque con los que inicio son "¿Puedo usar una tabla hash?" y "¿Puedo modelar esto como un grafo?"

- **Algoritmos de grafos**: cubiertos en los capítulos 6 y 7. Los grafos son una forma de modelar una red: una red social, o una red de carreteras, o neuronas, o cualquier otro conjunto de conexiones. La búsqueda por anchura (capítulo 6) y el algoritmo de Dijkstra's (capítulo 7) son formas de encontrar la distancia más corta entre dos puntos en una red: se puede utilizar este enfoque para calcular los grados de separación entre dos personas o la ruta más corta a un destino.

- **Los vecinos más cercanos (KNN)**: cubiertos en el capítulo 10. Este es un algoritmo de aprendizaje automático simple. Puede usar KNN para construir un sistema de recomendaciones, un motor OCR, un sistema para predecir valores de acciones - cualquier cosa que implique predecir un valor ("Creemos que Adit calificará esta película 4 estrellas") o clasificar un objeto ("Esa letra es Q").

- **Los siguientes pasos**: El capítulo 11 aborda 10 algoritmos que harían una buena lectura adicional.

## Como hacer uso de este libro

El orden y el contenido de este libro han sido cuidadosamente diseñados. Si usted está interesado en un tema, no dude en saltar adelante. De lo contrario, lea los capítulos por orden - se edifican entre sí.

Recomiendo encarecidamente ejecutar el código para los ejemplos usted mismo. No puedo enfatizar esta parte lo suficiente. Simplemente escriba mis muestras de código en forma literal (o descargalas desde www.manning.com/books/grokking-algorithms o https://github.com/egonschiele/grokking_algorithms), y ejecútalas. Retendrás mucho más si lo haces.

También recomiendo hacer los ejercicios de este libro. Los ejercicios son cortos, generalmente sólo un minuto o dos, a veces de 5 a 10 minutos. Te ayudarán a comprobar tu pensamiento, para que sepas cuándo te has desviado antes de haber ido demasiado lejos.

## Quienes deberían leer este libro

Este libro está dirigido a cualquiera que conozca los fundamentos de la codificación y quiera entender los algoritmos. Tal vez usted ya tiene un problema de codificación y está tratando de encontrar una solución algorítmica. O tal vez quieras entender para qué son útiles los algoritmos. He aquí una breve e incompleta lista de personas que probablemente encontrarán útil este libro:

- Los codificadores aficionados
- Estudiantes del campo de entrenamiento en codificación
- Graduados en ciencias de la computación que buscan una actualización
- Físicos/matemáticos/otros graduados interesados en la programación

## Convenciones de código y descargas

Todos los ejemplos de código en este libro utilizan Python 2.7. Todo el código del libro se presenta en una fuente `fixed-width` como esta para separarlo del texto ordinario. Las anotaciones de código acompañan algunas de las listas, destacando conceptos importantes.

Puede descargar el código para los ejemplos del libro desde la página web de la editorial en www.manning.com/books/grokking-algorithms
o desde https://github.com/egonschiele/grokking_algorithms. Creo que aprendes mejor cuando realmente disfrutas del aprendizaje, así que diviértete y ejecuta las muestras de código!

## Acerca del autor

Aditya Bhargava es ingeniero de software en Etsy, un mercado online para productos hechos a mano. Tiene una maestría en ciencias de la computación de la Universidad de Chicago. También dirige un popular blog de tecnología ilustrada en adit.io.

## Autor online

La compra de "Grokking Algorithms" incluye acceso gratuito a un foro web privado dirigido por Manning Publications donde puede hacer comentarios sobre el libro, hacer preguntas técnicas y recibir ayuda del autor y otros usuarios. Para acceder al foro y suscribirse, dirija su navegador web a los algoritmos www.manning.com/books/grokking-algorithms. Esta página proporciona información sobre cómo ingresar al foro una vez registrado, qué tipo de ayuda está disponible y las reglas de conducta en el foro.

El compromiso de Manning con nuestros lectores es proporcionar un lugar donde pueda tener lugar un diálogo significativo entre los lectores individuales y entre los lectores y el autor. No es un compromiso de participación específica por parte del autor, cuya contribución a Author Online sigue siendo voluntaria (y no pagada). Le sugerimos que trate de hacerle al autor algunas preguntas difíciles para no perder su interés. El foro Autor Online y los archivos de las discusiones anteriores serán accesibles desde la página web del editor mientras el libro esté impreso.
