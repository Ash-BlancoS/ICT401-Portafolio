# ICT401 · Semana 9 — Laboratorio integrador I-B

**Reconstrucción 3D a partir de un plano o conjunto de vistas — 10 %**

- Estudiante: Ashley Blanco Solis
- Grupo: 60
- Fecha: 17/09/2026
- Nombre del archivo de Fusion: `ICT401_S09_LabIB_Blanco_Ashley`
- Carpeta/proyecto de Fusion Cloud con acceso docente: [Respuesta]
- Commit de entrega: [Respuesta]

## Instrucciones de uso de esta ficha

Complete esta ficha durante el laboratorio. No borre respuestas iniciales aunque luego las corrija. Cuando cambie una decisión, explique qué evidencia del plano o del modelo motivó la modificación.

La ficha debe quedar en `Laboratorio_I/I-B` con el nombre `S09_Lab_IB_Evidencias_Blanco_Ashley.md`. Las imágenes enlazadas deben estar en la misma carpeta. El archivo nativo permanece en Fusion Cloud con acceso docente.

Esta ficha forma parte de la evidencia evaluable del Laboratorio integrador I-B y está estructurada para facilitar una revisión posterior por la persona docente o mediante ChatGPT. La calificación final corresponde siempre al instrumento oficial del curso.

---

## A. Interpretación inicial del plano

### A1 · Dimensiones generales

- X total: 90
- Y total: 60
- Z total: 42

### A2 · Características geométricas identificadas

| Nº | Característica | Descripción | Vista(s) que la definen | Dimensiones asociadas |
|---|---|---|---|---|
| 1 | [Respuesta] | [Respuesta] | [Respuesta] | [Respuesta] |
| 2 | [Respuesta] | [Respuesta] | [Respuesta] | [Respuesta] |
| 3 | [Respuesta] | [Respuesta] | [Respuesta] | [Respuesta] |
| 4 | [Respuesta] | [Respuesta] | [Respuesta] | [Respuesta] |
| 5 | [Respuesta] | [Respuesta] | [Respuesta] | [Respuesta] |

### A3 · Describa la pieza en una frase técnica antes de abrir Fusion

Modelo con contorno escalonado con un agujero y una ranura

### A4 · ¿Qué plano de boceto utilizará primero y por qué?

Top, es mas facil empezar el boceto desde ese plano. y leer el ancho total y la profundidad

### A5 · Estrategia inicial de modelado

1. Rectángulo de 90x60mm y Extruir 12mm
2. Rectángulo de 60x35mm y Extruir 16mm
3. Rectángulo de 25x35mm y Extruir 14mm
4. Hole de 14mm en el centro del segundo regtangulo
5. Ranura de 14x12mm en el rectángulo base
6. Revisar y corregir

---

## B. Desarrollo del modelo

### B1 · Boceto base

- Plano seleccionado: Top.
- Geometría principal: Regtangulo.
- Restricciones aplicadas: Horizontal/Vertical y Igual.
- Dimensiones aplicadas: 90,60,25 mm de ancho. Altura de 42,28,12 mm.
- Estado del boceto: Completamente restringido.

### B2 · Operaciones principales realizadas

| Orden | Operación | Propósito geométrico | Parámetro/dimensión principal | Resultado |
|---|---|---|---|---|
| 1 | Sketch| Definir el perfil principal de la pieza | X = 90 mm/alturas del plano |  | base
| 2 | Extrude | Generar el cuerpo principal | Y = 60 mm | Cuerpo base|
| 3 | Sketch + Extrude |Crear la segunda plataforma | X = 0–60 mm; Y = 25–60 mm | Plataforma elevada |
| 4 | Sketch + Extrude | Crear la torre |X = 0–25 mm; Y = 25–60 mm  |Torre elevada |
| 5 | Hole |Crear el agujero pasante  | Ø14 mm | Agujero  |
| 6 | Sketch + Extrude | Crear la ranura pasante | 14 × 12 mm; X = 68–82 mm; Y = 10–22 mm | Ranura rectangular |

### B3 · Cambios respecto a la estrategia inicial

| Cambio realizado | Motivo | Vista/dimensión que reveló el problema | Sketch/operación corregida |
|---|---|---|---|
|No se realizó ningún cambio  | La estrategia fue correcta  | comparación entre Front, Top y Right |No fue necesario corregir |
| No se realizó ningún cambio | La estrategia fue correcta | comparación entre Front, Top y Right | No fue necesario corregir  |
| No se realizó ningún cambio | La estrategia fue correcta  |comparación entre Front, Top y Right | No fue necesario corregir  |

---

## C. Verificación contra el plano

### C1 · Correspondencia de vistas

| Vista | ¿Coincide? | Evidencia geométrica | Diferencia detectada | Corrección realizada |
|---|---|---|---|---|
| Front | Sí | Se observa el perfil escalonado con alturas de 12, 28 y 42 mm y un ancho total de 90 mm. | No se detectaron diferencias. | No fue necesaria. |
| Top | Sí | Coinciden las dimensiones generales de 90 × 60 mm, la posición de la plataforma y torre, el agujero Ø14 y la ranura de 14 × 12 mm. | No se detectaron diferencias. | No fue necesaria. |
| Right | Sí | Coinciden la profundidad total de 60 mm y los diferentes niveles de altura de la pieza. | No se detectaron diferencias. | No fue necesaria. |

### C2 · Comprobación dimensional

| Nº | Dimensión crítica | Valor del plano | Valor medido en Fusion | Elemento seleccionado | ¿Coincide? |
|---|---|---|---|---|---|
| 1 | Ancho total X | 90 mm | 90 mm | Base | Sí |
| 2 | Profundidad total Y | 60 mm | 60 mm | Base | Sí |
| 3 | Altura total Z | 42 mm | 42 mm | Torre | Sí |
| 4 | Diámetro del agujero | Ø14 mm | Ø14 mm | Agujero circular | Sí |
| 5 | Dimensiones de la ranura | 14 × 12 mm | 14 × 12 mm | Ranura rectangular | Sí |

### C3 · Editabilidad paramétrica

Si una dimensión principal de la pieza cambiara, indique qué Sketch, dimensión u operación tendría que editar y por qué.

Para cambiar el tamaño general de la pieza se editaría el Sketch de la base y sus dimensiones de 90 mm y 60 mm. Para modificar la altura de la plataforma se editaría la extrusión de 16 mm, mientras que para modificar la altura de la torre se editaría la extrusión de 14 mm. El diámetro y la posición del agujero se modificarían desde su Sketch, y las dimensiones o posición de la ranura desde el Sketch utilizado para crearla.

---

## D. Evidencias

### D1 · Modelo final

Modelo completo en orientación pictórica, con nombre del diseño y ViewCube visibles.

![Lab I-B: Modelo final](S09_LabIB_Modelo_Blanco_Ashley.png)

### D2 · Vistas de verificación

Montaje de Front, Top y Right del modelo, presentado de manera clara para comparar con el plano base.

![Lab I-B: Vistas](S09_LabIB_Vistas_Blanco_Ashley.png)

### D3 · Boceto y restricciones

Captura del boceto más representativo con restricciones y dimensiones visibles.

![Lab I-B: Boceto](S09_LabIB_Boceto_Blanco_Ashley(2).png)

### D4 · Timeline / historial paramétrico

Captura donde se observen las operaciones principales del historial del modelo.

![Lab I-B: Timeline](S09_LabIB_Timeline_Blanco_Ashley.png)

### D5 · Verificación dimensional

Captura de `Inspect > Measure` con una dimensión crítica y el elemento seleccionado visibles.

![Lab I-B: Medicion](S09_LabIB_Medicion_Blanco_Ashley.png)

---

## E. Checklist de entrega

- [x ] Analicé el plano antes de comenzar el modelado.
- [x ] Registré X, Y y Z totales.
- [x ] Identifiqué las características principales y las vistas que las definen.
- [x ] Registré una estrategia inicial antes de modelar.
- [x ] El modelo final corresponde a Front, Top y Right.
- [ x] Verifiqué al menos cinco dimensiones críticas.
- [ x] Los bocetos principales tienen restricciones y dimensiones coherentes.
- [x ] El historial de operaciones es legible y editable.
- [x ] El nombre del archivo cumple la nomenclatura solicitada.
- [x ] El archivo editable está disponible en Fusion Cloud con acceso docente.
- [x ] Las cinco evidencias se visualizan correctamente en GitHub.
- [x ] Esta ficha está completa.

---

# F. Rubrica oficial del Laboratorio integrador I-B

La tabla siguiente registra la evaluacion aplicada exclusivamente a esta ficha y sus evidencias enlazadas o insertadas. Los valores coinciden con el Excel y el PDF individual.

| Criterio oficial | Valor maximo | Puntaje obtenido | Observaciones de evaluacion |
|---|---:|---:|---|
| Interpretacion correcta del plano o conjunto de vistas | 2.00 | 1.50 | Cumple mayoritariamente; quedan faltantes o verificaciones menores. |
| Reconstruccion tridimensional coherente | 2.50 | 1.88 | Cumple mayoritariamente; quedan faltantes o verificaciones menores. |
| Aplicacion de restricciones y dimensiones | 1.50 | 1.13 | Cumple mayoritariamente; quedan faltantes o verificaciones menores. |
| Precision geometrica y correspondencia con el plano | 2.00 | 1.50 | Cumple mayoritariamente; quedan faltantes o verificaciones menores. |
| Organizacion, nomenclatura y archivo editable | 1.00 | 0.00 | Sin evidencia verificable para este criterio. |
| Presentacion y cumplimiento del enunciado | 1.00 | 0.75 | Cumple mayoritariamente; quedan faltantes o verificaciones menores. |

**Total obtenido: 6.76 / 10,00 %**

La ruta `Laboratorio_I/I-B/` se acepta como ruta oficial alternativa junto con `Portafolio/semana09/`. No se inspeccionaron archivos de Fusion.

## G. Resumen para evaluación asistida por ChatGPT

Este bloque debe permitir una revisión rápida sin tener que inferir información faltante.

- ¿El estudiante interpretó correctamente X, Y y Z? [Respuesta]
- ¿Las características listadas corresponden con el plano? [Respuesta]
- ¿La estrategia inicial es coherente? [Respuesta]
- ¿El modelo final coincide con las tres vistas? [Respuesta]
- ¿Las dimensiones críticas coinciden? [Respuesta]
- ¿Los bocetos muestran restricciones y dimensiones adecuadas? [Respuesta]
- ¿El timeline muestra una reconstrucción paramétrica razonable? [Respuesta]
- ¿El archivo y las evidencias cumplen nomenclatura y presentación? [Respuesta]
- Incidencias que el evaluador debería revisar directamente en Fusion: [Respuesta]

## H. Retroalimentacion del evaluador

### Fortalezas

Las dimensiones y las cinco evidencias estan disponibles.

### Aspectos por corregir

Completar A2, acceso/commit declarados y ruta/nomenclatura oficial.

### Desglose del puntaje

| Criterio | Puntaje obtenido |
|---|---:|
| R1 - Interpretacion correcta del plano o conjunto de vistas | 1.50 |
| R2 - Reconstruccion tridimensional coherente | 1.88 |
| R3 - Aplicacion de restricciones y dimensiones | 1.13 |
| R4 - Precision geometrica y correspondencia con el plano | 1.50 |
| R5 - Organizacion, nomenclatura y archivo editable | 0.00 |
| R6 - Presentacion y cumplimiento del enunciado | 0.75 |

R5 se califica con 0,00 porque la ficha no respeta una ruta y nomenclatura oficial, o no presenta evidencia verificable. La revisión se basó exclusivamente en esta ficha y sus evidencias enlazadas o insertadas.
 No se inspeccionaron archivos de Fusion.

### Calificacion final

**6.76 / 10,0 %**