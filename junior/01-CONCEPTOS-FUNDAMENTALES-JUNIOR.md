# Conceptos Fundamentales Junior
### Como escribir prompts que de verdad funcionen (usando temas que te importan)

---

## Introduccion: La IA es como un amigo nuevo

Imagina que tienes un amigo que:
- Sabe muchisimo de todo
- Jamas te ha visto en persona
- No sabe nada de ti: ni tu edad, ni tus gustos, ni que te gusta Minecraft
- Hara exactamente lo que le pidas... pero solo si se lo pides bien

Si le dices "dame algo divertido", no sabe si para ti "divertido" es jugar futbol, ver anime o construir una base en Minecraft. Ese es el secreto: cuanto mas le cuentes sobre ti y lo que quieres, mejor te ayuda.

---

## 1. La Anatomia de un Prompt: Las 3 Partes que Nunca Faltan

Todo buen prompt tiene 3 partes, como un sandwich:

| Parte | Pregunta que responde | Ejemplo |
|---|---|---|
| **ROL** | Quien debe ser la IA? | "Eres un critico de videojuegos de IGN" |
| **CONTEXTO** | Cual es la situacion? | "Tengo 13 anos, me gustan los juegos de accion, tengo Xbox y $30 de presupuesto" |
| **INSTRUCCION** | Que quiero exactamente? | "Recomiendame 3 juegos, dime lo bueno y lo malo de cada uno, y cual elegirias tu" |

### Veamoslo en accion:

**MAL (asi escribe la mayoria):**
```
Recomiendame un juego
```
Resultado: la IA te recomienda un juego aleatorio que probablemente no te guste.

**BIEN (con las 3 partes):**
```
ROL: Eres un critico de videojuegos especializado en juegos para adolescentes.

CONTEXTO: Tengo 13 anos. Me gustan los juegos de accion y aventura como Minecraft
y Brawl Stars. Tengo una Xbox Series S. Mis papas me dejan jugar 2 horas al dia
maximo. Presupuesto: $30 dolares. Juego solo o con 2 amigos online.

INSTRUCCION: Recomiendame 3 juegos que:
- Sean de accion o aventura
- Funcionen en Xbox Series S
- Cuesten $30 o menos
- Se puedan jugar en sesiones de 1-2 horas
- Tengan modo multiplayer online

Para cada juego dime:
1. De que se trata (en 2 lineas)
2. Que es lo mejor (1 cosa)
3. Que es lo peor (1 cosa)
4. Tu puntuacion del 1 al 10
```

Resultado: la IA te da exactamente lo que necesitas.

### Otro ejemplo con otro tema:

**MAL:**
```
Que hago con mis amigos el fin de semana
```

**BIEN:**
```
ROL: Eres un organizador de planes divertidos para adolescentes.

CONTEXTO: Tengo 14 anos. Vivo en una ciudad mediana. Somos 5 amigos. Nos gustan
los deportes, los videojuegos y la pizza. Tenemos $15 dolares cada uno. Es sabado
por la tarde. No tenemos coche, nos movemos en bici o caminando. Hace buen clima.

INSTRUCCION: Dame 5 planes que podamos hacer. Para cada plan dime:
- Que necesitamos llevar
- Cuanto nos costaria por persona
- Cuanto tiempo toma
- Nivel de diversion del 1 al 10
```

---

## 2. Los 5 Niveles de Especificidad

Tu prompt puede ser desde "super vago" hasta "quirurgico". Veamos como evoluciona con un tema que conoces:

### Ejemplo: Quieres que la IA te ayude con un equipo de Pokemon

| Nivel | Prompt | Resultado |
|---|---|---|
| **1. Vago** | "Dime algo de Pokemon" | Basura. La IA no tiene idea de que quieres |
| **2. Basico** | "Recomiendame un equipo Pokemon" | Generico. Te dira cualquier cosa |
| **3. Dirigido** | "Recomiendame un equipo Pokemon para competitivo" | Mejor. Ya sabe que es para luchar en serio |
| **4. Detallado** | "Recomiendame un equipo Pokemon para competitivo en formato OU de Pokemon Escarlata/Purpura" | Bueno. Ya tiene contexto del juego y formato |
| **5. Quirurgico** | "Eres un campeon mundial de VGC. Arma un equipo para formato OU de Pokemon Escarlata/Purpura. Necesito: 1 lead, 2 sweepers, 1 wall, 1 support, 1 cleaner. Para cada Pokemon: nombre, objeto, habilidad, naturaleza, 4 movimientos, EVs. Mi rival usa mucho Gholdengo y Great Tusk." |

### Otro ejemplo: Quieres ayuda con un video de TikTok

| Nivel | Prompt | Resultado |
|---|---|---|
| **1. Vago** | "Ideas para TikTok" | Inutil |
| **2. Basico** | "Ideas para un TikTok de baile" | Muy generico |
| **3. Dirigido** | "Ideas para un TikTok de baile con amigos" | Mejorando |
| **4. Detallado** | "Ideas para un TikTok de baile con 3 amigos, en exteriores, con musica latina de moda" | Bastante bien |
| **5. Quirurgico** | "Eres un creador de contenido de TikTok con 2 millones de seguidores. Necesito un guion para un TikTok de baile de 30 segundos. Somos 4 amigos (2 chicos, 2 chicas, todos 15-16 anos). Queremos usar la cancion 'Quevedo BZRP Session' que es tendencia. Locacion: un parque con murales de graffiti. Incluye: idea del video, coreografia basica descrita paso a paso, outfits sugeridos, y 3 hashtags optimos." |

### La regla de oro:

Si no le darias una instruccion tan vaga a un amigo humano, no se la des a la IA.

---

## 3. Como "Piensa" la IA (y por que te conviene saberlo)

La IA no "piensa" como nosotros. Es mas como un adivinador de palabras super entrenado.

**Analogia:** Es como el auto-completar del teclado de tu telefono, pero con esteroides.

Cuando escribes "Hoy voy a...", tu telefono sugiere "la escuela", "casa", "jugar". La IA hace lo mismo pero con TODO el conocimiento de internet.

**Que significa esto para ti:**
- Las PRIMERAS palabras de tu prompt importan muchisimo. Marcan el camino.
- La IA predice palabra por palabra. Por eso si empiezas con un rol claro ("Eres un experto en..."), toda la respuesta seguira ese tono.
- El ORDEN importa. No es igual decir "Escribe un cuento de terror para ninos" que "Para ninos un cuento de terror escribe".

---

## 4. Iterar: Tu Superpoder Secreto

El secreto mejor guardado: **NADIE escribe el prompt perfecto al primer intento.**

Los profesionales hacen esto:

```
Paso 1: Escriben un prompt mas o menos
Paso 2: Ven que salio mal (muy generico? tono equivocado? falta info?)
Paso 3: Ajustan UNA sola cosa
Paso 4: Vuelven a probar
Paso 5: Repiten hasta que les gusta
```

### Ejemplo real de iteracion:

**Intento 1 (MAL):**
```
Hazme un cuento
```
Resultado: un cuento generico y aburrido.

**Intento 2 (agrego tema):**
```
Hazme un cuento de un dragon que no sabe volar
```
Resultado: mejor, pero muy infantil.

**Intento 3 (agrego tono):**
```
Hazme un cuento de un dragon adolescente que no sabe volar, en tono divertido,
como si fuera un episodio de una serie animada
```
Resultado: mas o menos lo que queria.

**Intento 4 (especifico formato):**
```
Eres un guionista de Pixar. Escribe un micro-cuento de 200 palabras sobre un
dragon de 15 anos que es el unico de su especie que no puede volar. Sus amigos
se burlan. Un dia descubre que en lugar de volar, puede hacerse invisible.
Tono: divertido pero con corazon, estilo "Como entrenar a tu dragon". Incluye
un dialogo comico entre el dragon y su mejor amigo (un murcielago).
```
Resultado: EXACTAMENTE lo que querias.

La diferencia entre el intento 1 y el 4 es ABISMAL. Eso es iterar.

---

## 5. La Formula Magica

Cuando no sepas como empezar, usa esto:

```
ROL + CONTEXTO + OBJETIVO + RESTRICCIONES + FORMATO = PROMPT GANADOR
```

### Aplicala a cualquier tema:

**Tema: Tarea de historia**
```
ROL: Eres un profesor de historia que explica las cosas como si fueran
una serie de Netflix

CONTEXTO: Tengo 13 anos. Manana tengo examen de la Revolucion Mexicana.
No entiendo nada de lo que dice mi libro de texto. Solo se que habia
un tal Pancho Villa.

OBJETIVO: Explicame las 5 cosas MAS importantes que necesito saber
para aprobar el examen

RESTRICCIONES: Usa lenguaje simple. Nada de palabras raras. Maximo 300
palabras en total. Nada de fechas exactas si no son esenciales.

FORMATO: Para cada punto: Titulo llamativo + explicacion de 3 lineas +
una comparacion con algo actual que yo conozca
```

**Tema: Planear mi cumpleanos**
```
ROL: Eres un organizador de fiestas de cumpleanos especializado en
adolescentes

CONTEXTO: Cumplo 14 anos. Somos 8 amigos. Me gusta el futbol y los
videojuegos. Presupuesto total: $100. El cumpleanos es en mi casa
(tengo patio trasero). Mis papas estaran en casa pero "sin molestar".

OBJETIVO: Crear un plan de fiesta de 4 horas

RESTRICCIONES: Nada que haga mucho ruido (vecinos). Nada que ensucie
demasiado (mi mama me mata). Presupuesto maximo $100 para TODO.

FORMATO: Timeline con: hora / actividad / materiales necesarios / costo
estimado
```

---

## Antes de ir al siguiente modulo

Prueba esto AHORA MISMO en ChatGPT, Copilot o Gemini:

```
ROL: Eres un amigo que sabe mucho de [TU TEMA FAVORITO: videojuegos, futbol,
musica, anime...]

CONTEXTO: [ESCRIBE 3 COSAS SOBRE TI: edad, gustos, que necesitas]

INSTRUCCION: [QUE QUIERES EXACTAMENTE: recomendacion, explicacion, idea...]
+ [COMO QUIERES LA RESPUESTA: lista, tabla, pasos, parrafos cortos...]
```

[→ Ir a Tecnicas de Prompting Junior](./02-TECNICAS-DE-PROMPTING-JUNIOR.md)
