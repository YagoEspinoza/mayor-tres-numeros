"""Módulo que contiene clases para realizar operaciones matemáticas básicas."""


class OperacionesBasicas:
    """Clase que permite realizar operaciones matemáticas básicas como suma y resta."""

    def __init__(self):
        """Inicializa la clase con un atributo resultado."""
        self.resultado = 0

    def sumar(self, a, b):
        """Suma dos números y almacena el resultado."""
        self.resultado = a + b

    def restar(self, a, b):
        """Resta dos números y almacena el resultado."""
        self.resultado = a - b

    def obtener_resultado(self):
        """Retorna el resultado de la última operación realizada."""
        return self.resultado


class CalculadoraPromedio:
    """Clase que permite calcular el promedio de una lista de valores numéricos."""

    def __init__(self, valores):
        """Inicializa la clase con una lista de valores."""
        self.valores = valores

    def calcular_promedio(self):
        """Calcula y retorna el promedio de los valores almacenados."""
        if not self.valores:
            return 0  # Evitar división por cero

        suma_total = sum(self.valores)
        return suma_total / len(self.valores)

    def obtener_valores(self):
        """Retorna la lista de valores almacenados."""
        return self.valores


# Variables globales (manteniendo nombres en mayúsculas según convención PEP 8)
NUMEROS = [1, 2, 3, 4, 5]
NUM1 = 10
NUM2 = 20

# Ejecución principal
if __name__ == "__main__":
    # Usar la clase OperacionesBasicas
    operaciones = OperacionesBasicas()
    operaciones.sumar(NUM1, NUM2)
    print(f"El resultado de la suma es: {operaciones.obtener_resultado()}")

    operaciones.restar(NUM1, NUM2)
    print(f"El resultado de la resta es: {operaciones.obtener_resultado()}")

    # Usar la clase CalculadoraPromedio
    calculadora_promedio = CalculadoraPromedio(NUMEROS)
    resultado_promedio = calculadora_promedio.calcular_promedio()
    print(f"El promedio de los números es: {resultado_promedio}")
