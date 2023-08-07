# RueltaEuropea
Ruleta Europea hecha en python

# Para instalar
pip install RuletaEuropea

# Tablero
```ansi
[2;37m[2;37m                      Calle    
     01 02 03 04   05 06 07 08  09  10 11 12 [0m[2;37m[2;33m[2;35m [0m[2;33m[0m[2;37m  [0m
 / | [2;31m03[0m [2;37m06[0m [2;31m09 12[0m | [2;37m15[0m [2;31m18 21[0m [2;37m24[0m | [2;31m27 30[0m [2;37m33 [0m[2;31m36[0m | [2;30m[0m[2;30m[0m[2;37mColumna3 [0m
 [2;36m0[0m | [2;37m02[0m [2;31m05[0m [2;37m08 [0m[2;37m11[0m | [2;31m14 [0m[2;37m17 20[0m [2;31m23 [0m|[2;37m 26 29[0m [2;31m32[0m [2;37m35[0m | [2;30m[0m[2;30m[2;37mColumna2[0m[2;30m[0m
 \ |[2;31m 01[0m [2;37m04[0m [2;31m07[0m [2;37m10[0m | [2;37m13[0m [2;31m16 19[0m [2;37m22 [0m| [2;31m25[0m [2;37m28 31[0m [2;31m34[0m | [2;30m[0m[2;30m[2;37mColumna1 [0m[2;30m[0m
       1Docena       2Docena       3Docena
        01-18       Par-Impar       19-36
       (Bajos)     [2;31mRojo[0m-[2;37mBlanco[0m     (Altos)
```

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
