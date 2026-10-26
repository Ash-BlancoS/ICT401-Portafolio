# Informe Fase 2: Boceto paramétrico y modelado 3D

ICT401 – Dibujo Técnico Asistido por Computadora · Proyecto integrador (7 %, Semana 12)

**Título del proyecto:** Organizador de Cables – Encaje Rápido

**Categoría:** Soporte

**Equipo:** 3WX – Ashley Y. Blanco Solís, Jassy Diaz Duarte, Libny Y. Urbina Salinas

**Docente:** Oscar Caravaca Mora

**Fecha:** 08/10/2026

**Archivo principal en Fusion Cloud:** 

- ICT401_F02_Tapa/P02
https://myuna182.autodesk360.com/g/projects/202607211116718881/data/dXJuOmFkc2sud2lwcHJvZDpmcy5mb2xkZXI6Y28uamJvSFFVdUhTd09xa09neFlZVmFkUQ/dXJuOmFkc2sud2lwcHJvZDpkbS5saW5lYWdlOm5IMGxXRzRRVDItMDZZcmwtMTdTaGc/viewer
- ICT401_F02_Gancho/P01
https://myuna182.autodesk360.com/g/projects/202607211116718881/data/dXJuOmFkc2sud2lwcHJvZDpmcy5mb2xkZXI6Y28ueFVMUzFOSkFUeW01Tmw0ZXU5cFQ4QQ/dXJuOmFkc2sud2lwcHJvZDpkbS5saW5lYWdlOkdSNHc3QWR5UmdtRkROZHplN2UxVlE/overview


## Presentación del proyecto 

**¿Qué estamos construyendo?** Un organizador de cables llamado *Encaje Rápido*, de la categoría Soporte. Está formado por dos piezas que se acoplan entre sí:

- **Gancho/P01 (la base):** se atornilla a una superficie y lleva un clip.
- **Tapa/P02:** cubre la base, deja salir los cables por dos ranuras y se sostiene por encaje a presión.

**¿Qué problema resuelve?** Los cables sueltos se enredan y se ven desordenados. El organizador los agrupa en un canal, los protege y se puede abrir y cerrar a mano, sin herramientas, tantas veces como se necesite.

**¿Cómo se ve el resultado final?** Una base firme fijada con tornillos, una tapa que encaja con un clic bajo el clip y se quita a mano, un canal de 30 mm donde caben cables de 4 a 8 mm (hasta tres de 8 mm uno junto al otro) y bordes redondeados, sin aristas filosas. Además, el diseño es paramétrico: si se cambia un solo número, como el ancho del canal, el modelo se ajusta solo sin rehacerse. Eso permite adaptar el organizador a otros cables sin empezar de cero.

**¿Qué requisitos cumple?** Cinco, definidos en la Fase 1:

- **R01:** la base se fija con tornillos.
- **R02:** el canal aloja cables de 4 a 8 mm.
- **R03:** la tapa se encaja y desencaja sin interferencias, de forma repetida.
- **R04:** ninguna superficie con bordes filosos.
- **R05:** el ancho del canal se modifica sin reconstruir el modelo.

**¿Qué se hace en la Fase 2?** Se pasa del croquis a mano a un modelo 3D paramétrico en Fusion, con las dos piezas ya acopladas en un ensamblaje. Las medidas dejan de ser números sueltos: quedan guardadas como parámetros con nombre, cada uno ligado al requisito que lo origina.

**Palabras clave de esta fase**

- **Boceto:** el dibujo plano en 2D con el que se empieza cada pieza.
- **Cota:** una medida escrita sobre el boceto.
- **Restricción:** una regla geométrica del boceto (por ejemplo, "esta línea es vertical" o "estas dos son iguales") que evita que se deforme.
- **Parámetro:** una medida con nombre (por ejemplo, `ancho_clip = 26`) que se puede cambiar en un solo lugar.
- **Chaflán y empalme:** el chaflán corta una esquina en diagonal y el empalme la redondea. Ambos quitan el filo del borde.

## Evolución de las piezas: croquis y sólido

Cada pieza se presenta en dos etapas: el croquis a mano de la Fase 1 y el sólido final de esta fase. Las tablas comparan las medidas del croquis con las del modelo final y explican cada cambio con el requisito que lo origina (R01 a R05).

Este informe recoge el estado de las piezas al 08/10/2026. Los ajustes posteriores (orejas del clip de Gancho/P01, parámetro del canal R05 y análisis de interferencias) se documentan en el Informe de la Fase 3.

### Gancho/P01 (Base)
![Figura A1](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/planos/Croquis%20de%20Base-P01(Alternativa%20A).jpeg)
 
*Figura A1. Croquis inicial a mano de Gancho/P01 (Fase 1).*


![Figura A2](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/modelos/ICT401_F02_Gancho_P01.jpeg)

*Figura A2. Sólido final de Gancho/P01 (versión Gancho A..02).*

| Medida | Croquis inicial (mm) | Modelo final (mm) | Motivo del cambio |
|---|---|---|---|
| Altura total | 138 | 200.416 | El clip no encajaba con P02 (R03) |
| Ancho total | 200 | 220 | El clip no encajaba con P02 (R03) |
| Profundidad de la base | 38 | 41 | Ajuste de la base para el encaje (R03) |
| Profundidad de barras y clip | 38 | 38 | Sin cambio (R03) |
| Ancho de las barras | 20 | 20 | Sin cambio |
| Alto de las barras | no acotado | 124.4 | Parámetro alto_barra (R03) |
| Placa superior (ancho x alto) | 60 x 18 | 70 x 10 | Mejor apoyo y encaje (R03) |
| Ancho del clip | 24 | 26 | Parámetro ancho_clip (R03) |
| Alto del clip | no acotado | 47.561 | Parámetro alto_clip (R03) |
| Diámetro del agujero | 4.5 | 4.7 | Tornillo de fijación (R01) |
| Chaflán del agujero | no existía | 3 | Guía del tornillo (R01, R04) |
| Profundidad del agujero | no acotada | 10 | Parámetro prof_agujero (R01) |
| Chaflanes y empalmes | no existían | Ver tabla de dimensiones finales de P01 (sección 3) | Acabado de bordes (R04) |

### Tapa/P02

![Figura B1](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/planos/Croquis%20de%20Tapa-P02(Alternativa%20A).jpeg)
*Figura B1. Croquis inicial a mano de Tapa/P02 (Fase 1).*

![Figura B2](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/modelos/ICT401_F02_Tapa_P02.jpeg)

*Figura B2. Sólido final de Tapa/P02.*

| Medida | Croquis inicial (mm) | Modelo final (mm) | Motivo del cambio |
|---|---|---|---|
| Ancho total | 210 | 233 | 220 de la base + 2 x 6.5 de pared (R03) |
| Profundidad total | 140 | 140 | Sin cambio |
| Altura total | 152 | 203.4 | Debe superar los 200.416 de Gancho/P01 (R03) |
| Ancho de cada ranura de cables | 30 | 30 | Mayor que el cable máximo de 8 (R02) |
| Separación entre ranuras | 40 | 40 | Sin cambio |
| Ranura del centro | 24 x 40 | 29 x 41 | Alojar el clip (R03) |
| Profundidad de la ranura de cables | no acotada | 5 | Parámetro prof_canal_cables (R02) |
| Alto de la ranura de cables | no acotado | 139.4 | Parámetro alto_canal_cables (R02) |
| Chaflanes y empalmes | no existían | Ver tabla de dimensiones finales de P02 (sección 3) | Acabado de bordes (R04) |

<!-- Confirmar antes de entregar: motivos de profundidad de la base, placa superior y ranura del centro. -->

## 1. Resumen del avance

En esta fase se modelaron en Fusion la base P01 (Gancho A..02), la tapa P02 y su ensamblaje. Respecto a la Fase 1, se corrigieron la altura y el ancho de P01 para que el clip sostuviera a P02, y se agregaron empalmes y chaflanes para cumplir R04. Las medidas se organizaron en parámetros y fórmulas. Para la Fase 3 queda aplicar más restricciones, comprobar la interferencia del ensamblaje y acordar su validación con el docente.

## 2. Cambios respecto a la Fase 1

El modelo original se corrigió en tres aspectos: la altura total y el ancho de P01, porque el clip que sostiene a P02 no encajaba correctamente, y se realizaron empalmes y chaflanes para mejorar la estética de la pieza y cumplir R04.

| Elemento | Antes (Gancho A) | Ahora (Gancho A..02) | Motivo |
|---|---|---|---|
| Distancia entre las dos aristas medidas (Figuras 2 y 3) | 26.542 mm | 27.042 mm | Ajuste de +0.5 mm para que el clip sostenga a P02 |
| Altura total de P01 | 138 mm | 200.416 mm | El clip que sostiene a P02 no encajaba |
| Ancho de P01 | 200 mm | 220 mm | Mismo problema de encaje del clip |

![Figura 1](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura01_modelo_inicial.jpeg)

*Figura 1. Modelo inicial de la base, con los cinco bocetos de la exploración.*

![Figura 2](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura02_gancho_a_medicion.jpeg)

*Figura 2. Base/P01 Gancho A: medida original de las barras centrales (distancia de 26.542 mm entre aristas de 134.258 mm y 68.00 mm).*

![Figura 3](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura03_gancho_a02_medicion.jpeg)

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

![Figura 4](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura04_base_isometrica.png)

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

![Figura 5](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura05_tapa_p02.jpeg)

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

![Figura 6](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura06_antes_del_cambio.jpeg)

*Figura 6. Antes del cambio: medida original de las barras centrales (distancia de 26.542 mm entre aristas de 134.258 mm y 68.00 mm).*

**Captura después:** Figura 7

![Figura 7](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura07_despues_del_cambio.jpeg)

*Figura 7. Después del cambio: medidas finales de las barras centrales (distancia de 27.042 mm entre aristas de 142.25 mm y 134.40 mm); el Boceto 14 (Boceto N5) se actualizó automáticamente.*

## 5. Verificaciones geométricas

![Figura 8](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura08_ensamblaje.jpeg)

*Figura 8. Ensamblaje de Tapa/P02 con Base/P01 Gancho A, usado para revisar el encaje (R03). Pendiente: captura del resultado de interferencia.*

![Figura 9](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura09_seccion_frontal.jpeg)

*Figura 9. Sección del ensamblaje en vista frontal: la base P01 (rayado rosa) dentro de la tapa P02 (rayado amarillo).*

![Figura 10](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/imagenes/Fase%2002/figura10_seccion_derecha.jpeg)

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

[Gancho/P01](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/modelos/ICT401_F02_Gancho_P01.jpeg)

[Tapa/P02](https://github.com/Ash-BlancoS/ICT401-Portafolio/blob/main/Proyecto_Integrador/modelos/ICT401_F02_Tapa_P02.jpeg)

## 10. Función de las operaciones principales

Cada operación del modelo responde a una necesidad de la pieza. Las medidas salen de la sección 3.

| Operación o elemento | Qué hace | Para qué sirve | Requisito |
|---|---|---|---|
| Barras y placas superiores de P01 (barras de 20 x 38 x 124.4 mm; placas de 70 x 10 x 38 mm) | Forman el cuerpo de la base | La base queda dentro de la tapa, como muestran las secciones de las Figuras 9 y 10 | R03 |
| Clip y orejas de P01 (26 x 47.561 x 38 mm; orejas de 15 mm de alto) | Sobresalen para entrar en el agarre de la tapa | Sostienen la tapa por encaje a presión; en la Figura 10 el clip atraviesa el fondo de la tapa y las orejas quedan por debajo | R03 |
| Agujeros de la base (Ø4.7 mm, 10 mm de profundidad, chaflán de 3 mm) | Permiten pasar el tornillo | Fijan la base a la superficie; el chaflán guía el tornillo y evita un borde filoso | R01, R04 |
| Pared de la tapa (6.5 mm) | Rodea a la base por los lados | Define el ancho de la tapa: 220 + 2 x 6.5 = 233 mm | R03 |
| Altura de la tapa (203.4 mm) | Deja la tapa más alta que la base | Da 2.984 mm de holgura sobre los 200.416 mm de la base | R03 |
| Agarre del clip en P02 (29.046 x 42 mm) y vaciado | Abren el espacio donde entra el clip | Dan 3.046 mm de holgura de ancho y 4 mm de profundidad para que el clip entre sin interferir | R03 |
| Ranura de cables (30 mm de ancho, 5 de profundidad, 139.4 de alto) | Abre el canal por donde pasan los cables | Aloja cables de 4 a 8 mm; 30 mm ≥ 8 mm | R02 |
| Chaflanes y empalmes en P01 y P02 (0.5 mm a 12 mm según la zona) | Redondean y biselan aristas | Eliminan bordes filosos y mejoran la estética | R04 |

---

## 11. Cómo esta fase cumple lo previsto

| Producto previsto | Evidencia en este informe |
|---|---|
| Archivos de Fusion organizados y editables | Dos archivos nativos en Fusion Cloud, `ICT401_F02_Gancho/P01` y `ICT401_F02_Tapa/P02`, con sus enlaces al inicio. Conservan el historial de operaciones en la línea de tiempo (Figuras 4 y 5) y se pueden editar. También existe el ensamblaje de ambas piezas (Figuras 8, 9 y 10). |
| Bocetos suficientemente definidos | Los bocetos están dimensionados con cotas ligadas a parámetros y con restricciones geométricas. Se nota en la modificación paramétrica: al cambiar una cota, el Boceto 14 se actualizó solo (sección 4, Figura 7). Quedan restricciones adicionales por aplicar, reconocidas en la sección 8. |
| Operaciones coherentes con la forma y función | Sección 10: cada operación principal se explica por lo que hace y por el requisito al que responde. |
| Dimensiones relacionadas con los requisitos | La tabla de parámetros (sección 3) indica el requisito que origina cada medida. Las fórmulas conectan las piezas: `ancho_tapa = ancho_base + 2 * espesor_pared_tapa`. La sección "Evolución de las piezas" compara cada medida del croquis inicial con la del modelo final y explica el motivo del cambio. Hay condiciones comprobables para R02 (30 mm ≥ 8 mm) y R03 (holguras mayores que cero). |
| Nombres, versiones e historial comprensibles | Los archivos llevan el prefijo `ICT401_F02_`, los parámetros tienen nombres descriptivos (por ejemplo `ancho_canal_cables`) y la sección 7 lista las versiones con fecha y cambio. |
| Evidencia de revisión | La sección 6 registra qué se detectó, la causa y la corrección: el clip no sostenía a P02, por lo que se cambió la altura y el ancho de P01 (Figuras 2 y 3). La sección 2 resume los cambios respecto a la Fase 1. |
| Evidencia de una modificación paramétrica | Sección 4: la distancia entre las aristas de las barras centrales pasó de 26.542 mm a 27.042 mm (Figuras 6 y 7), sin rehacer el modelo. |

**Qué quedó pendiente y dónde se cierra.** El informe reconoce tres pendientes en las secciones 3 y 8: más restricciones en los bocetos, la verificación de interferencia del ensamblaje y la vinculación del parámetro `ancho_canal_cables` (R05). El Informe de la Fase 3 documenta el análisis de interferencia y la prueba de R05, en la que el ancho del canal se cambió de 30 a 25 mm desde la tabla de parámetros y el boceto se actualizó solo.
