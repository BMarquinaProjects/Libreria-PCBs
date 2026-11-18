# altium

El yunque de Altium. Nace con Draupnir, si se hace en Altium, o con Telamon. Solo las piezas que se usan de verdad. Los pasos citados son los de `draupnir\guia-altium.html`.

| Qué | Archivo | Paso de la guía de Draupnir | Comprobado |
|---|---|---|---|
| Reglas de JLCPCB, con los valores de la tabla del README | `JLCPCB-2capas.RUL` | 4.2 | |
| Biblioteca de símbolos | `Forja.SchLib` | 0.4 y etapa 2 | |
| Biblioteca de huellas | `Forja.PcbLib` | 0.4 y etapa 2 | |
| Flujo de salida: Gerbers y taladros aceptados por el visor de JLCPCB | ajustes del paso 6.1 y 6.2 | 6.4 | |
| Plantilla de hoja con cajetín FORJA | por hacer, con Telamon | | |
| Logo FORJA importado | por hacer, con Telamon | | |

## Piezas

| Símbolo | Huella | Pad / taladro | De dónde salen las medidas | Comprobada a 1:1 |
|---|---|---|---|---|
| `RPi_Pico` | `PICO_THT` | 1,7 / 1,0 mm | Hoja de datos de la Pico, figura 3 (pág. 6) | |
| `R` | `RES_AXIAL_P10.16` | 1,6 / 0,8 mm | Resistencia axial de 1/4 W, patas a 10,16 mm | |
| `HDR_2x8` | `HDR_2x8_P2.54` | 1,7 / 1,0 mm | Tira de pines de 0,64 mm, paso 2,54 mm | |
| `LED` | `LED_3MM` | 1,6 / 0,9 mm | LED de 3 mm, patas a 2,54 mm | |
| `TP` | `TP_THT` | 2,0 / 1,0 mm | Punto de prueba de hilo | |

**Cómo se usa en un proyecto nuevo:** clic derecho en el proyecto, *Add Existing to Project*, y elige las dos bibliotecas. En *Design › Rules*, clic derecho, *Import Rules*, y elige el `.RUL`.

Altium guarda historial, registros y vistas previas junto a cada archivo: el `.gitignore` los deja fuera.

**Prueba:** Draupnir pasa el DRC de Altium con cero fallos usando solo estas bibliotecas y estas reglas.
