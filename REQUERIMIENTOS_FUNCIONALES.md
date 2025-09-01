# REQUERIMIENTOS FUNCIONALES - INTELLIGENCE HUB
## BAFAR - Plataforma de Gestión de Unidades de Negocio

---

## 📋 INFORMACIÓN DEL PROYECTO

**Proyecto:** Intelligence Hub - BAFAR  
**Versión:** 2.0  
**Fecha:** Agosto 2025  
**Cliente:** Grupo Bafar  
**Tipo:** Plataforma web de gestión empresarial  

---

## 🎯 OBJETIVO GENERAL

Desarrollar una plataforma web moderna tipo Google Material Design que permita la gestión, monitoreo y análisis de las 19 unidades de negocio de Grupo Bafar, proporcionando dashboards interactivos, reportes en tiempo real y herramientas de exportación.

---

## 👥 USUARIOS OBJETIVO

- **Administradores:** Acceso total a todas las unidades, modificar, agregar y borrar unidades y pestañas o archivos dentro de ahi
- **Responsables de Unidad:** Acceso a su unidad específica como editor
- **Directivos:** Vista consolidada y reportes ejecutivs de todas las unidades asi como la funcion de hacer solicitudes como un dash o una infomracion en espeficico 


---

## 🏗️ ARQUITECTURA REQUERIDA

### Frontend
- **Framework:** HTML5, CSS3, JavaScript (ES6+)
- **Diseño:** Google Material Design
- **Responsive:** Mobile-first design
- **Librerías:** Chart.js, XLSX.js

### Backend (Opcional - Fase 2)
- **API REST:** Node.js/Express o Python/Flask
- **Base de datos:** PostgreSQL o MongoDB
- **Autenticación:** JWT + OAuth2

### Hosting
- **Opción 1:** Servidor web estático (GitHub Pages, Netlify)
- **Opción 2:** Firebase Hosting + Firestore
- **Opción 3:** Servidor corporativo interno

---

## 📱 REQUERIMIENTOS DE INTERFAZ

### 1. HEADER (Barra Superior)
```
┌─────────────────────────────────────────────────────────────────┐
│ [☰] Intelligence Hub    [🔍 Buscar...]        [📤 Exportar] │
└─────────────────────────────────────────────────────────────────┘
```

**Elementos:**
- **Botón de menú hamburguesa (☰):**
  - Al hacer clic: Colapsa/expande el sidebar
  - Animación suave de 0.3s
  - Cambia icono a "X" cuando sidebar está abierto

- **Logo y título "Intelligence Hub":**
  - Logo: Ícono con gradiente azul-verde
  - Texto: Font Google Sans, 22px
  - Al hacer clic: Regresa al dashboard principal

- **Barra de búsqueda:**
  - Placeholder: "Buscar unidad de negocio..."
  - Búsqueda en tiempo real (debounce 300ms)
  - Filtrar por: nombre de unidad, responsable
  - Resultados destacados en amarillo
  - Escape/click afuera para cerrar

- **Botón Exportar:**
  - Ícono de descarga
  - Color: Azul Google (#1a73e8)
  - Al hacer clic: Genera archivo Excel de la vista actual
  - Toast notification: "Exportando..." → "Archivo descargado"
  - Nombre archivo: "IntelligenceHub_YYYY-MM-DD.xlsx"

### 2. SIDEBAR (Panel Lateral)
```
┌─────────────────────┐
│ PRINCIPAL           │
│ • Dashboard         │
│ • Unidades          │
│                     │
│ UNIDADES NEGOCIO    │
│ • DPC               │
│ • Retail            │
│ • Cadena suministro │
│ • [... 16 más]      │
│                     │
│ HERRAMIENTAS        │
│ • Reportes          │
│ • Análisis          │
│ • Configuración     │
└─────────────────────┘
```

**Comportamiento:**
- **Ancho:** 256px (expandido) / 0px (colapsado)
- **Animación:** Transform translateX con ease 0.3s
- **Secciones:**
  
  **A) PRINCIPAL**
  - Dashboard: Vista general con métricas
  - Unidades: Vista de tabla con todas las unidades
  
  **B) UNIDADES DE NEGOCIO (19 unidades)**
  - Cada unidad es un enlace individual
  - Al hacer clic: Abre vista detallada de la unidad
  - Ícono: Círculo con checkmark verde
  - Scroll vertical si no caben todas
  
  **C) HERRAMIENTAS**
  - Reportes: Generación de reportes customizados
  - Análisis: Gráficas comparativas avanzadas
  - Configuración: Ajustes del sistema

**Estados visuales:**
- **Item activo:** Fondo azul claro (#e8f0fe), texto azul (#1967d2)
- **Hover:** Fondo gris claro (#f1f3f4)
- **Normal:** Texto gris (#5f6368)

### 3. ÁREA PRINCIPAL DE CONTENIDO

#### 3.1 DASHBOARD PRINCIPAL
```
┌─────────────────────────────────────────────────────────────────┐
│ Dashboard General                                               │
│                                                                 │
│ [📅 Fecha inicio] hasta [📅 Fecha fin] [Filtrar] [Exportar]   │
│                                                                 │
│ ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐               │
│ │   19    │ │ $2.5M   │ │ 94.2%   │ │  847    │               │
│ │Unidades │ │Ventas   │ │Cumplim. │ │Empleados│               │
│ │ 100%↑   │ │+15.3%↑  │ │+2.8%↑   │ │-1.2%↓   │               │
│ └─────────┘ └─────────┘ └─────────┘ └─────────┘               │
│                                                                 │
│ ┌────────────────────┐ ┌────────────────────┐                  │
│ │ Tendencia Ventas   │ │ Distribución       │                  │
│ │ [📊 Gráfica línea] │ │ [🍩 Gráfica dona]  │                  │
│ └────────────────────┘ └────────────────────┘                  │
│                                                                 │
│ ┌─────────────────────────────────────────────────────────────┐ │
│ │ Resumen Unidades                        [+ Agregar Unidad] │ │
│ │ ┌─────────────────────────────────────────────────────────┐ │ │
│ │ │ Unidad    │Responsable│Frecuencia│Estado  │Acciones    │ │ │
│ │ │ DPC       │Gabriela M.│Semanal   │🟢Activo│[Ver detalles]│ │ │
│ │ │ Retail    │David V.   │Semanal   │🟢Activo│[Ver detalles]│ │ │
│ │ │ ...       │...        │...       │...     │...        │ │ │
│ │ └─────────────────────────────────────────────────────────┘ │ │
│ └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

**FILTROS DE FECHA:**
- **Input Fecha Inicio:** 
  - Tipo: date
  - Valor por defecto: 30 días atrás
  - Formato: YYYY-MM-DD
  - Al cambiar: Actualiza gráficas automáticamente

- **Input Fecha Fin:**
  - Tipo: date  
  - Valor por defecto: Hoy
  - Formato: YYYY-MM-DD
  - Al cambiar: Actualiza gráficas automáticamente

- **Botón Filtrar:**
  - Al hacer clic: Aplica filtros de fecha
  - Muestra spinner de carga 2 segundos
  - Toast: "Filtros aplicados: DD/MM/YYYY - DD/MM/YYYY"
  - Actualiza todas las métricas y gráficas

**TARJETAS DE MÉTRICAS (4 tarjetas):**
1. **Unidades Totales**
   - Valor: Número de unidades activas
   - Tendencia: % de unidades activas vs total
   - Color indicador: Verde (positivo) / Rojo (negativo)

2. **Ventas del Mes**
   - Valor: Suma total en formato moneda ($X.XM)
   - Tendencia: % cambio vs mes anterior
   - Al hacer clic: Abre desglose de ventas por unidad

3. **Cumplimiento Promedio**
   - Valor: % promedio de cumplimiento de objetivos
   - Tendencia: % cambio vs período anterior
   - Al hacer clic: Abre vista de cumplimiento detallada

4. **Total Empleados**
   - Valor: Suma de empleados de todas las unidades
   - Tendencia: % cambio vs período anterior
   - Al hacer clic: Abre desglose de personal por unidad

**GRÁFICAS:**
1. **Tendencia de Ventas (Línea)**
   - Librerla: Chart.js
   - Datos: Ventas mensuales últimos 6 meses
   - Ejes: X (meses), Y (ventas en millones)
   - Interactividad: Tooltip al hover
   - Chips de período: [Semana] [Mes] [Año]
   - Al cambiar chip: Actualiza datos de la gráfica

2. **Distribución por Unidad (Dona)**
   - Librería: Chart.js
   - Datos: % de ventas por unidad (top 5 + "Otros")
   - Colores: Paleta Google Material
   - Interactividad: Click en segmento resalta unidad
   - Leyenda: Abajo con porcentajes

**TABLA RESUMEN UNIDADES:**
- **Columnas:** 
  - Unidad (nombre, bold)
  - Responsable (nombre completo)
  - Frecuencia (Diaria/Semanal/Mensual/etc)
  - Estado (chip verde/amarillo/rojo)
  - Acciones (botón "Ver detalles")

- **Funcionalidades:**
  - Ordenamiento: Click en header para ordenar
  - Búsqueda: Filtro en tiempo real desde header
  - Paginación: 10 elementos por página
  - Hover: Fila resaltada en gris claro

- **Botón "Agregar Unidad":**
  - Posición: Top-right de la tabla
  - Al hacer clic: Abre modal/formulario
  - Modal incluye: Nombre, Responsable, Email, Frecuencia, etc.

#### 3.2 VISTA DE UNIDADES
```
┌─────────────────────────────────────────────────────────────────┐
│ Unidades de Negocio                                             │
│                                                                 │
│ [DPC] [Retail] [Cadena] [Marketing] [CAAS] [Capital Humano]... │
│                                                                 │
│ ┌─────────────────────────────────────────────────────────────┐ │
│ │ DPC                                          [Editar]       │ │
│ │ ┌─────────────────┐ ┌─────────────────────────────────────┐ │ │
│ │ │ Responsable:    │ │ Ubicación: México                   │ │ │
│ │ │ Gabriela M.     │ │ Presupuesto: $500K                  │ │ │
│ │ │ Email:          │ │ Empleados: 45                       │ │ │
│ │ │ gm@bafar.com    │ │ Ingresos: $1.2M                     │ │ │
│ │ │ Frecuencia:     │ │                                     │ │ │
│ │ │ Semanal         │ │                                     │ │ │
│ │ └─────────────────┘ └─────────────────────────────────────┘ │ │
│ └─────────────────────────────────────────────────────────────┘ │
└─────────────────────────────────────────────────────────────────┘
```

**TABS DE UNIDADES:**
- Diseño: Pills horizontales scrolleables
- Primera unidad: Activa por defecto
- Al hacer clic: Cambia contenido inferior
- Animación: Transición suave 0.3s

**DETALLE DE UNIDAD:**
- **Card principal** con información dividida en 2 columnas
- **Información básica (izquierda):**
  - Responsable: Nombre completo + puesto
  - Email: Link mailto al hacer clic
  - Frecuencia: Periodicidad de reportes
  - Estado: Chip con color

- **Métricas (derecha):**
  - Ubicación: Sede/ciudad principal
  - Presupuesto: Presupuesto anual asignado
  - Empleados: Número total de empleados
  - Ingresos: Ingresos generados YTD

- **Botón Editar:**
  - Posición: Top-right del card
  - Al hacer clic: Abre modal de edición
  - Modal: Formulario con todos los campos editables

---

## 🔧 REQUERIMIENTOS FUNCIONALES DETALLADOS

### RF-01: AUTENTICACIÓN (Opcional - Fase 2)
- Login con email/password corporativo
- Recuperación de contraseña vía email
- Sesión persistente (7 días)
- Logout manual y automático (inactividad)

### RF-02: NAVEGACIÓN
- **RF-02.1:** Sidebar colapsable con animación suave
- **RF-02.2:** Breadcrumb trail en páginas internas
- **RF-02.3:** Navegación responsive (mobile hamburger menu)
- **RF-02.4:** Deep linking (URLs únicas para cada vista)

### RF-03: BÚSQUEDA
- **RF-03.1:** Búsqueda global en header (unidades + responsables)
- **RF-03.2:** Debounce de 300ms para optimizar rendimiento  
- **RF-03.3:** Destacado de resultados (match highlighting)
- **RF-03.4:** Búsqueda por múltiples criterios

### RF-04: DASHBOARD
- **RF-04.1:** 4 métricas principales con tendencias
- **RF-04.2:** Gráficas interactivas (Chart.js)
- **RF-04.3:** Filtros de fecha con recarga automática
- **RF-04.4:** Actualización en tiempo real (polling cada 30s)

### RF-05: GESTIÓN DE UNIDADES
- **RF-05.1:** CRUD completo de unidades
- **RF-05.2:** Vista de detalle individual por unidad
- **RF-05.3:** Validación de datos obligatorios
- **RF-05.4:** Historial de cambios (audit log)

### RF-06: EXPORTACIÓN
- **RF-06.1:** Exportar a Excel (XLSX)
- **RF-06.2:** Exportar vista actual o datos filtrados
- **RF-06.3:** Múltiples hojas: Dashboard, Unidades, Detalles
- **RF-06.4:** Nombres de archivo con timestamp

### RF-07: NOTIFICACIONES
- **RF-07.1:** Toast notifications para acciones exitosas
- **RF-07.2:** Notificaciones de error con descripción
- **RF-07.3:** Loading states en todas las acciones async
- **RF-07.4:** Progress bars para operaciones largas

### RF-08: RESPONSIVIDAD
- **RF-08.1:** Mobile-first design (320px mínimo)
- **RF-08.2:** Tablet optimization (768px - 1024px)
- **RF-08.3:** Desktop optimization (1024px+)
- **RF-08.4:** Touch-friendly buttons (44px mínimo)

---

## ⚡ REQUERIMIENTOS NO FUNCIONALES

### Rendimiento
- **Carga inicial:** < 3 segundos
- **Navegación:** < 1 segundo entre páginas
- **Búsqueda:** Resultados en < 500ms
- **Exportación:** < 10 segundos para 1000 registros

### Compatibilidad
- **Navegadores:** Chrome 90+, Firefox 88+, Safari 14+, Edge 90+
- **Dispositivos:** Desktop, tablet, móvil
- **Resoluciones:** 320px a 2560px

### Seguridad
- **HTTPS obligatorio** en producción
- **Validación de inputs** en frontend y backend
- **Sanitización** de datos antes de mostrar
- **Control de acceso** basado en roles (Fase 2)

### UX/UI
- **Diseño:** Google Material Design 3.0
- **Tipografía:** Google Sans + Roboto
- **Paleta:** Colores corporativos + Google palette
- **Animaciones:** Smooth 0.3s ease transitions

---

## 📊 CASOS DE USO PRINCIPALES

### CU-01: Ver Dashboard General
**Actor:** Todos los usuarios  
**Flujo:**
1. Usuario accede a la aplicación
2. Se carga el dashboard por defecto
3. Se muestran 4 métricas principales
4. Se renderizan 2 gráficas interactivas
5. Se muestra tabla con resumen de unidades

### CU-02: Buscar Unidad Específica
**Actor:** Usuario administrativo  
**Flujo:**
1. Usuario escribe en barra de búsqueda
2. Sistema filtra resultados en tiempo real
3. Usuario hace clic en resultado
4. Se abre vista detallada de la unidad
5. Se muestra información completa

### CU-03: Exportar Datos a Excel
**Actor:** Analista/Director  
**Flujo:**
1. Usuario hace clic en botón "Exportar"
2. Sistema muestra toast "Exportando..."
3. Se genera archivo XLSX con datos actuales
4. Navegador descarga archivo automáticamente
5. Toast confirma: "Archivo descargado"

### CU-04: Filtrar por Fechas
**Actor:** Todos los usuarios  
**Flujo:**
1. Usuario selecciona fecha inicio
2. Usuario selecciona fecha fin
3. Usuario hace clic en "Filtrar"
4. Sistema actualiza métricas y gráficas
5. Toast confirma aplicación de filtros

### CU-05: Editar Información de Unidad
**Actor:** Administrador/Responsable de unidad  
**Flujo:**
1. Usuario navega a detalle de unidad
2. Usuario hace clic en "Editar"
3. Se abre modal con formulario
4. Usuario modifica campos necesarios
5. Usuario guarda cambios
6. Sistema valida y actualiza datos
7. Modal se cierra, vista se actualiza

---

## 📁 ESTRUCTURA DE DATOS

### Unidad de Negocio
```json
{
  "id": "number",
  "name": "string (requerido)",
  "responsible": "string (requerido)", 
  "email": "email (opcional)",
  "frequency": "enum (Diaria|Semanal|Quincenal|Mensual|Trimestral)",
  "status": "enum (Activo|Inactivo|Pendiente)",
  "location": "string (opcional)",
  "budget": "number (opcional)",
  "employees": "number (opcional)", 
  "revenue": "number (opcional)",
  "goals": "string (opcional)",
  "kpis": "array (opcional)",
  "createdAt": "datetime",
  "updatedAt": "datetime",
  "createdBy": "string"
}
```

### Métricas Dashboard
```json
{
  "totalUnits": "number",
  "activeUnits": "number", 
  "totalRevenue": "number",
  "avgCompliance": "number",
  "totalEmployees": "number",
  "trends": {
    "revenue": "number (% change)",
    "compliance": "number (% change)", 
    "employees": "number (% change)"
  }
}
```

---

## 🎨 ESPECIFICACIONES DE DISEÑO

### Paleta de Colores
```css
/* Colores principales */
--primary: #1a73e8;        /* Azul Google */
--primary-dark: #1765cc;
--accent: #34a853;         /* Verde Google */
--surface: #ffffff;
--background: #f8f9fa;
--text: #202124;
--text-secondary: #5f6368;
--border: #dadce0;

/* Colores funcionales */
--success: #34a853;
--warning: #fbbc04; 
--error: #ea4335;
--info: #4285f4;
```

### Tipografía
```css
/* Títulos */
h1: Google Sans, 24px, Regular
h2: Google Sans, 20px, Medium  
h3: Google Sans, 16px, Medium

/* Cuerpo */
body: Roboto, 14px, Regular
small: Roboto, 12px, Regular
```

### Componentes
- **Botones:** Altura 36px, border-radius 4px
- **Cards:** border-radius 8px, sombra sutil
- **Inputs:** Altura 36px, border Google style
- **Chips:** Altura 32px, border-radius 16px

---

## 🚀 PLAN DE DESARROLLO

### Fase 1 - Core (2-3 semanas)
- [x] Estructura HTML básica
- [x] CSS con Google Material Design  
- [x] JavaScript para navegación
- [x] Integración Chart.js
- [x] Exportación Excel
- [x] Datos estáticos (JSON)

### Fase 2 - Backend (1-2 semanas)
- [ ] API REST para CRUD unidades
- [ ] Base de datos PostgreSQL/MongoDB
- [ ] Autenticación JWT
- [ ] Validaciones servidor

### Fase 3 - Avanzado (1 semana)
- [ ] Tiempo real (WebSockets)
- [ ] Push notifications
- [ ] Reportes avanzados  
- [ ] Analytics/métricas de uso

### Fase 4 - Producción (1 semana)
- [ ] Testing automatizado
- [ ] CI/CD pipeline
- [ ] Deployment
- [ ] Monitoreo

---

## ✅ CRITERIOS DE ACEPTACIÓN

### Funcionalidad
- ✅ Todos los botones ejecutan su función esperada
- ✅ Navegación fluida sin errores 404
- ✅ Búsqueda funciona con términos parciales
- ✅ Exportación genera archivos válidos
- ✅ Formularios validan datos correctamente

### Rendimiento  
- ✅ Carga inicial < 3 segundos
- ✅ Sin memory leaks en navegación
- ✅ Responsive en todos los breakpoints
- ✅ Gráficas se renderizan < 2 segundos

### UX/UI
- ✅ Diseño consistente con Google Material
- ✅ Animaciones suaves y profesionales
- ✅ Feedback visual en todas las acciones
- ✅ Accesible con teclado y screen readers

### Calidad
- ✅ Código limpio y documentado
- ✅ Sin errores en consola del navegador
- ✅ Funciona offline (datos cached)
- ✅ Compatible con todos los navegadores target

---

## 📞 CONTACTO Y SOPORTE

**Desarrollador:** [Nombre del desarrollador]  
**Email:** [email@dominio.com]  
**Teléfono:** [+52 xxx xxx xxxx]  

**Cliente:** Grupo Bafar  
**Contacto técnico:** [Nombre contacto]  
**Email:** [contacto@bafar.com.mx]  

---

*Documento versión 1.0 - Agosto 2025*  
*© 2025 Grupo Bafar - Intelligence Hub Project*