# PARCIAL

## Punto 1

1. Diferencia entre flip-flop y latch
Latch:
Es un aparato asíncrono (no utiliza reloj).
Cuando la entrada cambia, su salida cambia de inmediato es más sencillo, pero tiene menos control.

Flip-Flop:
Es sincrónico (si utiliza reloj).
Su condición solo se modifica en un lado del reloj (ya sea que suba o baje) es más utilizado y estable en los sistemas digitales.


Tipos de Latch:
- SR Latch
- D Latch


Tipos de Flip-Flop:
- SR 
- D
- JK
- T
 
Características:
- SR: básico, puede tener estado inválido.
- D: evita estados inválidos.
- JK: mejora el SR.
- T: cambia de estado (toggle).


2. Diferencia entre Multiplexor y Demultiplexor
Multiplexor (MUX):
 
- Selecciona una entrada entre varias, tiene varias entradas y una salida.
 
Demultiplexor (DEMUX):
 
- Toma una entrada y la envía a una de varias salidas.
 
MUX de 8 entradas:
8 entradas (I0–I7)
 
3 líneas de selección
 
1 salida
 
Función: elegir una de las 8 entradas


 <img width="307" height="420" alt="multiplexor" src="https://github.com/user-attachments/assets/bca3409d-7ad1-4403-8fd7-380b83c7de8d" />

DEMUX de 8 salidas:
1 entrada
 
3 líneas de selección
 
8 salidas
 
Función: enviar la señal a una de las 8 salidas
 
 <img width="383" height="420" alt="demultiplexor" src="https://github.com/user-attachments/assets/6fe53835-6eb8-493b-950d-d2fe9d3da16c" />


3. Sumadores y circuitos secuenciales
Sumador medio:
Suma 2 bits
Salidas: suma y acarreo
Sumador completo:
Suma 3 bits (incluye acarreo)
Más completo que el medio
Circuitos secuenciales:
Dependen del estado anterior
Usan memoria (flip-flops)
Ejemplo: contadores, registros



4. Mapa de Karnaugh
Es una herramienta para simplificar funciones booleanas.
Sirve para:
Reducir expresiones lógicas, diseñar circuitos más simples y minimizar compuertas.

<img width="370" height="235" alt="mapa-" src="https://github.com/user-attachments/assets/207ba541-1994-4ac8-8079-c101c879c090" />


## Punto 2


2.a Ecuación:
X=A⋅B(C+BD+A⋅B)⋅C
Paso 1: Variables
 
A, B, C, D → 4 variables → 16 combinaciones
 
Paso 2: Tabla de verdad (resumen)
 
Se evalúa la ecuación para todas las combinaciones.
 
(Te dejo la lógica directa para que la copies rápido)
 
Si C = 0 → X = 0 (porque multiplica por C)
Entonces solo analizas cuando C = 1
 
Reduciendo:
 
X=A⋅B(1+BD+AB)
 
Como (1 + algo = 1):
 
X=A⋅B⋅C
Resultado simplificado:
X=ABC
 
Circuito:
3 compuertas AND:
A AND B
resultado AND C

tabla de verdad
 
| A | B | C | D | X = A·B·C |
| - | - | - | - | --------- |
| 0 | 0 | 0 | 0 | 0         |
| 0 | 0 | 0 | 1 | 0         |
| 0 | 0 | 1 | 0 | 0         |
| 0 | 0 | 1 | 1 | 0         |
| 0 | 1 | 0 | 0 | 0         |
| 0 | 1 | 0 | 1 | 0         |
| 0 | 1 | 1 | 0 | 0         |
| 0 | 1 | 1 | 1 | 0         |
| 1 | 0 | 0 | 0 | 0         |
| 1 | 0 | 0 | 1 | 0         |
| 1 | 0 | 1 | 0 | 0         |
| 1 | 0 | 1 | 1 | 0         |
| 1 | 1 | 0 | 0 | 0         |
| 1 | 1 | 0 | 1 | 0         |
| 1 | 1 | 1 | 0 | 1         |
| 1 | 1 | 1 | 1 | 1         |


<img width="463" height="348" alt="image" src="https://github.com/user-attachments/assets/146b5457-aa16-4e70-a3c5-e9d2cf53ecf4" />


2.b Ecuación:
X=ABCBD+CDE+AC
Simplificación:
ABCBD → se simplifica:
ABCBD=ABCD
 
Entonces:
 
X=ABCD+CDE+AC
 
Factor común C:
 
X=C(ABD+DE+A)
 
Simplificando:
 
X=C(A+DE)
Resultado final:
X=C(A+DE)
Circuito:
AND para D·E
OR con A
AND final con C

tabla de verdad:

| A | B | C | D | E | X |
| - | - | - | - | - | - |
| 0 | 0 | 0 | 0 | 0 | 0 |
| 0 | 0 | 0 | 0 | 1 | 0 |
| 0 | 0 | 0 | 1 | 0 | 0 |
| 0 | 0 | 0 | 1 | 1 | 0 |
| 0 | 0 | 1 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 | 1 | 0 |
| 0 | 0 | 1 | 1 | 0 | 0 |
| 0 | 0 | 1 | 1 | 1 | 1 |
| 0 | 1 | 0 | 0 | 0 | 0 |
| 0 | 1 | 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 1 | 0 | 0 |
| 0 | 1 | 0 | 1 | 1 | 0 |
| 0 | 1 | 1 | 0 | 0 | 0 |
| 0 | 1 | 1 | 0 | 1 | 0 |
| 0 | 1 | 1 | 1 | 0 | 0 |
| 0 | 1 | 1 | 1 | 1 | 1 |
| 1 | 0 | 0 | 0 | 0 | 0 |
| 1 | 0 | 0 | 0 | 1 | 0 |
| 1 | 0 | 0 | 1 | 0 | 0 |
| 1 | 0 | 0 | 1 | 1 | 0 |
| 1 | 0 | 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 | 1 | 1 |
| 1 | 0 | 1 | 1 | 0 | 1 |
| 1 | 0 | 1 | 1 | 1 | 1 |
| 1 | 1 | 0 | 0 | 0 | 0 |
| 1 | 1 | 0 | 0 | 1 | 0 |
| 1 | 1 | 0 | 1 | 0 | 0 |
| 1 | 1 | 0 | 1 | 1 | 0 |
| 1 | 1 | 1 | 0 | 0 | 1 |
| 1 | 1 | 1 | 0 | 1 | 1 |
| 1 | 1 | 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 | 1 | 1 |
