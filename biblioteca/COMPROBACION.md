# Piezas comprobadas

> La trampa de Akmon: fiarse de una huella descargada. Cada fila se cierra con la fecha en que la imprimiste a 1:1 y la pieza encajó.

| Pieza | Para | Encapsulado (lo eliges tú) | Hoja de datos o medida | Símbolo | Huella | Comprobada a 1:1 |
|---|---|---|---|---|---|---|
| LOGO_FORJA | todas | 6 / 8 / 10 mm | `FORJA\Concepto` | — | | |
| Raspberry Pi Pico | Draupnir, Narthex | Agujero pasante, sobre zócalos | pico-datasheet.pdf, figura 3 (pág. 6): filas a 17,78 mm, 20 pads a 2,54 mm (pin 1 a 20: 48,26 mm). Pad 1,6 / taladro 1,0 mm | `MCU_Module:RaspberryPi_Pico` | `Module:RaspberryPi_Pico_Common_THT` | |
| Conector de entrada de 2 × 8 | Draupnir | Tira de pines, paso 2,54 mm | Tira de pines de 0,64 mm, paso 2,54 mm. Pad 1,7 / taladro 1,0 mm (huella oficial) | `Connector_Generic:Conn_02x08_Odd_Even` | `Connector_PinHeader_2.54mm:PinHeader_2x08_P2.54mm_Vertical` | |
| Resistencia de 1 kΩ | Draupnir | Axial, patas a 10,16 mm, montadas a 2,54 mm una de otra | Cuerpo de 6,3 × 2,5 mm (DIN 0207). Parte de la oficial `Resistor_THT:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal`: pad 1,6 / taladro 0,8 mm; patio recortado a 2,5 mm de alto y serigrafía de 0,20 mm | `Device:R` | `forja:R_Axial_DIN0207_P10.16mm_Compacta` | |
| LED de 3 mm | Draupnir | Agujero pasante, patas a 2,54 mm | LED de 3 mm, patas a 2,54 mm. Pad 1,8 / taladro 0,9 mm (huella oficial) | `Device:LED` | `LED_THT:LED_D3.0mm` | |
| Punto de prueba | Draupnir | Pad de 2,0 mm | Punto de prueba de hilo. Pad 2,0 / taladro 1,0 mm (huella oficial) | `Connector:TestPoint` | `TestPoint:TestPoint_THTPad_D2.0mm_Drill1.0mm` | |
| Taladro de montaje M3 | Draupnir | Taladro con pad, tornillo M3 | Pad 6,4 / taladro 3,2 mm (huella oficial) | `Mechanical:MountingHole_Pad` | `MountingHole:MountingHole_3.2mm_M3_Pad` | |
| Borna de tornillo | Narthex | | | | | |
| Placa disparadora USB-C PD (módulo) | Narthex | | medida a mano | | | |
| XL4015 (módulo) | Narthex | | medida a mano | | | |
| INA226 (módulo) | Narthex | | medida a mano | | | |
| Fusible rearmable de 2 A | Narthex | | | | | |
| TVS SMBJ15A (huella sin montar) | Narthex | SMB | LCSC C435932 | | | |

Dónde están las piezas de Draupnir, según la herramienta:

- **En KiCad:** salen de la biblioteca oficial, comprobadas contra la hoja de datos, salvo la resistencia. Esa es propia: `forja.pretty/R_Axial_DIN0207_P10.16mm_Compacta`, con el patio ajustado al cuerpo (2,5 mm) para poder montarlas a 2,54 mm sin que el DRC dé solape de patios.
- **En Altium:** las cinco están dibujadas en `altium/Forja.SchLib` y `altium/Forja.PcbLib`.

Las de Narthex irán en `forja.pretty`, en diciembre.
