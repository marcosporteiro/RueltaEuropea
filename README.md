# RueltaEuropea
Ruleta Europea hecha en python

#Para instalar
pip install RuletaEuropea

#Ejemplo de uso

```python
from RuletaEuropea.Apuesta import *
from RuletaEuropea.Constantes import *
from RuletaEuropea.Ruleta import *

def main():

    print("Bienvenido a la ruleta \n")
    ruleta = Ruleta()

    print(ruleta.añadir_apuesta(Apuesta("Juan", APUESTA_COLOR, VERDE, 1)))
    print(ruleta.añadir_apuesta(Apuesta("Roberto", APUESTA_COLUMNA, 1, 1)))
    print(ruleta.añadir_apuesta(Apuesta("Alejandra", APUESTA_DOCENA, 3, 1)))
    print(ruleta.añadir_apuesta(Apuesta("Maria", APUESTA_NUMERO, 34, 1)))
    print(ruleta.añadir_apuesta(Apuesta("Rodrigo", APUESTA_PAR_IMPAR, PAR, 1)))
    print(ruleta.añadir_apuesta(Apuesta("Marcos", APUESTA_CALLE, 12, 1)))

    print("\n"+ruleta.girar_ruleta())

    print ("\nGanadores:")
    for ganador in ruleta.obtener_ganadores():
        print(ganador.str_ganador())

    print ("\nPerdedores:")
    for perdedor in ruleta.obtener_perdedores():
        print(perdedor.str_perdedor())

if __name__ == '__main__':
    main()

```
