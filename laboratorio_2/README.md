# ESCENARIO LABORATORIO
Se solicita que codifique una solución que cumpla con las siguientes características:
1. Generar una estructura de datos que almacene 10 millones de puntos en una distribución
normal con una media de 500 y una escala de 30.
2. Iterarla exclusivamente con estructuras de control.
3. Calcular la sumatoria de los puntos que son menores a 500,000.
4. Devolver el valor de la sumatoria y el tiempo en que la lógica de negocios del problema
tardo en ejecutarse.

## Resumen del código
1. Se importan las librerías a utilizar, numpy y time.
2. Generamos un muestreo aleatorio simple con NumPy(np.random).
3. Iniciamos la librería time(ejecución = time.time()) para empezar a contar el tiempo de ejecución desde el inicio del programa.
4. Creamos una lista vacía llamada puntos_menores para almacenar todos nuestros datos filtrados menores a 500,000.
5. Iniciamos un bucle para recorrer todos los datos de nuestro muestreo aleatorio.
6. Realizamos una condición if para obtener solo los datos menores a 500,000.
7. Almacenamos nuestros datos obtenidos en la lista vacía puntos_menores.
8. Utilizamos la función de suma de NumPy(np.sum) para obtener la suma total de nuestros datos.
9. Imprimimos la suma total de los datos y el tiempo de ejecución en segundos.
