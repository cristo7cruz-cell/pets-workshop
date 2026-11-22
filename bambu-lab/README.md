# Configuraciones Bambu Studio – Bambu Lab P1S Combo (prioridad: calidad)

> **Estado: PREPARADAS, NO IMPLEMENTADAS.** Estos archivos todavía no se han importado
> en Bambu Studio. Cuando llegue la impresora, sigue la sección "Cómo importarlas".

Hechas para **Bambu Lab P1S Combo (P1S + AMS) con boquilla de 0.4 mm** (la que trae de fábrica).
Cada preset **hereda** del perfil oficial de Bambu y solo cambia lo necesario para dar más calidad.
Así se conservan los valores probados por Bambu (retracción, g-code, flujo del AMS, etc.).

---

## 1. Qué hay en esta carpeta

### Procesos (`process/`) – cómo se imprime la pieza

| Preset | Basado en | Para qué |
|---|---|---|
| **PW Calidad Fina 0.12mm @P1S** | 0.12mm High Quality | Piezas pequeñas y con detalle: figuras, placas con nombre, letras en relieve. |
| **PW Calidad 0.16mm @P1S** ⭐ | 0.16mm High Quality | **El preset de uso diario.** Buen acabado, tiempo razonable. |
| **PW Resistente 0.20mm @P1S** | 0.20mm Strength | Piezas funcionales que van a recibir carga o golpes (sobre todo en PETG). |
| **PW TPU Flexible 0.20mm @P1S** | 0.20mm Standard | Solo para TPU: velocidades y aceleraciones bajas. |

Cambios clave respecto a Bambu:

| Ajuste | Fina 0.12 | Calidad 0.16 | Resistente 0.20 | TPU 0.20 |
|---|---|---|---|---|
| Paredes | 3 | 3 | 4 | 3 |
| Capas superiores / inferiores | 7 / 5 | 6 / 4 | 5 / 4 | 4 / 4 |
| Relleno | 15 % giroide | 20 % giroide | 30 % giroide | 15 % giroide |
| Vel. pared externa | 50 mm/s | 60 mm/s | 60 mm/s | 25 mm/s |
| Vel. superficie superior | 100 mm/s | 120 mm/s | 120 mm/s | 25 mm/s |
| Acel. pared externa | 1500 | 2000 | 2000 | 1000 |
| Generador de paredes | Arachne | Arachne | Clásico | Arachne |
| Costura | Alineada + costura biselada (scarf) externa | igual | igual | Alineada, sin bisel |
| Compensación pata de elefante | 0.15 mm | 0.15 mm | 0.15 mm | 0.15 mm |
| Borde (brim) | Automático | Automático | Automático | Sin borde |
| Soportes | Apagados (activar por pieza; tipo árbol) | igual | igual | igual |

### Filamentos (`filament/`) – temperaturas, ventilador y flujo

| Ajuste | **PW PLA Calidad** | **PW PETG Calidad** | **PW TPU 95A Calidad** |
|---|---|---|---|
| Basado en | Bambu PLA Basic | Bambu PETG HF | Bambu TPU 95A HF |
| Boquilla (1ª capa / resto) | 220 / 215 °C | 240 / 240 °C | 230 / 225 °C |
| Cama Textured PEI (1ª capa / resto) | 60 / 55 °C | 75 / 70 °C | 40 / 35 °C |
| Velocidad volumétrica máx. | 15 mm³/s | 12 mm³/s | 4 mm³/s |
| Ventilador de pieza | 100 % | 15–40 % (90 % en voladizos) | 80–100 % |
| Ventilador apagado las primeras | 1 capa | 3 capas | 1 capa |
| Tiempo mínimo por capa | 8 s | 12 s | (Bambu) |
| Retracción | (Bambu) | (Bambu) | 0.6 mm |

La **velocidad volumétrica máxima** es el freno real de calidad: aunque el proceso pida más
velocidad, la impresora nunca empuja más plástico que ese límite.

---

## 2. Cómo importarlas (cuando llegue la impresora)

1. Instalar Bambu Studio y agregar la impresora: **Bambu Lab P1S, boquilla 0.4 mm**.
2. En Bambu Studio: **Archivo → Importar → Importar configuraciones…**
3. Seleccionar los 7 archivos `.json` de `process/` y `filament/`.
4. Aparecerán en la sección **"Usuario"** de los menús de Proceso y Filamento.
5. En cada ranura del AMS, asignar el filamento "PW … Calidad" que corresponda.

Si alguno no se importa (por ejemplo, si una versión futura de Bambu Studio cambia el nombre
de un perfil base), selecciona el perfil base que aparece en la tabla, cambia a mano los valores
de las tablas de arriba y guárdalo con el mismo nombre.

---

## 3. Calibración el primer día (importante para la calidad)

Hazlo una vez por cada rollo/marca nueva:

1. **Calibración automática** de la impresora al encenderla por primera vez (nivelación + vibraciones).
2. **Calibración → Dinámica de flujo (Pressure Advance)** – método manual con patrón.
   La P1S no tiene lidar, así que este paso manual sí mejora mucho las esquinas.
3. **Calibración → Relación de flujo** (pasadas 1 y 2). Guarda el valor en el preset del filamento.
4. **Calibración → Velocidad volumétrica máxima** solo si usas filamento de otra marca.
5. Para TPU, PETG y cualquier filamento que absorba humedad: **secarlo antes** (PETG 65 °C / 6 h,
   TPU 55 °C / 6 h).

---

## 4. Reglas importantes de la P1S Combo

- **El TPU NO va en el AMS.** Se atasca. Ponlo en el portarrollos externo de la parte trasera
  y en Bambu Studio elige la ranura **"Ext"**. Imprime TPU solo (sin cambios de color).
- **PETG en una placa lisa (Smooth PEI, si compras una):** usar **pegamento en barra** como
  separador; el PETG se pega tanto que puede arrancar trozos de la placa.
  En la **Textured PEI** (la que viene con la P1S) no hace falta.
- **PLA:** con la puerta y la tapa cerradas el PLA se puede deformar; deja la **puerta abierta o
  la tapa superior levantada** al imprimir PLA.
- **PETG:** puerta cerrada, tapa cerrada.
- Limpiar la placa con agua y jabón de vez en cuando (no tocar la superficie con los dedos).
- Mezclar PLA y PETG en la misma pieza con el AMS solo para la **interfaz de soportes**
  (PETG no se pega bien al PLA, por eso sirve como soporte fácil de retirar).

---

## 5. Ajustes opcionales por pieza (no están activados en los presets)

- **Planchado (Ironing):** Calidad → Planchado → "Superficie superior". Deja tapas planas
  como espejo, pero añade tiempo. Úsalo solo en piezas con tapa superior plana.
- **Soportes:** activarlos solo cuando la pieza los necesite; tipo **Árbol (auto)**.
- **Capa de 0.08 mm:** para miniaturas muy finas, usa el perfil oficial "0.08mm High Quality".
- **Más resistencia:** subir paredes a 5–6 antes que subir el relleno.
