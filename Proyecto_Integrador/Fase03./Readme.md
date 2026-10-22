# Informe Fase 3: Integración y validación

ICT401 – Dibujo Técnico Asistido por Computadora · Proyecto integrador (6 %, Semana 14)

**Título del proyecto:** Organizador de Cables – Encaje Rápido

**Categoría:** Soporte

**Equipo:** 3WX – Ashley Y. Blanco Solís, Jassy Diaz Duarte, Libny Y. Urbina Salinas

**Docente:** Óscar Caravaca Mora

**Fecha:** 21/10/2026

**Archivos principales en Fusion Cloud:**

ICT401_F02_Gancho/P01

ICT401_F02_Tapa/P02

ICT401_F03_Ensamblaje  https://myuna182.autodesk360.com/g/projects/202607211116718881/data/dXJuOmFkc2sud2lwcHJvZDpmcy5mb2xkZXI6Y28ueFVMUzFOSkFUeW01Tmw0ZXU5cFQ4QQ/dXJuOmFkc2sud2lwcHJvZDpkbS5saW5lYWdlOmpsaWwzbG1XU3phTjFkbC05c1pDa1E/overview

---

## 1. Resumen del avance

En esta fase se integraron en un ensamblaje la base P01 (Gancho A..02) y la tapa P02, modeladas en la Fase 2. Se definió la relación de posición entre ambas piezas, se revisaron la alineación, el contacto y las interferencias, y se validó la geometría contra los requisitos R01 a R05 de la matriz de requisitos de la Fase 1. Las contribuciones de cada integrante quedan identificadas en la sección 8.

Resultado: el ensamblaje funciona con una unión deslizante de 0 a 200 mm y la tapa como pieza fija; el canal de cables mide 30.00 mm (R02) y el análisis de interferencia detectó 14.888 mm³ con la tapa cerrada, en las puntas de las orejas del clip, que se corregirán, y 955.76 mm³ a media apertura (30 mm), asociados al paso del clip por el agarre. Quedan por documentar la verificación de los agujeros (R01), la revisión de bordes (R04) y la prueba paramétrica del canal (R05).

## 2. Punto de partida (Fase 2)

| Elemento | Estado al cerrar la Fase 2 |
| --- | --- |
| P01 Base/Gancho A..02 | Altura 200.416 mm, ancho 220 mm, profundidad 41 mm; clip de 26 x 47.561 x 38 mm |
| P02 Tapa | Ancho 233 mm, altura 203.4 mm, profundidad 140 mm; pared de 6.5 mm |
| Ensamblaje | Creado para revisar el encaje; sin captura del resultado de interferencia |
| Parámetros | Medidas organizadas con fórmulas (Modificar → Cambiar parámetros) |
| Pendientes | Más restricciones en los bocetos; vincular ancho_canal_cables a la geometría (R05); acordar la validación del ensamblaje con el docente |

## 3. Integración del conjunto

**Componentes integrados**

| Componente | Rol en el ensamblaje | Cómo se ubica |
| --- | --- | --- |
| P01 Base/Gancho A..02 | Base; en el uso real se atornilla a la superficie (R01) | Se mueve respecto de P02 mediante la unión Deslizante_Tapa, en la práctica la Tapa es la que se mueve respecto a la Base. |
| P02 Tapa | Cubre el gancho y el cable | Pieza fija (Ground) del ensamblaje. Pieza fija en Fusion, sin embargo en la práctica es movible. |

![Figura 1](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig01_ensamblaje_isometrico.png)

*Figura 1. Ensamblaje de P01 y P02 en Fusion. "Configuración 1:1" corresponde a P01 Base/Gancho A..02.*

## 4. Relaciones de posición o movimiento (justificadas)

| Relación | Tipo de unión | Justificación | Grados de libertad |
| --- | --- | --- | --- |
| P02 contra el ensamblaje | Fija (Ground) | En el modelo la tapa es la pieza de referencia del ensamblaje, porque al fijar la base el conjunto queda volteado en el espacio de trabajo; el movimiento relativo entre ambas piezas es el mismo que si la base estuviera fija | 0 |
| P01 respecto de P02 | Deslizante | La tapa se encaja a presión bajo el clip y debe poder quitarse a mano sin herramientas (R03 y sección 4.3 de la Fase 1); en el modelo esto se representa moviendo la base respecto de la tapa fija | 1 |

**Recorrido de la tapa:** deslizamiento a lo largo del eje Z, de 0 a 200 mm; 0 mm es la posición cerrada. El recorrido lo limitan los límites de movimiento del joint (mínimo 0 mm y máximo 200 mm).

![Figura 2](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig02_tapa_cerrada_0mm.png)

*Figura 2. Ensamblaje cerrado, con el deslizador de Deslizante_Tapa en 0 mm.*

![Figura 3](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig03_tapa_media_apertura_30mm.png)

*Figura 3. Media apertura, con el deslizador en 30 mm: la base se desplaza hacia arriba respecto de la tapa fija.*

## 5. Revisión de alineación, contacto e interferencias

**5.1 Alineación**

| Qué se revisó | Resultado | Evidencia |
| --- | --- | --- |
| Alineación del clip de P01 con el agarre de P02 (ancho del agarre 29.046 mm) | El corte muestra el clip de P01 dentro del agarre de P02, entre las dos paredes de la tapa; los parámetros dan una holgura total de 3.046 mm (1.523 mm por lado si está centrado), sin medirla por separado | Figura 4 |
| Alineación de la ranura de cables con el área de salida | Con la tapa cerrada, las dos ranuras en U quedan libres, sin que la base las tape, y miden 30.00 mm de ancho (Figura 8) | Figura 5 |

![Figura 4](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig04_alineacion_clip_agarre.png)

*Figura 4. Sección por el centro del clip: la base P01 (rayado rosa) dentro de la tapa P02 (rayado amarillo).*

![Figura 5](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig05_alineacion_ranura_cables.png)

*Figura 5. Vista Right del ensamblaje cerrado: las dos ranuras de cables de la tapa quedan libres.*

**5.2 Contacto**

Contactos previstos por diseño: el clip de P01 con el agarre de P02, donde las orejas del clip sostienen la tapa por encaje a presión, y las paredes interiores de la tapa con los lados de la base.

El ancho interior de la tapa (233 − 2 × 6.5 = 220 mm) es igual al ancho de la base (220 mm), es decir, 0 mm de holgura lateral. En el análisis con Include Coincident Faces activado, ese contacto no apareció como interferencia (solo se reportó el grupo de las puntas de las orejas), por lo que se acepta como contacto de apoyo entre la base y la tapa.

**5.3 Interferencias**

Herramienta usada: Inspeccionar → Interferencia, con ambos componentes seleccionados, en la posición cerrada (0 mm) y a media apertura (30 mm).

| Posición | Interferencias encontradas | Volumen | Acción |
| --- | --- | --- | --- |
| Cerrada (0 mm) | 1 grupo de interferencia (con Include Coincident Faces activado) | 14.888 mm³ | Corregir: ajustar el empalme o chaflán de la punta inferior de las orejas del clip de P01 y recalcular hasta 0 mm³ |
| Media apertura (30 mm) | 1 grupo de interferencia | 955.76 mm³ | Justificar: corresponde al paso del clip por el agarre durante el encaje a presión, que en un modelo rígido aparece como solape; se comprobará a 60 mm que no queda interferencia fuera del agarre |

![Figura 6](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig06_detalle_interferencia_cerrada.png)

*Figura 6. Resultado de Inspeccionar → Interferencia con la tapa cerrada (0 mm): 1 grupo, volumen de 14.888 mm³ entre P02 y P01.*

![Detalle de la Figura 6](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig06_interferencia_cerrada.png)

*Detalle de la Figura 6: la interferencia aparece como dos pequeños triángulos rojos en las puntas inferiores de las orejas del clip.*

![Figura 6b](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig06b_interferencia_media_apertura.png)

*Figura 6b. Resultado de Inspeccionar → Interferencia con la tapa a media apertura (30 mm): 1 grupo, volumen de 955.76 mm³.*

## 6. Validación geométrica respecto de requisitos

Matriz de requisitos tomada de la sección 4.5 de la Fase 1; valores tomados de la tabla de parámetros de la Fase 2.

| ID | Requisito | Comprobación | Valor en el modelo | Resultado | Evidencia |
| --- | --- | --- | --- | --- | --- |
| R01 | La base tiene interfaz para tornillos de fijación, sin interferir con el resto de la geometría | Verificación geométrica del sistema de fijación | Agujero Ø4.7 mm, chaflán 3 mm, profundidad 10 mm | Cumple: el diámetro medido del agujero es 4.70 mm (Figura 7), igual al parámetro diametro_tornillo, y no coincide con ninguna zona de interferencia (Figura 6) | Figura 7 |
| R02 | El canal aloja cables de 4 a 8 mm sin holgura excesiva | Medición del canal en el modelo 3D | Canal de 30.00 mm de ancho (medido en Fusion, Figura 8) x 5 mm de profundidad; cable de 4 a 8 mm | Cumple en capacidad (30.00 ≥ 8 mm); el ancho se justifica por alojar uno o varios cables | Figura 8 |
| R03 | La tapa se encaja y desencaja sin interferencias, de forma repetida | Simulación de ensamble y análisis de interferencia | Holgura de ancho del clip 3.046 mm; holgura de profundidad 4 mm; altura de tapa − altura de base = 2.984 mm | Parcial: la tapa se desliza y encaja (Figuras 2 y 3), pero hay interferencia de 14.888 mm³ en cerrado, pendiente de corrección, y de 955.76 mm³ a 30 mm, asociada al paso del clip | Figuras 2, 3, 6 y 6b |
| R04 | Ninguna superficie con bordes filosos | Inspección visual de bordes y transiciones | Chaflanes y empalmes en P01 y P02 (parámetros radio_empalme_tapa 1 mm, chaflan_tapa 0.5 mm) | Cumple en la zona revisada de P01: las orejas del clip y la columna tienen transiciones redondeadas, sin aristas vivas (Figura 9); la tapa P02 lleva chaflanes de 0.5 mm y empalmes de 1 mm según la Fase 2 | Figura 9 |
| R05 | El diámetro (ancho) del canal se modifica sin reconstruir el modelo | Edición paramétrica en el historial | Cota d75 del boceto ancho_canal_cables = 30 mm | Cumple: al cambiar la cota de 30 a 25 mm desde la tabla de parámetros, el boceto de la ranura se actualizó a 25.00 mm sin rehacerlo (Figuras 10 y 11) | Figuras 10 y 11 |

**Notas por requisito**

**R01.** Con Measure, el agujero de tornillo mide 4.70 mm de diámetro (radio de 2.35 mm), igual al parámetro diametro_tornillo. El área medida de la pared cilíndrica (103.358 mm²) corresponde a unos 7 mm de alto, que coincide con los 10 mm de profundidad menos los 3 mm del chaflán.

![Figura 7](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig07_R01_agujeros_tornillo.png)

*Figura 7. Medición del agujero de tornillo de P01 con Measure: diámetro de 4.70 mm.*

**R02.** El canal mide 30 mm y el cable más grueso mide 8 mm, por lo que cumple en capacidad (30 ≥ 8). Como el requisito exige "sin holgura excesiva", se mantiene el ancho de 30 mm porque la Fase 1 pide sujetar uno o varios cables (sección 4.1) y en 30 mm caben hasta 3 cables de 8 mm uno junto al otro. La profundidad de 5 mm queda por comprobar con una medición adicional.

![Figura 8](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig08_R02_canal_cables.png)

*Figura 8. Medición del ancho de la ranura de cables con Measure: 30.00 mm entre las dos aristas.*

**R04.** Con el estilo Shaded with Visible Edges Only se revisaron los bordes de la base P01 en la zona del clip: las orejas tienen curvas amplias y la esquina de la columna vertical está redondeada, por lo que no se ven aristas vivas que puedan dañar el recubrimiento del cable.

![Figura 9](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig09_R04_bordes.png)

*Figura 9. Revisión visual de bordes de P01 (tapa oculta) con Shaded with Visible Edges Only.*

**R05.** En la tabla de parámetros de la tapa, el ancho de la ranura corresponde a la cota d75 del boceto ancho_canal_cables. Se cambió de 30 mm a 25 mm (Figuras 10 y 11) y el boceto se actualizó a 25.00 mm sin rehacerlo, con lo que el ancho del canal se puede modificar sin reconstruir el modelo.

![Figura 10](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig10_R05_antes_canal_30mm.png)

*Figura 10. Antes del cambio: la cota d75 del boceto ancho_canal_cables vale 30 mm en la tabla de parámetros de la tapa.*

![Figura 11](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2003/fig11_R05_despues_canal_25mm.png)

*Figura 11. Después del cambio: la cota d75 vale 25 mm y el boceto de la ranura se actualizó a 25.00 mm.*

## 7. Registro de revisión

| Fecha | Qué se detectó | Causa | Corrección | Verificación |
| --- | --- | --- | --- | --- |
| 20/10/2026 | Interferencia de 14.888 mm³ entre P01 y P02 con la tapa cerrada (0 mm) | Las puntas inferiores de las orejas del clip de P01 se solapan con P02 por la forma y el tamaño de las orejas (detalle de la Figura 6) | Ajustar el empalme o chaflán de la punta inferior de las orejas en P01 (aprox. 1 mm) y recalcular | Figura 6 (antes del ajuste); nuevo análisis de interferencia en 0 mm tras la corrección |
| 20/10/2026 | Interferencia de 955.76 mm³ con la tapa a media apertura (30 mm) | Tramo del recorrido en que el clip pasa por el agarre; en el modelo rígido el encaje a presión aparece como solape | Se justifica como paso del clip a presión; la posición cerrada debe quedar en 0 mm³ | Figura 6b; comprobación a 60 mm |

**Versiones guardadas**

| Versión | Fecha | Descripción del cambio importante |
| --- | --- | --- |
| ICT401_F02_Gancho/P01 y ICT401_F02_Tapa/P02 | 08/10/2026 | Versión de entrega de la Fase 2 |
| ICT401_F03_Ensamblaje | 21/10/2026 | Integración de P01 y P02 y validación (versión "Entrega Fase 3") |

## 8. Contribuciones individuales

Responsables según el plan de trabajo de la Fase 1 (sección 8.2).

| Integrante | Contribución en la Fase 3 |
| --- | --- |
| Ashley Y. Blanco Solís | Ajustes en P01 (base y orejas del clip) y restricciones de sus bocetos |
| Jassy Diaz Duarte | Ajustes en P02 (tapa) y vínculo del parámetro del canal (R05) |
| Libny Y. Urbina Salinas | Ensamblaje con unión deslizante, análisis de interferencia, mediciones de validación y bitácora de revisión |

## 9. Problemas pendientes y cierre

- Interferencia de 14.888 mm³ en la posición cerrada (puntas inferiores de las orejas del clip de P01): pendiente de corregir y volver a calcular (Figura 6).
- Interferencia de 955.76 mm³ con la tapa a media apertura (30 mm): pendiente de decidir si se justifica como paso del clip a presión o se corrige (Figura 6b).
- Pasos hacia la Fase 4 (Documentación): con el ensamblaje validado, preparar los planos de P01, P02 y el conjunto (vistas, cortes, acotación, cajetín y lista de componentes) y exportar PDF y DXF de la versión aprobada.
