# Escenario del parcial
1. Codificar una solución que optimice la ejecución del planteamiento del laboratorio.
2. La solución debe optimizar el tiempo de ejecución al menos en un 300%.
3. subir la solución a una rama denominada “desarrollo2”, el nombre del archivo debe ser
parcial2_<carnet>.<extension>
4. Si la meta de optimización se cumple consolide en la rama master la nueva solución.

## Enlace al video de youtube
https://youtu.be/pNT_Btvrm5c

## Resumen del código
1. Se importan las librerías a utilizar, numpy y time.
2. Generamos un muestreo aleatorio simple con NumPy(np.random).
3. Iniciamos la librería time(ejecución = time.time()) para empezar a contar el tiempo de ejecución desde el inicio del programa.
4. Creamos una matriz de NumPy(np.array) en donde almacenamos todo nuestro muestreo aleatorio.
5. Realizamos un recorrido en nuestra matriz(matriz_puntos) y una condición simple donde filtramos solo los datos menores a 500,000 y guardamos el resultado en la variable puntos_menores.
6. Sumamos con NumPy(np.sum) todos los datos que se encuentran en la variable con los datos obtenidos (puntos_menores).
7. Imprimimos la suma total de los datos menores a 500,000 y el tiempo de ejecución del programa en segundos.
