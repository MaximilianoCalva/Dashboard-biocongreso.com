# Dashboard BioCongreso 🧬

**Versión**: 1.0.1  
**Última actualización**: Enero 2026

Panel de control para el evento BioCongreso, desarrollado con HTML, CSS y diseñado para integración con WordPress y Elementor.

## 🎨 Colores Institucionales

- **Azul Oscuro Principal**: `#1a2332`
- **Azul Medio**: `#2a3f5f`
- **Amarillo/Dorado (Acento)**: `#FFC107`
- **Verde (WhatsApp)**: `#10b981`
- **Rojo (Logout)**: `#ef4444`

## 📁 Estructura del Proyecto

```
Dashboard-biocongreso.com/
├── Header/
│   ├── header-logged-in-biocongreso.html      # Header para usuarios autenticados
│   └── header-logged-out-biocongreso.html     # Header para usuarios no autenticados
├── Footer/
│   └── footer-dashboard-biocongreso-snippet.html  # Footer con botón cerrar sesión
├── Acceso a dashboard/
│   ├── login-biocongreso-snippet.html         # Tarjeta de bienvenida (usuario logueado)
│   └── logout-biocongreso-snippet.html        # Formulario de login (usuario no logueado)
├── dashboard/
│   └── dashboard-complete.html                # Dashboard completo
└── README.md                                  # Este archivo
```

## 🚀 Componentes Disponibles

### Headers

#### 1. Header Logged In (Usuario Autenticado)
**Archivo**: `Header/header-logged-in-biocongreso.html`

Header completo para usuarios que ya iniciaron sesión.

**Características:**
- Logo BioCongreso con gradiente
- Subtítulo: "Dashboard"
- Botón "Dashboard" → `https://panel.biocongreso.com/usuario/`
- Botón "¿Necesitas ayuda?" (WhatsApp) → `https://wa.me/5213334054655`
- Botón "Cerrar sesión" (logout)
- Diseño responsive con iconos SVG
- Colores institucionales (#1a2332, #FFC107)

#### 2. Header Logged Out (Usuario No Autenticado)
**Archivo**: `Header/header-logged-out-biocongreso.html`

Header para usuarios que no han iniciado sesión.

**Características:**
- Logo BioCongreso con gradiente (sin subtítulo)
- Botón "Acceso al Dashboard" → `https://panel.biocongreso.com/`
- Botón "Registro" (amarillo/dorado) → `https://panel.biocongreso.com/` (misma URL)
- Diseño limpio y minimalista
- Responsive con botones lado a lado
- **Nota**: Ambos botones redirigen a la misma página donde el usuario puede elegir entre login o registro

### Footer

#### 3. Footer Dashboard
**Archivo**: `Footer/footer-dashboard-biocongreso-snippet.html`

Footer simple con botón de cerrar sesión.

**Características:**
- Botón "🚪 Cerrar Sesión"
- Color base: #1a2332
- Hover: #c62828 (rojo)

### Acceso a Dashboard

#### 4. Login Snippet (Usuario Autenticado)
**Archivo**: `Acceso a dashboard/login-biocongreso-snippet.html`

Tarjeta de bienvenida para usuarios que ya están logueados.

**Características:**
- Icono de graduación en círculo con gradiente
- Título: "¡Empecemos a Aprender!"
- Mensaje: "Bienvenido de nuevo. Tu dashboard está listo para acceder a toda la información del evento."
- Botón "Ir al Dashboard" → `https://panel.biocongreso.com/usuario/`
- Diseño tipo card con sombra
- **Uso**: Mostrar a usuarios autenticados

#### 5. Logout Snippet (Usuario No Autenticado)
**Archivo**: `Acceso a dashboard/logout-biocongreso-snippet.html`

Contenedor para formularios de login y registro.

**Características:**
- Header con gradiente institucional
- Título "BioCongreso"
- Instrucciones: "¿Ya tienes cuenta? Inicia sesión. ¿Eres nuevo? Regístrate para el evento."
- **Sección 1**: "Iniciar Sesión" con shortcode `[ultimatemember form_id="23"]`
- Separador visual (línea horizontal)
- **Sección 2**: "Crear Cuenta Nueva" con shortcode `[ultimatemember form_id="22"]`
- Diseño tipo card con sombra
- **Uso**: Mostrar a usuarios NO autenticados (permite elegir entre login o registro)

## 🔐 Integración con WordPress

### Shortcodes de Ultimate Member

```html
<!-- Formulario de Login -->
[ultimatemember form_id="23"]

<!-- Formulario de Registro -->
[ultimatemember form_id="22"]
```

### URLs del Sistema

- **Panel Principal**: `https://panel.biocongreso.com/`
- **Dashboard de Usuario**: `https://panel.biocongreso.com/usuario/`
- **WhatsApp Soporte**: `https://wa.me/5213334054655`
- **Logout**: `https://panel.biocongreso.com/wp-login.php?action=logout&redirect_to=https%3A%2F%2Fpanel.biocongreso.com`

## 📝 Uso en Elementor

### Implementación por Tipo de Página

#### Página de Login (Usuario NO autenticado)
```
├── Header: header-logged-out-biocongreso.html
├── Contenido: logout-biocongreso-snippet.html
└── Footer: (opcional)
```

#### Página de Dashboard (Usuario autenticado)
```
├── Header: header-logged-in-biocongreso.html
├── Contenido: login-biocongreso-snippet.html (tarjeta de bienvenida)
└── Footer: footer-dashboard-biocongreso-snippet.html
```

### Método de Integración

1. **Abrir página en Elementor**
2. **Agregar widget HTML**
3. **Copiar contenido del archivo HTML completo**
4. **Pegar en el widget**
5. **Guardar y publicar**

## 🎯 Flujo de Usuario

### Usuario NO Autenticado
1. Ve `header-logged-out` con botón "Acceso al Dashboard"
2. Ve `logout-biocongreso-snippet` con formulario de login
3. Ingresa credenciales en formulario Ultimate Member
4. Después de login exitoso → redirige a dashboard

### Usuario Autenticado
1. Ve `header-logged-in` con Dashboard, Ayuda y Logout
2. Ve `login-biocongreso-snippet` con tarjeta de bienvenida
3. Click en "Ir al Dashboard" → accede a panel personal
4. Click en WhatsApp → soporte técnico
5. Click en "Cerrar sesión" → logout

## 🎨 Características de Diseño

### Headers Completos
- **Branding**: Logo con gradiente institucional
- **Botones**: Iconos SVG + texto
- **Responsive**: Adaptación automática a móvil
- **Efectos**: Hover con elevación y cambio de color

### Snippets de Acceso
- **Login**: Card con icono, mensaje y botón
- **Logout**: Container con header y formulario
- **Diseño**: Cards con sombras y bordes redondeados

### Colores por Componente
- **Dashboard/Login**: Gradiente #1a2332 → Hover #FFC107
- **WhatsApp**: Verde #10b981
- **Logout**: Transparente → Hover rojo #ef4444

## 🛠️ Personalización

### Cambiar URLs

```html
<!-- Dashboard -->
href="https://panel.biocongreso.com/usuario/"

<!-- WhatsApp (cambiar número) -->
href="https://wa.me/5213334054655"

<!-- Logout -->
href="https://panel.biocongreso.com/wp-login.php?action=logout..."
```

### Cambiar Shortcodes

```html
<!-- En logout-biocongreso-snippet.html -->
[ultimatemember form_id="23"]  <!-- Cambiar ID según tu instalación -->
```

### Cambiar Textos

```html
<!-- Header logged-in -->
<span class="brand-subtitle">Dashboard</span>

<!-- Login snippet -->
<h1>¡Empecemos a Aprender!</h1>
<p>Bienvenido de nuevo. Tu dashboard está listo para acceder a toda la información del evento.</p>
```

## 📊 Dashboard - Secciones Separadas

El dashboard de BioCongreso está dividido en 3 secciones independientes para facilitar su integración en WordPress/Elementor:

### Sección 01: Menú Lateral
**Archivo**: `dashboard/seccion-01-menu.html`

Menú lateral con las ediciones de BioCongreso.

**Contenido:**
- Logo BioCongreso (🧬)
- 5to BioCongreso (activo) → Link al curso
- 6to BioCongreso
- 7mo BioCongreso

**Uso en Elementor:**
1. Agregar widget HTML
2. Copiar contenido de `seccion-01-menu.html`
3. Pegar en el widget
4. Colocar en la columna izquierda del layout

### Sección 02: Contenido Principal
**Archivo**: `dashboard/seccion-02-contenido.html`

Contenido central con todas las conferencias del 5to BioCongreso.

**Contenido:**
- Header: "Dashboard BioCongreso"
- Card destacada: 5to BioCongreso "Sanar Emocional" (grid-column: span 2)
- **14 Cards de conferencias** (en orden):
  1. María de la O - Presentación
  2. Osmary Acebal - La Magia del Placebo
  3. Gilma Barragan - Despertar de la Conciencia
  4. Luz María Zetina - Más Allá de la Historia
  5. Paty Bens - Ejercicio Día 1
  6. Denisse Jiménez - Ejercicio Día 2
  7. Laura García - Des-aprender con Todo tu Cuerpo
  8. Ivette Ferrer - Hipnosis Biológica Integrativa
  9. Mary Zamacona - Cuando el Alma Llora en Silencio
  10. Benito Agrega - Geometría Sagrada
  11. Iván Martz - Gestión Emocional
  12. Fernando Sánchez - Árbol Transgeneracional
  13. César Lozano - Actitudes Positivas
  14. Paty Bens - Ejercicio Final Día 2

**Uso en Elementor:**
1. Agregar widget HTML
2. Copiar contenido de `seccion-02-contenido.html`
3. Pegar en el widget
4. Colocar en la columna central del layout

### Sección 03: Avisos y Comunidad
**Archivo**: `dashboard/seccion-03-conferencias.html`

Sidebar derecho para avisos y comunidad de WhatsApp.

**Contenido:**
- **Canal de WhatsApp BioCongreso:**
  - Card especial con gradiente verde
  - Descripción: Avisos importantes, actualizaciones y conexión con la comunidad
  - Botón "Unirse al Canal" → https://whatsapp.com/channel/0029VbB4sIw9mrGZcf6T0Z0F

**Uso en Elementor:**
1. Agregar widget HTML
2. Copiar contenido de `seccion-03-conferencias.html`
3. Pegar en el widget
4. Colocar en la columna derecha del layout

### Estructura de Layout Recomendada en Elementor

```
┌─────────────────────────────────────────────────────────┐
│                    Header (opcional)                     │
├──────────┬─────────────────────────────┬─────────────────┤
│          │                             │                 │
│ Sección  │      Sección 02             │   Sección 03    │
│   01     │      Contenido              │  Conferencias   │
│  Menú    │      Principal              │  y Comunidad    │
│          │                             │                 │
│ (280px)  │      (1fr - flexible)       │    (320px)      │
│          │                             │                 │
└──────────┴─────────────────────────────┴─────────────────┘
```

**Configuración de columnas en Elementor:**
- Desktop: 3 columnas (280px | 1fr | 320px)
- Tablet: 2 columnas (Menú + Contenido arriba, Conferencias abajo)
- Mobile: 1 columna (apiladas verticalmente)

### Notas Importantes

- ✅ **Sin padding externo**: Las secciones no tienen padding externo, ajusta los espacios desde Elementor
- ✅ **Colores BioCongreso**: Todos los estilos usan la paleta institucional
- ✅ **Responsive**: Cada sección se adapta automáticamente
- ✅ **Font Awesome**: Requiere Font Awesome 6.4.0+ para los iconos
- ✅ **Links funcionales**: Todos los enlaces apuntan a las URLs correctas

## 📱 Compatibilidad

- ✅ WordPress 5.0+
- ✅ Elementor 3.0+
- ✅ Ultimate Member 2.0+
- ✅ Chrome, Firefox, Safari, Edge
- ✅ Responsive (Desktop, Tablet, Mobile)

## 📄 Archivos del Proyecto

| Archivo | Propósito | Estado Usuario |
|---------|-----------|----------------|
| `header-logged-in-biocongreso.html` | Header completo | Autenticado |
| `header-logged-out-biocongreso.html` | Header simple | No autenticado |
| `footer-dashboard-biocongreso-snippet.html` | Footer con logout | Autenticado |
| `login-biocongreso-snippet.html` | Tarjeta bienvenida | Autenticado |
| `logout-biocongreso-snippet.html` | Formulario login | No autenticado |

## 🔗 Recursos

- **WordPress**: https://panel.biocongreso.com/wp-admin/
- **Ultimate Member**: Plugin de gestión de usuarios
- **Elementor**: Constructor visual de páginas
- **WhatsApp**: Soporte técnico

---

**BioCongreso** © 2025 - Evento Anual
