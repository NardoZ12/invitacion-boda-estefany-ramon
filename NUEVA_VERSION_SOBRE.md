# 📬 NUEVA VERSIÓN - ANIMACIÓN DEL SOBRE

## ✨ Cambios Principales

La invitación ha sido actualizada con un diseño mucho más elegante e interactivo. Ahora inicia con una **animación de sobre que se abre como un libro**.

---

## 🎬 ¿Cómo Funciona Ahora?

### 1️⃣ **Pantalla Inicial: Sobre Cerrado**
```
┌─────────────────────────────────┐
│                                 │
│      Estefany & Ramón           │
│                                 │
│   "El amor es la poesía de      │
│    los sentidos"                │
│                                 │
│      ↑ TOQUE PARA ABRIR ↑       │
│                                 │
└─────────────────────────────────┘
```

**Características:**
- Sobre cerrado con bordes elegantes dorados
- Texto "TOQUE PARA ABRIR" parpadeante
- Nombres de los novios en tipografía elegante
- Frase romántica
- Cursor indica que es clickeable

### 2️⃣ **Al Hacer Clic: Animación del Sobre Abriéndose**

**Lo que sucede:**
- El sobre se divide en dos mitades (izquierda y derecha)
- Ambas mitades rotan 95 grados hacia afuera (como un libro)
- Efecto 3D suave y elegante (perspectiva)
- Duración: 1.2 segundos
- Emojis decorativos (✨💕) aparecen en las páginas

### 3️⃣ **Contenido Aparece: Invitación Personalizada**

Después de que el sobre se abre (0.8 segundos después):
- Aparece la bienvenida personalizada
- Se carga el nombre del invitado
- Se muestra el número de pases
- Reproducción automática de música elegante
- Resto de secciones visibles con animaciones suaves

---

## 🎨 Diferencias Visuales

### ANTES (Versión Original)
```
┌─────────────────────────────┐
│  Pantalla de Bienvenida     │
│                             │
│  Estefany & Ramón           │
│  (Frase romántica)          │
│                             │
│  [Botón: Abrir Invitación]  │
└─────────────────────────────┘
↓ Click en botón
Desaparece la pantalla y aparece contenido
```

### AHORA (Versión Mejorada)
```
┌──────────────┬──────────────┐
│              │              │
│ Sobre Cerrado│ Con Bordes    │
│              │ Dorados       │
│              │              │
│ TOQUE PARA   │              │
│ ABRIR        │              │
│              │              │
└──────────────┴──────────────┘
↓ Click en cualquier parte
┌────────┐ ✨ ┌────────┐
│        │←   →│        │
│  Rot   │ 95° │  Rot   │
│ ↙     │     │     ↘  │
└────────┘     └────────┘
↓ Animación completa (1.2s)
Aparece contenido principal con música
```

---

## 🔊 Automatización de Música

**Cambio importante:**
- ❌ Antes: Requerías un botón adicional para iniciar la música
- ✅ Ahora: La música se reproduce **automáticamente al abrir el sobre**

Esta interacción del usuario (hacer clic) permite que el navegador inicie la música sin problemas.

---

## 📱 Responsividad

La animación del sobre funciona perfectamente en:
- ✅ Desktop (versión completa con perspectiva 3D)
- ✅ Tablet (adaptado al tamaño)
- ✅ Mobile (sobre redimensionado, animación suave)

---

## 🎯 Ejemplos de Flujo Completo

### Para un Invitado Sin Personalización
```
1. Abre: https://tu-dominio.com/index.html
2. Ve: Sobre cerrado con "Estefany & Ramón"
3. Hace clic: Sobre se abre
4. Ve: "Nos encantaría que nos acompañes, Estimado Invitado"
5. Ve: "Pases reservados: 1"
6. Escucha: Música elegante
7. Continúa: Secciones de evento, vestimenta, RSVP
```

### Para un Invitado Personalizado (Rosa)
```
1. Abre: https://tu-dominio.com/index.html?guest=rosa
2. Ve: Sobre cerrado
3. Hace clic: Sobre se abre
4. Ve: "Nos encantaría que nos acompañes, Rosa Corona"
5. Ve: "Pases reservados: 1"
6. Escucha: Música elegante
7. Continúa: Resto del contenido personalizado
```

### Para un Grupo (Carolin y Familia)
```
1. Abre: https://tu-dominio.com/index.html?guest=carolin-familia
2. Ve: Sobre cerrado
3. Hace clic: Sobre se abre
4. Ve: "Nos encantaría que nos acompañes, Carolin Rodríguez, 
       Adriana Rodríguez y Génesis de Jesús"
5. Ve: "Pases reservados: 3"
6. Escucha: Música
7. Continúa: Contenido personalizado para 3 personas
```

---

## 🔧 Detalles Técnicos

### Animaciones CSS Utilizadas

1. **openLeft** (Página Izquierda)
   - Rotación en eje Y: 0deg → -95deg
   - Duración: 1.2s
   - Easing: ease-in-out
   - Z-index: cambia de 2 a 0

2. **openRight** (Página Derecha)
   - Rotación en eje Y: 0deg → 95deg
   - Duración: 1.2s
   - Easing: ease-in-out
   - Z-index: cambia de 2 a 0

3. **fadeInContent** (Contenido)
   - Opacidad: 0 → 1
   - Duración: 1.5s
   - Delay: 0.8s (espera a que se abra el sobre)

### Propiedades 3D

- `perspective: 1000px` - Da profundidad al efecto 3D
- `transform-style: preserve-3d` - Mantiene la perspectiva en elementos hijos
- `transform-origin: center` - El eje de rotación es el centro

---

## 🎬 Secuencia de Eventos

```
t=0.0s  → Usuario ve sobre cerrado
t=0.0s  → Usuario hace clic en el sobre
t=0.3s  → Inicia rotación de páginas (con delay)
t=1.5s  → Termina animación de rotación
t=0.8s  → Inicia fade-in del contenido (paralelo a rotación)
t=2.3s  → Termina fade-in del contenido
t=2.3s  → Música comienza a sonar (fue disparada en el clic)
```

---

## 💡 Ventajas de la Nueva Versión

✅ **Más elegante**: Efecto 3D profesional
✅ **Más interactivo**: El usuario participa activamente
✅ **Mejor experiencia**: Transición suave y cinematográfica
✅ **Más memorable**: El efecto del sobre es impactante
✅ **Mismo contenido**: Toda la funcionalidad se mantiene
✅ **Compatible**: Funciona en todos los navegadores modernos
✅ **Accesible**: El sobre es claramente clickeable

---

## ⚠️ Notas Importantes

1. **La música no suena (móviles)**: En iOS/Android, algunos navegadores requieren que el usuario interactúe primero. Hacer clic en el sobre es suficiente.

2. **Si quieres editar el sobre**: Los estilos están en las líneas 70-195 de `index.html`

3. **Para cambiar los emojis**: Modifica las líneas en `.envelope-left` y `.envelope-right` (busca "✨" y "💕")

4. **Para ajustar velocidad**: Cambia `1.2s` en las animaciones `openLeft` y `openRight`

---

## 🔄 Migración Desde la Versión Anterior

**Si ya compartiste enlaces:**
- ✅ Los enlaces siguen funcionando exactamente igual
- ✅ La personalización se mantiene
- ✅ Solo cambia la animación inicial
- ✅ No necesitas actualizar nada en los invitados

**Lo único que cambia para el invitado:**
- Ver el sobre al abrir el enlace
- Hacer clic para ver la invitación
- Experiencia más elegante y interactiva

---

## 📊 Comparación de Versiones

| Característica | v1 Original | v2 Con Sobre |
|---|---|---|
| Pantalla inicial | Botón | Sobre cerrado |
| Interacción | Clic en botón | Clic en sobre |
| Animación | Fade simple | Efecto 3D rotación |
| Duración | Inmediata | 1.5s elegante |
| Música | Manual después | Automática al abrir |
| Personalización | Sí | Sí |
| Responsividad | Sí | Sí |
| Impacto visual | Bueno | Excelente |

---

## 🎉 Conclusión

La nueva versión con la animación del sobre eleva significativamente la experiencia de los invitados, haciendo la invitación digital más memorables y elegante, mientras mantiene toda la funcionalidad original.

**¡Tus invitados dirán "WOW" cuando vean la animación!** 💍✨

---

*Actualizado: Septiembre 18, 2026*
*Rama: claude/wedding-invitation-estefany-ramon-n9o6lp*
