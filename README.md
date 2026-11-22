# Akmon Libreria propia que uso para mis diseños


Base para el diseño de las PCB, con las reglas de diseño de **JLCPCB** en las dos herramientas tanto Kicad como Altium.

- **Altium Designer 26** (`altium/`): bibliotecas `Forja.SchLib` y `Forja.PcbLib` con piezas comprobadas, y las reglas exportadas. De aquí sale Telamon, y Draupnir si se hace en Altium.
- **KiCad 10** (`plantilla/` y `biblioteca/`): la biblioteca `forja.pretty` con las huellas propias (la primera, la resistencia compacta de Draupnir) y, en diciembre, la plantilla de proyecto con cajetín FORJA y la

## Reglas de diseño (JLCPCB, 2 capas, 1,6 mm)

Sacadas de la [página de capacidades de JLCPCB](https://jlcpcb.com/capabilities/pcb-capabilities), no de memoria. Cada valor, con la fecha en que se comprobó contra la página.

| # | Parámetro | Mínimo del fabricante | Mi regla (con margen) | Comprobado el |
|---|---|---|---|---|
| 1 | Ancho de pista | 0,10 mm | 0,20 mm (señal por defecto: 0,25 mm) | 2026-11-10 |
| 2 | Separación pista–pista | 0,10 mm | 0,20 mm | 2026-11-10 |
| 3 | Taladro mínimo (vía) | 0,15 mm (vía de 0,25 mm de diámetro) | 0,30 mm (vía de 0,60 mm de diámetro) | 2026-11-10 |
| 4 | Anillo: vía / agujero de componente | 0,05 mm (preferido 0,075 mm) / 0,18 mm (recomendado ≥ 0,25 mm) | 0,15 mm / 0,25 mm | 2026-11-10 |
| 5 | Separación al borde de placa | 0,20 mm | 0,50 mm | 2026-11-10 |
| 6 | Serigrafía: ancho de línea / alto de texto | 0,15 mm / 1,0 mm | 0,20 mm / 1,2 mm en el texto propio | 2026-11-10 |

Mínimos de la fila «2-layer» con cobre de 1 oz. Entre paréntesis, el valor recomendado cuando la página lo da.

**Por qué estos márgenes** (placas de 2 capas, soldadas a mano, hasta 2 A):

- **Pista y separación (1 y 2):** el doble del mínimo. A 0,10 mm la placa se puede fabricar, pero cualquier defecto de grabado ya es un corte o un corto. En placas de módulos sobra sitio para 0,20 mm.
- **Vía (3):** 0,30 / 0,60 mm no lleva recargo. La página cobra más por los taladros de 0,10 y 0,15 mm, y por los de 0,20 y 0,25 mm si la vía mide menos de 0,45 mm.
- **Anillos (4):** son dos cosas distintas. La página no tiene fila para el anillo de la vía: sale de «el diámetro de la vía debe ser 0,1 mm mayor que el taladro (0,15 mm preferido)», es decir, 0,05 mm por lado. La fila «PTH annular ring» (0,18 / 0,25 mm) la aplico a los agujeros de componente, porque una vía mínima de 0,15 / 0,25 mm no podría cumplirla. La página no lo dice con estas palabras: es la lectura que hace encajar las dos filas.
- **Anillo en huellas propias:** en módulos y bornas, 0,30 mm o más. Un anillo ancho aguanta mejor el soldador sin despegarse.
- **Borde (5):** 0,50 mm cubre la tolerancia del fresado (±0,2 mm) y deja margen.
- **Serigrafía (6):** 0,20 / 1,2 mm guarda la proporción 1 : 6 que prefiere el fabricante. Las referencias de las huellas de KiCad van a 0,15 / 1,0 mm, justo en el mínimo, y se quedan así.
- **Corriente:** estas reglas no fijan el ancho por corriente. Eso va en la clase de red Potencia de la plantilla: 2 A con 10 °C de subida piden unos 0,8 mm en cobre de 1 oz (IPC-2221), así que la clase va a 1,0 mm.

**Notas para la plantilla** (misma página, misma fecha):

- **Agujero metalizado a pista (PTH to Track):** mínimo 0,28 mm; recomendado 0,35 mm. Mi regla: 0,35 mm.
- **Tolerancia de taladro (agujeros pasantes):** +0,13 / −0,08 mm. Cuenta con ella al dibujar las huellas de los módulos y de la Pico.
- **Tolerancia del contorno fresado:** ±0,2 mm (precisión normal).
- **Proporción de la serigrafía:** ancho de trazo : alto de texto = 1 : 6 (preferida).
- **Grosor:** 1,6 mm está en la lista de FR-4 (0,4 / 0,6 / 0,8 / 1,0 / 1,2 / 1,6 / 2,0 mm).

## Contenido

| Ruta | Qué es |
|---|---|
| `plantilla/` | Proyecto plantilla FORJA de KiCad: cajetín, capas, reglas, clases de red y jobset |
| `biblioteca/` | `forja.pretty` (con `LOGO_FORJA`), símbolos propios y [la lista de piezas comprobadas](biblioteca/COMPROBACION.md) |
| `altium/` | El yunque de Altium: `Forja.SchLib`, `Forja.PcbLib` y las reglas `JLCPCB-2capas.RUL`. Para Draupnir y Telamon |

## Bitácora de fallos

| Fecha | Qué falló | Por qué | Cómo se arregló |
|---|---|---|---|
| | | | |

## Licencia

Por decidir antes de pasar a Hierro.
