# Configuraciones Bambu Studio – Bambu Lab P1S Combo (prioridad: calidad)

> **Estado: PREPARADAS, NO IMPLEMENTADAS.** Ningún archivo se ha importado todavía en Bambu Studio.
> Cuando quieras aplicarlas, sigue la sección **3. Cómo importarlas**.

- Impresora: **Bambu Lab P1S (Combo con AMS), boquilla 0.4 mm**, placa **PEI texturizada**.
- Todos los presets empiezan con **"PW"** (Pets Workshop). Así no chocan con tus presets actuales
  (`PERFIL ONE`, `ELEEGO_PLA`, etc.); **importarlos no borra ni cambia nada de lo que ya tienes**.
- Cada preset **hereda** de un perfil oficial de Bambu (o de los genéricos que trae Bambu Studio)
  y solo cambia lo necesario para dar más calidad.
- Todos los archivos se revisaron contra el código fuente de Bambu Studio: claves válidas, valores
  permitidos y perfiles base compatibles con la P1S. Todavía no se han probado en el programa real.

---

## 1. Procesos (`process/`) – cómo se imprime la pieza

| Preset | Basado en | Para qué |
|---|---|---|
| **PW Calidad Fina 0.12mm** | 0.12mm High Quality | Figuras, placas con nombre, letras pequeñas. **Ideal para el PLA Silk.** |
| **PW Calidad 0.16mm** ⭐ | 0.16mm High Quality | **El de uso diario.** Sustituye al "0.20mm Standard" que usas ahora. |
| **PW Resistente 0.20mm** | 0.20mm Strength | Piezas funcionales con carga o golpes (PETG, ABS, ASA). |
| **PW Transparente 0.20mm** | 0.20mm Standard | Piezas con filamento transparente: relleno 100 %, líneas en una sola dirección, lento. |
| **PW TPU Flexible 0.20mm** | 0.20mm Standard | Solo TPU: muy lento y sin costura bufanda. |

| Ajuste | Fina 0.12 | Calidad 0.16 | Resistente 0.20 | Transparente 0.20 | TPU 0.20 |
|---|---|---|---|---|---|
| Paredes | 3 | 3 | 4 | 2 | 3 |
| Capas sup. / inf. | 7 / 5 | 6 / 4 | 5 / 4 | 4 / 4 | 4 / 4 |
| Relleno | 15 % giroide | 20 % giroide | 30 % giroide | **100 %** zig-zag | 15 % giroide |
| Pared externa | 50 mm/s | 60 mm/s | 60 mm/s | 40 mm/s | 25 mm/s |
| Superficie superior | 100 mm/s | 120 mm/s | 120 mm/s | 50 mm/s | 25 mm/s |
| Acel. pared externa | 1500 | 2000 | 2000 | 1500 | 1000 |
| **Costura** | Alineada + **bufanda** | Alineada + **bufanda** | Alineada + **bufanda** | Alineada + **bufanda** | Alineada, sin bufanda |
| Pata de elefante | 0.15 mm | 0.15 mm | 0.15 mm | 0.15 mm | 0.15 mm |
| Borde (brim) | Auto | Auto | Auto | Auto | Sin borde |
| Soportes | Apagados (actívalos por pieza; tipo **Árbol auto**) | igual | igual | igual | igual |

---

## 2. Filamentos (`filament/`) – uno por cada filamento que tienes (y los que puedas comprar)

**Qué preset usar con tus filamentos actuales:**

| Lo que tienes ahora en Bambu Studio / en mano | Usa este preset nuevo |
|---|---|
| Rollo **PLA Silk – Silk Gold** (el de la foto) | **PW PLA Silk** |
| `ELEEGO_PLA` | **PW PLA Elegoo** |
| `ELEEGO-HIGHSPEED PETG` (los dos) | **PW PETG Elegoo Rapid-HighSpeed** |
| `MexicoMakers_PLA` y cualquier PLA sin perfil | **PW PLA MexicoMakers-Generico** |
| `SUNLU PLA+ 2.0 @BBL X1C - Copiar` | **PW PLA+ SUNLU 2.0** |
| `PETG_GENERICO` | **PW PETG Generico** |
| `FILAMENTO_TRANSPARENTE` (si es PETG) | **PW PETG Transparente** + proceso **PW Transparente** |
| `FILAMENTO_TRANSPARENTE` (si es PLA) | **PW PLA MexicoMakers-Generico** + proceso **PW Transparente** |
| Bambu PLA Basic / PLA Matte / PETG HF | **PW PLA Bambu Basic** / **PW PLA Bambu Matte** / **PW PETG Bambu HF** |
| TPU 95A (cualquier marca) | **PW TPU 95A** |
| ABS / ASA (por si compras) | **PW ABS** / **PW ASA** |

**Valores principales** (boquilla 1ª capa / resto · cama PEI 1ª capa / resto · flujo máx.):

| Preset | Basado en | Boquilla | Cama | Flujo máx. | Ventilador |
|---|---|---|---|---|---|
| PW PLA Bambu Basic | Bambu PLA Basic | 220 / 215 °C | 60 / 55 °C | 15 mm³/s | 100 % |
| PW PLA Bambu Matte | Bambu PLA Matte | 220 / 220 °C | 60 / 55 °C | 15 mm³/s | 100 % |
| **PW PLA Silk** | Generic PLA Silk | 225 / 220 °C | 60 / 55 °C | **8 mm³/s** | 100 % |
| PW PLA Elegoo | Generic PLA | 215 / 210 °C | 60 / 55 °C | 15 mm³/s | 100 % |
| PW PLA MexicoMakers-Generico | Generic PLA | 215 / 210 °C | 60 / 55 °C | 12 mm³/s | 100 % |
| PW PLA+ SUNLU 2.0 | SUNLU PLA+ 2.0 | 225 / 220 °C | 60 / 55 °C | 15 mm³/s | 100 % |
| PW PETG Bambu HF | Bambu PETG HF | 240 / 240 °C | 75 / 70 °C | 12 mm³/s | 15–40 % |
| PW PETG Elegoo Rapid-HighSpeed | Generic PETG HF | 245 / 240 °C | 75 / 70 °C | 14 mm³/s | 15–40 % |
| PW PETG Generico | Generic PETG | 240 / 235 °C | 75 / 70 °C | 10 mm³/s | 15–40 % |
| PW PETG Transparente | Bambu PETG Translucent | 250 / 250 °C | 75 / 70 °C | 6 mm³/s | 10–30 % |
| PW TPU 95A | Bambu TPU 95A HF | 230 / 225 °C | 40 / 35 °C | 4 mm³/s | 80–100 % |
| PW ABS | Bambu ABS | 260 / 260 °C | 95 / 90 °C | 12 mm³/s | 10–30 % |
| PW ASA | Generic ASA | 260 / 260 °C | 100 / 100 °C | 10 mm³/s | 10–30 % |

El **flujo máximo (velocidad volumétrica)** es el freno de calidad: aunque el proceso pida más
velocidad, la impresora nunca empuja más plástico que ese límite.

### Tu rollo de PLA Silk (Silk Gold)

- La etiqueta dice **190–230 °C**. El preset usa **220 °C** (225 °C en la 1ª capa), que es donde el
  silk saca más brillo. Si ves hilos, baja a 215 °C; si se ve opaco o se rompen las capas, sube a 225 °C.
- **Sécalo antes de usarlo: 55 °C durante 8 h** (lo dice la etiqueta). Al silk húmedo se le va el brillo.
- Usa el proceso **PW Calidad Fina 0.12mm** o **PW Calidad 0.16mm**. El brillo se ve mejor con capas finas.
- **No uses alisado (planchado)** con silk: le quita el brillo.
- El silk es más **frágil** que el PLA normal; úsalo para piezas decorativas, no funcionales.

---

## 3. Cómo importarlas

1. En Bambu Studio: **Archivo → Importar → Importar configuraciones…**
2. Selecciona **todos** los `.json` de `process/` y de `filament/` (18 archivos).
3. Aparecerán en **Ajustes de usuario** (dentro de **Personalizado**), igual que tus presets actuales.
4. Si eso no funciona, abre el perfil base que dice la tabla, cambia a mano los valores de las tablas y
   guárdalo con el mismo nombre (ver la sección 4).

---

## 4. Cómo se guarda una configuración de filamento (para cualquier filamento nuevo)

Así se hace en Bambu Studio cuando compras un filamento que no tiene perfil:

1. En **Filamentos del proyecto**, abre el menú del filamento y elige un **perfil base parecido**
   en **Ajustes del sistema**:
   - PLA normal → `Generic` → **Generic PLA**
   - PLA Silk → `Generic` → **Generic PLA Silk**
   - PETG de alta velocidad → `Generic` → **Generic PETG HF**
   - PETG normal → `Generic` → **Generic PETG**
   - TPU → `Generic` → **Generic TPU**
   - Si la marca aparece en la lista (Bambu, Polymaker, Overture, eSUN, SUNLU…), usa el perfil de esa marca.
2. Haz clic en el **icono de editar** (junto al filamento) para abrir sus ajustes.
3. Cambia **temperatura de boquilla** y **cama** según la etiqueta del rollo, y la **velocidad volumétrica máxima**.
4. Activa la **costura bufanda** (sección 5). Puedes hacerlo aquí, en el filamento.
5. Haz clic en el **icono de guardar (disquete)** → **Guardar como** → escribe un nombre claro,
   por ejemplo `Elegoo PLA Silk Oro`.
6. Quedará en **Ajustes de usuario → Personalizado**. Si tienes sesión iniciada en tu cuenta Bambu,
   se sincroniza solo con la nube y lo verás en cualquier computadora.
7. **Copia de seguridad:** Archivo → Exportar → **Exportar Preset Bundle** (guarda todos tus presets en un archivo).
   En Windows también quedan en `%APPDATA%\BambuStudio\user\<tu número>\filament\` y `...\process\`.
8. **En el AMS:** pestaña **Dispositivo** → haz clic en la ranura del AMS → elige el preset y el color.
   Ahí mismo se guarda el valor de **dinámica de flujo (K)** que salga de la calibración.

---

## 5. Costura bufanda (scarf seam) – para que no se vea la costura

La **costura bufanda** hace que el inicio y el final de cada vuelta se **traslapen en rampa**
(como un corte en diagonal), en lugar de empezar y terminar en el mismo punto. Así desaparece la
"cicatriz" vertical que deja la costura normal, sobre todo en piezas **redondas o curvas**.

**Qué ya hacen los presets PW:**

- **Procesos PW** (salvo TPU): costura **alineada** + bufanda en el **contorno externo**,
  con **aplicación inteligente** activada. En piezas con esquinas, la costura normal se esconde en una esquina.
  En piezas redondas (donde no hay esquina) se usa la bufanda. Es la mejor combinación.
  Ajustes: longitud 15 mm, inicio al 10 % de la altura de capa, 10 pasos, también en paredes internas.
- Los procesos PW tienen activado **"Anular el ajuste de costura de filamento para bufanda"**. Así la
  bufanda funciona **con cualquier filamento**, incluidos tus presets actuales (`ELEEGO_PLA`, etc.).
- **Filamentos PW** (salvo TPU): también traen la bufanda activada (contorno, 15 mm, 10 %), así que
  funciona aunque uses tus procesos viejos (`PERFIL ONE`, `perfil_1`…).

**Para activarla a mano en un preset tuyo** (en español, Bambu Studio la llama a veces
"costura de **cicatriz**" o "**Scarf**"; es lo mismo):

- Primero activa el interruptor **Avanzado** en los ajustes; si no, estas opciones no aparecen.
- **En el proceso:** pestaña **Calidad** → grupo **Costura**:
  - *Posición de la costura*: **Alineado**
  - *Anular el ajuste de costura de filamento para bufanda*: ✅
  - *Tipo de costura de cicatriz*: **Contorno**
  - *Aplicación inteligente de costura de cicatriz*: ✅
  - *Longitud de Scarf*: **15** · *Altura inicial de la Scarf*: **10 %**
  - *Junta tipo Scarf para paredes interiores*: ✅
- **En el filamento:** editar filamento → busca *Tipo de costura de cicatriz* → **Contorno**,
  *Longitud de Scarf* **15**, *Altura inicial de la Scarf* **10 %** → **Guardar**.

**Por qué el TPU no lleva bufanda:** el TPU es elástico y no responde con precisión a los cambios
de flujo de la rampa; la costura sale peor. Para TPU se usa la costura alineada normal.

---

## 6. Calibración el primer día (y con cada rollo/marca nueva)

1. **Calibración automática** al encender por primera vez (nivelación + vibraciones).
2. **Calibración → Dinámica de flujo** (método manual con patrón). La P1S no tiene lidar,
   así que este paso mejora mucho las esquinas y la costura. Guarda el resultado con el nombre del filamento.
3. **Calibración → Velocidad de flujo** (pasada 1 y 2). Guarda el valor en el preset del filamento.
4. Si un filamento nuevo no se ve bien, imprime una **torre de temperatura** (hay muchas gratis en
   MakerWorld) y quédate con la temperatura que se vea mejor. Es lo más útil para silk y marcas desconocidas.
5. **Secar** PETG (65 °C / 6 h), TPU (55 °C / 6 h) y silk (55 °C / 8 h) antes de usarlos.

---

## 7. Reglas importantes de la P1S Combo

- **El TPU NO va en el AMS** (se atasca). Va en el portarrollos trasero y en Bambu Studio eliges la
  ranura **"Ext"**. Imprime TPU solo, sin cambios de color.
- **PLA y PLA Silk:** deja la **puerta abierta o la tapa superior levantada**; con todo cerrado el PLA
  se ablanda antes de tiempo y se deforma.
- **PETG:** puerta y tapa cerradas.
- **ABS y ASA:** puerta y tapa **cerradas**, calienta la cama 5–10 min antes, y la impresora en un
  **cuarto ventilado** (sueltan gases). Usa el proceso **PW Resistente 0.20mm**.
- **PETG en placa lisa (Smooth PEI, si compras una):** usa **pegamento en barra** como separador;
  si no, el PETG puede arrancar trozos de la placa. En la PEI texturizada no hace falta.
- **No imprimas** filamentos con fibra de carbono, brillan en la oscuridad (glow) o con madera
  con la boquilla de acero inoxidable original: se desgasta. Para eso se necesita una **boquilla de acero endurecido**.
- Limpia la placa con agua y jabón de vez en cuando y no toques la superficie con los dedos.
- **Truco con el AMS:** PLA para la pieza + PETG solo en la **interfaz de soportes**. No se pegan
  bien entre sí, así que el soporte se quita fácil y deja la cara de abajo limpia.

---

## 8. Ajustes opcionales por pieza (no activados en los presets)

- **Alisado (planchado):** Calidad → Alisado → *Tipo de planchado*: "Superficies superiores". Deja las tapas planas como espejo
  (no en silk ni en piezas curvas). Añade tiempo.
- **Soportes:** actívalos solo cuando la pieza los necesite; tipo **Árbol (auto)**.
- **Capa de 0.08 mm:** para miniaturas muy finas, usa el perfil oficial "0.08mm High Quality".
- **Más resistencia:** sube las paredes a 5–6 antes de subir el relleno.
