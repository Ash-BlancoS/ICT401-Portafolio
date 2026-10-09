# Informe Fase 2: Boceto paramétrico y modelado 3D

ICT401 – Dibujo Técnico Asistido por Computadora · Proyecto integrador (7 %, Semana 12)

**Título del proyecto:** Organizador de Cables – Encaje Rápido

**Categoría:** Soporte

**Equipo:** 3WX – Ashley Y. Blanco Solís, Jassy Diaz Duarte, Libny Y. Urbina Salinas

**Docente:** Óscar Caravaca Mora

**Fecha:** 08/10/2026

**Archivo principal en Fusion Cloud:**

- ICT401_F02_Tapa/P02:
https://myuna182.autodesk360.com/g/projects/202607211116718881/data/dXJuOmFkc2sud2lwcHJvZDpmcy5mb2xkZXI6Y28ueFVMUzFOSkFUeW01Tmw0ZXU5cFQ4QQ/dXJuOmFkc2sud2lwcHJvZDpkbS5saW5lYWdlOlJENERqZVRqUndlM1NyS0J1S29ERXc/overview

- ICT401_F02_Gancho/P01:
https://myuna182.autodesk360.com/g/projects/202607211116718881/data/dXJuOmFkc2sud2lwcHJvZDpmcy5mb2xkZXI6Y28ueFVMUzFOSkFUeW01Tmw0ZXU5cFQ4QQ/dXJuOmFkc2sud2lwcHJvZDpkbS5saW5lYWdlOkdSNHc3QWR5UmdtRkROZHplN2UxVlE/overview

## 1. Resumen del avance

En esta fase se modelaron en Fusion la base P01 (Gancho A..02), la tapa P02 y su ensamblaje. Respecto a la Fase 1, se corrigieron la altura y el ancho de P01 para que el clip sostuviera a P02, y se agregaron empalmes y chaflanes para cumplir R04. Las medidas se organizaron en parámetros y fórmulas. Para la Fase 3 queda aplicar más restricciones, comprobar la interferencia del ensamblaje y acordar su validación con el docente.

## 2. Cambios respecto a la Fase 1

El modelo original se corrigió en tres aspectos: la altura total y el ancho de P01, porque el clip que sostiene a P02 no encajaba correctamente, y se realizaron empalmes y chaflanes para mejorar la estética de la pieza y cumplir R04.

| Elemento | Antes (Gancho A) | Ahora (Gancho A..02) | Motivo |
|---|---|---|---|
| Distancia entre las dos aristas medidas (Figuras 2 y 3) | 26.542 mm | 27.042 mm | Ajuste de +0.5 mm para que el clip sostenga a P02 |
| Altura total de P01 | 138 mm | 200.416 mm | El clip que sostiene a P02 no encajaba |
| Ancho de P01 | 200 mm | 220 mm | Mismo problema de encaje del clip |

![Figura 1](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura01_modelo_inicial.jpeg)

*Figura 1. Modelo inicial de la base, con los cinco bocetos de la exploración.*

![Figura 2](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura02_gancho_a_medicion.jpeg)

*Figura 2. Base/P01 Gancho A: medida original de las barras centrales (distancia de 26.542 mm entre aristas de 134.258 mm y 68.00 mm).*

![Figura 3](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura03_gancho_a02_medicion.jpeg)

*Figura 3. Base/P01 Gancho A..02: medidas finales de las barras centrales (distancia de 27.042 mm entre aristas de 142.25 mm y 134.40 mm).*

## 3. Parámetros del modelo

Tabla tomada de Modificar → Cambiar parámetros.

| Parámetro | Valor o fórmula | Unidad | Requisito que lo origina (comentario) |
|---|---|---|---|
| ancho_base | 220 | mm | R03 |
| altura_base | 200.416 | mm | R03 |
| prof_base | 41 | mm | R03 |
| ancho_barra | 20 | mm | R03 |
| alto_barra | 124.4 | mm | R03 |
| prof_barra | 38 | mm | R03 |
| ancho_clip | 26 | mm | R03 |
| alto_clip | 47.561 | mm | R03 |
| prof_clip | prof_barra | mm | R03 |
| ancho_barra_medio | ancho_clip | mm | R03 |
| ancho_orejas | ancho_clip | mm | R03 |
| prof_placa | prof_barra | mm | R03 |
| diametro_tornillo | 4.7 | mm | R01 |
| chaflan_agujero | 3 | mm | R01, R04 |
| prof_agujero | 10 | mm | R01 |
| holgura_ancho_clip | 3.046 | mm | R03 |
| holgura_prof_clip | 4 | mm | R03 |
| ancho_agarre_clip | ancho_clip + holgura_ancho_clip | mm | R03 |
| prof_agarre_clip | prof_clip + holgura_prof_clip | mm | R03 |
| alto_vaciado | prof_agarre_clip | mm | R03 |
| espesor_pared_tapa | 6.5 | mm | R03 |
| ancho_tapa | ancho_base + 2 * espesor_pared_tapa | mm | R03 |
| altura_tapa | 203.4 | mm | R03 |
| prof_tapa | 140 | mm | R03 |
| diametro_cable_min | 4 | mm | R02 |
| diametro_cable_max | 8 | mm | R02 |
| ancho_canal_cables | 30 | mm | R02, R05 |
| prof_canal_cables | 5 | mm | R02 |
| alto_canal_cables | 139.4 | mm | R02 |
| radio_empalme_tapa | 1 | mm | R04 |
| chaflan_tapa | 0.5 | mm | R04 |

**Fórmulas entre parámetros**

- ancho_tapa = ancho_base + 2 * espesor_pared_tapa → 220 + 2 * 6.5 = 233 mm
- ancho_agarre_clip = ancho_clip + holgura_ancho_clip → 26 + 3.046 = 29.046 mm
- prof_agarre_clip = prof_clip + holgura_prof_clip → 38 + 4 = 42 mm
- alto_vaciado = prof_agarre_clip → 42 mm
- prof_clip = prof_barra y prof_placa = prof_barra → 38 mm en las tres piezas
- ancho_barra_medio = ancho_clip y ancho_orejas = ancho_clip → 26 mm en las tres piezas
- Condiciones de R03 (sin interferencias): holgura_ancho_clip > 0 (3.046 mm), holgura_prof_clip > 0 (4 mm) y altura_tapa − altura_base > 0 (203.4 − 200.416 = 2.984 mm)
- Condición de R02: ancho_canal_cables ≥ diametro_cable_max → 30 mm ≥ 8 mm

Al cambiar ancho_clip, prof_barra, ancho_base o espesor_pared_tapa, las medidas dependientes se actualizan solas.

Pendiente para la Fase 3: vincular ancho_canal_cables a la geometría que depende del canal, para comprobar R05 con ese parámetro.

**Dimensiones finales de P01 (Base/P01 Gancho A..02)**

![Figura 4](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura04_base_isometrica.png)

*Figura 4. Base P01 (ICT401_F02/Gancho/P01) en vista isométrica, con el historial de bocetos y operaciones.*

| Elemento | Medida | Valor (mm) |
|---|---|---|
| General | Altura total | 200.416 |
| General | Profundidad total | 41 |
| General | Ancho total | 220 |
| Barras rectangulares | Profundidad | 38 |
| Barras rectangulares | Alto | 124.4 |
| Barras rectangulares | Ancho | 20 |
| Placa superior de las barras | Alto | 10 |
| Placa superior de las barras | Ancho | 70 |
| Placa superior de las barras | Profundidad | 38 |
| Clip de la base | Alto | 47.561 |
| Clip de la base | Profundidad | 38 |
| Clip de la base | Ancho | 26 |
| Orejas del clip | Alto | 15 |
| Orejas del clip | Ancho | 26 |
| Orejas del clip | Profundidad inicial | 9.5 |
| Barra del medio | Profundidad | 6.234 |
| Barra del medio | Ancho | 26 |
| Barra del medio | Altura de abajo hacia arriba antes de la forma de tridente | 20.613 |
| Agujeros de tornillo | Diámetro | 4.7 |
| Agujeros de tornillo | Chaflán | 3 |
| Agujeros de tornillo | Profundidad hacia abajo | 10 |
| Chaflanes | N2 | 5 |
| Chaflanes | N3 | 9 y 1 |
| Chaflanes | N4 | 5 y 2 |
| Chaflanes | N5 | 4 y 2 |
| Chaflanes | N6 | 26 y 0.5 |
| Chaflanes | N7 | 1 |
| Empalmes | N1 | 11.5 |
| Empalmes | N2 | 12 |
| Empalmes | N3 | 2 |
| Empalmes | N4 | 41 |
| Empalmes | N5 | 0.9 |
| Empalmes | N6 | 0.4 |
| Empalmes | N7 | 4 |
| Empalmes | N8 | 0.6 |
| Empalmes | N9 | 2 |

**Dimensiones finales de P02 (Tapa/P02)**

![Figura 5](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura05_tapa_p02.jpeg)

*Figura 5. Tapa/P02 con sus ranuras y el clip inferior, con la línea de tiempo de operaciones.*

| Elemento | Medida | Valor (mm) |
|---|---|---|
| General | Ancho total | 233 |
| General | Profundidad total | 140 |
| General | Altura total | 203.4 |
| Ranura de los cables | Ancho | 30 |
| Ranura de los cables | Profundidad | 5 |
| Ranura de los cables | Alto | 139.4 |
| Ranura del centro | Largo x ancho | 41 x 29 |
| Agarre del clip | Alto | 44 |
| Agarre del clip | Ancho | 29.046 |
| Agarre del clip | Profundidad | 42 |
| Agujeros | Ancho entre agujeros | 29.059 |
| Agujeros | Alto de los agujeros | 14.058 |
| Ranura de agarre | Dimensiones | 34.826 x 22.86 |
| Vaciado | Alto | 42 |
| Chaflanes | Los primeros 4 | 0.5 y 21 |
| Chaflanes | El 5 | 0.5 |
| Empalmes | Los primeros 2 | 4 |
| Empalmes | El 3 | 75 |
| Empalmes | El 4 | 7.5 |
| Empalmes | El 5 | 70.5 |
| Empalmes | El 6 | 2 |
| Empalmes | El 7, 8 y 9 | 1 |

## 4. Modificación paramétrica

**Valor original → valor nuevo:** distancia entre las aristas de las barras centrales de 26.542 mm → 27.042 mm

**Captura antes (con el valor visible):** Figura 6

![Figura 6](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura06_antes_del_cambio.jpeg)

*Figura 6. Antes del cambio: medida original de las barras centrales (distancia de 26.542 mm entre aristas de 134.258 mm y 68.00 mm).*

**Captura después:** Figura 7

![Figura 7](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura07_despues_del_cambio.jpeg)

*Figura 7. Después del cambio: medidas finales de las barras centrales (distancia de 27.042 mm entre aristas de 142.25 mm y 134.40 mm); el Boceto 14 (Boceto N5) se actualizó automáticamente.*

## 5. Verificaciones geométricas

![Figura 8](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura08_ensamblaje.jpeg)

*Figura 8. Ensamblaje de Tapa/P02 con Base/P01 Gancho A, usado para revisar el encaje (R03). Pendiente: captura del resultado de interferencia.*

![Figura 9](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura09_seccion_frontal.jpeg)

*Figura 9. Sección del ensamblaje en vista frontal: la base P01 (rayado rosa) dentro de la tapa P02 (rayado amarillo).*

![Figura 10](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/figura10_seccion_derecha.jpeg)

*Figura 10. Sección del ensamblaje en vista derecha: la base P01 (rayado rosa) dentro de la tapa P02 (rayado amarillo).*

## 6. Registro de revisión

| Fecha | Qué se detectó | Causa | Corrección | Verificación |
|---|---|---|---|---|
| 06/10/2026 | El clip de P01 no sostiene correctamente a P02 | Altura total y ancho de P01 mal dimensionados | Se modificaron bocetos y cotas de P01 (versión Gancho A..02, Figuras 2 y 3) | [Interferencia o simulación de ensamble, Figura 8] |
| 06/10/2026 | Bordes y transiciones poco estéticos | Medidas iniciales de empalmes y chaflanes | Se reajustaron las medidas y algunas operaciones de acabado | Inspección visual de bordes (R04), [Figura 5] |

## 7. Versiones guardadas

| Versión | Fecha | Descripción del cambio importante |
|---|---|---|
| Tapa/P02 | 06/10/2026 | Modelo inicial de P01 con el clip para P02 |
| Base/P01./Gancho A..2 | 07/10/2026 | Corrección de altura total y ancho de P01; empalmes y chaflanes para mejorar la estética |
| ICT401_F02_Tapa/P02<br>ICT401_F02_Gancho/P01 | 08/10/2026 | Versión de entrega |

## 8. Problemas pendientes y plan hacia la Fase 3

- Pendiente: aplicar más restricciones para que la geometría no se modifique.
- Actividades para el ensamblaje y la validación: pendiente de acordar con el docente.

 ## 9. Imágenes de las piezas de los modelos
![Gancho/P01](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/modelos/ICT401_F02_Gancho_P01.jpeg)
![Tapa/P02](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/modelos/ICT401_F02_Tapa_P02.jpeg)

