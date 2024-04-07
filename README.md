# Calculadora-de-IMC
Programa en Python que calcula el índice de masa corporal que los datos que nos proporciona el usuario.
El programa se inicia declarando las variables que de peso y estatura para la obtención del Índice de Masa Corporal, después está la sección donde el usuario ingresa su nombre, apellidos, edad, peso y estatura, mientras qué el bloque try y except aseguran que los campos de edad, peso y estura no queden vacío en caso de ser así se mostrará en pantalla un mensaje con la leyenda "Por favor ingrese valores válidos" y volverá a mostrar el mensaje hasta que el usuario conteste correctamente.
En el main se mandan a llamar los datos de usuario y la operación para calcular el IMC con los datos que el usuario ya proporcionó y por último se desplagará el pantalla los datos en forma de lista al igual que su IMC.

Código:
def calcular_IMC(peso, estatura):
    return peso / (estatura ** 2)

def datos_usuario():
    nombre = input("Ingrese su nombre: ")
    apellido1 = input("Ingrese su apellido paterno: ")
    apellido2 = input("Ingrese su apellido materno: ")
   
    while True:
        try:
            edad = int(input("Ingrese su edad: "))
            peso = float(input("Ingrese su peso en kg: "))
            estatura = float(input("Ingrese su estatura en metros: "))
            if edad <= 0 or peso <= 0 or estatura <= 0:
                raise ValueError("Por favor ingrese valores válidos.")
            break
        except ValueError:
            print("Por favor ingrese valores válidos.")

    return nombre, apellido1, apellido2, edad, peso, estatura

def main():
    nombre, apellido1, apellido2, edad, peso, estatura = datos_usuario()
    IMC = calcular_IMC(peso, estatura)
    print("\nDatos del usuario:")
    print("Nombre completo:", nombre, apellido1, apellido2)
    print("Edad:", edad)
    print("Peso:", peso, "kg")
    print("Estatura:", estatura, "m")
    print("Índice de Masa Corporal (IMC):", IMC)

if __name__ == "__main__":
    main()


Reflexiones:
Python es un lenguaje muy completo donde la practica de lógica y sintaxis son muy importantes para la resolución de problemas que se pueden tener al escribir y ejecutar un programa por sencillo que parezca, estoy feliz de poder hacer mi primer programa en python a pesar de los problemas lógicos que enfrenté.
