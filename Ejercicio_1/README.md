# Calculadora standard y cientifica con Python 3.8 y Tkinter

## Importando librerías
Empezamos importando todas las librerías que vamos a utilizar. Importamos tkinter, math, parser y tkinter.messagebox.

## Configurando la vista de la calculadora e inicializando tkinter
1. Primeramente debemos configurar tkinter para obtener nuestro widget o ventana donde posteriormente agregaremos los botones y funciones de la calculadora.
2. Inicializamos tkinter con root = Tk() para crear una ventana de Tkinter.
3. Asignamos un titulo al widget o ventana que generamos con root.title("Titulo deseado")
4. Aplicamos un color de fondo a nuestro widget o ventana con root.configure(background = "nombre_color")
5. En nuestro caso no queremos que el widget o ventana sea redimencionable para que la calculadora mantenga su tamaño y orden ideal, por ello utilizamos root.resizable(width = False, height = False)
6. Ahora creamos las dimenciones que queremos que tenga nuestra calculadora al iniciar por primera vez, para ello utilizamos root.geometry("ancho"x"alto"+0+0)
7. Para darle forma y orden a nuestro widget necesitamos crear un marco o cuadro y ordenarlo en forma de cuadrícula, para esto hacemos calc = Frame(root) y calc.grid() este último ordena en forma de cuadrícula nuestros botones.
8. Ya que nuestra calculadora va a tener dos modos, 'standard' y 'cientifica' necesitamos crear un Menu en forma de cascada. Para esto hacemos: barra_menu = Menu(calc) y agregamos las opciones que deseamos en este caso agregamos 3 que son, standard, científica y salir, de esta forma el usuario puede navegar entre stantard y cientifica.

## Agregando botones numéricos y el campo de texto donde se mostraran nuestras operaciones y resultados.
1. Asignamos y almacenamos en nuestra variable teclas_numericas los numeros que deseamos mostrar, en este caso del 1 al 9 pero, lo ordenaremos de esta forma teclas_numericas = "789456123", para que posteriormente realicemos un recorrido con for por nuestras filas y columnas donde queremos que se muestren nuestros botones en este caso   
* for filas in range(2,5):  
* for columnas in range(3):
2. Recordemos que la función range() cuenta de esta manera range(6) = 0,1,2,3,4,5 y en nuestra calculadora queremos una cuadrícula 3x3 por lo que hacemos un rango de 2,5 para que se creen los botones a partir de la fila 3 a la 5 y nuestro segundo for nos indica el numero de columnas en las que queremos repartir nuestras filas. 
3. Creamos y configuramos una variable llamada vistaTexto la cual utilizaremos para crear nuestro input de texto donde mostraremos lo que el usuario selecciona.
* Le ponemos un estilo a nuestro texto, tipo de letra, tamaño, justificado y color de fondo.
* vistaTexto = Entry(calc, font = ('Kozuka Mincho Pr6N',20,'bold'), bg = "white", bd = 30, width = 28, justify = RIGHT)
* vistaTexto.grid asigna la posición en nuestra cuadrícula donde queremos que se muestre nuestro texto.
* vistaTexto.grid(row = 0, column = 0, columnspan = 4, pady = 1)
* Y agregamos un valor por defecto que se muestre al iniciar la calculadora.
* vistaTexto.insert(0,"0")

## Explicando la creación y las funciones de los botones de la calculadora.
1. Ya que nuestros botones operacionales utilizan la misma estructura se explicará uno de ellos.
2. Creamos un botón y le asignamos un nombre en este caso boton_suma, llamamos la función Button de Tkinter para crear este botón en nuestra cuadrícula en el campo text = "+" se asigna el símbolo que queremos que muestre este botón en la cuadrícula, luego el tamaño a nuestro gusto en mi caso width = 6 y height = 2, en el campo font podemos escoger el tipo de letra de nuestra preferencia, el valor bd = 4 asigna el tamaño del borde del botón en píxeles y bg = "grey" asigna el color de fondo del botón row y column son el posicionamiento deseado en nuestra cuadrícula y pady es el margen externo entre cada botón en este caso solo asignamos un margen externo para el eje Y, pero también puede utilizarse padx para el eje X. 
2. Ahora que ya tenemos nuestro estilo terminado, podemos observar el valor 'command', en Tkinter esta opción sirve para realizar acciones o pasar argumentos al botón, y este se activa al momento en que el usuario pulsa dicho botón.
* boton_suma = Button(calc, text = "+", width = 6, height = 2, font = ('Kozuka Mincho Pr6N',20,'bold'), bd = 4, bg = "grey", command = lambda: valor_agregado.operacion("Suma")).grid(row = 1, column = 3, pady = 1)

## Creando la clase que manejará nuestras operaciones.
1. Creamos una clase llamada Calc() en la cual iniciaremos definiciendo un método __init__ donde asignaremos el nombre de las variables y su valor con el cual deseamos que inicien al ejecutar el programa.
