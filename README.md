# Redes-Neuronales-Ejercicios-Python
Janeth Jamilet Cardiel Cortes
1867586

Escribe un programa que solicite al usuario un número y que indique si es par o impar.

# Solicitar al usuario un número entero
numero = int(input("Por favor, ingresa un número entero: "))

# Comprobar si el número es par o impar
if numero % 2 == 0:
    print(f"{numero} es un número par.")
else:
    print(f"{numero} es un número impar.")

     
Por favor, ingresa un número entero: 3
3 es un número impar.
Escribe un programa que tome una lista de números ingresados por el usuario y muestre la lista en orden inverso.


entrada = input("Ingresa una lista de números separados por comas: ")

numeros = entrada.split(",")

numeros_enteros = [int(numero.strip()) for numero in numeros]

# Mostrar la lista en orden inverso
numeros_enteros.reverse()

print("Lista en orden inverso:", numeros_enteros)
     
Ingresa una lista de números separados por comas: 1,2,3,4,5
Lista en orden inverso: [5, 4, 3, 2, 1]
Juego de adivinar el número: Crea un programa que genere un número aleatorio entre 1 y 100, y luego le pida al usuario que adivine el número. El programa debe proporcionar pistas al usuario si el número es mayor o menor que el número objetivo, y seguir solicitando un nuevo intento hasta que el usuario adivine correctamente.

import random

# Generar un número aleatorio entre 1 y 100
numero_objetivo = random.randint(1, 100)

intentos = 0

while True:
    # Solicitar al usuario que adivine el número
    intento = int(input("Adivina el número (entre 1 y 100): "))
    intentos += 1

    # Comprobar si el usuario adivinó el número
    if intento == numero_objetivo:
        print(f"¡Felicidades! Adivinaste el número {numero_objetivo} en {intentos} intentos.")
        break
    elif intento < numero_objetivo:
        print("El número es mayor. ¡Sigue intentando!")
    else:
        print("El número es menor. ¡Sigue intentando!")
     
Adivina el número (entre 1 y 100): 5
El número es mayor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 60
El número es mayor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 90
El número es menor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 70
El número es mayor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 85
El número es menor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 77
El número es menor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 73
El número es mayor. ¡Sigue intentando!
Adivina el número (entre 1 y 100): 75
¡Felicidades! Adivinaste el número 75 en 8 intentos.
Ejercicio de cálculo de números primos en un rango dado:
Escribe un programa que solicite al usuario un rango de números y muestre todos los números primos dentro de ese rango.


# Función para verificar si un número es primo
def es_primo(numero):
    if numero <= 1:
        return False
    for i in range(2, int(numero**0.5) + 1):
        if numero % i == 0:
            return False
    return True

# Solicitar al usuario el rango de números
inicio = int(input("Ingresa el número inicial del rango: "))
fin = int(input("Ingresa el número final del rango: "))


print(f"Números primos en el rango de {inicio} a {fin}:")
for num in range(inicio, fin + 1):
    if es_primo(num):
        print(num)
     
Ingresa el número inicial del rango: 40
Ingresa el número final del rango: 80
Números primos en el rango de 40 a 80:
41
43
47
53
59
61
67
71
73
79
