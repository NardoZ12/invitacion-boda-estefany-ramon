# 🎨 Guía de Personalización - Invitación de Boda

Documento detallado sobre cómo personalizar la invitación según tus necesidades.

---

## 📝 Tabla de Contenidos

1. [Editar Información Básica](#editar-información-básica)
2. [Agregar/Modificar Invitados](#agregarmodificar-invitados)
3. [Cambiar Música](#cambiar-música)
4. [Personalizar Colores](#personalizar-colores)
5. [Modificar Textos](#modificar-textos)
6. [Ejemplos Prácticos](#ejemplos-prácticos)

---

## 📅 Editar Información Básica

### Cambiar Fecha del Evento

**Ubicación:** Línea ~463 en `index.html`

```javascript
// ANTES:
const eventDate = new Date('2026-11-27T16:30:00').getTime();

// DESPUÉS (para cambiar a una fecha diferente):
const eventDate = new Date('2025-06-15T18:00:00').getTime();
```

**Formato:** `YYYY-MM-DDTHH:mm:ss`
- Año-Mes-Día + T + Hora:Minuto:Segundo

### Cambiar Nombre de los Novios

**Ubicación:** Líneas 256, 268 en `index.html`

```html
<!-- ANTES: -->
<h1>Estefany <span class="ampersand">&</span> Ramón</h1>

<!-- DESPUÉS: -->
<h1>María <span class="ampersand">&</span> Juan</h1>
```

Búscalo 2 veces en el archivo (una en pantalla de bienvenida, otra en hero).

### Cambiar Frase Romántica

**Ubicación:** Línea 269

```html
<!-- ANTES: -->
<p>"El amor es la poesía de los sentidos"</p>

<!-- DESPUÉS: -->
<p>"Dos almas, un corazón, un destino"</p>
```

### Cambiar Hora del Evento

**Ubicación:** Línea ~400

```html
<!-- ANTES: -->
<p>4:30 PM</p>

<!-- DESPUÉS: -->
<p>6:00 PM</p>
```

### Cambiar Día de la Semana

**Ubicación:** Línea ~395

```html
<!-- ANTES: -->
<p>Viernes</p>

<!-- DESPUÉS: -->
<p>Sábado</p>
```

---

## 👥 Agregar/Modificar Invitados

### Localizar la Base de Datos

**Ubicación:** Línea ~470-520

```javascript
const guestsData = {
    'carolin-familia': {
        names: ['Carolin Rodríguez', 'Adriana Rodríguez', 'Génesis de Jesús'],
        passes: 3
    },
    // ... más invitados
};
```

### Agregar Nuevo Grupo de Invitados

Añade una entrada nueva antes de la última llave `}`:

```javascript
'nuevo-id': {
    names: ['Nombre Invitado 1', 'Nombre Invitado 2'],
    passes: 2
},
```

### Ejemplo: Agregar a la Familia García

```javascript
'familia-garcia': {
    names: ['Carlos García', 'María García', 'Laura García'],
    passes: 3
},
```

### Modificar Invitados Existentes

**Antes:**
```javascript
'rosa': {
    names: ['Rosa Corona'],
    passes: 1
},
```

**Después (si Rosa quiere llevar a un acompañante):**
```javascript
'rosa': {
    names: ['Rosa Corona', 'José Antonio'],
    passes: 2
},
```

### Eliminar un Grupo de Invitados

Simplemente borra la entrada completa:

```javascript
// Elimina estas líneas:
'rosa': {
    names: ['Rosa Corona'],
    passes: 1
},
```

### Reglas Importantes para IDs

- ✅ Usa minúsculas y guiones: `familia-rodriguez`
- ✅ Sin espacios ni caracteres especiales
- ✅ Debe ser único (no repetido)
- ✅ El ID debe coincidir en el URL: `?guest=familia-rodriguez`

---

## 🎵 Cambiar Música

### Ubicación: Línea ~515

```html
<!-- ANTES: -->
<audio id="backgroundMusic" loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<!-- DESPUÉS: -->
<audio id="backgroundMusic" loop>
    <source src="https://tu-url-de-musica.com/cancion-boda.mp3" type="audio/mpeg">
</audio>
```

### Dónde Encontrar Música Libre de Derechos

1. **Pixabay Music:** https://pixabay.com/es/music/
2. **Free Music Archive:** https://freemusicarchive.org/
3. **Incompetech:** https://incompetech.com/
4. **YouTube Audio Library:** https://www.youtube.com/audiolibrary

### Cambiar Volumen de la Música

**Ubicación:** Línea ~503

```javascript
// ANTES (30%):
audio.volume = 0.3;

// DESPUÉS (50%):
audio.volume = 0.5;

// DESPUÉS (70%):
audio.volume = 0.7;
```

Usa valores entre 0 (silencio) y 1 (máximo volumen).

---

## 🎨 Personalizar Colores

### Ubicación: Líneas 8-15

```css
:root {
    --color-primary: #f5f1ed;      /* Fondo principal */
    --color-secondary: #f9f7f4;    /* Fondo secundario */
    --color-accent: #d4af37;       /* Dorado/Acento */
    --color-text: #3a3a3a;         /* Texto oscuro */
    --color-light-text: #6b6b6b;   /* Texto claro */
    --color-white: #ffffff;        /* Blanco puro */
}
```

### Ejemplos de Cambios

#### Tema Elegante (Actual)
```css
--color-primary: #f5f1ed;      /* Marfil suave */
--color-accent: #d4af37;       /* Dorado elegante */
--color-text: #3a3a3a;         /* Gris oscuro */
```

#### Tema Romántico (Rosas y Plata)
```css
--color-primary: #ffe4e1;      /* Rosa muy suave */
--color-accent: #c0c0c0;       /* Plata */
--color-text: #4a1f2f;         /* Rojo vino oscuro */
```

#### Tema Tropical (Turquesa y Oro)
```css
--color-primary: #e0f7f6;      /* Turquesa muy suave */
--color-accent: #ff9800;       /* Oro anaranjado */
--color-text: #00695c;         /* Turquesa oscuro */
```

#### Tema Clásico (Negro y Oro)
```css
--color-primary: #fafafa;      /* Gris muy claro */
--color-accent: #ffd700;       /* Oro puro */
--color-text: #000000;         /* Negro puro */
```

### Herramientas para Elegir Colores

- **Coolors.co:** https://coolors.co/
- **Color-hex.com:** https://www.color-hex.com/
- **Adobe Color:** https://color.adobe.com/

---

## ✏️ Modificar Textos

### Saludo de Bienvenida (Pantalla de Entrada)

**Ubicación:** Línea ~257

```html
<!-- ANTES: -->
<p>Nos encantaría que fueras parte de nuestro gran día</p>

<!-- DESPUÉS: -->
<p>Tu presencia es lo más importante para nosotros</p>
```

### Encabezado Personalizado

**Ubicación:** Línea ~276

```html
<!-- ANTES: -->
<h2>Nos encantaría que nos acompañes, <span class="guest-name" id="guestName">Estimado Invitado</span></h2>

<!-- DESPUÉS: -->
<h2>¡Queremos que celebres con nosotros, <span class="guest-name" id="guestName">Estimado Invitado</span>!</h2>
```

### Etiqueta de Pases

**Ubicación:** Línea ~280

```html
<!-- ANTES: -->
<p>Pases reservados para ti:</p>

<!-- DESPUÉS: -->
<p>Te hemos reservado:</p>
```

### Indicación de Vestimenta

**Ubicación:** Línea ~378

```html
<!-- ANTES: -->
<p style="text-align: center; margin-bottom: 2rem; color: var(--color-light-text);">Formal / Elegante</p>

<!-- DESPUÉS: -->
<p style="text-align: center; margin-bottom: 2rem; color: var(--color-light-text);">White Tie Optional</p>
```

### Texto del Botón RSVP

**Ubicación:** Línea ~431

```html
<!-- ANTES: -->
<a href="#" class="rsvp-btn" id="rsvpBtn">Confirmar Asistencia</a>

<!-- DESPUÉS: -->
<a href="#" class="rsvp-btn" id="rsvpBtn">Sí, Confirmo Mi Asistencia</a>
```

### Footer

**Ubicación:** Líneas ~440-444

```html
<!-- ANTES: -->
<p>Viernes, 27 de Noviembre de 2026</p>
<p>Estefany & Ramón</p>
<p style="margin-top: 1rem; font-size: 0.9rem;">Gracias por ser parte de nuestro grande día ✨</p>

<!-- DESPUÉS: -->
<p>Sábado, 15 de Junio de 2025</p>
<p>María & Juan</p>
<p style="margin-top: 1rem; font-size: 0.9rem;">Con amor y gratitud ✨</p>
```

---

## 📌 Ejemplos Prácticos

### Ejemplo 1: Crear una Boda de Verano

1. **Cambiar Fecha:**
   ```javascript
   const eventDate = new Date('2025-07-20T19:00:00').getTime();
   ```

2. **Cambiar Colores:**
   ```css
   --color-primary: #fff8e1;      /* Amarillo muy suave */
   --color-accent: #ff9100;       /* Naranja */
   --color-text: #e65100;         /* Naranja oscuro */
   ```

3. **Cambiar Frase:**
   ```html
   <p>"Como el sol, nuestro amor ilumina cada día"</p>
   ```

4. **Cambiar Música:**
   - Busca en Pixabay: "summer wedding upbeat"

### Ejemplo 2: Agregar Nueva Familia de Invitados

1. **Abre `index.html`**

2. **Busca la línea ~470** (donde está `guestsData`)

3. **Añade antes de la última llave:**
   ```javascript
   'familia-nueva': {
       names: ['Pedro López', 'Sandra López', 'Andrés López'],
       passes: 3
   },
   ```

4. **Guarda el archivo**

5. **El enlace será:**
   ```
   https://tudominio.com/index.html?guest=familia-nueva
   ```

### Ejemplo 3: Cambiar Tema Completamente

Para un evento corporativo/profesional:

```css
/* Cambiar a tonos azules y plateados */
--color-primary: #f0f4f8;      /* Azul muy claro */
--color-accent: #1976d2;       /* Azul profesional */
--color-text: #1a237e;         /* Azul muy oscuro */
```

```javascript
/* Cambiar a música clásica seria */
<source src="https://ejemplo.com/musica-clasica.mp3">
```

```html
<!-- Cambiar a "Formal / Business Attire" -->
<p>Formal / Atire de Negocio</p>
```

---

## 🔍 Checklist de Personalización

- [ ] Cambiar nombres de novios
- [ ] Actualizar fecha y hora del evento
- [ ] Personalizar frase romántica
- [ ] Ajustar colores según tema
- [ ] Cargar nueva música de fondo
- [ ] Verificar/agregar todos los invitados
- [ ] Cambiar textos de bienvenida
- [ ] Actualizar información de vestimenta
- [ ] Probar en móvil
- [ ] Probar diferentes navegadores
- [ ] Subir a hosting
- [ ] Compartir enlaces con invitados

---

## ⚠️ Errores Comunes

### Error: "Los invitados no ven sus nombres"

**Causa:** El ID en la URL no coincide exactamente con el de la base de datos.

**Solución:**
```javascript
// ✅ CORRECTO
'maria-familia'  // URL: ?guest=maria-familia

// ❌ INCORRECTO
'Maria Familia'  // URL: ?guest=Maria Familia (no funciona)
'maria_familia'  // URL: ?guest=maria-familia (no coincide)
```

### Error: "La música no se escucha"

**Causa:** URL inválida o formato no soportado.

**Solución:**
- Verifica que la URL termine en `.mp3`
- Prueba la URL directamente en el navegador
- Asegúrate de tener conexión a internet
- Usa una fuente confiable (Pixabay, Free Music Archive)

### Error: "La página se ve rara en móvil"

**Causa:** El navegador cachó la versión antigua.

**Solución:**
- Limpia el caché (Ctrl+Shift+Delete en Chrome)
- Abre en modo incógnito
- Accede nuevamente al sitio

### Error: "Los colores no cambian"

**Causa:** CSS no se actualiza correctamente.

**Solución:**
- Verifica que las variables estén entre las comillas: `#d4af37`
- No añadas espacios: `#d4af37` ✅ vs `# d4af37` ❌
- Usa formato hexadecimal válido

---

## 📞 Soporte Rápido

### Necesito cambiar solo UNA cosa

1. Abre `index.html` en un editor (Notepad, VS Code, etc)
2. Usa Ctrl+F para buscar el texto
3. Haz el cambio
4. Guarda con Ctrl+S
5. Sube el archivo nuevamente

### Necesito agregar más invitados

1. Busca `const guestsData = {`
2. Copia un formato existente
3. Personaliza nombres, ID y pases
4. Asegúrate de que no falten comas
5. Guarda y sube

### Necesito una vista previa antes de publicar

1. Abre `index.html` directamente en el navegador
2. Prueba todos los parámetros: `?guest=carolin-familia`
3. Verifica animaciones, música y responsividad
4. Una vez satisfecho, sube a tu servidor

---

**¡Que tu invitación sea perfecta! 💍✨**
