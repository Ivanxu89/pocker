# Pocker · Texas Hold'em

Texas Hold'em sin límite para navegador: juegas contra tres rivales que controla la máquina (Lola, Ramón y Carmen).

Es un único archivo, `index.html`, sin dependencias ni compilación. Ábrelo en el navegador para jugar.

## Reglas

- Cada jugador empieza con 1000 fichas.
- Ciegas de 10 / 20 que se doblan cada 8 manos.
- Dos cartas propias y cinco comunitarias (flop, turn y river), con cuatro rondas de apuestas.
- Sin límite: se puede subir cualquier cantidad desde la subida mínima hasta el all-in.
- Botes laterales cuando alguien va all-in y reparto del bote en caso de empate.
- Ganas cuando dejas a los tres rivales sin fichas.

## Controles

| Tecla | Acción |
|---|---|
| F | Retirarse |
| C | Pasar / igualar |
| R | Apostar / subir |
| Enter | Siguiente mano |

## Estructura del código

Todo está en `index.html`:

- **Evaluación de manos**: `evaluate()` puntúa 5 cartas y `best()` elige la mejor combinación de 5 entre 7.
- **Flujo de la mano**: `playHand()` reparte, cobra ciegas y recorre preflop, flop, turn y river; `bettingRound()` gestiona cada ronda.
- **Rivales**: `aiAct()` decide según la fuerza de la mano (`preflopStrength()` / `postflopStrength()`), el bote y el carácter de cada rival.
- **Reparto**: `showdown()` calcula botes principal y laterales.

## Próximos pasos

Integrar el juego como minijuego dentro de [Casino Idle Tycoon](https://github.com/Ivanxu89/casino-idle-tycoon).
