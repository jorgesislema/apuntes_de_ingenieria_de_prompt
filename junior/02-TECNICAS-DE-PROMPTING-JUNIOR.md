# Tecnicas de Prompting Junior
### 5 tecnicas para dominar la IA (explicadas con cosas que te gustan)

---

## Introduccion: De usuario basico a PRO

Hasta ahora aprendiste a escribir prompts decentes. Pero hay 5 tecnicas que te convierten en un PRO. Piensa en ellas como las herramientas de tu inventario en un videojuego: cada una sirve para una mision diferente.

---

## Tecnica 1: Zero-Shot (Sin Ejemplos)

**En una frase:** Pedirle a la IA que haga algo sin darle ejemplos. Confiar en que ya sabe del tema.

**Analogia:** Como decirle a tu amigo "dibuja un dragon". No le muestras ningun dragon, confias en que el sabe como se ve un dragon.

**Cuando usarlo:**
- Tareas simples y directas
- Cuando solo necesitas una respuesta rapida
- Es la tecnica que usaras el 80% del tiempo

**Formula:**
```
[ROL] + [TAREA ESPECIFICA] + [CONTEXTO BREVE] + [FORMATO]
```

**Ejemplo con Zero-Shot:**

```
MAL:
"Hablame de futbol"

BIEN:
"Eres un comentarista deportivo de ESPN. Explicame que es el fuera de lugar
en el futbol usando una analogia con Minecraft. Maximo 50 palabras."
```

**Otro ejemplo:**

```
MAL:
"Que serie me recomiendas"

BIEN:
"Eres un critico de series de Netflix. Recomiendame 3 series parecidas a
Stranger Things que pueda ver con mis papas sin que haya escenas incomodas.
Para cada una: nombre, de que trata en 1 linea, y puntuacion del 1 al 10.
Todas deben estar disponibles en Netflix Latinoamerica."
```

---

## Tecnica 2: Few-Shot (Con Pocos Ejemplos)

**En una frase:** Darle a la IA 2 o 3 ejemplos de lo que quieres ANTES de pedirle la tarea real.

**Analogia:** Como cuando le enseñas a tu hermanito a hacer algo: primero lo haces tu 2 o 3 veces, luego le dices "ahora hazlo tu".

**Cuando usarlo:**
- Cuando necesitas un formato o estilo muy especifico
- Cuando Zero-Shot no te da el resultado que buscas
- Para que la IA "copie" tu estilo

**Formula:**
```
[INSTRUCCION] + [EJEMPLO 1] + [EJEMPLO 2] + [NUEVA TAREA]
```

**Ejemplo con Few-Shot:**

```
Convierte estas frases normales a estilo Tiktok (maximo 5 palabras, con emojis):

"Me fue mal en el examen" -> "RIP mi promedio 😭 F"
"Gane la partida de Fortnite" -> "Crown royale facil 🏆 GG"
"Mi crush me hablo hoy" -> "Ya gane el ano 🥰"

Ahora convierte:
"Hoy no hay tarea"
```

**Otro ejemplo - creando nombres para un equipo de futbol:**

```
Convierte estas ideas en nombres epicos para equipos de futbol callejero.
El patron es: [Animal/Objeto] + [Adjetivo epico] + FC:

"Leones furiosos" -> "Leones Indomables FC"
"Tiburones rapidos" -> "Tiburones Letales FC"
"Fenix de fuego" -> "Fenix Legendarios FC"

Ahora convierte: "Dragones salvajes"
```

**Error tipico en Few-Shot:** Dar ejemplos que siguen patrones diferentes.

```
MAL (3 patrones distintos):
"Perro" -> "Mejor amigo del hombre"
"Gato" -> "G: El rey de la casa"
"Hamster" -> "Como cuidar a tu hamster"

BIEN (mismo patron):
"Perro" -> "El Perro: tu compañero para siempre"
"Gato" -> "El Gato: independencia y carino"
"Hamster" -> "El Hamster: diversion en tamano pequeno"
```

---

## Tecnica 3: Chain-of-Thought (Cadena de Pensamiento)

**En una frase:** Pedirle a la IA que muestre su razonamiento PASO A PASO, no solo la respuesta final.

**Analogia:** Como cuando en un examen de matematicas el profe te dice "no solo quiero la respuesta, muestra como llegaste a ella".

**Cuando usarlo:**
- Problemas complejos que requieren analisis
- Decisiones importantes
- Cuando necesitas entender el "por que" de una respuesta

**Formula:**
```
[PROBLEMA] + "Piensa paso a paso" o [PASO 1, PASO 2, PASO 3...]
```

**Ejemplo 1: Decidiendo que hacer el fin de semana**

```
Tengo que decidir entre ir a jugar futbol con mis amigos (partido importante
de la liga del barrio) o ir al cumpleanos de mi prima (que cumple 8 anos y
soy el unico primo "grande" invitado). Ayudame a decidir pensando paso a paso:

PASO 1: Sin mi en el partido, mi equipo pierde un jugador clave? O hay suplente?
PASO 2: Si no voy al cumpleanos, mi prima se enojara mucho? O no se dara cuenta?
PASO 3: El partido es a las 4 PM y el cumpleanos a las 5 PM. Hay forma de ir a los dos?
PASO 4: Que me divierte mas? Que me importa mas?
PASO 5: Existe una tercera opcion (ir al partido y llegar tarde al cumpleanos con un buen regalo)?

Dame tu recomendacion final y por que.
```

**Ejemplo 2: Analizando que skin de Fortnite comprar**

```
Soy jugador de Fortnite. Tengo 2,000 V-Bucks ahorrados. Estoy entre 3 skins
que me gustan. Ayudame a decidir pensando paso a paso:

PASO 1: Cual de las 3 skins es MAS rara (aparece menos en la tienda)?
PASO 2: Cual combina mejor con mis otros cosmeticos (mochilas, picos, gestos)?
PASO 3: Si compro X skin, cuantos V-Bucks me sobran para el pase de batalla?
PASO 4: Cual skin me gusta realmente MAS, ignorando el precio y la rareza?
PASO 5: Recomendacion final con justificacion.

Las skins son: [nombre de skin 1], [nombre de skin 2], [nombre de skin 3]
```

**Ejemplo 3: Tarea escolar dificil**

```
Necesito escribir un ensayo de 500 palabras sobre "Por que es importante
cuidar el medio ambiente". Ayudame a planearlo pensando paso a paso:

PASO 1: Cuales son los 3 argumentos mas fuertes que puedo usar?
PASO 2: Que ejemplo de la VIDA REAL de un adolescente puedo usar para cada argumento?
PASO 3: Como conecto los 3 argumentos para que el ensayo fluya bien?
PASO 4: Cual seria un buen titulo que atrape la atencion de mi profe?
PASO 5: Cual seria un buen cierre (frase final impactante)?

IMPORTANTE: No escribas el ensayo completo. Solo el plan y la estructura.
Soy yo quien debe escribirlo.
```

---

## Tecnica 4: ReAct (Razonar y Actuar)

**En una frase:** La IA alterna entre PENSAR que hacer y ACTUAR, luego OBSERVA el resultado y decide el siguiente paso. Como un detective resolviendo un caso.

**Analogia:** Como cuando armas un rompecabezas dificil: miras las piezas (piensas), pruebas una (actuas), ves si encaja (observas), y decides que hacer despues.

**Ciclo basico:**
```
PENSAMIENTO: Que necesito saber/hacer?
ACCION: Voy a intentar esto...
OBSERVACION: Paso esto...
PENSAMIENTO: Con esta nueva informacion, ahora necesito...
ACCION: Siguiente paso...
...y asi hasta resolverlo
```

**Ejemplo 1: Investigando que celular comprar**

```
Actua como un experto en tecnologia. Necesito decidir que celular comprar
con mis ahorros de $300 dolares. Usa el metodo ReAct:

PENSAMIENTO: Primero necesito saber para que usa el celular el usuario y
que es lo que mas valora.
ACCION: Voy a analizar sus necesidades: redes sociales, fotos, gaming,
bateria, almacenamiento.
OBSERVACION: El usuario valora: [analiza cada necesidad]
PENSAMIENTO: Con ese presupuesto, hay unas 4-5 opciones relevantes.
ACCION: Voy a comparar las 3 mejores opciones en ese rango de precio.
OBSERVACION: [Compara specs, reviews, pros y contras de cada opcion]
PENSAMIENTO: El factor decisivo parece ser camara vs bateria.
ACCION: Voy a priorizar segun lo que mas valora el usuario.
OBSERVACION: [Recomendacion final con justificacion]

Datos sobre mi: Uso el celular para TikTok, Instagram, fotos con amigos,
y jugar Brawl Stars. La bateria me importa mucho. No me importa la marca.
```

**Ejemplo 2: Planear una base en Minecraft**

```
Actua como un arquitecto experto de Minecraft. Quiero construir una base
epica en mi mundo survival. Usa ReAct para planearla:

PENSAMIENTO: Necesito saber que recursos tiene disponibles y que estilo
de base quiere.
ACCION: Voy a hacer un inventario mental de lo que necesita una base
survival funcional (almacenamiento, granja, proteccion, estetica).
OBSERVACION: [Lista de necesidades basicas de una base]
PENSAMIENTO: Ahora necesito priorizar: primero funcionalidad, luego estetica.
ACCION: Voy a planear el orden de construccion.
OBSERVACION: [Plan paso a paso: dia 1, dia 2, dia 3...]
PENSAMIENTO: Que bloques conseguira mas facil en early game?
ACCION: Recomendar materiales accesibles, no solo los mas bonitos.

Mi situacion: Estoy en early game (tengo hierro, poca piedra, madera abundante,
nada de diamante). Juego en survival normal. Mi base esta junto a un rio en
un bioma de planicie.
```

---

## Tecnica 5: Tree-of-Thought (Arbol de Pensamiento)

**En una frase:** En lugar de pensar en un solo camino, exploras VARIOS caminos al mismo tiempo, evaluas cada uno, y eliges el mejor.

**Diferencia con Chain-of-Thought:**

| Chain-of-Thought | Tree-of-Thought |
|---|---|
| Una sola linea de pensamiento | Varias lineas exploradas en paralelo |
| "Piensa paso a paso" | "Piensa en 3 opciones, evalua cada una, elige la mejor" |
| Como un rio | Como las ramas de un arbol |

**Analogia:** Como si enviaras 3 exploradores por 3 caminos diferentes en un bosque. Al final, comparas lo que encontro cada uno y eliges el mejor camino.

**Ejemplo 1: Decidiendo a que prepa / universidad ir**

```
Mis amigos y yo estamos decidiendo entre 3 opciones de preparatoria.
Ayudame a evaluarlas:

OPCION A: Prepa cerca de casa, publica, plan de estudios regular,
puedo ir caminando.
OPCION B: Prepa un poco lejos (30 min en camion), privada con beca
del 50%, tiene equipo de futbol competitivo.
OPCION C: Prepa tecnica, lejos (1 hora), publica, enseña programacion
y robotica, horario pesado.

Para CADA opcion evalua:
1. Que tan buena es la educacion? (del 1 al 5)
2. Que tanto tiempo y dinero gasto en transporte? ($ por semana)
3. Puedo seguir jugando futbol? (si/no/parcial)
4. Que tan pesado es el horario? (horas libres al dia)
5. Mis amigos van ahi? (si/no/algunos)

COMPARA las 3 opciones en una mini-tabla y RECOMIENDA cual es mejor para
alguien que valora: buena educacion, tiempo libre para deportes, y estar
cerca de amigos.
```

**Ejemplo 2: Eligiendo videojuego para jugar con amigos**

```
Somos 4 amigos buscando un juego nuevo para jugar juntos online.
Estamos entre 3 opciones:

OPCION A: Minecraft (ya lo tenemos 2 de 4, los otros 2 tendrian que comprarlo)
OPCION B: Fortnite (gratis, pero 2 amigos dicen que esta "muerto")
OPCION C: Roblox (gratis, pero hay tantos juegos dentro que no sabemos cual elegir)

Para CADA opcion evalua:
1. Costo total para los 4 (si alguien ya lo tiene, no cuenta)
2. Cuantas horas de diversion antes de que aburra?
3. Nos podemos comunicar bien mientras jugamos?
4. Que tan facil es aprender a jugar?
5. Hay contenido nuevo seguido o ya esta abandonado?

COMPARA las 3 opciones en una tabla y RECOMIENDA cual empezar esta semana.
```

---

## Tecnica 6 (Bonus): Prompting con Imagenes

**En una frase:** Subir una foto o imagen a la IA y hacerle preguntas sobre lo que ve.

**Como funciona:** Arrastras una imagen al chat de ChatGPT (o Copilot, o Gemini), escribes tu pregunta, y la IA te responde combinando lo que "ve" con lo que "sabe".

**Ejemplos de tu mundo:**

```
[Subes una foto de tu tarea de matematicas]

Prompt: "Esta es una foto de mi tarea de matematicas. No entiendo el problema
numero 3. Explicamelo como si tuviera 10 anos, paso a paso, sin darme solo la
respuesta. Quiero entender COMO se resuelve."
```

```
[Subes una foto de tu perro/gato]

Prompt: "Mira la foto de mi mascota. Que raza crees que es? Tiene algo en su
apariencia que indique si esta sano o si necesita algo? No es diagnostico
veterinario, solo curiosidad."
```

```
[Subes el dibujo de un personaje que creaste]

Prompt: "Este es un personaje que dibuje para un comic que quiero hacer.
Analiza el diseño y dime: 1) Que te transmite el personaje con solo verlo?
2) Sugiereme un nombre que combine con su apariencia. 3) Que tipo de historia
crees que tendria este personaje? 4) Alguna idea para mejorar el diseño?"
```

```
[Subes una foto de tu setup gamer / espacio de estudio]

Prompt: "Esta es una foto de mi escritorio donde juego y estudio. Analiza el
espacio y dime 3 cosas que podria cambiar para que sea mas comodo para jugar
y hacer tarea. No tengo mucho presupuesto, cosas que pueda mejorar con lo que
ya tengo."
```

---

## Tabla final: Que tecnica usar y cuando

| Situacion | Tecnica | Por que |
|---|---|---|
| Quiero algo rapido y simple | **Zero-Shot** | Sin rodeos, directo |
| Quiero un formato o estilo especifico | **Few-Shot** | Los ejemplos guian a la IA |
| Necesito analizar algo a fondo | **Chain-of-Thought** | La IA razona antes de responder |
| Estoy resolviendo un misterio o problema | **ReAct** | La IA investiga paso a paso |
| Tengo varias opciones y debo elegir | **Tree-of-Thought** | Comparo todas las opciones |
| Quiero preguntar sobre una foto o dibujo | **Prompting con Imagenes** | La IA "ve" y analiza |

---

## Desafio final

Toma esta situacion y aplica CADA tecnica. El tema: **organizar un torneo de videojuegos con mis amigos.**

Escribe 5 prompts diferentes (uno por tecnica) para planear tu torneo.

[→ Ir al Laboratorio Junior](./07-LABORATORIO-JUNIOR.md)
