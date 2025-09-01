# GUÍA VISUAL - INTELLIGENCE HUB
## Para Diseñador Gráfico (Wireframes y Mockups)

---

## 🎨 PALETA DE COLORES

```
Azul Principal:    #1a73e8  ████████
Azul Oscuro:       #1565c0  ████████  
Verde Success:     #34a853  ████████
Amarillo Warning:  #fbbc04  ████████
Rojo Error:        #ea4335  ████████
Gris Texto:        #5f6368  ████████
Gris Claro:        #f8f9fa  ████████
Blanco:            #ffffff  ████████
```

---

## 📱 PANTALLA 1: DASHBOARD PRINCIPAL

### LAYOUT BASE:
```
┌─────────────────────────────────────────────────────────────┐
│ [☰] Intelligence Hub              🔍[Buscar...]  [Exportar] │ ← HEADER FIJO
├─────────────────────────────────────────────────────────────┤
│ SIDEBAR     │ CONTENIDO PRINCIPAL                           │
│ (256px)     │                                               │
│             │ Dashboard General                             │
│ • Dashboard │                                               │
│ • Unidades  │ [📅 01/01] hasta [📅 31/01] [Filtrar]       │
│             │                                               │
│ UNIDADES:   │ ┌─────┐┌─────┐┌─────┐┌─────┐                │
│ • DPC       │ │ 19  ││$2.5M││94.2%││ 847 │                │
│ • Retail    │ │Unis ││Ventas│Cumpl││Empl │ ← 4 CARDS      │
│ • Cadena    │ │🟢100%││🔼15%││🔼2.8%││🔻1.2%│                │
│ • Marketing │ └─────┘└─────┘└─────┘└─────┘                │
│ • [15 más]  │                                               │
│             │ ┌──────────────┐┌──────────────┐             │
│ HERRAM:     │ │ 📊 GRÁFICA   ││ 🍩 GRÁFICA   │             │
│ • Reportes  │ │   LÍNEAS     ││    DONA      │ ← 2 CHARTS  │
│ • Análisis  │ │              ││              │             │
│ • Config    │ └──────────────┘└──────────────┘             │
│             │                                               │
│             │ TABLA DE UNIDADES:                            │
│             │ ┌─────────────────────────────────────────┐   │
│             │ │Unidad│Reqs│Días│%Cumpl│Estado │Acciones│   │
│             │ │DPC   │ 5  │ 2  │ 98%  │🟢Activo│[Ver]   │   │
│             │ │Retail│ 12 │ 15 │ 87%  │🟡Atraso│[Ver]   │   │
│             │ │Cadena│ 8  │ 45 │ 23%  │🔴Crítico│[Ver]  │   │
│             │ └─────────────────────────────────────────┘   │
└─────────────────────────────────────────────────────────────┘
```

### INTERACCIONES:
- **Botón ☰:** Colapsa sidebar → contenido se expande
- **Cards de métricas:** Click → abre vista detallada de esa métrica
- **Botón [Ver] en tabla:** → Navega a vista de unidad específica
- **Filtros de fecha:** → Actualiza todas las gráficas y números

---

## 📋 PANTALLA 2: VISTA DE UNIDAD INDIVIDUAL

### LAYOUT:
```
┌─────────────────────────────────────────────────────────────┐
│ [☰] Intelligence Hub              🔍[Buscar...]  [Exportar] │
├─────────────────────────────────────────────────────────────┤
│ SIDEBAR     │ UNIDAD: DPC - Gabriela Mariñelarena          │
│             │                                               │
│ • Dashboard │ [Principal][Noticias][Reportes][Organigrama][Solicitudes] │
│ • Unidades  │ ────────── ← PESTAÑAS HORIZONTALES            │
│             │                                               │
│ UNIDADES:   │ 📝 PESTAÑA ACTIVA: PRINCIPAL                 │
│ ⚫ DPC      │                                               │ ← ACTIVA
│ • Retail    │ 📋 Últimos Reportes:                          │
│ • Cadena    │ ┌─────────────────────────────────────────┐   │
│ • Marketing │ │ • Reporte Ventas Q1 (hace 2 días)      │   │
│ • [15 más]  │ │ • Análisis Mercado (hace 5 días)       │   │
│             │ │ • Plan Marketing (hace 1 semana)       │   │
│ HERRAM:     │ └─────────────────────────────────────────┘   │
│ • Reportes  │                                               │
│ • Análisis  │ 💬 Comentarios Admin:                         │
│ • Config    │ ┌─────────────────────────────────────────┐   │
│             │ │ 📌 FIJADO: Revisar objetivos Q2        │   │
│             │ │ • Excelente trabajo en enero            │   │
│             │ │ • Pendiente: actualizar organigrama     │   │
│             │ └─────────────────────────────────────────┘   │
│             │                                               │
│             │ 📊 Métricas Rápidas:                          │
│             │ Solicitudes: 5 activas | 12 completadas      │
│             │ Última actualización: hace 2 días            │
└─────────────────────────────────────────────────────────────┘
```

### COMPORTAMIENTO DE PESTAÑAS:
- **Click en pestaña:** Cambia contenido inferior con animación
- **Badge rojo:** Aparece cuando hay actividad nueva (ej: "Noticias (3)")
- **Pestaña activa:** Subrayado azul y texto bold

---

## 📰 PANTALLA 3: PESTAÑA NOTICIAS

### LAYOUT:
```
│ [Principal][NOTICIAS][Reportes][Organigrama][Solicitudes] │
│ ─────────── ← PESTAÑA ACTIVA                              │
│                                                           │
│ [+ Nueva Noticia] [📌 Solo Fijadas] [🔍 Buscar]         │
│                                                           │
│ 📌 NOTICIAS FIJADAS:                                      │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 🔴 URGENTE: Cambio en proceso de reportes              │ │
│ │    Por: Admin | hace 3 horas | 👁️ 15 vistas           │ │
│ │    📌 [Desfijar] ✏️ [Editar] 🗑️ [Archivar]            │ │
│ └─────────────────────────────────────────────────────────┘ │
│                                                           │
│ 📰 TODAS LAS NOTICIAS:                                    │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 🔵 INFO: Nueva plantilla de reporte disponible         │ │
│ │    Por: Admin | hace 2 días | 👁️ 8 vistas             │ │
│ │    ✏️ [Editar] 🗑️ [Archivar] 📌 [Fijar]               │ │
│ └─────────────────────────────────────────────────────────┘ │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 🟡 CAMBIO: Nuevo responsable de área                   │ │
│ │    Por: Admin | hace 1 semana | 👁️ 22 vistas          │ │
│ │    ✏️ [Editar] 🗑️ [Archivar] 📌 [Fijar]               │ │
│ └─────────────────────────────────────────────────────────┘ │
```

### INTERACCIONES:
- **[+ Nueva Noticia]:** Abre modal con editor de texto
- **Badge de categoría:** 🔴 Urgente, 🔵 Info, 🟡 Cambio, 🟢 Anuncio
- **[Fijar]:** Mueve noticia arriba con distintivo 📌
- **Click en título:** Expande contenido completo

---

## 📊 PANTALLA 4: PESTAÑA REPORTES

### LAYOUT:
```
│ [Principal][Noticias][REPORTES][Organigrama][Solicitudes] │
│ ─────────── ← PESTAÑA ACTIVA                              │
│                                                           │
│ [📤 Subir Reporte] [📋 Nueva Plantilla] [📊 Estadísticas] │
│                                                           │
│ 🔍 Filtros: [Todos ▼] [2025 ▼] [PDF ▼] [Aprobados ▼]    │
│                                                           │
│ 📁 REPOSITORIO DE REPORTES:                               │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 📄 Reporte Ventas Q1.pdf                    v2.1       │ │
│ │    📅 15/01/2025 | 👤 Juan Pérez | ✅ Aprobado         │ │
│ │    💬 2 comentarios | 📥 [Descargar] ✏️ [Comentar]     │ │
│ └─────────────────────────────────────────────────────────┘ │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 📊 Análisis Mercado.xlsx                    v1.0       │ │
│ │    📅 10/01/2025 | 👤 María García | ⏳ Pendiente      │ │
│ │    💬 0 comentarios | 📥 [Descargar] ✏️ [Comentar]     │ │
│ └─────────────────────────────────────────────────────────┘ │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 📑 Plan Marketing.pptx                      v3.2       │ │
│ │    📅 08/01/2025 | 👤 Carlos López | ❌ Rechazado      │ │
│ │    💬 5 comentarios | 📥 [Descargar] ✏️ [Comentar]     │ │
│ └─────────────────────────────────────────────────────────┘ │
```

### INTERACCIONES:
- **[📤 Subir Reporte]:** Modal drag & drop para archivos
- **Click en nombre de archivo:** Preview del documento
- **Estados:** ✅ Aprobado (verde), ⏳ Pendiente (amarillo), ❌ Rechazado (rojo)
- **Versiones:** Sistema automático v1.0, v1.1, v2.0, etc.

---

## 👥 PANTALLA 5: PESTAÑA ORGANIGRAMA

### LAYOUT:
```
│ [Principal][Noticias][Reportes][ORGANIGRAMA][Solicitudes] │
│ ─────────── ← PESTAÑA ACTIVA                              │
│                                                           │
│ [✏️ Editar] [📥 Exportar PNG] [📄 Exportar PDF] [↶ Historial] │
│                                                           │
│ 🏢 ESTRUCTURA ORGANIZACIONAL:                             │
│                                                           │
│              ┌─────────────────┐                          │
│              │  DIRECTOR DPC   │                          │
│              │ Gabriela M.     │                          │
│              │ gm@bafar.com    │                          │
│              └─────────────────┘                          │
│                      │                                    │
│          ┌───────────┼───────────┐                        │
│          │           │           │                        │
│    ┌──────────┐ ┌──────────┐ ┌──────────┐               │
│    │SUPERVISOR│ │SUPERVISOR│ │SUPERVISOR│               │
│    │ Área A   │ │ Área B   │ │ Área C   │               │
│    │Juan P.   │ │María G.  │ │Carlos L. │               │
│    └──────────┘ └──────────┘ └──────────┘               │
│         │           │           │                        │
│    [5 empleados][8 empleados][3 empleados]               │
```

### INTERACCIONES:
- **[✏️ Editar]:** Activa modo drag & drop para mover cajas
- **Click en caja:** Abre popup para editar nombre, email, puesto
- **Líneas de conexión:** Se dibujan automáticamente
- **Zoom:** Scroll wheel para acercar/alejar

---

## 📝 PANTALLA 6: PESTAÑA SOLICITUDES

### LAYOUT:
```
│ [Principal][Noticias][Reportes][Organigrama][SOLICITUDES] │
│ ─────────── ← PESTAÑA ACTIVA                              │
│                                                           │
│ [+ Nueva Solicitud] [📊 Dashboard] [📋 Plantillas]       │
│                                                           │
│ 📊 RESUMEN: 5 Activas | 12 Completadas | 2 Vencidas     │
│                                                           │
│ 🔍 Filtros: [Todas ▼] [Alta Prioridad ▼] [Este Mes ▼]   │
│                                                           │
│ 📋 SOLICITUDES ACTIVAS:                                   │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 🔴 VENCIDA: Reporte financiero mensual                 │ │
│ │    📅 Vencía: 20/01/2025 (hace 5 días)                │ │
│ │    👤 Solicitado por: Director Finanzas                │ │
│ │    👷 Asignado a: Juan Pérez                           │ │
│ │    📄 Formato: Excel | 🔄 Mensual | ⚠️ Alta prioridad  │ │
│ │    [⚠️ Escalar] [💬 Comentar] [✅ Completar]           │ │
│ └─────────────────────────────────────────────────────────┘ │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 🟡 EN PROCESO: Análisis de ventas Q1                   │ │
│ │    📅 Vence: 30/01/2025 (en 5 días)                   │ │
│ │    👤 Solicitado por: Gerente Comercial                │ │
│ │    👷 Asignado a: María García                         │ │
│ │    📄 Formato: PowerPoint | 🔄 Trimestral | 🔵 Media   │ │
│ │    [💬 Comentar] [✅ Completar] [📅 Extender]          │ │
│ └─────────────────────────────────────────────────────────┘ │
│ ┌─────────────────────────────────────────────────────────┐ │
│ │ 🟢 NUEVA: Dashboard de KPIs                            │ │
│ │    📅 Vence: 15/02/2025 (en 20 días)                  │ │
│ │    👤 Solicitado por: Subdirector                      │ │
│ │    👷 Asignado a: Carlos López                         │ │
│ │    📄 Formato: Excel | 🔄 Una vez | 🔵 Media prioridad │ │
│ │    [💬 Comentar] [✅ Completar] [📝 Editar]            │ │
│ └─────────────────────────────────────────────────────────┘ │
```

### INTERACCIONES:
- **Estados visuales:** 🔴 Vencida, 🟡 En proceso, 🟢 Nueva
- **[+ Nueva Solicitud]:** Abre formulario wizard paso a paso
- **[⚠️ Escalar]:** Envía notificación al supervisor inmediato
- **[✅ Completar]:** Marca como completada y pide archivo adjunto

---

## 📝 MODAL: NUEVA SOLICITUD

### LAYOUT:
```
┌─────────────────────────────────────────────────────────┐
│ ✖️              Nueva Solicitud de Información          │
├─────────────────────────────────────────────────────────┤
│                                                         │
│ Paso 1 de 4: Información Básica                        │
│ ●●●○                                                    │
│                                                         │
│ 📝 Título de la solicitud: *                           │
│ [_________________________________]                    │
│                                                         │
│ 📋 Descripción detallada: *                            │
│ [_________________________________]                    │
│ [_________________________________]                    │
│ [_________________________________]                    │
│                                                         │
│ 🎯 ¿Para qué se necesita? (Justificación): *           │
│ [_________________________________]                    │
│ [_________________________________]                    │
│                                                         │
│ 📊 Formato de entrega: *                               │
│ ○ Excel    ○ PDF    ○ PowerPoint    ○ Word    ○ Otro   │
│                                                         │
│                         [Cancelar] [Siguiente →]       │
└─────────────────────────────────────────────────────────┘
```

### FLUJO DEL WIZARD:
**Paso 1:** Información básica (título, descripción, justificación, formato)
**Paso 2:** Fechas y frecuencia (fecha límite, recurrente?, prioridad)  
**Paso 3:** Asignación (responsable, supervisor, notificaciones)
**Paso 4:** Confirmación (resumen de todo, botón "Crear Solicitud")

---

## 🎨 ESTADOS Y ANIMACIONES

### HOVER EFFECTS:
- **Botones:** Sombra sutil + lift (2px hacia arriba)
- **Cards:** Borde azul + sombra más marcada
- **Filas de tabla:** Background gris muy claro

### LOADING STATES:
- **Gráficas:** Skeleton placeholder gris con shimmer
- **Tablas:** Filas vacías con skeleton text
- **Botones:** Spinner dentro + texto "Cargando..."

### NOTIFICACIONES TOAST:
```
┌─────────────────────────────────────┐
│ ✅ Solicitud creada exitosamente    │ ← Verde, 3 segundos
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ ⚠️ Faltan campos obligatorios       │ ← Amarillo, manual
└─────────────────────────────────────┘

┌─────────────────────────────────────┐
│ ❌ Error al subir archivo           │ ← Rojo, manual
└─────────────────────────────────────┘
```

---

## 📐 MEDIDAS Y ESPACIADO

### TAMAÑOS:
- **Header:** Altura 64px
- **Sidebar:** Ancho 256px
- **Botones:** Altura 36px, padding 0-24px
- **Cards:** border-radius 8px
- **Inputs:** Altura 36px

### TIPOGRAFÍA:
- **Títulos grandes:** 24px Google Sans
- **Títulos cards:** 16px Google Sans Medium
- **Texto normal:** 14px Roboto
- **Texto pequeño:** 12px Roboto

### ICONOS:
- **Navegación:** 20x20px
- **Botones:** 16x16px
- **Estados:** 12x12px (círculos de colores)

---

## 💡 NOTAS PARA EL DISEÑADOR

1. **Usar Google Material Icons** para todos los iconos
2. **Sombras sutiles** estilo Google (no muy marcadas)
3. **Espaciado consistente:** Múltiplos de 8px (8, 16, 24, 32...)
4. **Responsive:** Mobile collapse sidebar a drawer overlay
5. **Estados vacíos:** Mostrar ilustraciones + texto explicativo
6. **Breadcrumbs:** Mostrar ruta actual en páginas internas
7. **Loading:** Usar skeleton screens en vez de spinners cuando sea posible

**HERRAMIENTAS RECOMENDADAS:**
- Figma o Adobe XD para wireframes
- Material Design color palette
- Google Fonts (Google Sans + Roboto)
- Material Icons library

---

*Esta guía cubre todos los screens principales y comportamientos para crear mockups completos*