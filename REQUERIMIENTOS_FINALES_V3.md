# REQUERIMIENTOS FUNCIONALES - INTELLIGENCE HUB V3.0
## Sistema Integral de Gestión de Unidades de Negocio - BAFAR

---

## 🎯 OBJETIVO GENERAL

Desarrollar una plataforma web moderna tipo Google Material Design que permita la gestión, monitoreo y análisis integral de las 19 unidades de negocio de Grupo Bafar, incluyendo dashboards detallados, gestión de solicitudes, reportes, noticias, organigramas y administración completa de proyectos.

---

## 📊 DASHBOARD PRINCIPAL - MÉTRICAS CONSOLIDADAS

### Información Crítica por Unidad:
- **Peticiones activas:** Solicitudes pendientes de cada unidad
- **Peticiones cumplidas:** Completadas en el período
- **Peticiones vencidas:** Que pasaron su fecha límite
- **Días sin actualización:** Desde último check de la unidad
- **Proyectos activos:** En curso por unidad
- **% Avance proyectos:** Progreso promedio de proyectos activos
- **Estado general:** Semáforo basado en métricas críticas

### Cards de Métricas Principales (6 cards):
1. **19 Unidades:** Total con % activas vs total
2. **$2.5M Ventas:** Ingresos del período con tendencia
3. **94.2% Cumplimiento:** Promedio de cumplimiento general
4. **847 Empleados:** Total de personal en todas las unidades
5. **127 Peticiones:** Total de solicitudes activas en sistema
6. **45 Proyectos:** Total de proyectos activos en curso

### Tabla de Unidades Detallada:
**Columnas:**
- Unidad (nombre)
- Pets Act (peticiones activas)
- Cumplidas (peticiones completadas)
- Vencidas (peticiones vencidas)
- Días Sin (días desde última actualización)
- Proy Act (proyectos activos)
- % Avance Proy (progreso promedio proyectos)
- Estado (🟢 Activo / 🟡 Atención / 🔴 Crítico)
- Última Check (fecha último check)
- Acciones (botón Ver detalles)

### Sistema de Alertas Automáticas:
- **🔴 Crítico:** +30 días sin actualizar OR >3 peticiones vencidas
- **🟡 Atención:** 15-30 días sin actualizar OR 1-2 peticiones vencidas
- **🟢 Activo:** <15 días sin actualizar AND todas las peticiones al día

---

## 🏢 ESTRUCTURA DE CADA UNIDAD DE NEGOCIO - 6 PESTAÑAS

### PESTAÑA 1: PRINCIPAL
**Contenido:**
- Resumen ejecutivo de la unidad con métricas clave
- Últimos reportes subidos (últimos 10 con fechas)
- Comentarios administrativos personalizables
- Próximas fechas importantes y deadlines
- Estado actual con indicadores de salud
- Alertas y notificaciones pendientes

### PESTAÑA 2: NOTICIAS
**Sistema completo de comunicación interna:**
- Feed cronológico de noticias con timestamps
- Sistema de noticias fijadas (siempre arriba)
- Categorización: 🔴 Urgente, 🔵 Info, 🟡 Cambios, 🟢 Anuncios
- Editor rich text para crear/editar noticias
- Programación de publicación futura
- Archivo automático de noticias antiguas
- Push notifications para noticias urgentes
- Contador de noticias no leídas por usuario
- Sistema de vistas y estadísticas de lectura

### PESTAÑA 3: REPORTES
**Repositorio documental completo:**
- Upload de archivos múltiples formatos (PDF, Excel, Word, PowerPoint)
- Sistema de versionado automático (v1.0, v1.1, v2.0...)
- Búsqueda avanzada por contenido y metadatos
- Sistema de aprobación/rechazo con comentarios
- Plantillas reutilizables de reportes frecuentes
- Compresión automática para archivos grandes
- Preview en línea para formatos compatibles
- Organización por categorías y etiquetas
- Historial completo de cambios y versiones

### PESTAÑA 4: ORGANIGRAMA
**Editor visual de estructura organizacional:**
- Editor drag & drop para crear/modificar estructura
- Información detallada de cada posición (nombre, email, puesto, responsabilidades)
- Exportación en múltiples formatos (PNG, PDF, SVG)
- Zoom in/out para organigramas complejos
- Plantillas predefinidas de estructuras organizacionales
- Integración con directorio de empleados
- Historial de cambios organizacionales con fechas
- Vista de responsabilidades por área

### PESTAÑA 5: SOLICITUDES DE INFORMACIÓN
**Sistema completo de gestión de requerimientos:**

#### Estructura de cada solicitud:
- **Qué se necesita:** Descripción detallada del requerimiento
- **Quién lo solicita:** Persona/área solicitante con datos de contacto
- **Para qué se necesita:** Justificación y propósito específico
- **Cuándo se necesita:** Fecha límite de entrega
- **Frecuencia:** Una vez, diario, semanal, mensual, trimestral, anual
- **Formato requerido:** Excel, PDF, PowerPoint, Word, otro
- **Responsable asignado:** Persona específica encargada de entregar
- **Prioridad:** Alta (🔴), Media (🟡), Baja (🟢)
- **Estado:** Pendiente, En Proceso, Completado, Vencido
- **Comentarios:** Historial de comunicación sobre la solicitud
- **Archivos adjuntos:** Documentos relacionados o entregables

#### Automatizaciones:
- **Asignación automática** de responsables basada en reglas
- **Recordatorios programados:**
  - 7 días antes del vencimiento
  - 3 días antes del vencimiento
  - 1 día antes del vencimiento
  - Alerta roja inmediata al vencerse
- **Escalamiento automático:** Si se vence +3 días, notifica al supervisor
- **Notificaciones push** para solicitudes críticas
- **Reportes automáticos** de cumplimiento semanal/mensual

### PESTAÑA 6: PROYECTOS ⭐ NUEVA
**Sistema integral de gestión de proyectos:**

#### Información General de Proyectos:
- **Nombre y descripción** del proyecto
- **Objetivos específicos** y entregables esperados
- **Fechas:** Inicio, fin planeado, fin real, hitos críticos
- **Presupuesto:** Asignado, gastado, disponible
- **Responsable principal** y equipo asignado
- **Estado:** 🟢 Nuevo, 🟡 En Proceso, 🔴 Crítico, ✅ Completado, ⏸️ En Pausa
- **Prioridad:** Alta, Media, Baja
- **% Progreso general** y por fases

#### Gestión por Fases:
- **División del proyecto** en fases/etapas específicas
- **Progreso individual** por cada fase (0-100%)
- **Dependencias** entre fases (Fase A antes que Fase B)
- **Entregables específicos** por fase
- **Fechas de inicio/fin** por fase
- **Responsable** de cada fase

#### Sistema de Actividades/Tareas:
- **Lista detallada de actividades** con fechas y responsables
- **Check-list de entregables** por actividad
- **Dependencias entre actividades** claramente definidas
- **Comentarios y notas** en cada actividad
- **Adjuntos** por actividad (documentos, imágenes, etc.)
- **Notificaciones automáticas** cuando se completa actividad

#### Gestión de Archivos del Proyecto:
- **Upload múltiple** de documentos relacionados
- **Organización por categorías:** Contratos, Reportes, Presentaciones, Técnicos
- **Control de versiones** automático
- **Control de acceso:** Solo equipo del proyecto accede a archivos
- **Preview en línea** para formatos compatibles
- **Búsqueda dentro de archivos** del proyecto

#### Timeline/Cronograma Visual:
- **Vista Gantt** con barras de tiempo por fase
- **Dependencias visuales** entre actividades
- **Hitos críticos** destacados en timeline
- **Línea de "hoy"** para identificar retrasos
- **Zoom temporal:** Vista por semanas, meses o proyecto completo
- **Identificación visual** de actividades críticas

#### Dashboard de Proyectos:
- **Resumen ejecutivo** de todos los proyectos de la unidad
- **Gráficas de progreso:** General, por estado, timeline
- **Métricas clave:** Proyectos a tiempo, atrasados, completados
- **Filtros avanzados:** Por responsable, fecha, presupuesto, estado
- **Alertas:** Proyectos próximos a vencer, sobrepresupuesto
- **Exportación:** Reporte Excel consolidado de proyectos

---

## 🔧 REQUERIMIENTOS FUNCIONALES ESPECÍFICOS

### RF-011: Dashboard Principal Mejorado
- Mostrar 6 métricas principales en cards interactivos
- Tabla expandida con 9 columnas de información crítica
- Sistema de alertas automáticas por colores (verde/amarillo/rojo)
- Filtros por estado, fecha, unidad específica
- Gráficas actualizadas: tendencia de peticiones y distribución de proyectos
- Exportación de reporte consolidado con todas las métricas

### RF-012: Sistema Integral de Noticias
- CRUD completo con editor rich text
- Sistema de categorización y priorización
- Funcionalidad de fijar/desfijar noticias importantes
- Programación de publicación y archivo automático
- Push notifications configurables por tipo de noticia
- Analytics de lectura por noticia y usuario
- Búsqueda avanzada en historial de noticias

### RF-013: Repositorio de Reportes Avanzado
- Upload con drag & drop múltiple
- Versionado automático inteligente
- Sistema de workflow: borrador → revisión → aprobado/rechazado
- Plantillas reutilizables con campos predefinidos
- Búsqueda full-text dentro de documentos
- Compresión y optimización automática
- Control granular de permisos por reporte

### RF-014: Editor de Organigrama Visual
- Interfaz drag & drop intuitiva
- Templates de estructuras organizacionales comunes
- Exportación en formatos múltiples (PNG, PDF, SVG, Excel)
- Integración con base de datos de empleados
- Histórico de cambios con fechas y responsables
- Vista imprimible optimizada
- Función de búsqueda dentro del organigrama

### RF-015: Gestión Avanzada de Solicitudes
- Formulario wizard paso a paso para crear solicitudes
- Sistema de templates para solicitudes recurrentes
- Motor de reglas para asignación automática
- Escalamiento multinivel configurable
- Dashboard personalizado por rol (solicitante/responsable/supervisor)
- Reportes de productividad y cumplimiento
- Integración con calendario para deadlines

### RF-016: Sistema Completo de Proyectos ⭐ NUEVO
- **Gestión de proyectos:** CRUD completo con wizard de creación
- **Fases y actividades:** Estructura jerárquica configurable
- **Timeline visual:** Vista Gantt interactiva con dependencias
- **Gestión presupuestaria:** Control de costos por fase y total
- **Colaboración:** Comentarios, adjuntos, notificaciones
- **Reportes:** Dashboard ejecutivo y reportes detallados
- **Templates:** Plantillas de proyectos por tipo común
- **Control de calidad:** Sistema de aprobaciones por fase

### RF-017: Sistema de Notificaciones Avanzado
- **En tiempo real:** WebSockets para notificaciones instantáneas
- **Email programado:** Resúmenes diarios, semanales, mensuales
- **Push notifications:** Para eventos críticos y urgentes
- **Centro de notificaciones:** Hub central con historial
- **Configuración granular:** Preferencias por tipo y frecuencia
- **Badges:** Contadores de actividad nueva en pestañas
- **Escalamiento:** Notificaciones automáticas a supervisores

---

## 📋 ESTRUCTURA DE DATOS ACTUALIZADA

### Unidad de Negocio (Actualizada)
```json
{
  "id": "string",
  "name": "string", 
  "responsible": "string",
  "email": "string",
  "status": "Activo|Atención|Crítico",
  "lastUpdated": "datetime",
  "daysSinceUpdate": "number",
  "activeRequests": "number",
  "completedRequests": "number",
  "overdueRequests": "number", 
  "complianceRate": "number",
  "activeProjects": "number",
  "projectsProgress": "number",
  "newsCount": "number",
  "reportsCount": "number",
  "employees": "number",
  "budget": "number",
  "revenue": "number"
}
```

### Proyecto (Nueva entidad)
```json
{
  "id": "string",
  "unitId": "string",
  "name": "string",
  "description": "text",
  "objectives": "array",
  "startDate": "datetime",
  "plannedEndDate": "datetime", 
  "actualEndDate": "datetime",
  "budget": "number",
  "spent": "number",
  "manager": "string",
  "team": "array",
  "status": "New|InProgress|Critical|Completed|Paused",
  "priority": "High|Medium|Low",
  "overallProgress": "number",
  "phases": "array",
  "activities": "array", 
  "files": "array",
  "comments": "array",
  "risks": "array",
  "createdAt": "datetime",
  "updatedAt": "datetime"
}
```

### Fase de Proyecto (Nueva entidad)
```json
{
  "id": "string",
  "projectId": "string",
  "name": "string",
  "description": "text", 
  "startDate": "datetime",
  "endDate": "datetime",
  "progress": "number",
  "status": "NotStarted|InProgress|Completed|Blocked",
  "responsible": "string",
  "deliverables": "array",
  "dependencies": "array",
  "budget": "number",
  "activities": "array"
}
```

### Actividad de Proyecto (Nueva entidad)
```json
{
  "id": "string",
  "phaseId": "string",
  "projectId": "string",
  "name": "string",
  "description": "text",
  "startDate": "datetime", 
  "endDate": "datetime",
  "estimatedHours": "number",
  "actualHours": "number",
  "assignedTo": "string",
  "status": "NotStarted|InProgress|Completed|Blocked",
  "priority": "High|Medium|Low",
  "dependencies": "array",
  "deliverables": "array",
  "files": "array",
  "comments": "array"
}
```

---

## 🎨 ESPECIFICACIONES DE DISEÑO

### Paleta de Colores (Actualizada)
```css
/* Colores principales */
--primary: #1a73e8;        /* Azul Google */
--primary-dark: #1565c0;
--accent: #34a853;         /* Verde Google */
--warning: #fbbc04;        /* Amarillo Google */
--error: #ea4335;          /* Rojo Google */

/* Estados de proyectos */
--new: #4caf50;           /* Verde nuevo */
--in-progress: #ff9800;   /* Naranja proceso */
--critical: #f44336;      /* Rojo crítico */  
--completed: #9c27b0;     /* Morado completado */
--paused: #607d8b;        /* Gris pausado */

/* Estados de unidades */
--active: #4caf50;        /* Verde activo */
--attention: #ff9800;     /* Naranja atención */
--critical-unit: #f44336; /* Rojo crítico */
```

### Componentes Nuevos
- **Cards de proyecto:** Con barra de progreso visual
- **Timeline Gantt:** Barras horizontales con dependencias
- **Wizard de formularios:** Multi-paso con navegación
- **Badges de actividad:** Contadores numéricos en pestañas
- **Progress bars:** Circulares y lineales para proyectos
- **Chips de estado:** Con colores específicos por estado

---

## ⚡ FLUJOS DE TRABAJO CRÍTICOS

### Flujo 1: Seguimiento Automático de Unidades
1. Sistema ejecuta proceso diario a las 6:00 AM
2. Calcula días desde última actualización de cada unidad
3. Cuenta peticiones vencidas y proyectos atrasados
4. Actualiza estado de semáforo (verde/amarillo/rojo)
5. Envía alertas automáticas a responsables de unidades críticas
6. Genera reporte ejecutivo para dirección
7. Programa seguimiento escalado si persiste estado crítico

### Flujo 2: Gestión Completa de Proyectos
1. Usuario crea nuevo proyecto con wizard paso a paso
2. Sistema asigna ID único y configura estructura de fases
3. Se crean actividades automáticamente basadas en template
4. Sistema programa recordatorios para hitos críticos
5. Notificaciones automáticas a equipo asignado
6. Seguimiento diario de progreso y actualización de métricas
7. Alertas automáticas por retrasos o desviaciones presupuestarias
8. Reportes semanales de avance a stakeholders

### Flujo 3: Escalamiento de Solicitudes Críticas
1. Sistema identifica solicitud vencida +3 días
2. Marca como "Crítica" y notifica al responsable inmediato
3. Si no hay respuesta en 24 horas, escala al supervisor
4. Supervisor recibe notificación con contexto completo
5. Si supervisor no actúa en 48 horas, escala a dirección
6. Se genera reporte de incidencia para auditoría
7. Sistema programa revisión de procesos si es patrón recurrente

---

## 📊 MÉTRICAS Y KPIs PRINCIPALES

### Dashboard Ejecutivo:
- **Índice de salud general:** Promedio ponderado de todas las unidades
- **Tiempo promedio de respuesta:** Para solicitudes por unidad
- **Tasa de cumplimiento:** % de solicitudes completadas a tiempo
- **Eficiencia de proyectos:** % de proyectos completados dentro de presupuesto y tiempo
- **Participación:** % de usuarios activos vs total registrados
- **Crecimiento:** Tendencia de métricas mes a mes

### Por Unidad de Negocio:
- **Score de salud:** Algoritmo que considera múltiples factores
- **Productividad:** Solicitudes completadas vs asignadas
- **Calidad:** % de reportes aprobados en primera revisión
- **Colaboración:** Participación en sistema de comentarios/noticias
- **Innovación:** Número de proyectos nuevos iniciados

---

## 🎯 CRITERIOS DE ACEPTACIÓN ACTUALIZADOS

### Funcionalidad Core:
- ✅ Dashboard principal carga todas las métricas en <3 segundos
- ✅ Sistema de proyectos maneja hasta 100 proyectos simultáneos
- ✅ Notificaciones llegan en <30 segundos desde evento
- ✅ Búsqueda global devuelve resultados en <1 segundo
- ✅ Exportaciones se generan en <15 segundos

### Gestión de Proyectos:
- ✅ Timeline Gantt se renderiza para proyectos de hasta 50 actividades
- ✅ Drag & drop funciona fluidamente en editores visuales
- ✅ Cálculo automático de fechas críticas y dependencias
- ✅ Upload de archivos hasta 100MB por proyecto
- ✅ Sincronización en tiempo real entre colaboradores

### Rendimiento y Escalabilidad:
- ✅ Soporte para 100 usuarios concurrentes
- ✅ Base de datos optimizada para 50,000 registros combinados
- ✅ Tiempo de respuesta <2 segundos para cualquier operación
- ✅ Backup automático sin afectar rendimiento
- ✅ Recuperación ante fallas en <2 horas

---

## 🚀 PLAN DE DESARROLLO ACTUALIZADO

### Fase 1 - Core y Dashboard (3-4 semanas)
- Dashboard principal con métricas detalladas
- Sistema básico de 5 pestañas originales
- CRUD de solicitudes y noticias
- Notificaciones básicas

### Fase 2 - Proyectos y Avanzado (3-4 semanas)
- Sistema completo de gestión de proyectos
- Timeline Gantt interactivo
- Repositorio avanzado de reportes
- Editor de organigrama visual
- Sistema de permisos granular

### Fase 3 - Automatización e Integración (2-3 semanas)
- Recordatorios y escalamientos automáticos
- Reportes programados y analytics
- API para integraciones externas
- Optimizaciones de rendimiento
- Testing comprehensivo

### Fase 4 - Producción y Mantenimiento (1-2 semanas)
- Deployment en servidores de producción
- Configuración de backups y monitoreo
- Capacitación a usuarios finales
- Documentación técnica y de usuario
- Soporte post-lanzamiento

---

## 📈 ESTIMACIÓN FINAL

**TOTAL ESTIMADO: 9-13 semanas de desarrollo**

**COMPLEJIDAD: Muy Alta** (por integración de sistema completo de proyectos)

**EQUIPO RECOMENDADO:**
- 1 Desarrollador Full-Stack Senior (backend + frontend)
- 1 Desarrollador Frontend (UX/UI especializado)
- 1 Diseñador UX/UI (wireframes y mockups)
- 1 Project Manager/QA (opcional pero recomendado)

**TECNOLOGÍAS SUGERIDAS:**
- **Frontend:** React.js/Vue.js + Material-UI
- **Backend:** Node.js/Express + PostgreSQL
- **Gráficas:** Chart.js + D3.js (para Gantt)
- **Hosting:** AWS/Azure con CDN
- **Notificaciones:** Socket.io + EmailJS

---

**DOCUMENTO VERSIÓN 3.0 - Agosto 2025**  
**© 2025 Grupo Bafar - Intelligence Hub Project**

*Este documento incluye todas las funcionalidades solicitadas incluyendo métricas detalladas por unidad, sistema completo de gestión de proyectos, y especificaciones técnicas para desarrollo.*