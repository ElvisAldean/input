# input
#Monte-Carlo
#Calcular el valor  pi con el método Monte Carlo
El objetivo de este programa es de hallar el valor más cercano a Pi por el método monte carlo la cual es un método probabilístico 

Versión=   Python 2.7.3

El programa nos ayuda a buscar el valor  que más se acerque a Pi.
Teniendo una muestra de N# para saber cuál de ella es la que más se acerca a Pi,  la cual va hacer el objetivo.
Mientras más  muestra tenemos más nos acercamos a punto de origen 

declaramos la liberias 
import math
import random

# Esta dos variable nos va ayudar a ingresar los punto que va a estar afuera o dentro del circulo para localizar el origen 
Npontos = 100  # Caracteristica Bag-of-Task
Acirc = 0

# 2 - Obtener  el area com numeros aleatorios
acumulador = 1
while acumulador <= Npontos:
    Px = random.random()
    Py = random.random()
    
#calculamos el valor de cada punto para saber cual se aproxima a valor 
    deltaX = math.pow((Px-0.5),2)
    deltaY = math.pow((Py-0.5),2)
    DistE = math.sqrt(deltaX+deltaY)
    if DistE < 0.5:
        Acirc = Acirc + 1
    acumulador = acumulador + 1

# 3 - Obtener el Valor de Pi
ValorPi = 4*(float(Acirc)/float(Npontos))
print ("===========================================")
print ("     ***  HOLA  Grupo #4   ***            ")
print ("El valor que se acerca a Pi  es:==>  %.3f      " %ValorPi)
print ("===========================================")

y mostramos el punto que mas se acerco a Pi

