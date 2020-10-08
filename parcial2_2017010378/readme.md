# Escenario del parcial 2
1. Codificar una solución que optimice la ejecución del planteamiento del laboratorio.
2. La solución debe optimizar el tiempo de ejecución al menos en un 300%.
3. subir la solución a una rama denominada “desarrollo2”, el nombre del archivo debe ser
parcial2_<carnet>.<extension>
4. Si la meta de optimización se cumple consolide en la rama master la nueva solución.

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
