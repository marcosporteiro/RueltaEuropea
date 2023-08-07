# RueltaEuropea
Ruleta Europea hecha en python

# Para instalar
pip install RuletaEuropea

# Tablero

                      Calle    
     01 02 03 04   05 06 07 08  09  10 11 12    
 / | [2;31m03[0m 06 [2;31m09 12[0m | 15 [2;31m18 21[0m 24 | [2;31m27 30[0m 33 [2;31m36[0m | Columna3 
 [2;36m0[0m | 02 [2;31m05[0m 08 11 | [2;31m14[0m 17 20 [2;31m23[0m | 26 29 [2;31m32[0m 35 | Columna2
 \ | [2;31m01[0m 04 [2;31m[2;31m07[0m[2;31m[0m 10 | 13 [2;31m16 19[0m 22 | [2;31m25[0m 28 31 [2;31m34[0m | Columna1 
       1Docena       2Docena       3Docena
        01-18       Par-Impar       19-36
       (Bajos)     [2;31mRojo[0m-Negro      (Altos)

# Ejemplo de uso

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
