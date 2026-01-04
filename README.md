# Dashboard BioCongreso 🧬

**Versión**: 1.0.1  
**Última actualización**: Enero 2026

Panel de control para el evento BioCongreso, desarrollado con HTML, CSS y diseñado para integración con WordPress y Elementor.

## SEO y Metadata

### Dashboard
**Título del Sitio:** BioCongreso Dashboard - Encuentro de Salud y Consciencia
**Descripción Corta:** Panel de control para asistentes y ponentes de BioCongreso. Gestiona tu acceso al evento líder en salud holística, conferencias y talleres internacionales.

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
│   ├── dashboard-complete.html                # Dashboard completo
│   ├── seccion-01-menu.html                   # Menú lateral dashboard
│   ├── seccion-02-contenido.html              # Contenido principal
│   └── seccion-03-conferencias.html           # Sidebar conferencias/comunidad
└── README.md                                  # Documentación consolidada
```

## 🚀 Componentes Disponibles

### Headers (Optimizados Tablet/Mobile)

El sistema incluye headers completamente responsivos con menú hamburguesa para dispositivos tablet (≤1024px) y móviles.

#### 1. Header Logged In (Usuario Autenticado)
**Archivo**: `Header/header-logged-in-biocongreso.html`

Header completo para usuarios que ya iniciaron sesión.

**Características:**
- Logo BioCongreso clickeable (redirige a `https://biocongreso.com/`)
- Subtítulo: "Dashboard"
- **Navegación Desktop**: Botones visibles (Dashboard, Ayuda, Logout)
- **Navegación Tablet/Móvil**: Menú hamburguesa lateral deslizante con overlay
- Colores institucionales (#1a2332, #FFC107)

#### 2. Header Logged Out (Usuario No Autenticado)
**Archivo**: `Header/header-logged-out-biocongreso.html`

Header para usuarios que no han iniciado sesión.

**Características:**
- Logo BioCongreso clickeable
- Botón "Acceso al Dashboard"
- Menú hamburguesa responsivo

### Footer

#### 3. Footer Dashboard
**Archivo**: `Footer/footer-dashboard-biocongreso-snippet.html`

Footer simple con botón de cerrar sesión.

### Acceso a Dashboard

#### 4. Login Snippet (Usuario Autenticado)
**Archivo**: `Acceso a dashboard/login-biocongreso-snippet.html`

Tarjeta de bienvenida para usuarios logueados.

#### 5. Logout Snippet (Usuario No Autenticado)
**Archivo**: `Acceso a dashboard/logout-biocongreso-snippet.html`

Contenedor para formularios de login y registro.

---

## 📖 Guía de Implementación en Elementor (WordPress)

Nota: Esta guía aplica para la sección de Dashboard (archivos en carpeta `dashboard/`).

### ✅ Archivos Relacionados
1. **dashboard-complete.html**: Vista previa completa.
2. **seccion-01-menu.html**: Menú lateral (Congresos, Diplomados).
3. **seccion-02-contenido.html**: Contenido principal (Cards).
4. **seccion-03-conferencias.html**: Sidebar (Avisos/WhatsApp).

### 🚀 Pasos para Implementar

#### Paso 1: Configurar el Layout en Elementor
1. Añade una **Sección** nueva con 3 columnas.
2. **Configuración de ancho**:
   - **Desktop**: 3 columnas (20% - 50% - 30% aprox)
   - **Tablet**: 2 columnas (30% - 70%), Sidebar abajo
   - **Móvil**: 1 columna (100%)

#### Paso 2: Añadir los Bloques HTML
Usa el widget **HTML** de Elementor para cada columna.

1. **Columna 1 (Izquierda)**: Copia y pega TODO el contenido de `seccion-01-menu.html`.
2. **Columna 2 (Centro)**: Copia y pega TODO el contenido de `seccion-02-contenido.html`.
3. **Columna 3 (Derecha)**: Copia y pega TODO el contenido de `seccion-03-conferencias.html`.

#### Paso 3: Ajustes Finales
1. **Elimina padding/margin** de la sección y columnas en Elementor (los archivos ya traen su propio espaciado interno).
2. **Fondo de página**: Recomendado `#f5f5f7` (gris claro).
3. **Responsive**: Verifica en modo Tablet y Móvil de Elementor.

### 🔧 Personalización
- **Iconos**: Se usa Font Awesome 6. Asegúrate de tenerlo cargado o usa el link CDN incluido en los snippets.
- **Fuentes**: Se usa "Inter". Puedes cambiarlo en el CSS dentro de cada widget HTML si prefieres otra.

---

## 🔐 Integración con Ultimate Member (Login/Logout)

### Shortcodes
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

---

## 📱 Compatibilidad
- ✅ WordPress 5.0+
- ✅ Elementor 3.0+
- ✅ Ultimate Member 2.0+
- ✅ Responsive Total (Desktop, Tablet, Mobile)
- ✅ Navegadores Modernos (Chrome, Safari, Edge, Firefox)

---

**BioCongreso** © 2026
