# Fase 4 — Documentación y archivos finales

**Curso:** ICT401 · Dibujo Técnico Asistido por Computadora

**Proyecto:** Proyecto integrador — organizador de cables (base/gancho + tapa)

**Universidad:** Universidad Nacional (UNA), Sede Liberia

**Docente:** Óscar Caravaca Mora

**Ponderación:** 7 % · **Entrega oficial:** Semana 16

**Equipo:** Ashley Blanco · Jassy Díaz Duarte · Libny Urbina Salinas

---

## 1. Descripción

Este archivo contiene la documentación técnica final del proyecto integrador. El modelo aprobado en la Fase 3 (ensamblaje con las piezas P01 y P02) se convierte en planos normalizados, con cajetín, lista de componentes, acotación y archivos de intercambio.

## 2. Producto previsto (según el enunciado)

- Plano técnico coherente con el modelo.
- Vistas, cortes, secciones o detalles pertinentes.
- Acotación y criterios introductorios de tolerancia.
- Formato, cajetín y notas técnicas.
- Lista de componentes cuando corresponda.
- Archivos de intercambio o fabricación solicitados (PDF, DXF, STEP o STL).
- Verificación de que las salidas corresponden a la versión aprobada.

## 3. Contenido de la carpeta

```
Fase04/
├── README.md
├── ICT401_F04_Registro_Urbina_Libny.md
├── planos/
│   ├── ICT401_F04_Ensamblaje_D_Final.pdf
│   ├── ICT401_F04_Gancho_P01_Dibujo.pdf
│   └── ICT401_F04_Tapa_P02_Dibujo.pdf
└── exportaciones/        (DXF)
```



## 4. Planos

| Plano | Archivo | Dibujante | Hoja | Escala en cajetín | Rev. |
|---|---|---|---|---|---|
| Ensamblaje | `ICT401_F04_Ensamblaje_D_Final.pdf` | Libny Urbina Salinas | A3 | 1:3 | A |
| Gancho / P01 | `ICT401_F04_Gancho_P01_Dibujo.pdf` | Ashley Blanco | A3 | 1:2 | A |
| Tapa / P02 | `ICT401_F04_Tapa_P02_Dibujo.pdf` | Jassy Díaz Duarte | A3 | 1:2.5 | A |

- **Unidades:** milímetros (mm)
- **Tolerancia general:** ISO 2768-m
- **Tolerancias específicas:** 42 ±0.2 y 44.66 ±0.2 (plano de ensamblaje)
- **Número de dibujo del ensamblaje:** ICT401-F04-01
- **Fecha de emisión:** 03/11/2026

## 5. Lista de componentes (ensamblaje)

| Ítem | Cant. | Pieza | Material |
|---|---|---|---|
| 1 | 1 | Base / Gancho (P01) | Plastic PLA |
| 2 | 1 | Tapa (P02) | Plastic PLA |

> El material se define en las propiedades de cada pieza en Fusion y la lista lo toma de allí. Los Part Number aún aparecen como números de fecha y hora (2026-10-06-17-45-56-483 y 2026-11-03-19-08-29-650); se dejan tal como los genera Fusion.

## 6. Cómo se generó

1. Se congeló la versión aprobada del modelo en Fusion.
2. Se creó un dibujo nuevo (Drawing) desde el ensamblaje y desde cada pieza, en hoja A3 con cajetín ISO.
3. Se colocaron las vistas ortogonales y una isométrica; en el ensamblaje, una vista explosionada con globos numerados y un corte A-A (1:3).
4. Se acotaron las piezas individuales y se indicó la tolerancia general en el cajetín.
5. Se llenó el cajetín (departamento, referencia técnica, autor, aprobador, tipo y estado del documento, título, número de dibujo, revisión, fecha y hoja).
6. Se exportaron los PDF y los archivos DXF desde la misma versión.

## 7. Herramientas

- Autodesk Fusion (licencia educativa) — modelado, ensamblaje y dibujos
- Exportación: PDF y DXF
- 

## 8. Autoría

| Integrante | Contribución |
|---|---|
| Ashley Blanco | Plano de Gancho / P01 |
| Jassy Díaz Duarte | Plano de Tapa / P02 |
| Libny Urbina Salinas | Plano de ensamblaje, cajetín y lista de component
