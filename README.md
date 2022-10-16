# CajeroPython. 

'''Hacer un programa que simule un cajero con un saldo inicial de $1000 y tendrá el
siguiente menú de opciones:
1.-Ingresar dinero en la cuenta.
2.-Retirar dinero de la cuenta.
3.-Mostrar dinero disponible.
4.-salir.
'''
# \t 4 espacios al iniciar el mensaje (tabulación).
saldo = 1000
while True:
    print("\t.        :Menú:. ")
    print("1.Ingresar dinero en la cuenta.")
    print("2.-Retirar dinero de la cuenta.")
    print("3.-Mostrar dinero disponible.")
    print("4.-salir.")
    opcion = int(input("Digite una opción de menú:"))
    print()
    if opcion == 1:
        try:
            extra = float(input("¿Cúanto dinero desea ingresar? ->"))
            saldo += extra
            print(f"El dinero en la cuenta es de:${saldo}")
        except:
            print("Ha ocurrido un error, digite una opción válida.")
    elif opcion == 2:
        try:
            retiro = float(input("¿Cúanto dinero desea retirar? ->"))
            if retiro > 1000:
                print("No cuenta con la cantidad indicada.")
            else:
                saldo -= retiro
                print(f"Le queda un saldo de:${saldo}")
        except:
            print("Ha ocurrido un error, digite una opción válida.")
        else:  # Sino hay excepción, se ejecuta el else.
            print("Transacción realizada con éxito.")
        finally:  # Se ejecuta siempre y es útil en bases de datos.
            print("Iteración finalizada.")
    elif opcion == 3:
        print(f"Dinero en la cuenta:${saldo}")

    elif opcion == 4:
        print("Gracias por utilizar su cajero automático.")
        break
    else:
        print("Opción inválida, digite un número correcto.")
