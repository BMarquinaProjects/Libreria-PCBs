# plantilla

Proyecto plantilla FORJA de KiCad 10 (10 nov). Lo que sale de aquí, cada proyecto nuevo lo hereda.

| Qué | Dónde se configura | Comprobado |
|---|---|---|
| Cajetín FORJA con variables `${TITLE}`, `${REVISION}`, `${ISSUE_DATE}` | Editor de cajetines | |
| 2 capas, 1,6 mm | Configuración de la placa › Capas | |
| Restricciones de la tabla del README | Configuración de la placa › Restricciones | |
| Clases de red Default y Potencia | Configuración de la placa › Clases de red | |
| Tabla de huellas con `${AKMON}/biblioteca/forja.pretty` | Preferencias › Gestionar bibliotecas de huellas | |
| Jobset de salidas (Gerbers, taladros, BOM) | `*.kicad_jobset` | |

**Instalación:** Preferencias › Configurar rutas. `KICAD_USER_TEMPLATE_DIR` apunta a esta carpeta y `AKMON` a la raíz del repositorio.

**Prueba:** un proyecto nuevo desde la plantilla, con un contorno de 50 × 50 mm, pasa el DRC con 0 errores.
