# Lab-1
Reporte de la primer práctica de LRT4012

Diego de Jesús Gutiérrez Reyes
165096

**Introducción**

Python es un lenguaje de programación de código abierto empleado en desarrollo de software, ciencias de datos y el machine learning (ML), fue desarrollado en 1991, se trata de un lenguaje interpretado, lo que implica que el código generado se convierte en byteocde t se ejecuta por la máquina virtual de Python.

Se trata de un lengujae de alto nivel, puesto que considera las capacidaddes cognitivas del programador, de modo que se vuelve un lenguaje sencillo y fácil de entender, dentro de las características principales de este lenguaje se enecuentran las siguientes:

1) Multiplataforma: es un lenguaje que puede ser empleado en distintos tipos de sistemas operativos, incliyendo Windows, Linux y macOS.
2) Dinámico: las variables pueden tomar valores de diferentes tipos.
3) Multiparadigma: la programción es imperativa, orientada a objetos y funcional.

Las funciones básicas de Python son las mismas que otros lenguajes de programación, de modo que contiene comandos para diversas operaciones, los más básicos y empleados son los siguientes:

- main: es el punto de partida de cualqueir código desarrollado en Python, y se emplea para declarar o crear nuevas clases.
- class: función empelada para definir métodos y propiedades de un objeto.
- object: comando que permite asignar un objeto a una variable.
- private: hace que la función solo se ejecute dentro de la calse correspondiente.
- print: es un comando empleado para mostrar al usuario una variable o un mensaje.

Para definir las variables que se emplearán durante un código, se usan diferentes comandos, cada uno asignado a un tipo de variable en específico, por ejemplo:
- int: crea una variable de tipo integer.
- double: especifica un valor numético con sus decimales.
- char: se emplea para crear una variable que incluye exactamente un carácter.
- string: define una cadena de carácteres en Java.
- bool: representa una variable de valor booleana, es decir, qe toma como valores solo 1 o 0.

  Así como los tipos de variables, existen diversos tipos de estructuras que pueden emplearse en Python, de las más comunes, pero más empleadas son:
  
- if / else: con "if" y "else" se comprueba si una variable cumple una condición en específico, si la cumple se ejecutará una indicación, en caso de que no se cumpla se realizará la instrucción dictada por "else".

  El comando completo se emplea de la siguiente forma:

  if (condición)
    [Instrucción si la condición se cumple]
  else (
    [Instrucción si la condición no se cumple]
  
- for: es una sentencia que genera un bucle en el programa mientras una condición establecida se esté cumpliendo, el for posee la característica de poder limitar la frecuencia de repetición.

  La estructura del comando for es la siguiente:

  for (inte i=1, i<=5, i++)
    [Ejecutar instrucción mientras que i sea menor a 1, en cada ejecución el valor de i aumenta en 1]
  
- while: comando empleado para generar un bucle mientras la condición definida se cumpla, ejecutandose de manera infinita.

  Su estructura correspondiente es la siguiente:

  while (condición de termino)
    [Ejecutar instrucción hasta que la condición sea válida]

**Problemas a resolver**

**1) Escribir un programa que lea un entero positivo “n” introducido por el usuario y después muestreen pantalla la suma de todos los enteros desde 1 hasta n . La suma de los primeros enterospositivos puede ser calculada de la siguiente forma.**

Para resolver el ejercicio, basta con implementar la operación dada con suma (+), multiplicación (*) y división (/), antes de esta operación se debe solicitar al usuario el valor del número "n", al final del código debe de imprimirse el resultado.

  #La biblioteca numpy permite la creación de vectores y matrices
  
  import numpy
  
  #Se solicita al usuario el valor de n en la ecuación dada
  
  n = int(input("Introduzca el valor de n "))

  #Se realiza la operación
  
  suma = n*(n+1)/2

  #Se imprime el resultado
  
  print("el valor de la operación es", suma)

  ![ejercicio 1](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/a110b27d-3a09-4d9c-8b53-b4862e6c3930)

   
**2) Escribir un programa que pregunte al usuario por el número de horas trabajadas y el costo por hora. Después debe mostrar por pantalla la paga que le corresponde.**

La paga correspondiente se hace multiplicando el número de horas trabajadas por el costo de cada hora, al tratarse de valores que pueden ser decimales, se ocupasn variables float, en lugar de enteros, lo siguiente es realizar la multiplicación entre los dos valores y multiplicar el resultado.

  #Se solicita al usuario el número de horas trabajadas, así como el costp (salario) por horashoras = float(input("Horas trabajadas "))
  
  horas = float(input("Las horas trabajadas por el empleado son: "))
  
  costo = float(input("El costo por hora del empleado es: "))
  
  total = horas * costo
  
  print("El costo del empleado es: ", total)

![ejercicio2](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/4e926ba1-1a20-4433-af28-6af259dba4dc)


   
**3) Crea una lista de nombre + sueldo por hora + horas trabajadas de al menos seis operadores. Imprime el nombre y el sueldo a pagar de cada operador.**

Para la generación de las listas es necesario implementar vectores, sin definir su tamaño, dado que el usuario podrá decidir el tamaño de cada vector,  especificado el tamaño que tendrán las listas, se implementará una repetición de introducción de datos, de modo que puedan ingresarse el nombre, costo y horas trabajadas para cada usuario, los datos del nombre y el sueldo a pagar se implementarán en otra lista, la cual se imprimirá al final para obtener la información de todos los empleados.

  #Se solicita el núero de empleados
  n = int(input("Numero de empleados "))

  #Se crean 3 listas, unoa para cada variable que se empleará, así como 1 extra para la lista final de nombre y sueldo
  list_nombres = []
  list_horas = []
  list_salario = []
  Lista = []

  #Se crea un for que se repetirá las mismas veces que el tamaño del vectores
  #Se solicitan el nombre, costo y horas trabajadas de cada empleado
  
  for i in range(n):
      nombre = str(input("Ingrese el nombre del empleado: "))
      costo = float(input("Ingrese el costo por hora del empelado: "))
      horas = float(input("Ingrese las horas trabajadas por el empelado: "))
      
      #Se realiza la operación y se guardan en cada una de las listas creadas
      total = horas * costo
      list_nombres.append(nombre)
      list_horas.append(horas)
      list_salario.append(total)
  
  #Se imprimen los resultados de cada empleado
  for i in range(n):
      Lista.append(list_nombres[i] + "  $" + str(list_salario[i]))
  print(Lista)

  ![ejercicio3_1](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/9864d3fe-8777-4c2e-85de-08676f03c2cc)
  ![ejercicio3_2](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/b7b7e17d-969c-4756-a138-62a5f4d1597f)



**4) Crea una lista llamada numeros que contenga al menos 10 números. Calcula el promedio de los números pares y el producto de los números impares. Imprime los resultados.**

Para generar el tamño de la lista, se pedirá al usuario ingresar un número mayor a 10, de modo que se cree un rango entre el 1 y el valor dado por el usuario, a partir de esto se harán 2 vectores, uno para los números pares y otro para los impares, luego se realizará un proceso para discenir en que vector colocar cada uno de los números, para ello puede implementarse una división entre 2, puesto que los pares nunca tendrán residuo, mientras que los impares lo tendrán, almacenados los números en sus listas correspondientes, se realizan los procesos del promedio y la multiplicación, sumando y multiplicando los valores respectivos a cada lista, teniendo en consideración que lel resultado de la suma de los pares se dividirá entre el tamaño del vector para obtener el promedio.

    import numpy
    #Se solicita el número 
    a = int(input("Ingrese un número mayor a 10, se creará una lista de 1 hasta el valor indicado :"))
    
    #Se creará un rango entre 1 y el valor dado por el usuario
    num = range(1,a+1)
    
    #Se crean 2 listas, una para los números pares y otra para los número impares
    numP=[]
    numI=[]
    sumap=0
    producto=1
    x =0
    
    #Se crea un for para determinar si el número es par o impar, se hace mediante división entre 2
    #Al ser par no hay residuo
    #Al ser impar hay residuo 1
    for i in num:
        #PAR
        if i%2== 0:
            #Se agregan los pares
            numP.append(i)
            #Se suman los pares
            sumap = sumap + i
    
            x = x+1
        #IMPAR
        if i%2!=0:
            #Se agregan los impares
            numI.append(i)
            #Se multiplican los impares
            producto = producto*i
    
    #Se realiza e imprime el proceso de promedio de los pares
    print("El promedio de los números pares es:")
    print("(", end="")
    for i in range(len(numP)):
        if i != len(numP)-1:
            print(numP[i], "+ ", end="")
        else:
            print(numP[i], ")", "/",len(numP), " = " ,end="")
    promedio = sumap/len(numP)
    print(promedio)
    
    
    #Se realiza e imprime el producto de los impares
    print("El producto de los números impares es: ")
    print("(", end="")
    for i in range(len(numI)):
        if i != len(numP):
            print(numI[i], "*", end="")
        else:
            print(numI[i], ")", " = " ,end="")
    print(producto)

    ![ejercicio4](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/c5bd0395-c62f-4015-8308-b638e37503ac)


**5) Crea un programa que solicite al usuario adivinar un número secreto. El programa debe generarun número aleatorio entre 1 y 10, y el usuario debe intentar adivinarlo. El programa debe proporcionar pistas si el número ingresado por el usuario es demasiado alto o bajo. El bucle while debe continuar hasta que el usuario adivine correctamente. Al final se debe imprimir en cuantos intentos el usuario logró adivinar el número.**

Lo primeroe s crear el rango de valores, posteriormente se pedirá al usuario ingresar un valor para ver si lo adivinó, se realiza la comparación entre el número secreto y el valor introducido por el usuario, si este es diferente se dará por incorrecto el intento y se comparará con la respuesta correcta, esto para determinar si se trata de un valor mayor o menor, de modo que sea una ayuda para el usuario, este proceso se repetirá de maenra indefinida hasta que el usuario logre acertar el número, cuando lo adivine se romperá el bucle creado y se felicitará al usuario, mostrando además el número de intentos que le costó adivinar.

    import random
    
    #Se genera un número aleatorio entre el 1 y el 10
    numerosecreto = random.randint(1, 10) 
    
    #Se le solicita la usuario que intente adivinarlo
    print("Se generó un número secreto aleatorio, adivinelo si puede: ")
    a = int(input("Ingresa el numero que crees que es :" )) 
    #Se crea una variable que llevará el conteo de intentos
    intentos=1
    
    #Se crea un while que funcionará hasta que el usuario adivine correctamente el número
    while (a!= numerosecreto):
        dif = numerosecreto - a
        print("El número es incorrecto: ", end="")
        intentos=intentos+1
        if dif > 0:
            print("Es número es más alto")
        else:
            print("El número es mas bajo")
        #Se da al usuario otra oportunidad de adivinar
        a = int(input("Ingresa otro número :"))
    
    #Se felicita al usuario por adivinar el número secreto y se dice el número de intentos
    print("¡¡¡¡¡¡FELICIDADES!!!!!")
    print("El número secreto era", a)
    print("Número de intentos: ", intentos)

    ![ejercicio5](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/c93b15af-3040-4d1f-83ef-eed06f8be46c)


**6) Robot explorador: El programa debe generar una matriz de al menos 5x5. El robot inicia su camino en la posición (0,0) de la matriz y debe salir en la posición (4,4) o la máxima posición si se cambia el tamaño de matriz. El numero y la posición de los obstáculos es aleatoria. El robot solo puede avanzar, girar a la izquierda o a la derecha para buscar un camino libre, en el eventual caso que el robot no pueda salir debe imprimir en pantalla “Imposible llegar al destino”. En caso de que el robot llegue a su destino final deberá imprimir el mapa, con los espacios libres yobstáculos de la siguiente forma:
X obstáculo o libre.**

o o o X o

o o o o o

o o o o X

o o o o o

o X X X o 

**Deberá imprimir también la ruta que siguió. Mostrar un segundo mapa con el “camino” seguido por el robot mediante flechas**

Para resolver el ejercicio, y emplear un comando más ordenado, se harpa uso de la creación de varias funciones, esto para llamarlas al código principal, la primera función es la de buscar, en la cual se creará la matriz que será el mapa que el robot tendrá que completar.

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/78d358f6-1311-4718-a9c7-dd2a5346b5c3)

Posteriormente se define el movimiento para cada una de las direcciones que el robot puede tomar, es decir, para derecha, abajo, izquierda o arriba, cada dirección se define en una función diferente. La estructura es muy similar entre ellas, puesto que define un movimiento que realiza el robot, las diferencias entre las 4 secciones radica en el símbolo que se imprimirá, dicho simbolo muestra el camino que se toma, siendo ->, V. <- y A respectivamente, además, para cada movimiento se deja la opción de regresar a la posición anterior, esto para cuando choque con algún obstáculo:

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/dbf3b2e8-be8d-4946-964d-54381615a04f)

El siguiente paso es la creación de la función "buscar" este se encargará de trazar la ruta para el destino, se realiza mediante la aplicación de comandos if, los cuales harán que en caso de que la condición sea diferente a un obstáculo (X) se avance en esa casilla, y en caso de que la condición se cumpla, mandará a retroceder al robot, este proceso se aplica para las 4 direcciones, probando primeramente para abajo, después a la izquierda, luego hacia arriba y al final a la derecha. Parte de esta función se observa a continuación:

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/eea544c8-2e94-4534-be56-0008e453bd15)

Establecidas las funciones se crea el código principal, definiendo que existe una matriz de tamaño 5x5, y que habrá, como máximo 10 obstáculos, lo primero es crear la matriz sin obstáculos, y despué sagregarlos de forma aleatoria, esto permite la creación de un mapa diferente cada vez que se ejecute el código:

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/73d972ee-3d98-4e64-96ca-43abfcb4537c)

Una vez creado el mapa, se procede a la resolución del mismo, esto se hace empleando un while hasta llegar a la meta, y llamando a las funciones de movimientos, de modo que se prueba una por una hasta llegar al destino establecido, posterioemnte se imprime el mapa con la ruta trazada, lo que refleja los simbolos que marcan la ruta que el robot siguio.

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/ab4d76a8-7c6d-486d-9d75-ccadca666843)

Se muestran dos ejecuciones del código para mostrar que en cada ejecución se tiene una ruta diferente:

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/b81f3f02-93cc-417f-9861-cdc1e4882c79)

![image](https://github.com/DiegoJGutierrezReyes/Lab-1/assets/132300202/f6c2a506-3acc-40dc-80d2-fbe242de75f8)













https://blog.hubspot.es/website/que-es-python#que-es

https://www.ionos.mx/digitalguide/paginas-web/desarrollo-web/comandos-java/
