# Laboratorio Junior
### 10 ejercicios practicos para convertirte en PRO del prompting

---

## Instrucciones

Cada ejercicio tiene:
- Una situacion de tu mundo (videojuegos, redes sociales, escuela, amigos)
- Un "prompt cliente" (el prompt MALO que escribio alguien)
- Tu mision: reescribirlo usando lo que aprendiste
- Una guia de que tecnica usar

**Reglas:**
1. Abre ChatGPT, Copilot o Gemini
2. PRIMERO prueba el prompt malo. Mira la respuesta mala.
3. DESPUES escribe tu version mejorada. Compara los resultados.
4. Si no te gusta tu primer intento, ITERA. Mejoralo.

---

## Ejercicio 1: Tu Primer Prompt Mejorado

**Tema:** Ayuda con tarea escolar  
**Nivel:** Principiante  
**Tecnica:** Anatomia basica (Rol + Contexto + Instruccion)

**Prompt MALO:**
```
Ayudame con mi tarea de ciencias
```

**Tu mision:** Reescribelo pensando en:
- Que edad tienes?
- Cual es EXACTAMENTE el tema?
- Que tipo de ayuda necesitas (explicacion, resumen, ejemplos)?
- Como quieres la respuesta (lista, parrafos, tabla)?
- Cuanto tiempo tienes?

**Pista de como empezar:**
```
ROL: Eres...
CONTEXTO: Tengo X anos...
INSTRUCCION: Necesito que...
```

---

## Ejercicio 2: De Vago a Especifico

**Tema:** Planes con amigos  
**Nivel:** Principiante  
**Tecnica:** Los 5 niveles de especificidad

**Prompt MALO:**
```
Que hago con mis amigos
```

**Tu mision:** Escribe el mismo prompt pero en nivel 3 (dirigido), nivel 4 (detallado) y nivel 5 (quirurgico). Piensa en:
- Cuantos amigos son?
- Edad?
- Presupuesto?
- Donde viven?
- Que les gusta hacer?
- Cuanto tiempo tienen?

**Ejemplo de como empezar nivel 5:**
```
ROL: Eres un organizador de planes para adolescentes.
CONTEXTO: Tengo X anos, somos X amigos, vivimos en...
```

---

## Ejercicio 3: El Poder del Rol

**Tema:** Un mismo tema, 3 roles diferentes  
**Nivel:** Intermedio  
**Tecnica:** Zero-Shot con diferentes personas

**Situacion:** Quieres saber sobre el espacio y los planetas.

Escribe 3 prompts CON EL MISMO TEMA pero con roles diferentes:

**Version 1 - El Cientifico:**
```
ROL: Eres un astronomo de la NASA...
```

**Version 2 - El Aventurero:**
```
ROL: Eres un astronauta que ha viajado a Marte...
```

**Version 3 - El Youtuber:**
```
ROL: Eres un youtuber de ciencia que explica cosas con memes...
```

**Para reflexionar:** Como cambio la respuesta con cada rol? Cual fue mas divertida de leer? Cual fue mas educativa?

---

## Ejercicio 4: Few-Shot con Estilo

**Tema:** Crear descripciones epicas  
**Nivel:** Intermedio  
**Tecnica:** Few-Shot

**Situacion:** Eres moderador de un servidor de Discord de gaming y necesitas crear descripciones epicas para los canales.

**Prompt base:**
```
Convierte estos nombres de canales en descripciones epicas de UNA linea.
Sigue el patron: [Emoji] + [Frase epica] + [Emoji]:

"general" -> "🗿 La taberna donde las leyendas se encuentran 🍺"
"memes" -> "😂 Donde la seriedad viene a morir 💀"
"anuncios" -> "📢 La voz de los dioses del server ⚡"

Ahora convierte:
"bienvenida"
"clips"
"musica"
```

**Tu mision:** Crea 3 ejemplos de Few-Shot para tu propio servidor o grupo de chat.

---

## Ejercicio 5: Chain-of-Thought - Decidiendo Algo Dificil

**Tema:** Una decision personal  
**Nivel:** Intermedio  
**Tecnica:** Chain-of-Thought

**Situacion:** Elige UNA de estas situaciones (o inventa la tuya):

**Opcion A - Elegir equipo deportivo:**
```
Estoy decidiendo entre unirme al equipo de futbol de mi escuela o al
club de futbol del barrio...
```

**Opcion B - Elegir que regalar:**
```
Es el cumpleanos de mi mejor amigo/a. Tengo $20. Estoy entre 3 regalos...
```

**Opcion C - Elegir que estudiar:**
```
En la escuela me gustan DOS materias. No se cual elegir para enfocarme...
```

**Tu mision:** Escribe un prompt Chain-of-Thought con al menos 5 pasos de razonamiento.

---

## Ejercicio 6: ReAct - Modo Detective

**Tema:** Resolver un misterio  
**Nivel:** Intermedio  
**Tecnica:** ReAct

**Situacion:** Tu cuenta de un videojuego fue "hackeada" (o al menos eso crees). Perdiste skins/items. Usa ReAct para diagnosticar que paso.

**Ejemplo de estructura:**
```
PENSAMIENTO: Primero necesito saber que cambio exactamente.
ACCION: Voy a comparar lo que tenia antes vs lo que tengo ahora.
OBSERVACION: [Lista lo que tenias y lo que falta]
PENSAMIENTO: Las cosas que faltan son...
ACCION: Voy a investigar que pudo haber pasado.
...
```

---

## Ejercicio 7: Tree-of-Thought - Eligiendo Entre Varias Opciones

**Tema:** Comparar 3 opciones  
**Nivel:** Intermedio-Avanzado  
**Tecnica:** Tree-of-Thought

**Situacion (elige una):**

**Opcion A:** Elegir entre 3 videojuegos para comprar
**Opcion B:** Elegir entre 3 lugares para vacaciones familiares
**Opcion C:** Elegir entre 3 disfraces para Halloween
**Opcion D:** Elegir entre 3 posters para tu cuarto

**Tu mision:** Escribe un prompt que compare las 3 opciones usando al menos 4 criterios. Incluye una tabla comparativa y recomendacion final.

---

## Ejercicio 8: Prompting con Imagenes

**Tema:** Analizar una imagen  
**Nivel:** Intermedio  
**Tecnica:** Prompting multimodal

**Tu mision:** Toma una foto con tu celular de:

**Opcion A:** Tu espacio de estudio/gaming. Pregunta: "Como puedo organizarlo mejor?"

**Opcion B:** Tu mascota. Pregunta: "Que raza es? Describe su personalidad probable."

**Opcion C:** Un dibujo que hayas hecho. Pregunta: "Como puedo mejorar esta ilustracion?"

**Opcion D:** Tu outfit del dia. Pregunta: "Que accesorios le agregarias?"

---

## Ejercicio 9: Proyecto - Crea Tu Propio Bot o Asistente

**Tema:** Proyecto integrador  
**Nivel:** Avanzado  
**Tecnica:** Combinacion de tecnicas

**Tu mision:** Crea UN prompt maestro para un asistente de IA que se especialice en uno de estos temas:

1. **Asistente de Minecraft:** Sabe todo sobre crafteos, builds, y estrategias
2. **Coach de Futbol:** Analiza tu tecnica y te da ejercicios
3. **Critico de Anime/Series:** Te recomienda que ver segun tus gustos
4. **Tutor de [tu materia mas dificil]:** Te explica temas complicados de forma simple
5. **Creador de Personajes:** Te ayuda a diseñar personajes para tus historias/comics
6. **Organizador de Torneos:** Te ayuda a planear torneos de tu juego favorito
7. **DJ Personal:** Te recomienda musica basado en tu estado de animo

**Incluye en tu prompt maestro:**
- Rol super detallado (experto en X con Y anos de experiencia)
- Que tipo de respuestas debe dar (tono, estilo, formato)
- Que NO debe hacer jamas (limites)
- Como debe manejar cuando no sabe algo

---

## Ejercicio 10: Desafio Final - Enseña a Alguien

**Tema:** Demuestra lo que aprendiste  
**Nivel:** Maestro

**Tu mision:** Toma TODO lo que aprendiste y enseñale a un amigo, hermano o familiar como escribir un buen prompt.

**Pasos:**
1. Preguntale a tu "alumno" que tema le interesa
2. Escribe un prompt malo juntos sobre ese tema (intencionalmente malo)
3. Muestrale el resultado malo
4. Enseñale a mejorarlo usando Rol + Contexto + Instruccion
5. Ejecuten el prompt mejorado
6. Comparen resultados

**Bonus:** Si tu alumno tiene menos de 12 anos, ganas +100 puntos de maestro.

---

## Tabla de puntuacion (para competir con amigos)

| Ejercicio | Puntos base | Bonus si lo haces con creatividad |
|---|---|---|
| 1. Primer Prompt Mejorado | 10 | +5 si el resultado es util de verdad |
| 2. De Vago a Especifico | 15 | +5 si llegaste a nivel 5 |
| 3. El Poder del Rol | 15 | +5 si hiciste los 3 roles |
| 4. Few-Shot con Estilo | 15 | +5 si los ejemplos son originales |
| 5. Chain-of-Thought | 20 | +5 si usaste un tema personal real |
| 6. ReAct | 20 | +5 si encontraste "algo" interesante |
| 7. Tree-of-Thought | 20 | +5 si la tabla comparativa esta completa |
| 8. Prompting con Imagenes | 10 | +5 si la IA detecto algo sorprendente |
| 9. Proyecto Integrador | 30 | +10 si tu asistente funciona de verdad |
| 10. Enseña a Alguien | 25 | +10 si tu alumno aprendio algo |

**Puntaje maximo: 250 puntos**

- 0-80: Aprendiz de prompt
- 81-150: Ingeniero de prompts nivel medio
- 151-220: PRO del prompting
- 221-250: Maestro Jedi del prompt

---

## Comparte tus resultados

Si quieres compartir tus mejores prompts o ver lo que crearon otros, el repositorio completo tiene una comunidad donde puedes contribuir.

[← Volver al README Junior](./README.md)
