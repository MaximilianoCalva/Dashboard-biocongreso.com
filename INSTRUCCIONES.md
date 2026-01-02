# 📋 Guía de Implementación en Elementor

## ✅ Archivos Creados

He creado **5 archivos** para tu dashboard de WordPress:

### 1. **dashboard-complete.html**
Vista previa completa del dashboard funcionando. Abre este archivo en tu navegador para ver cómo se ve todo junto.

### 2. **seccion-01-menu.html**
Bloque HTML del menú lateral vertical con:
- 4 opciones de menú (Congresos, Diplomados, Talleres, Eventos)
- Iconos de Font Awesome
- Efectos hover y animaciones
- Completamente responsive

### 3. **seccion-02-contenido.html**
Bloque HTML del área de contenido principal con:
- Título "Tablero"
- Grid de tarjetas responsive
- 6 tarjetas de ejemplo (Congresos, Diplomados, Talleres, Eventos)
- Botones de acción

### 4. **seccion-03-eventos.html**
Bloque HTML del sidebar de próximos eventos con:
- Lista de eventos próximos
- Fechas y descripciones
- Badges de estado
- Responsive (sidebar en desktop, abajo en móvil)

### 5. **paletas-de-colores.html**
Documento visual con 3 opciones de paletas de colores para elegir.

---

## 🚀 Cómo Pegar en Elementor

### Paso 1: Preparar la Página
1. En WordPress, ve a **Páginas → Añadir nueva** (o edita una existente)
2. Haz clic en **Editar con Elementor**

### Paso 2: Configurar el Layout
1. Añade una **Sección** nueva
2. Configura la estructura de columnas:
   - **Desktop**: 3 columnas (20% - 50% - 30%)
   - **Tablet**: 2 columnas (30% - 70%)
   - **Móvil**: 1 columna (100%)

### Paso 3: Añadir los Bloques HTML

#### Columna 1: Menú Lateral
1. Arrastra el widget **HTML** a la primera columna
2. Abre el archivo `seccion-01-menu.html`
3. Copia TODO el contenido (incluyendo el `<style>` y el `<script>`)
4. Pégalo en el widget HTML de Elementor

#### Columna 2: Contenido Principal
1. Arrastra el widget **HTML** a la segunda columna
2. Abre el archivo `seccion-02-contenido.html`
3. Copia TODO el contenido
4. Pégalo en el widget HTML de Elementor

#### Columna 3: Próximos Eventos
1. Arrastra el widget **HTML** a la tercera columna
2. Abre el archivo `seccion-03-eventos.html`
3. Copia TODO el contenido
4. Pégalo en el widget HTML de Elementor

### Paso 4: Ajustes Finales
1. **Elimina padding/margin** de la sección principal en Elementor
2. **Configura el fondo** de la página como `#f5f5f7` (gris claro)
3. Guarda y previsualiza

---

## 🎨 Cambiar Paleta de Colores

Si quieres cambiar la paleta de colores:

1. Abre `paletas-de-colores.html` en tu navegador
2. Elige una de las 3 opciones
3. Copia el código CSS del gradiente
4. Busca y reemplaza en los 3 archivos de secciones:

**Buscar:**
```css
linear-gradient(135deg, #667eea 0%, #764ba2 100%)
```

**Reemplazar con** (ejemplo Azul Corporativo):
```css
linear-gradient(135deg, #2193b0 0%, #6dd5ed 100%)
```

También reemplaza:
- `#667eea` → Color principal de tu paleta elegida

---

## 📱 Responsive

El diseño es **completamente responsive**:

- **Desktop (>1200px)**: 3 columnas (Menú | Contenido | Eventos)
- **Tablet (768px-1200px)**: 2 columnas (Menú | Contenido) + Eventos abajo
- **Móvil (<768px)**: 1 columna vertical (Menú → Contenido → Eventos)

En móvil, el menú tiene un botón hamburguesa automático.

---

## 🔧 Personalización

### Cambiar Elementos del Menú
Edita en `seccion-01-menu.html`:
```html
<li class="sidebar-menu-item">
    <a href="#tu-enlace" class="sidebar-menu-link">
        <i class="fas fa-tu-icono"></i>
        <span>Tu Texto</span>
    </a>
</li>
```

### Añadir/Editar Tarjetas de Contenido
Duplica este bloque en `seccion-02-contenido.html`:
```html
<article class="content-card">
    <div class="content-card-icon">
        <i class="fas fa-tu-icono"></i>
    </div>
    <h3>Título</h3>
    <p>Descripción</p>
    <div class="content-card-meta">
        <span class="content-meta-item">
            <i class="fas fa-calendar"></i>
            Fecha
        </span>
    </div>
    <a href="#" class="content-card-button">
        Ver detalles
        <i class="fas fa-arrow-right"></i>
    </a>
</article>
```

### Añadir/Editar Eventos
Duplica este bloque en `seccion-03-eventos.html`:
```html
<div class="events-sidebar-item">
    <div class="events-item-date">
        <i class="fas fa-calendar-day"></i>
        Fecha
    </div>
    <div class="events-item-title">Título del Evento</div>
    <div class="events-item-description">
        Descripción breve
    </div>
    <span class="events-item-badge">Estado</span>
</div>
```

---

## 🎯 Iconos de Font Awesome

Los iconos vienen de Font Awesome 6. Busca más iconos en:
👉 https://fontawesome.com/icons

Ejemplos útiles:
- `fa-users` - Grupos/Congresos
- `fa-certificate` - Diplomas/Certificados
- `fa-chalkboard-teacher` - Talleres/Clases
- `fa-calendar-alt` - Eventos/Fechas
- `fa-graduation-cap` - Educación
- `fa-book` - Libros/Módulos
- `fa-video` - Online/Webinar
- `fa-globe` - Internacional/Híbrido

---

## ⚠️ Notas Importantes

1. **Font Awesome**: Los bloques ya incluyen el link a Font Awesome. Si tu tema de WordPress ya lo tiene, puedes eliminar la línea:
   ```html
   <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
   ```

2. **Fuente Inter**: Los bloques usan la fuente Google Font "Inter". Si prefieres otra fuente, cámbiala en el CSS.

3. **Enlaces**: Todos los enlaces (`href="#"`) son de ejemplo. Reemplázalos con tus URLs reales.

4. **Contenido dinámico**: Si quieres que el contenido sea dinámico desde WordPress, necesitarás integrar PHP o usar un plugin como ACF (Advanced Custom Fields).

---

## 🆘 Solución de Problemas

### Los estilos no se aplican
- Asegúrate de copiar TODO el contenido, incluyendo las etiquetas `<style>`
- Verifica que Elementor permita CSS personalizado en widgets HTML

### Los iconos no aparecen
- Verifica que Font Awesome esté cargado
- Revisa la consola del navegador para errores

### El responsive no funciona
- Asegúrate de que tu tema de WordPress tenga configurado el viewport meta tag
- Verifica que no haya CSS del tema que sobrescriba los estilos

### El menú móvil no funciona
- Asegúrate de copiar también el código `<script>` al final del archivo

---

## 📞 Próximos Pasos

1. ✅ Abre `dashboard-complete.html` en tu navegador para ver la vista previa
2. ✅ Elige tu paleta de colores en `paletas-de-colores.html`
3. ✅ Pega los 3 bloques en Elementor siguiendo esta guía
4. ✅ Personaliza el contenido con tu información real
5. ✅ Ajusta los enlaces a tus páginas reales

---

**¿Necesitas ayuda?** Pregúntame cualquier duda sobre la implementación. 😊
