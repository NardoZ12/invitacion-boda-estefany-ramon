# 💍 Invitación de Boda - Estefany & Ramón

Una elegante página web de invitación de boda interactiva con personalización dinámica por invitado, diseño responsivo y características premium.

## ✨ Características Principales

### 🎨 Diseño Elegante
- Paleta de colores lujosa: blanco perla, marfil, dorado y detalles sofisticados
- Tipografía refinada (serif + sans-serif)
- Diseño minimalista y profesional
- Totalmente responsivo (móvil, tablet, desktop)

### 🎯 Personalización Dinámica
- Cada invitado recibe un enlace único con su nombre
- Muestra automáticamente sus pases asignados
- Personaliza el mensaje de confirmación por WhatsApp
- Parámetro URL: `?guest=ID` carga datos específicos

### 🎵 Experiencia Multimedia
- Reproductor de música flotante discreto
- Melodía orquestal elegante de fondo
- Control manual de reproducción (play/pause)
- Volumen optimizado para no perturbar

### ⏳ Funcionalidades Interactivas
- Contador regresivo al evento (días, horas, minutos)
- Pantalla de bienvenida elegante
- Animaciones suaves al hacer scroll
- Efectos hover en elementos interactivos

### 📱 RSVP Integrado
- Botón de confirmación que abre WhatsApp
- Mensaje pre-llenado personalizado por invitado
- Fácil confirmación en un clic

### 👗 Código de Vestimenta
- Sección visual de código de vestimenta (Formal/Elegante)
- Paleta armónica sugerida con 5 colores coordinados
- Ejemplos de atuendos con iconos

---

## 📁 Estructura de Archivos

```
invitacion-boda-estefany-ramon/
├── index.html              # Página principal (todo en uno)
├── README.md               # Este archivo
├── GUEST_LINKS.md          # Enlaces personalizados para cada invitado
└── .gitignore              # Configuración de Git
```

---

## 🚀 Cómo Usar

### 1. Descargar/Clonar
```bash
git clone https://github.com/tu-usuario/invitacion-boda-estefany-ramon.git
```

### 2. Abrir Localmente
- Abre `index.html` en un navegador web
- O usa un servidor local: `python -m http.server` (Python 3)

### 3. Subir a un Servidor

#### Opción A: GitHub Pages (Recomendado - Gratis)
1. Asegúrate de que tu repositorio sea público
2. Ve a Settings > Pages
3. Selecciona "Deploy from a branch"
4. Elige `main` (o tu rama principal)
5. Tu sitio estará en: `https://tu-usuario.github.io/invitacion-boda-estefany-ramon/`

#### Opción B: Netlify (Gratis)
1. Ve a [netlify.com](https://netlify.com)
2. Arrastra la carpeta o conecta tu repositorio
3. Obtén URL automáticamente

#### Opción C: Servidor Personalizado
1. Sube `index.html` a tu servidor
2. Accede con tu dominio

### 4. Compartir Enlaces

Ver archivo `GUEST_LINKS.md` para los 20 enlaces personalizados.

Ejemplo:
```
https://tu-usuario.github.io/invitacion-boda-estefany-ramon/index.html?guest=carolin-familia
```

---

## 👥 Invitados Configurados

| ID | Invitados | Pases |
|---|---|---|
| carolin-familia | Carolin Rodríguez, Adriana Rodríguez, Génesis de Jesús | 3 |
| rosa | Rosa Corona | 1 |
| marcia-familia | Marcia A. Castillo, Day Nova Castillo, Jenifer Alexandra, Javier Nova Castillo, Sebastián Michel Castillo | 5 |
| carmen-daiana | Carmen Castillo, Daiana Franco | 2 |
| ana | Ana Corona | 1 |
| anairis-cristal | Anairis Corona, Cristal | 2 |
| engel-maria | Engel David Rodríguez, María Fernanda | 2 |
| richeimily-samuel | Richeimily Rodríguez, Samuel Frica | 2 |
| martires-teresa | Mártires Rodríguez, Teresa | 2 |
| jenifer-jonathan | Jenifer Melo, Jonathan Soliman | 2 |
| pastores-tita-valentin | Pastores Tita Calderón, Valentín Santana | 2 |
| familia-santana | Dorian Santana, Solibel Jiménez, Tael Santana | 3 |
| elizabeth-ezequiel | Elizabeth Marte, Ezequiel Álvarez | 2 |
| ivania-emilio | Ivania Germán, Emilio Ramos | 2 |
| darlin-laudina | Darlin Rodríguez, Laudina Guerrero | 2 |
| reina | Reina Flores | 1 |
| arianna-ruth | Arianna Hernández, Ruth Hernández | 2 |
| emely | Emely de Pablos | 1 |
| daniel-olga | Daniel Ramos, Olga Lidia | 2 |
| santa-jessy | Santa Castillo, Jessy Pérez | 2 |

**Total: 20 grupos de invitados, 47 personas, 49 pases**

---

## 🔧 Editar Información

### Cambiar Fecha/Hora del Evento
Busca en `index.html` línea ~463:
```javascript
const eventDate = new Date('2026-11-27T16:30:00').getTime();
```

Modifica `2026-11-27T16:30:00` al formato: `YYYY-MM-DDTHH:mm:ss`

### Agregar Nuevos Invitados
Localiza la sección `guestsData` (línea ~470) y agrega:
```javascript
'nuevo-id': {
    names: ['Nombre Invitado 1', 'Nombre Invitado 2'],
    passes: 2
},
```

### Cambiar URL de Música
Busca línea ~515:
```html
<source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
```

Reemplaza con tu URL de música (debe ser `.mp3` libre de derechos)

### Personalizar Colores
Modifica las variables CSS (línea ~8):
```css
:root {
    --color-primary: #f5f1ed;      /* Fondo principal */
    --color-accent: #d4af37;       /* Dorado */
    --color-text: #3a3a3a;         /* Texto */
}
```

---

## 📊 Detalles del Evento

- **Novios:** Estefany & Ramón
- **Fecha:** Viernes, 27 de Noviembre de 2026
- **Hora:** 4:30 PM
- **Código de Vestimenta:** Formal / Elegante
- **Total de Invitados:** 20 grupos, 47 personas

---

## 🎵 Música de Fondo

- **Fuente:** SoundHelix (libre de derechos)
- **Tipo:** Orquestal instrumental
- **Volumen:** 30% (ajustable en código)
- **Control:** Botón flotante play/pause

---

## 📱 Compatibilidad

- ✅ Chrome/Chromium
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Mobile (iOS/Android)
- ✅ Tablets

---

## 🛠️ Requisitos Técnicos

- Navegador web moderno (HTML5, CSS3, ES6 JavaScript)
- Conexión a internet (para música y fuentes)
- No requiere backend o base de datos

---

## 📄 Secciones de la Página

1. **Pantalla de Bienvenida**
   - Nombre de los novios
   - Frase romántica
   - Botón "Abrir Invitación"

2. **Portada/Hero**
   - Título elegante (Estefany & Ramón)
   - Frase poética

3. **Bienvenida Personalizada**
   - Saludo con nombre del invitado
   - Cantidad de pases reservados

4. **Detalles del Evento**
   - Fecha: Viernes 27 de Noviembre
   - Hora: 4:30 PM
   - Contador regresivo

5. **Código de Vestimenta**
   - Indicación: Formal/Elegante
   - Ejemplos visuales de atuendos
   - Paleta armónica de 5 colores

6. **Confirmación RSVP**
   - Botón integrado con WhatsApp
   - Mensaje personalizado por invitado

7. **Footer**
   - Información del evento
   - Agradecimiento

---

## 🎨 Paleta de Colores Sugerida para Vestimenta

| Color | Código | Descripción |
|---|---|---|
| Marfil Suave | #f5f1ed | Tonos claros y elegantes |
| Dorado Elegante | #d4af37 | Detalles y acentos |
| Negro Sofisticado | #2c2c2c | Formalidad clásica |
| Marrón Cálido | #8b7355 | Tonos tierra elegantes |
| Crema Refinada | #e8dcc8 | Alternativa a blanco |

---

## 🔒 Privacidad y Seguridad

- No se almacenan datos personales
- Los nombres de invitados son visibles en URLs (considéralo al compartir)
- La música es de una fuente pública
- No hay cookies ni rastreo

---

## 🐛 Solución de Problemas

### La música no se reproduce
- Algunos navegadores requieren interacción del usuario primero
- Clickea el botón "Abrir Invitación"
- Si persiste, verifica la URL de la música

### Los nombres no se personalizan
- Verifica que el parámetro `?guest=ID` está correctamente escrito
- Los IDs son sensibles a mayúsculas/minúsculas
- Compara con la lista en `GUEST_LINKS.md`

### La página se ve rara en móvil
- Limpia el caché del navegador (Ctrl+Shift+Delete)
- Abre en modo incógnito
- Prueba con otro navegador

---

## 📞 Contacto y Soporte

Para preguntas o cambios:
1. Edita directamente el `index.html`
2. Busca la sección relevante (está comentada)
3. Guarda y sube los cambios

---

## 🎁 Créditos

- **Diseño:** Personalizado para Estefany & Ramón
- **Tecnología:** HTML5 + CSS3 + Vanilla JavaScript
- **Música:** SoundHelix (libre de derechos)
- **Hosting:** GitHub Pages / Netlify / Servidor personalizado

---

**¡Que disfrutes tu gran día! 💍✨**

*"El amor es la poesía de los sentidos"*
