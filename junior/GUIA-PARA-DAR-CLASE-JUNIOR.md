# Guia para Dar Clase de Ingenieria de Prompt (Version Junior)
### Para profesores que enseñan a alumnos de 10 a 17 anos

---

## Sobre esta guia

Esta guia adapta el contenido del repositorio completo para una clase dirigida a niños y adolescentes. El lenguaje, los ejemplos y la dinamica estan diseñados para mentes jovenes, manteniendo la esencia tecnica pero haciendola accesible y divertida.

---

## Antes de la clase: Checklist del profe

- [ ] Confirmar que los alumnos tienen acceso a ChatGPT, Copilot o Gemini (todos tienen version gratuita)
- [ ] Tener al menos 3 ejemplos preparados de ANTES vs DESPUES de mejorar un prompt
- [ ] Leer los archivos junior: [Glosario](./00-GLOSARIO-JUNIOR.md), [Fundamentos](./01-CONCEPTOS-FUNDAMENTALES-JUNIOR.md), [Tecnicas](./02-TECNICAS-DE-PROMPTING-JUNIOR.md)
- [ ] Preparar 2-3 "prompts malos" escritos en grande en una pizarra/diapositiva
- [ ] Tener a mano ejemplos juveniles de respaldo si los alumnos no saben que preguntar

---

## Estructura de clase (90 minutos)

| Tiempo | Bloque | Actividad |
|---|---|---|
| 0:00 - 0:10 | Apertura | Que es una IA y por que deberia importarte |
| 0:10 - 0:25 | Bloque 1: Vocabulario | 4 terminos clave con analogias juveniles |
| 0:25 - 0:45 | Bloque 2: Anatomia del Prompt | Las 3 partes + los 5 niveles de especificidad |
| 0:45 - 0:60 | Bloque 3: Ejercicio en vivo | Los alumnos mejoran un prompt MALO frente a todos |
| 0:60 - 0:75 | Bloque 4: Tecnicas estrella | Zero-Shot, Few-Shot y Chain-of-Thought |
| 0:75 - 0:85 | Bloque 5: Errores y cierre | Los 3 errores mas comunes + principios finales |
| 0:85 - 0:90 | Desafio final | "El prompt del millon" - competencia amistosa |

---

## Bloque 0: Apertura (10 min)

### Que decir (3 minutos):

> "Levanten la mano si alguna vez usaron ChatGPT, Copilot o Gemini."
>
> (Casi todas las manos se levantan.)
>
> "Levanten la mano si ALGUNA VEZ la IA les dio una respuesta que no servia para nada."
>
> (Risas, muchas manos.)
>
> "Hoy vamos a aprender por que pasa eso... y como arreglarlo. En 90 minutos van a pasar de 'meh, mas o menos' a 'WOW, justo lo que necesitaba'."

### Dinamica rompehielo (7 minutos):

Pide a 3 voluntarios que lean en voz alta EL PEOR prompt que se les ocurra. Escribelo en la pizarra.

Ejemplos que sugerir si no se les ocurre:
- `"Dime algo"`
- `"recomiendame una pelicula"`
- `"Ayuda"`

Pregunta a la clase: **"Si le dijeran esto a un amigo humano, su amigo sabria que quieren?"**

---

## Bloque 1: Vocabulario (15 min)

Enseña SOLO estos 4 terminos con sus analogias:

### 1. TOKEN (3 min)

> "Un token es como un bloque de Minecraft. Solo no hace mucho, pero juntos construyen un castillo. Es la pieza mas pequeña de texto que la IA entiende."

**Ejercicio:** Pide a un alumno que cuente las palabras de "Hola, como estas?". Explica que eso son ~5 tokens.

### 2. VENTANA DE CONTEXTO (4 min)

> "Juguemos al telefono descompuesto. Yo le digo algo al primer alumno, ese se lo dice al de al lado... Cuando llega al final, que paso con el mensaje original?"

Haz una mini-demo con 5-6 alumnos. Explica: "La IA tiene el mismo problema. En conversaciones muy largas, olvida lo del principio."

### 3. TEMPERATURA (4 min)

> "En un videojuego, tienes diferentes modos: historia, normal, creativo. La temperatura es el selector de modo de la IA."

| Temperatura | Modo videojuego | Cuando usarlo |
|---|---|---|
| Baja (0.1-0.3) | Modo historia | Tarea de matematicas, datos exactos |
| Media (0.4-0.6) | Modo normal | La mayoria de las cosas |
| Alta (0.7-1.0) | Modo sandbox | Crear canciones, inventar historias, memes |

### 4. ALUCINACION (4 min)

> "¿Alguna vez un amigo les conto algo de un partido que no vio, pero lo dijo con tanta seguridad que le creyeron? ESO es una alucinacion."

Muestra este ejemplo:

```
Pregunta: "Cual es la formula del agua?"
Respuesta correcta: H2O
Alucinacion: "La formula del agua es H3O2"
```

> "Moraleja: Si la IA te dice algo importante para tu tarea o examen, VERIFICALO en otra fuente."

---

## Bloque 2: Anatomia del Prompt (20 min)

### Las 3 partes (10 min)

Dibuja o proyecta esto:

```
PROMPT = ROL + CONTEXTO + INSTRUCCION
```

Explica cada parte con un ejemplo que ellos entiendan:

**Tema: Recomendar un videojuego**

| Parte | Pregunta | Ejemplo |
|---|---|---|
| ROL | Quien debe ser la IA? | "Eres un critico de videojuegos de IGN" |
| CONTEXTO | Cual es la situacion? | "Tengo 13 anos, Xbox, $30, me gusta accion" |
| INSTRUCCION | Que quiero exactamente? | "Recomiendame 3 juegos con pros, contras y puntuacion" |

### Los 5 niveles de especificidad (10 min)

Muestra la evolucion con un tema que les importe. El mejor: VIDEOJUEGOS o TIKTOK.

**Ejemplo con TikTok:**

| Nivel | Prompt |
|---|---|
| 1. Vago | "Ideas para TikTok" |
| 2. Basico | "Ideas para un TikTok de baile" |
| 3. Dirigido | "Ideas para un TikTok de baile con amigos, musica latina" |
| 4. Detallado | Agrega: cuantos amigos, locacion, duracion del video |
| 5. Quirurgico | Agrega: cancion especifica, coreografia, hashtags, hora de publicacion |

> **"La regla de oro: si no le darias una instruccion tan vaga a un amigo, no se la des a la IA."**

**Mini-ejercicio rapido (3 min):**
Entre todos en clase, tomen un prompt nivel 1 y subanlo juntos a nivel 5. Que los alumnos griten ideas. El profe escribe en la pizarra.

---

## Bloque 3: Ejercicio en Vivo (15 min)

### Dinamica: "El antes y el despues"

1. **Muestra este prompt MALO en la pizarra:**
   ```
   Que puedo hacer el fin de semana
   ```

2. **Pide a la clase que identifique QUE LE FALTA:**
   - No dice edad
   - No dice con quien
   - No dice presupuesto
   - No dice donde viven
   - No dice que les gusta

3. **Un voluntario ejecuta el prompt MALO en ChatGPT/Copilot en tiempo real.** Todos ven la respuesta... mediocre.

4. **Entre todos construyen la version MEJORADA** usando Rol + Contexto + Instruccion. El profe guia con preguntas:
   - "Tienen 15 anos?"
   - "Son 4 amigos?"
   - "Cuanto dinero tienen?"
   - "Que les gusta hacer?"

5. **El resultado en la pizarra deberia verse algo como:**
   ```
   ROL: Eres un organizador de planes divertidos para adolescentes.
   CONTEXTO: Tengo 15 anos. Somos 4 amigos. Tenemos $15 cada uno.
   Vivimos en [ciudad]. Nos gustan los deportes y comer pizza.
   Es sabado, hace buen clima. Nos movemos en bici.
   INSTRUCCION: Sugiere 3 planes con: que necesitamos, costo
   por persona, duracion, y diversion del 1 al 10.
   ```

6. **Ejecutan el prompt BUENO. Comparan resultados.**

La diferencia es tan grande que los alumnos lo entienden al instante.

---

## Bloque 4: Las 3 Tecnicas Estrella (15 min)

Para alumnos jovenes, enseña SOLO estas 3. Las demas (ReAct, ToT) son para los mayores de 15 que tengan interes.

### 1. Zero-Shot: Sin ejemplos (5 min)

> "Es la tecnica que usas todos los dias. Pedir algo directo, sin dar ejemplos. El 80% de lo que haces es Zero-Shot. El truco es no ser vago."

```
MAL: "Hablame de futbol"
BIEN: "Eres un comentarista de ESPN. Explicame el fuera de lugar en el futbol
usando una analogia de Minecraft. Maximo 50 palabras."
```

### 2. Few-Shot: Con ejemplos (5 min)

> "Es como cuando le enseñas a tu hermanito a hacer algo: primero lo haces tu 2 o 3 veces, luego le dices 'ahora hazlo tu'."

```
Convierte frases a estilo TikTok (5 palabras max):

"Me fue mal en el examen" -> "RIP mi promedio 😭"
"Gane en Fortnite" -> "Crown royale facil 🏆"

Ahora convierte: "Manana no hay clases"
```

### 3. Chain-of-Thought: Paso a paso (5 min)

> "Como cuando el profe de mates te dice 'no solo la respuesta, muestrame como llegaste'."

Haz un ejemplo en vivo: "Ayudame a decidir entre ir al cine con mis amigos o estudiar para un examen mañana. Piensa paso a paso."

---

## Bloque 5: Errores y Cierre (10 min)

### Los 3 errores que TODOS cometen:

**Error 1: Ser demasiado vago**
```
MAL: "Ayudame"
BIEN: [Lo que sea, pero con contexto]
```

**Error 2: No definir el formato**
```
MAL: "Dime sobre los dinosaurios"
BIEN: "...en 5 bullets, con nombre y dato curioso de cada uno"
```

**Error 3: No iterar (rendirse tras el primer intento)**
> "El primer prompt NUNCA es el mejor. Los PROs escriben, prueban, ajustan, repiten."

### 3 Principios para recordar:

1. **La IA no lee mentes:** Si eres vago, respuesta vaga. Si eres especifico, respuesta util.
2. **Rol + Contexto + Instruccion:** El 80% de un buen prompt.
3. **Itera sin miedo:** Primera respuesta = borrador. Tercera respuesta = oro.

---

## Bloque 6: Desafio Final - "El Prompt del Millon" (5 min)

**Consigna:** "Tienen 3 minutos para escribir el MEJOR prompt que se les ocurra. El tema es libre. Gana el que obtenga la respuesta mas impresionante de la IA."

Los alumnos escriben y ejecutan su prompt. 2-3 voluntarios comparten su resultado con la clase.

**El profe elige ganador basado en:**
- Uso de las 3 partes (Rol + Contexto + Instruccion)
- Creatividad del tema
- Calidad del resultado obtenido

---

## Material de apoyo para el profe

### Ejemplos de respaldo (si un alumno no sabe sobre que escribir):

**Temas que siempre funcionan con jovenes:**
- "Recomiendame un juego para mi celular que no pese mucho"
- "Escribe el final alternativo de [serie/pelicula favorita]"
- "Creame un personaje para mi comic/manga"
- "Como le digo a mi crush que me gusta sin que sea incomodo"
- "Ayudame a planear mi fiesta de cumpleanos con $100 de presupuesto"
- "Explicame [tema escolar dificil] como si fuera un TikTok"
- "Arma el mejor equipo Pokemon para ganarle a mi amigo que usa puros legendarios"
- "Escribe una cancion de rap sobre mi gato"

### Frases motivadoras para la clase:

- "No existe el prompt perfecto. Existe el prompt que funciona para TI."
- "La IA es como un amigo muy inteligente que acabas de conocer. No sabe nada de ti hasta que tu se lo cuentas."
- "Hace 2 anos esto no existia. En 2 anos, el que no sepa hacer prompts va a estar en desventaja."
- "El prompting no es programacion. Es comunicacion. Y comunicarse bien sirve para TODO en la vida."

---

## Recursos extra

- [Glosario Junior](./00-GLOSARIO-JUNIOR.md) - Para repasar terminos
- [Fundamentos Junior](./01-CONCEPTOS-FUNDAMENTALES-JUNIOR.md) - Anatomia del prompt en detalle
- [Tecnicas Junior](./02-TECNICAS-DE-PROMPTING-JUNIOR.md) - Las 5 tecnicas explicadas
- [Laboratorio Junior](./07-LABORATORIO-JUNIOR.md) - 10 ejercicios para practicar

---

*"Un buen profe no enseña prompts. Enseña a pensar antes de escribir."*
