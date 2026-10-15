# ICT401 · Semana 13 — Registro de ensamblaje básico

12 al 17 de octubre de 2026.

- Estudiante: Ashley Blanco
- Grupo: 60
- Proyecto de Fusion Cloud con acceso docente: Ashley Blanco
- Nombre del diseño de ensamblaje: ICT401_S13_Ensamblaje_Basico
- Piezas base utilizadas: CT401_S13_01_Base_100x70x10_Ashley_Blanco, ICT401_S13_02_Soporte_60x70x40_Ashley_Blanco, ICT401_S13_03_Pasador_D16x80_Ashley_Blanco
- Fecha de trabajo de laboratorio: 15/10

## Instrucciones

Utilice esta plantilla en `Portafolio/semana13/` y guárdela como `S13_Registro_Apellido_Nombre.md`. Sustituya `Apellido_Nombre` por un apellido y un nombre sin espacios ni tildes. Complete cada `[Respuesta]` durante las cuatro lecciones prácticas y agregue las imágenes solicitadas junto con la ficha.

La sesión virtual del miércoles se dedica a la revisión oral del Proyecto Integrador. Este registro corresponde únicamente a las cuatro lecciones prácticas de laboratorio. La actividad es formativa y no sustituye las evaluaciones oficiales posteriores.

Trabaje con las piezas base proporcionadas por la persona docente. Si todavía no se han distribuido, use las imágenes PNG y las dimensiones de esta ficha para construirlas. No modifique los archivos originales ni oculte un componente para evitar una interferencia. Si su versión de Fusion utiliza otro nombre de comando, escriba el nombre real utilizado y describa su función.

Ayuda oficial de Fusion: [Fusion Help](https://help.autodesk.com/view/fusion360/ENU/), sección `Assemblies`.

## Conjunto de trabajo

Dimensiones nominales de referencia: base maciza `100 x 70 x 10 mm`; soporte de `60 mm` de ancho, `70 mm` de alto y `40 mm` de fondo, con alojamiento pasante `diametro 16 mm`; pasador `diametro 16 x 80 mm`.

![Ensamblaje básico de referencia](ICT401_S13_Ensamblaje_Basico.png)

### Posicionamiento exacto

El soporte se centra sobre la base, no se coloca en una esquina:

- Margen lateral: `20 mm` a cada lado, porque `(100 - 60) / 2 = 20 mm`.
- Margen frontal y posterior: `15 mm` a cada lado, porque `(70 - 40) / 2 = 15 mm`.
- Cara inferior del soporte coincidente con la cara superior de la base.
- Relación base-soporte: `Rígida (Rigid)`.
- Centro del alojamiento: `40 mm` desde la cara inferior del soporte y `30 mm` desde cada lado del soporte.
- Pasador: coaxial con el alojamiento, centrado en el espesor de la pared y con relación `Revolute (Revoluta)`.
- Si la pared mide `10 mm`, el pasador de `80 mm` sobresale aproximadamente `35 mm` a cada lado.

No registre una distancia desde una esquina para ubicar el pasador. Su posición queda definida por el centro del alojamiento.

| Componente | Nombre en Fusion | Función dentro del conjunto | Observación inicial |
|---|---|---|---|
| Base | CT401_S13_01_Base_100x70x10_Ashley_Blanco | sirve de apoyo para el soporte vertial | Se inserta primero y se fija con Ground|
| Soporte vertical | ICT401_S13_02_Soporte_60x70x40_Ashley_Blanco | une la base con el pasador y permite que el pasador gire | Se centra sobre la base y queda rígido |
| Eje o pasador | ICT401_S13_03_Pasador_D16x80_Ashley_Blanco| Ser el pasador| Se coloca en el soporte vertical y puede girar |

## Comandos bilingues de Fusion

| Accion | Ruta o comando | Resultado esperado |
|---|---|---|
| Crear diseño | `Archivo > Nuevo diseño (File > New Design)` | Diseño vacío y proyecto confirmado en el Panel de datos. |
| Insertar pieza | `Insertar en el diseño actual (Insert into Current Design)` | Componente visible en el Navegador. |
| Fijar base | Clic derecho en Navegador > `Fijar (Ground)` | La base no se desplaza ni gira. |
| Relacionar soporte | `Ensamblar > Unión (Assemble > Joint)` > `Rígida (Rigid)` | El soporte queda unido a la base. |
| Relacionar pasador | `Ensamblar > Unión (Assemble > Joint)` > `Revoluta (Revolute)` | El pasador gira alrededor de su eje. |
| Probar relación | Clic derecho en la unión > `Animar unión (Drive Joint)` | Se comprueba el movimiento permitido. |
| Revisar interferencias | `Inspeccionar > Interferencia (Inspect > Interference)` > `Calcular (Compute)` | Se identifican cuerpos que ocupan el mismo volumen. |
| Editar relación | Clic derecho en la relación > `Editar (Edit)` | Se corrige origen, orientación, tipo o desplazamiento. |

Registre en cada lección qué componente seleccionó, qué comando utilizó y qué resultado observó. No se considera suficiente escribir solo el nombre de la herramienta.

## L1 — Reconocimiento de piezas y componente base

### Diagnóstico

- ¿Qué pieza funcionará como base y por qué?:  La base porque es plana y sirve de apoyo.
- ¿Qué superficies de la base y del soporte podrían entrar en contacto?:  La cara superior de la base y la cara inferior del soporte.
- ¿Qué eje o alojamiento utilizará el pasador?: El agujero del soporte
- ¿Qué movimiento estaba libre antes de aplicar relaciones?: Todas las piezas podían moverse y girar.
- ¿Qué orientación inicial seleccionó y por qué?: Isométrica, me parece mas fácil de ver mas características de todas la piezas.

### Estado inicial

| Comprobación | Resultado |
|---|---|
| Base insertada como componente | Sí, al intentar moverlo sale que el componente no se puede mover|
| Base fija o establecida como referencia | Sí,al intentar moverlo sale que el componente no se puede mover |
| Soporte insertado |Sí |
| Eje o pasador disponible |si|
| Nombres identificables en el navegador | Sí |

### Evidencia L1

`S13_PiezasBase_Blanco_Ashley.png`: captura del ensamblaje con la base y el soporte visibles, el navegador de componentes abierto y los nombres identificables.

![L1: piezas base](S13_PiezasBase_Blanco_Ashley.png)

## L2 — Relaciones entre componentes

### Decisiones

| Relación | Componentes o geometrías vinculadas | Movimiento que elimina | Movimiento que conserva | Resultado |
|---|---|---|---|---|
| 1 | 	Base con soporte | Cualquier movimiento del soporte en el que no este centrado con la base | ninguno | el soporte esta fijo a la base |
| 2 | Pasador con soporte|  | mover se a cualquier lado | revolucion |

- Comando o herramienta utilizada: join
- ¿Por qué esa relación representa la intención del conjunto?: Porque el soporte debe quedar rígido y el pasador debe girar
- ¿La orientación del soporte quedó correcta?: Sí, centrado en la base y en vertical.
- ¿Qué movimiento debe conservar el eje?: sobre su propio eje .. z
- ¿Qué movimiento inesperado observó y cómo lo corrigió?: temblor en el ensamble y movimiento de remo en el pasador, restringiendo el movimiento a solo revolucion.

### Evidencia L2

`S13_Relaciones_Blanco_Ashley.png`: captura del navegador de componentes y de la relación aplicada, con el conjunto orientado para leer la posición del soporte y del eje.

![L2: relaciones](S13_Relaciones_Blanco_Ashley.png)

## L3 — Revisión de interferencias

- Herramienta utilizada: inspeccionar-- interferencia
- Componentes comparados: base,pasador y soporte
- ¿Se encontró una interferencia?: no
- Ubicación de la condición: agujero del soporte y parte y cara inferior de este
- ¿Se trata de interferencia, contacto previsto o separación intencional?: contacto previsto
- Causa probable: las dimensiones coinciden
- ¿Qué efecto tendría sobre el funcionamiento del conjunto?: el pasador gira libremente en el eje z.
| Componente A | Componente B | Zona revisada | Resultado | Evidencia |
|---|---|---|---|---|
|Soporte| Pasador | agujero de soporte | sin interferencia | captura del analisis |

### Evidencia L3

`S13_Interferencia_Blanco_Ashley.png`: captura del análisis o de la zona problemática, con los componentes involucrados identificables.

![L3: interferencia](S13_Interferencia_Blanco_Ashley.png)

## L4 — Corrección, verificación y cierre

### Registro de corrección

- Problema seleccionado: ninguno
- Corrección prevista antes de modificar: ninguna
- Componente o relación modificada: ninguna
- Cambio aplicado: ninguna
- Resultado del segundo análisis: El pasador gira correctamente sin desplazarse.
- ¿La base continúa estable?: Sí
- ¿El soporte conserva su orientación?: Sí
- ¿El eje conserva el movimiento esperado?: Sí
- Versión o nombre final en Fusion Cloud: ICT401_S13_Ensamblaje_Basico_Blanco_Ashley.

| Comprobación final | Resultado | Evidencia o explicación |
|---|---|---|
| Componentes visibles y nombrados | [Conforme| en el navegador se ven con sus nombres correctos|
| Relaciones comprensibles | Conforme| Base rígida y pasador con unión de revolucion.|
| Movimiento esperado | Conforme | Pasador gira sobre mismo eje |
| Interferencia revisada | Conforme | segun el analisis mostro 0.00 mm³ |
| Corrección documentada | Conforme | se documento y se soluciono|

### Evidencia L4

`S13_Correccion_Blanco_Ashley.png`: captura comparativa o lámina con el estado problemático y el estado corregido, ambos etiquetados.
**no hubo correciones**

![L4: corrección](S13_Correccion_Blanco_Ashley.png)

## Checklist de cierre

- [x ] Las tres piezas base corresponden al conjunto indicado.
- [ x] La base está fija o definida como referencia.
- [ x] Los componentes tienen nombres identificables.
- [ x] Cada relación aplicada tiene una intención explicable.
- [ x] El movimiento permitido corresponde a la función del conjunto.
- [ x] Se ejecutó una revisión de interferencias.
- [ x] La interferencia o ausencia de interferencia quedó interpretada.
- [ x] La corrección quedó registrada antes y después.
- [ x] El ensamblaje fue guardado en Fusion Cloud.
- [ x] La ficha y las imágenes utilizan la nomenclatura solicitada.
- [ x] No se adelantaron vistas explosionadas ni listas de componentes.

## Reflexión final

1. ¿Qué diferencia encontró entre insertar piezas y construir un ensamblaje con relaciones?: Insertar piezas solo las coloca en el diseño, pero no tienen conexión entre sí. Construir un ensamblaje con relaciones hace que las piezas trabajen juntas, fijas o con movimiento, según la unión aplicada.
2. ¿Qué relación fue más difícil de definir y por qué?: La relación del pasador con el alojamiento (Revoluta), porque había que ajustar bien el origen en el centro del agujero para que no se desplazara.
3. ¿Cómo distinguió una interferencia de un contacto previsto?: La interferencia aparece con volumen distinto de cero en el análisis. El contacto previsto muestra volumen 0.00 mm³, lo que significa que encajan sin solaparse.
4. ¿Qué comprobará en Semana 14 antes de generar una vista explosionada o una lista de componentes?: 

## Revisión docente

- Observación sobre componentes y nombres: [Respuesta]
- Observación sobre relaciones: [Respuesta]
- Observación sobre interferencias: [Respuesta]
- Corrección sugerida: [Respuesta]
- Estado del registro: [Pendiente/Completo]
