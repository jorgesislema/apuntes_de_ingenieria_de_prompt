# Ficha Express: ANATOMIA DEL PROMPT

---

## Las 3 partes que NUNCA fallan

```
PROMPT = ROL + CONTEXTO + INSTRUCCION
```

| Parte | Pregunta | Ejemplo |
|---|---|---|
| **ROL** | Quien debe ser la IA? | "Eres un critico de videojuegos" |
| **CONTEXTO** | Cual es mi situacion? | "Tengo 13 anos, Xbox, $30" |
| **INSTRUCCION** | Que quiero exactamente? | "Recomiendame 3 juegos con pros y contras" |

---

## Ejemplo completo

```
MAL:
Recomiendame un juego

BIEN:
ROL: Eres un critico de videojuegos de IGN.
CONTEXTO: Tengo 13 anos. Me gusta la accion. Tengo Xbox y $30 dolares.
INSTRUCCION: Recomiendame 3 juegos. Para cada uno: nombre, de que trata
(2 lineas), lo mejor, lo peor, puntuacion del 1 al 10.
```

---

## Regla de oro
Si no le darias una instruccion tan vaga a un amigo humano, no se la des a la IA.
