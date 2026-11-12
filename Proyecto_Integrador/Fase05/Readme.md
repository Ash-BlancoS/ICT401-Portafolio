# Organizador de Cables – Encaje Rápido

**Proyecto integrador · ICT401 Dibujo Técnico Asistido por Computadora**

Universidad Nacional (UNA), Sede Chorotega, Liberia 

Docente: Óscar Caravaca Mora

Equipo 3WX: Ashley Y. Blanco Solís · Jassy Díaz Duarte · Libny Y. Urbina Salinas

Categoría: Soporte

Cierre del proyecto (Fase 5): 12 de noviembre de 2026

**Presentación:**

(https://github.com/Yahel-ctrl/ICT401-Portafolio/blob/main/Proyecto_Integrador/Presentaci%C3%B3n/PROY_F05_Organizador%20de%20Cables.pdf)

---

## Contenido

1. [Explicación del proyecto](#1-explicación-del-proyecto)
2. [Proceso](#2-proceso)
3. [Modelo 3D](#3-modelo-3d)
4. [Documentación técnica](#4-documentación-técnica)
5. [Archivos técnicos](#5-archivos-técnicos)
6. [Resultados obtenidos](#6-resultados-obtenidos)
7. [Limitaciones y mejoras](#7-limitaciones-y-mejoras)
8. [Fases del proyecto](#8-fases-del-proyecto)

---

## 1. Explicación del proyecto

### Nombre del proyecto
**Organizador de Cables – Encaje Rápido**: soporte para agrupar y proteger cables de escritorio.

### Problema o necesidad que resuelve
Los cables sueltos se enredan, generan desorden y representan un riesgo de tropiezos. Afecta a estudiantes, teletrabajadores y profesionales que usan varios dispositivos.

### Objetivo del diseño
Diseñar un organizador de dos piezas, una base con clip (P01, Gancho) y una tapa (P02), que encaje a presión y deslice sin interferencias. Debe permitir pasar y agrupar cables, y quedar completamente documentado con planos normalizados y un modelo paramétrico en Fusion.

### Requisitos verificables

| Código | Requisito |
|---|---|
| R01 | Fijación con tornillos |
| R02 | Canal para cables de 4 a 8 mm |
| R03 | Tapa que encaja y desencaja sin interferencias |
| R04 | Sin bordes filosos |
| R05 | Ancho del canal modificable sin reconstruir el modelo |

Se evaluaron dos alternativas. La **Alternativa A** se seleccionó por su cumplimiento funcional y su compacidad, y la B quedó de respaldo. El criterio fue el equilibrio entre función, facilidad de modelado, ensamblaje y documentación normalizada.

---

## 2. Proceso

### Bocetos o ideas iniciales
El proceso fue **croquis a mano → boceto paramétrico acotado → sólido final en Fusion**.

- **Fase 1 (Definición):** croquis a mano de la base, la tapa y el cilindro, con medidas iniciales (tapa de 152 mm de alto, clip de 24 mm de ancho).
- **Fase 2 (Modelado):** bocetos paramétricos en Fusion de P01 (Base/Gancho A) y P02 (Tapa), con parámetros con nombre ligados a cada requisito.

**Se utilizó el croquis a mano de la fase 01 para los parámetros en Fusion de la fase 02**

### Cambios realizados durante el desarrollo

| Elemento | Inicio | Final |
|---|---|---|
| Alto de P01 (Gancho) | 138 mm | aprox. 200 mm (199.57 mm en plano) |
| Ancho de P01 | 200 mm | 220 mm |
| Alto de P02 (Tapa) | 152 mm | 203.4 mm |
| Ancho de P02 | 210 mm | 233 mm (220 + 2 × 6.5 mm de pared) |


### Dificultades encontradas y cómo se resolvieron

| # | Dificultad | Solución |
|---|---|---|
| 1 | El clip de P01 no sostenía a P02 porque la altura y el ancho estaban mal dimensionados. | Se corrigieron las dimensiones en la versión **Gancho A..02**. |
| 2 | Aristas y uniones con bordes agudos (R04). | Se ajustaron chaflanes y empalmes para cumplir R04, sin bordes filosos. |
| 3 | Interferencia en el encaje a presión: **14.88 mm³** con la tapa cerrada, en las puntas de las orejas del clip, y **955.76 mm³** a 30 mm de apertura, asociado al paso del clip por el agarre. | Se reportó con su estado final y se previó un ajuste de empalme o chaflán. |
| 4 | Comprobar R05 (ancho del canal modificable). | Prueba paramétrica: el ancho del canal pasó de 30 a 25 mm sin rehacer el boceto. |

---

## 3. Modelo 3D

### Capturas del modelo final
![Modelo final](ICT401_F04_Ensamblaje_Drawing.pdf)
![Vista explosionada](Vista_explosionada.jpeg)

### Componentes o piezas principales

| Pieza | Nombre | Descripción | Material | Dimensiones principales (según plano) |
|---|---|---|---|---|
| P01 | Gancho / Base con clip | Base con el clip que sostiene a P02. Tiene agujeros de Ø4.7 y Ø10.7 mm para la fijación. | Plastic PLA | 200 × 199.57 × 41 mm |
| P02 | Tapa | Caja abierta con ranuras laterales de 30 mm para el paso de cables. | Plastic PLA | 233 × 203.4 × 140 mm |

### Ensamblaje
- Archivo de ensamblaje: `ICT401_F03_Ensamblaje`, con la tapa P02 como pieza fija (Ground).
- Unión deslizante **Deslizante_Tapa** de 1 grado de libertad entre P01 y P02, con recorrido de **0 a 200 mm**.

**Validación frente a los requisitos**

| Requisito | Resultado |
|---|---|
| R01 | Agujero de 4.70 mm |
| R02 | Canal de 30.00 mm, mayor que 8 mm |
| R03 | La tapa encaja y se desliza; interferencias reportadas con su estado final |
| R04 | Bordes redondeados |
| R05 | Cumple (canal de 30 a 25 mm sin rehacer el boceto) |

---

## 4. Documentación técnica

### Planos finales en PDF

| Plano | Archivo | Escala | 
|---|---|---|
| Ensamblaje (DWG ICT401-F04-01, Rev. A) | `ICT401_F04_Ensamblaje_D_Final.pdf` https://github.com/Yahel-ctrl/ICT401-Portafolio/blob/main/Proyecto_Integrador/Planos/ICT401_F04_Ensamblaje%20D_Final.pdf| 1:3 |Libny Urbina S. |
| Gancho / P01 | `ICT401_F04_Gancho_P01_Dibujo.pdf`https://github.com/Yahel-ctrl/ICT401-Portafolio/blob/main/Proyecto_Integrador/Planos/ICT401_F04_Gancho_P01%20Dibujo.pdf| 1:2 |Ashley Blanco |
| Tapa / P02 | `ICT401_F04_Tapa_P02_Dibujo.pdf`https://github.com/Yahel-ctrl/ICT401-Portafolio/blob/main/Proyecto_Integrador/Planos/ICT401_F04_Tapa_P02%20Dibujo.pdf| 1:2.5 |Jassy Díaz Duarte |

### Vistas, cotas y escala
- Hoja A3 con cajetín ISO completo, unidades en mm y tolerancia general **ISO 2768-m**.
- Vistas ortogonales, vista isométrica y **corte A-A (1:3)** en el ensamblaje.
- Método de proyección: **primer diedro** (europeo, ISO).
- Cotas con tolerancia en el ensamblaje: **42 ±0.2** y **44.66 ±0.2 mm**.
- P01 acotado con ancho total de 200, agujeros Ø4.7 y Ø10.7, y canal central de 26.
- P02 acotado con 233, 203.4, 140, canal de 30 y posición del orificio central.

### Vista explosionada y lista de piezas
El plano de ensamblaje incluye la vista explosionada con globos 1 y 2, y la lista de piezas:

| Ítem | Cant. | Pieza | Part Number | Material |
|---|---|---|---|---|
| 1 | 1 | Tapa (P02) | 2026-10-06-17-45-56-483 | Plastic PLA |
| 2 | 1 | Gancho (P01) | 2026-11-03-19-08-29-650 | Plastic PLA |

---

## 5. Archivos técnicos

### Archivos CAD editables
- Piezas nativas de Fusion: P01 Base/Gancho A y P02 Tapa.
- Ensamblaje: `ICT401_F03_Ensamblaje`, con el respaldo `ICT401_F04_Ensamblaje D_Final(Respaldo)`.

### Formatos de exportación

| Formato | Para qué sirve |
|---|---|
| **PDF** | Entrega y revisión de los planos. Se ve igual en cualquier equipo y conserva escala, cotas y cajetín. |
| **DXF** | Dibujo 2D vectorial editable. Se abre en otros programas CAD y sirve para corte láser o CNC. |
| **STEP** | Modelo 3D neutro para intercambiar la geometría entre programas CAD distintos. |

---

## 6. Resultados obtenidos

### Qué se logró con el proyecto
- Un organizador de cables **funcional y documentado**, con dos piezas que se ensamblan y se deslizan con una unión de 1 grado de libertad.
- Un modelo **paramétrico** con parámetros ligados a los requisitos, comprobado con el cambio del canal de 30 a 25 mm.
- Documentación técnica normalizada: planos de ensamblaje y de cada pieza, con cajetín, lista de piezas, corte A-A, cotas con tolerancia y tolerancia general ISO 2768-m.
- Archivos finales identificados y entregados en los formatos técnicos del proyecto.

### Evidencias de calidad o funcionamiento
- Cumplimiento verificado de R01, R02, R04 y R05, y encaje y deslizamiento de la tapa (R03).
- Cotas críticas con tolerancia (42 ±0.2 y 44.66 ±0.2 mm).
- Análisis de interferencia medido y reportado (14.88 mm³ cerrada, 955.76 mm³ a 30 mm de apertura).
- Video de demostración del ensamblaje y bitácoras de cada fase.

---

## 7. Limitaciones y mejoras

### Qué problemas quedaron pendientes
- El diseño **no se ha validado en físico**: falta imprimirlo en PLA y comprobar el encaje, la holgura y la resistencia del clip.
- Quedan interferencias en el encaje a presión (14.88 mm³ con la tapa cerrada y 955.76 mm³ a 30 mm de apertura) que dependen de un ajuste final de empalme o chaflán.

### Qué mejoraríamos en una siguiente versión
- Imprimir un prototipo en PLA, probar el encaje y ajustar holguras y tolerancias según el resultado.
- Eliminar las interferencias con chaflanes o empalmes en las orejas del clip.
- Parametrizar todas las dimensiones principales, para adaptar el organizador a distintos grosores y cantidades de cables.
- Completar el plano de ensamblaje con cotas generales y el símbolo del método de proyección.
---

## 8. Fases del proyecto

| Fase | Entregable | Peso |
|---|---|---|
| 1 | Definición: necesidad, requisitos, alternativas y croquis | 5 % |
| 2 | Modelado: bocetos paramétricos y piezas P01 y P02 en Fusion | 7 % |
| 3 | Integración y validación: ensamblaje con unión deslizante e interferencias | 6 % |
| 4 | Documentación y archivos finales: planos, tolerancias y exportaciones | 7 % |
| 5 | Comunicación: presentación y defensa técnica | 5 % |

---

*ICT401 · UNA Sede Chorotega, Liberia · 2026*
