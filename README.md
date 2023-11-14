# Redes-Neuronales-Ejercicios-Python
{
  "nbformat": 4,
  "nbformat_minor": 0,
  "metadata": {
    "colab": {
      "provenance": []
    },
    "kernelspec": {
      "name": "python3",
      "display_name": "Python 3"
    },
    "language_info": {
      "name": "python"
    }
  },
  "cells": [
    {
      "cell_type": "markdown",
      "source": [
        "# A2: Ejercicios en Pyhton\n",
        "Hugo Alejandro Mendoza Flores   1991950   N1 Sabatino"
      ],
      "metadata": {
        "id": "WFxFkSVC2y0B"
      }
    },
    {
      "cell_type": "markdown",
      "source": [
        "1. Escribe un programa que solicite al usuario un número y que indique si es par o impar."
      ],
      "metadata": {
        "id": "a_2ulUYG3JRg"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# Solicitar al usuario un número entero\n",
        "numero = int(input(\"Por favor, ingresa un número entero: \"))\n",
        "\n",
        "# Comprobar si el número es par o impar\n",
        "if numero % 2 == 0:\n",
        "    print(f\"{numero} es un número par.\")\n",
        "else:\n",
        "    print(f\"{numero} es un número impar.\")\n",
        ""
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "xeVXHqGj26F-",
        "outputId": "b5f14e56-f29f-42db-8669-f85edf95c7d1"
      },
      "execution_count": 2,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Por favor, ingresa un número entero: 3\n",
            "3 es un número impar.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "2. Escribe un programa que tome una lista de números ingresados por el usuario y muestre la lista en orden inverso."
      ],
      "metadata": {
        "id": "Ph_h1MG93UyP"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "\n",
        "entrada = input(\"Ingresa una lista de números separados por comas: \")\n",
        "\n",
        "numeros = entrada.split(\",\")\n",
        "\n",
        "numeros_enteros = [int(numero.strip()) for numero in numeros]\n",
        "\n",
        "# Mostrar la lista en orden inverso\n",
        "numeros_enteros.reverse()\n",
        "\n",
        "print(\"Lista en orden inverso:\", numeros_enteros)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "P5y5KYYJ3fE7",
        "outputId": "67e7cbf3-0cef-44fb-d8f5-bc1de989d9d4"
      },
      "execution_count": 3,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Ingresa una lista de números separados por comas: 1,2,3,4,5\n",
            "Lista en orden inverso: [5, 4, 3, 2, 1]\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "3. Juego de adivinar el número: Crea un programa que genere un número aleatorio entre 1 y 100, y luego le pida al usuario que adivine el número. El programa debe proporcionar pistas al usuario si el número es mayor o menor que el número objetivo, y seguir solicitando un nuevo intento hasta que el usuario adivine correctamente."
      ],
      "metadata": {
        "id": "Wz6UoPSc392d"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "import random\n",
        "\n",
        "# Generar un número aleatorio entre 1 y 100\n",
        "numero_objetivo = random.randint(1, 100)\n",
        "\n",
        "intentos = 0\n",
        "\n",
        "while True:\n",
        "    # Solicitar al usuario que adivine el número\n",
        "    intento = int(input(\"Adivina el número (entre 1 y 100): \"))\n",
        "    intentos += 1\n",
        "\n",
        "    # Comprobar si el usuario adivinó el número\n",
        "    if intento == numero_objetivo:\n",
        "        print(f\"¡Felicidades! Adivinaste el número {numero_objetivo} en {intentos} intentos.\")\n",
        "        break\n",
        "    elif intento < numero_objetivo:\n",
        "        print(\"El número es mayor. ¡Sigue intentando!\")\n",
        "    else:\n",
        "        print(\"El número es menor. ¡Sigue intentando!\")"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "4zZffGAL4BhE",
        "outputId": "1cf5979a-f80e-4cf1-d35e-5358dc3b3262"
      },
      "execution_count": 5,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Adivina el número (entre 1 y 100): 5\n",
            "El número es mayor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 60\n",
            "El número es mayor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 90\n",
            "El número es menor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 70\n",
            "El número es mayor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 85\n",
            "El número es menor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 77\n",
            "El número es menor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 73\n",
            "El número es mayor. ¡Sigue intentando!\n",
            "Adivina el número (entre 1 y 100): 75\n",
            "¡Felicidades! Adivinaste el número 75 en 8 intentos.\n"
          ]
        }
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "4. Ejercicio de cálculo de números primos en un rango dado:\n",
        "Escribe un programa que solicite al usuario un rango de números y muestre todos los números primos dentro de ese rango."
      ],
      "metadata": {
        "id": "QWW-vAuk5_uN"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# Función para verificar si un número es primo\n",
        "def es_primo(numero):\n",
        "    if numero <= 1:\n",
        "        return False\n",
        "    for i in range(2, int(numero**0.5) + 1):\n",
        "        if numero % i == 0:\n",
        "            return False\n",
        "    return True\n",
        "\n",
        "# Solicitar al usuario el rango de números\n",
        "inicio = int(input(\"Ingresa el número inicial del rango: \"))\n",
        "fin = int(input(\"Ingresa el número final del rango: \"))\n",
        "\n",
        "\n",
        "print(f\"Números primos en el rango de {inicio} a {fin}:\")\n",
        "for num in range(inicio, fin + 1):\n",
        "    if es_primo(num):\n",
        "        print(num)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "UeIMMmVi6IAO",
        "outputId": "0ccd8f57-ecf0-4721-b600-c3154297f1f6"
      },
      "execution_count": 6,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Ingresa el número inicial del rango: 40\n",
            "Ingresa el número final del rango: 80\n",
            "Números primos en el rango de 40 a 80:\n",
            "41\n",
            "43\n",
            "47\n",
            "53\n",
            "59\n",
            "61\n",
            "67\n",
            "71\n",
            "73\n",
            "79\n"
          ]
        }
      ]
    }
  ]
}
