# Presets Bambu Studio – Bambu Lab P1S Combo (calidad tipo porcelana)

Impresora: **Bambu Lab P1S (Combo con AMS)**, placa **PEI texturizada**, boquilla **0.4**
(y presets opcionales para boquilla **0.2**).

## Cómo funciona: elige 2 cosas

En Bambu Studio cada impresión usa **dos** ajustes:

| Qué eliges | Dónde | Qué controla |
|---|---|---|
| **Proceso** = *qué tipo de pieza vas a hacer* | Menú **Proceso** | Altura de capa, paredes, relleno, **planchado**, costura, velocidad |
| **Filamento** = *qué rollo tienes puesto* | **Filamentos del proyecto** / ranura del AMS | **Temperaturas**, ventilador, flujo máximo |

Los procesos están **numerados del 01 al 12** para que salgan en orden en el menú.
Los filamentos tienen **el nombre del rollo**. No hay que combinarlos a mano: el filamento pone
la temperatura correcta y el proceso pone la calidad.

---

## Recetas rápidas (necesidad → qué seleccionar)

| Quiero hacer… | Proceso | Filamento |
|---|---|---|
| Figura o pieza decorativa **tipo porcelana** | **01 Porcelana 0.12 - Decorativa** | **PLA Bambu Matte - Porcelana** (blanco = porcelana) |
| Pieza normal, bonita y sin tardar tanto | **02 Uso Diario 0.16 - Planchado** | El PLA o PETG que tengas |
| Pieza dorada brillante | **01 Porcelana 0.12** o **02 Uso Diario 0.16** | **PLA Silk Dorado** |
| **Tapa** con logo o letras | **03 Tapa con Logo 0.12** | PLA (2 colores con el AMS) |
| Caja con logo **grabado en los lados** | **04 Laterales con Logo 0.08** | PLA o PETG |
| Pieza que aguante peso o golpes | **05 Resistente 0.20 - Funcional** | **PETG** (Elegoo Rapid / Genérico / Bambu HF) |
| **Pantalla de lámpara** de una sola pared (forma de jarrón) | **06 Lampara Jarron - Pantalla** | **PETG Translucido - Lamparas** |
| **Lámpara** con formas o piezas cerradas | **07 Lampara Difusa - 2 Paredes** | **PETG Translucido - Lamparas** |
| Pieza **transparente** sólida | **08 Transparente Solida 0.20** | **PETG Translucido** o **PLA Translucido** |
| Miniatura con boquilla normal | **09 Miniatura 0.08 (boquilla 0.4)** | **PLA Bambu Matte - Porcelana** (gris) |
| Miniatura muy chica (1:100, 1:144) | **10 Miniatura 0.06 (boquilla 0.2)** | **… (boquilla 0.2)** |
| Pieza chica con mucho detalle | **11 Detalle 0.10 (boquilla 0.2)** | **… (boquilla 0.2)** |
| Pieza flexible | **12 TPU Flexible 0.20** | **TPU 95A - Solo Ext** |

---

## 1. Procesos (`process/`)

**Todos llevan planchado** (*Alisado* → *Tipo de planchado: Superficies superiores*), excepto
**06** (en modo jarrón no hay tapas que planchar) y **12** (el TPU se embarra al planchar).
El planchado está más fino que el de Bambu: líneas a **0.12 mm** (0.08 mm en boquilla 0.2),
flujo **10 %** y velocidad **25 mm/s**.

Todos llevan también la **costura bufanda** (ver sección 4), excepto 06 y 12.

| Proceso | Capa | Paredes | Relleno | Pared externa | Notas |
|---|---|---|---|---|---|
| **01 Porcelana 0.12 - Decorativa** | 0.12 | 3 | 15 % | 45 mm/s | 8 capas arriba para tapas perfectas; aceleración baja |
| **02 Uso Diario 0.16 - Planchado** | 0.16 | 3 | 20 % | 60 mm/s | Equilibrio calidad / tiempo |
| **03 Tapa con Logo 0.12** | 0.12 | 3 | 15 % | 50 mm/s | Costura atrás; 8 capas arriba |
| **04 Laterales con Logo 0.08** | 0.08 | 3 | 15 % | 40 mm/s | Capas muy finas para logos en paredes; costura atrás |
| **05 Resistente 0.20 - Funcional** | 0.20 | 4 | 30 % | 60 mm/s | Pared clásica, más resistente |
| **06 Lampara Jarron - Pantalla** | 0.20 | 1 | 0 % | 40 mm/s | **Modo jarrón en espiral**: sin costura; línea de 0.5 mm, más firme |
| **07 Lampara Difusa - 2 Paredes** | 0.20 | 2 | **0 %** | 40 mm/s | Hueca por dentro: la luz pasa pareja, sin sombras del relleno |
| **08 Transparente Solida 0.20** | 0.20 | 2 | **100 %** | 40 mm/s | Líneas en una dirección: lo más transparente posible |
| **09 Miniatura 0.08 (boquilla 0.4)** | 0.08 | 2 | 15 % | 30 mm/s | Soportes de árbol activados |
| **10 Miniatura 0.06 (boquilla 0.2)** | 0.06 | 3 | 15 % | 30 mm/s | Solo con boquilla 0.2; soportes activados |
| **11 Detalle 0.10 (boquilla 0.2)** | 0.10 | 3 | 15 % | 40 mm/s | Solo con boquilla 0.2 |
| **12 TPU Flexible 0.20** | 0.20 | 3 | 15 % | 25 mm/s | Sin planchado, sin bufanda, sin borde |

Todos usan pared externa **precisa**, paredes **Arachne** (excepto 05), compensación de pata de
elefante de **0.15 mm** y borde automático. Los soportes van **apagados**, menos en las miniaturas:
actívalos por pieza (tipo **Árbol auto**).

---

## 2. Filamentos (`filament/`)

| Filamento | Boquilla (1ª capa / resto) | Cama PEI (1ª / resto) | Flujo máx. | Ventilador | Vent. al planchar |
|---|---|---|---|---|---|
| **PLA Bambu Basic** | 220 / 215 °C | 60 / 55 °C | 15 mm³/s | 100 % | 50 % |
| **PLA Bambu Matte - Porcelana** | 220 / 220 °C | 60 / 55 °C | 15 mm³/s | 100 % | 50 % |
| **PLA Silk Dorado** | 225 / 220 °C | 60 / 55 °C | 8 mm³/s | 100 % | 50 % |
| **PLA Elegoo** | 215 / 210 °C | 60 / 55 °C | 15 mm³/s | 100 % | 50 % |
| **PLA MexicoMakers - Generico** | 215 / 210 °C | 60 / 55 °C | 12 mm³/s | 100 % | 50 % |
| **PLA+ SUNLU 2.0** | 225 / 220 °C | 60 / 55 °C | 15 mm³/s | 100 % | 50 % |
| **PLA Translucido - Lamparas** | 230 / 225 °C | 60 / 55 °C | 8 mm³/s | 80–100 % | 50 % |
| **PETG Bambu HF** | 240 / 240 °C | 75 / 70 °C | 12 mm³/s | 15–40 % | 20 % |
| **PETG Elegoo Rapid** | 245 / 240 °C | 75 / 70 °C | 14 mm³/s | 15–40 % | 20 % |
| **PETG Generico** | 240 / 235 °C | 75 / 70 °C | 10 mm³/s | 15–40 % | 20 % |
| **PETG Translucido - Lamparas** | 250 / 250 °C | 75 / 70 °C | 6 mm³/s | 10–30 % | 20 % |
| **TPU 95A - Solo Ext** | 230 / 225 °C | 40 / 35 °C | 4 mm³/s | 80–100 % | – |
| **ABS** | 260 / 260 °C | 95 / 90 °C | 12 mm³/s | 10–30 % | 10 % |
| **ASA** | 260 / 260 °C | 100 / 100 °C | 10 mm³/s | 10–30 % | 10 % |
| **PLA Bambu Basic (boquilla 0.2)** | 220 / 215 °C | 60 / 55 °C | 2 mm³/s | 100 % | 50 % |
| **PLA Bambu Matte (boquilla 0.2)** | 220 / 220 °C | 60 / 55 °C | 2 mm³/s | 100 % | 50 % |
| **PLA Generico (boquilla 0.2)** | 215 / 210 °C | 60 / 55 °C | 1.6 mm³/s | 100 % | 50 % |
| **PETG Generico (boquilla 0.2)** | 245 / 240 °C | 75 / 70 °C | 1 mm³/s | 15–40 % | 20 % |

**Por qué estos valores:**
- **Flujo máximo bajo:** frena la impresora para que cada capa se asiente bien. Es el ajuste que más
  influye en la calidad de las paredes.
- **Ventilador al planchar más bajo:** la plancha alisa mejor el plástico si está un poco más caliente.
- **PLA Silk:** 220 °C y lento es donde saca más brillo. Su etiqueta dice 190–230 °C. **Sécalo a 55 °C
  durante 8 h** antes de usarlo. El planchado deja las tapas un poco menos brillantes que los lados.
  Si quieres todo brillante, quita el planchado en esa pieza (Calidad → Alisado → *Ninguno*).
- **Translúcidos:** más temperatura y menos velocidad = capas mejor fundidas = pasa más luz y se ve
  más limpio.
- **El TPU va siempre en la ranura Ext**, nunca en el AMS.
- **Elegoo, MexicoMakers y SUNLU con boquilla 0.2:** usa **PLA Generico (boquilla 0.2)**.

---

## 3. Lámparas con filamento translúcido

- **Usa PETG translúcido para lámparas**, no PLA. El PLA se empieza a deformar a ~55 °C y el PETG
  aguanta ~75 °C.
- **Usa solo focos LED.** Los focos incandescentes o halógenos calientan demasiado y pueden deformar
  o quemar la pieza.
- **06 Lampara Jarron - Pantalla:** para pantallas de **una sola pared** (cilindros, conos, formas
  onduladas). La impresora sube en espiral sin parar, así que **no hay costura** y la luz sale pareja.
  Solo funciona con piezas de **una sola pieza y abiertas por arriba**.
- **07 Lampara Difusa - 2 Paredes:** para lámparas con formas cerradas, esferas o figuras. Van
  **huecas por dentro** (relleno 0 %) para que el relleno no haga sombras.
- **08 Transparente Solida 0.20:** para piezas **macizas y transparentes** (prismas, bloques). Relleno
  al 100 % con todas las líneas en la misma dirección.
- La pieza con translúcido **nunca queda transparente como vidrio**: queda como vidrio esmerilado.
  Con más temperatura y menos velocidad (ya incluido) se ve más clara.
- Puedes guardar el **PLA Translucido** para piezas decorativas sin foco o con LED de poca potencia.

---

## 4. Para que no se vea "en escalones"

- **Las capas siempre se notan un poco en curvas y en superficies inclinadas.** Es como funcionan
  las impresoras de filamento. El planchado solo alisa las **superficies planas de arriba**.
- **Así se reducen al mínimo:**
  1. Usa capa fina: **01 Porcelana 0.12** o **04 Laterales con Logo 0.08**.
  2. Selecciona la pieza → icono **Altura de capa variable** (en la barra de herramientas sobre la vista 3D) →
     **Adaptativo** → **Alisado**. Bambu Studio pone capas más finas solo en las curvas y más gruesas en
     lo recto. Se hace con cada pieza (no se puede guardar en el preset) y tarda 5 segundos.
  3. Usa **PLA mate** (*PLA Bambu Matte - Porcelana*): el acabado mate esconde las líneas de capa. En
     blanco parece porcelana.
  4. Orienta la pieza para que las curvas más visibles queden **de lado** y no "acostadas".
- **Si quieres que parezca porcelana de verdad:** lija con grano 400 → 800 → 1500 y aplica primer en
  aerosol (relleno de imprimación) y pintura brillante.

---

## 5. Costura bufanda (que no se vea la costura)

La costura bufanda empalma el inicio y el final de cada vuelta **en rampa** y quita la "cicatriz"
vertical. Los procesos 01–05 y 07–11 la tienen activada en modo **inteligente**:
- En piezas con esquinas, la costura normal se esconde en una esquina.
- En piezas redondas se usa la bufanda.

Si lo quieres ajustar a mano (activa el interruptor **Avanzado**), está en la pestaña **Calidad** →
grupo **Costura**. En español Bambu Studio la llama a veces "costura de **cicatriz**" o "**Scarf**":
- *Anular el ajuste de costura de filamento para bufanda*: ✅
- *Tipo de costura de cicatriz*: **Contorno**
- *Aplicación inteligente de costura de cicatriz*: ✅
- *Longitud de Scarf*: **15**
- *Altura inicial de la Scarf*: **10 %**

---

## 6. Cómo importarlas (y quitar las anteriores)

1. **Borra los presets viejos** que empiezan con **"PW"**:
   - **Proceso:** elige el preset → icono de **papelera** junto al disquete → **Sí**.
   - **Filamento:** elige el preset → icono de **editar** → **papelera** (*Borrar Perfil*) → **Sí**.
   - Si no aparece la papelera, cambia primero a otro preset: no se puede borrar el que está en uso.
2. **Archivo → Importar → Importar configuraciones** → carpeta `process` → **Ctrl + A** → **Abrir**.
3. Repite con la carpeta `filament`.
4. Deben quedar **12 procesos** (01–12) y **18 filamentos** en **Ajustes de usuario**.
   Los de **boquilla 0.2** solo se ven cuando eliges la impresora con **boquilla 0.2**.
5. Se suben solos a tu cuenta de **Bambu Cloud**.

---

## 7. Calibración (una vez por cada rollo)

1. **Calibración → Dinámica de flujo**:
   - Configúrala así: método **Manual**, placa **PEI texturizada**, el filamento del rollo y su ranura del AMS.
   - Imprime la prueba y elige la línea más pareja.
   - Guarda el resultado y asígnalo a la ranura en **Dispositivo**.
2. **Calibración → Velocidad de flujo**:
   - Haz la pasada 1 y la pasada 2, y elige el cuadrito más liso.
   - Guarda el filamento (disquete).
3. **Velocidad volumétrica máxima**: sáltala, ya está ajustada.
4. **En la impresora**, una sola vez: Configuración → Calibración → nivelación, vibraciones y ruido del motor.
5. **Secado:** PETG 65 °C / 6 h · TPU 55 °C / 6 h · PLA Silk 55 °C / 8 h.

---

## 8. Tapas y logos en los laterales

**Tapa con logo – el mejor acabado (logo boca abajo):**
1. Diseña el logo **embutido al ras** de la tapa, con 0.4–0.6 mm de grosor.
2. Voltea la tapa para que la cara del logo quede **contra la placa**.
3. Asigna los colores: clic derecho en el logo → *Cambiar el filamento* (o **Pintura de colores**).
4. Proceso **01 Porcelana 0.12**. La cara copia la textura de la placa: textura fina mate con PEI
   texturizada, brillante con placa lisa.

**Tapa con logo hacia arriba:**
1. Proceso **03 Tapa con Logo 0.12**: el planchado deja la tapa y el logo lisos.
2. Usa un logo en relieve o embutido de 0.36–0.6 mm.

**Logo en una pared lateral:**
1. Proceso **04 Laterales con Logo 0.08**. La costura va **atrás** (en el menú puede salir como
   *Volver*), así que no pongas el logo en la cara trasera. También puedes usar **Pintar la costura**.
2. **Para ahorrar tiempo:** clic derecho en la pieza → **Añadir rango de altura** → 0.08 mm solo en la zona
   del logo, y el resto con 02.
3. **Grabado (hundido)** se ve mejor que en relieve en paredes verticales.

**Medidas mínimas de diseño:**

| Detalle | Boquilla 0.4 | Boquilla 0.2 |
|---|---|---|
| Grosor de línea del logo / letra | 0.5 mm | 0.25 mm |
| Altura de letra (fuente gruesa) | 4 mm | 2 mm |
| Separación entre líneas | 0.4 mm | 0.2 mm |
| Profundidad / relieve | 0.4–0.6 mm | 0.2–0.4 mm |

---

## 9. Miniaturas (cualquier escala)

Fíjate en **el detalle más pequeño**, no en la escala:

| Detalle más pequeño | Usa |
|---|---|
| Mayor a 1 mm | **01 Porcelana 0.12** (boquilla 0.4) |
| 0.5 – 1 mm (1:35, 1:48) | **09 Miniatura 0.08 (boquilla 0.4)** |
| 0.25 – 0.5 mm (1:72, 1:87) | **11 Detalle 0.10 (boquilla 0.2)** |
| Menor a 0.25 mm (1:100, 1:144) | **10 Miniatura 0.06 (boquilla 0.2)** |

**Boquilla 0.2:**
- Compra el **hotend de 0.2 mm para P1S**.
- Pon el diámetro **0.2** en la pantalla de la impresora y en Bambu Studio.
- Usa los filamentos que dicen **(boquilla 0.2)**.
- No uses TPU, filamentos con carga (carbono, madera, glow) ni filamento húmedo.

**Consejos para miniaturas:**
- El **PLA mate gris** es el que mejor muestra el detalle.
- Inclina la figura **30–45°** hacia atrás para que la cara no lleve soportes.
- Imprime varias a la vez: cada capa tiene más tiempo para enfriarse y los detalles salen más definidos.

---

## 10. Reglas de la P1S Combo

- **PLA:** puerta abierta o tapa levantada.
- **PETG:** puerta cerrada.
- **ABS / ASA:** puerta cerrada, proceso **05 Resistente** y cuarto ventilado.
- **TPU:** siempre en la ranura **Ext**, nunca en el AMS.
- **PETG en placa lisa:** usa pegamento en barra para que no arranque trozos de la placa.
- **Filamentos con carbono, madera o glow:** solo con boquilla de **acero endurecido**.
- **AMS:** no mezcles PLA y PETG en la misma pieza (solo como interfaz de soportes).
  Si cambias de un color oscuro a uno claro, sube los **volúmenes de purga** a ×1.2–1.5.
