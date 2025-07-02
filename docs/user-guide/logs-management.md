# Gestión de Logs de Fail2Ban

La sección de logs es fundamental para monitorear la actividad de seguridad en tiempo real y analizar patrones de ataques.

## :page_facing_up: Vista General de Logs

### Pantalla Principal

![Placeholder: Vista completa de la gestión de logs](assets/logs-management-full.png)

La sección de logs está dividida en:

1. **Estadísticas Generales** - Métricas rápidas del sistema
2. **Herramientas de Filtrado** - Búsqueda y filtros avanzados
3. **Tabla de Logs** - Visualización detallada de eventos
4. **Panel de Detalles** - Información específica de eventos

## :1234: Estadísticas de Logs

### Métricas Principales

![Placeholder: Tarjetas de estadísticas de logs](assets/logs-stats-cards.png)

#### Indicadores Clave

| Métrica | Descripción | Interpretación |
|---------|-------------|----------------|
| **Total IPs** | IPs únicas registradas | Mayor diversidad = más actividad |
| **Total Logs** | Eventos totales del sistema | Volumen general de actividad |
| **Logs Info** | Eventos informativos | Actividad normal del sistema |
| **Logs Alerta** | Eventos críticos | Amenazas detectadas |

#### Códigos de Color

=== "Verde"
    - **Actividad normal** del sistema
    - **Valores esperados** según histórico
    - **Sin amenazas críticas**

=== "Amarillo"
    - **Incremento moderado** en actividad
    - **Requiere monitoreo** adicional
    - **Posibles patrones** emergentes

=== "Rojo"
    - **Actividad anómala** detectada
    - **Múltiples amenazas** activas
    - **Requiere acción inmediata**

## :mag: Búsqueda y Filtros

### Barra de Búsqueda

![Placeholder: Barra de búsqueda de logs](assets/logs-search-bar.png)

#### Búsqueda por Mensaje
- **Búsqueda en tiempo real** mientras escribes
- **Coincidencias parciales** en el contenido del log
- **Resaltado automático** de términos encontrados

```
Ejemplos de búsqueda:
• "Failed password" - Busca intentos de login fallidos
• "Invalid user" - Encuentra usuarios inexistentes
• "Connection refused" - Localiza conexiones rechazadas
```

### Filtros Avanzados

#### Filtro por Nivel de Log

![Placeholder: Filtro de nivel de log](assets/log-level-filter.png)

=== "INFO"
    - **Color**: Azul
    - **Descripción**: Información general del sistema
    - **Ejemplos**: Conexiones exitosas, estadísticas

=== "WARNING"
    - **Color**: Amarillo
    - **Descripción**: Advertencias que requieren atención
    - **Ejemplos**: Intentos de acceso sospechosos

=== "ERROR"
    - **Color**: Rojo
    - **Descripción**: Errores críticos del sistema
    - **Ejemplos**: Fallos de autenticación, ataques detectados

#### Filtro por Fecha y Hora

![Placeholder: Selector de fechas](assets/date-time-filter.png)

**Opciones Disponibles:**
- **Fecha específica** usando calendario
- **Rango de fechas** para análisis histórico
- **Filtros rápidos**: Última hora, último día, última semana
- **Hora específica** para análisis granular

### Aplicación de Filtros

#### Uso Combinado
- **Múltiples filtros** se pueden aplicar simultáneamente
- **Filtrado incremental** para refinar resultados
- **Reset rápido** para limpiar todos los filtros

#### Persistencia
- **Filtros mantenidos** durante la sesión
- **URL actualizada** para compartir búsquedas
- **Historial de filtros** en navegador

## :table: Tabla de Logs

### Estructura de la Tabla

![Placeholder: Tabla completa de logs](assets/logs-table-complete.png)

#### Columnas Disponibles

| Columna | Descripción | Características |
|---------|-------------|-----------------|
| **Timestamp** | Fecha y hora del evento | Ordenable, formato local |
| **Level** | Nivel de severidad | Badge con color |
| **Message** | Contenido del log | Texto completo, buscable |
| **Actions** | Acciones disponibles | Ver detalles, copiar |

#### Funcionalidades de Tabla

=== "Ordenación"
    - **Clic en headers** para ordenar columnas
    - **Orden ascendente/descendente** disponible
    - **Ordenación múltiple** manteniendo Shift

=== "Paginación"
    - **10, 25, 50** logs por página
    - **Navegación rápida** entre páginas
    - **Salto directo** a página específica

=== "Selección"
    - **Checkbox individual** por fila
    - **Selección múltiple** con Ctrl/Cmd
    - **Seleccionar todo** en página actual

### Visualización de Logs

#### Formato de Timestamp
- **Formato local** según configuración del navegador
- **Precisión de segundos** para análisis detallado
- **Indicador relativo** (hace 5 minutos)

#### Indicadores Visuales
- **Badges de nivel** con códigos de color
- **Iconos contextuales** según tipo de evento
- **Resaltado de texto** para términos de búsqueda

## :eye: Panel de Detalles

### Hoja de Detalles Lateral

![Placeholder: Panel de detalles de log](assets/log-details-panel.png)

#### Información Completa

**Metadatos del Evento:**
- **ID único** del log
- **Timestamp preciso** con milisegundos
- **Nivel de severidad** con descripción
- **Fuente** del evento

**Contenido del Log:**
- **Mensaje completo** sin truncar
- **Contexto adicional** si está disponible
- **Información técnica** relevante

**Análisis Contextual:**
- **Frecuencia** de eventos similares
- **Patrones relacionados** detectados
- **Recomendaciones** de acción

### Navegación en Detalles

#### Controles Disponibles
- **Cerrar panel** con botón X o Escape
- **Copiar contenido** al portapapeles
- **Navegación previa/siguiente** entre logs
- **Enlace directo** para compartir

#### Información Técnica

=== "Detalles del Sistema"
    - **Servidor de origen**
    - **Proceso que generó el log**
    - **Configuración aplicada**

=== "Contexto de Seguridad"
    - **Tipo de amenaza** detectada
    - **Nivel de riesgo** calculado
    - **Acciones recomendadas**

=== "Información de Red"
    - **IP de origen** (cuando aplique)
    - **Puerto utilizado**
    - **Protocolo de conexión**

## :gear: Herramientas de Gestión

### Acciones en Lote

![Placeholder: Barra de acciones en lote](assets/logs-bulk-actions.png)

#### Operaciones Disponibles

=== "Exportación"
    - **Formato CSV** para análisis externo
    - **Formato JSON** para integración técnica
    - **Filtros aplicados** incluidos en exportación

=== "Análisis"
    - **Generación de reportes** automática
    - **Detección de patrones** con IA
    - **Recomendaciones** de seguridad

#### Configuración de Exportación

**Opciones de Formato:**
- **CSV**: Ideal para Excel y análisis de datos
- **JSON**: Perfecto para integración con APIs
- **PDF**: Para reportes ejecutivos

**Personalización:**
- **Columnas seleccionables** para incluir
- **Rango de fechas** específico
- **Nivel de detalle** configurable

### Funciones Administrativas

#### Solo para Administradores

=== "Gestión Avanzada"
    - **Purga de logs** antiguos
    - **Configuración de retención**
    - **Optimización de rendimiento**

=== "Integración"
    - **API endpoints** para logs
    - **Webhooks** para notificaciones
    - **SIEM integration** para sistemas externos

## :arrows_clockwise: Actualización en Tiempo Real

### Sistema WebSocket

#### Logs en Vivo
- **Nuevos eventos** aparecen automáticamente
- **Notificación visual** para nuevos logs críticos
- **Scroll automático** opcional a eventos recientes

![Placeholder: Indicador de logs en tiempo real](assets/real-time-logs.png)

#### Gestión de Volumen
- **Límite de 1000 logs** visibles simultáneamente
- **Paginación automática** para volumen alto
- **Agregación inteligente** de eventos similares

### Notificaciones Push

#### Alertas Críticas
- **Toast notifications** para eventos ERROR
- **Sonido opcional** para alertas críticas
- **Persistencia** hasta reconocimiento

#### Configuración
- **Umbral personalizable** para notificaciones
- **Filtros de ruido** para eventos repetitivos
- **Horarios de silencio** disponibles

## :chart_with_upwards_trend: Análisis de Patrones

### Detección Automática

#### Patrones Comunes Identificados

| Patrón | Descripción | Acción Sugerida |
|--------|-------------|-----------------|
| **Brute Force** | Múltiples intentos fallidos | Bloqueo automático IP |
| **Port Scanning** | Acceso a múltiples puertos | Investigación adicional |
| **SQL Injection** | Patrones de inyección SQL | Alerta inmediata |
| **DDoS** | Volumen anormal de requests | Activar protecciones |

#### Métricas de Análisis
- **Frecuencia de eventos** por IP
- **Distribución temporal** de ataques
- **Geolocalización** de amenazas
- **Vectores de ataque** más comunes

### Reportes Automáticos

#### Generación Programada
- **Reportes diarios** de actividad
- **Resúmenes semanales** de seguridad
- **Alertas mensuales** de tendencias

#### Contenido de Reportes
- **Top 10 IPs** más problemáticas
- **Eventos críticos** del período
- **Recomendaciones** de mejora
- **Comparativas** con períodos anteriores

## :bulb: Mejores Prácticas

### Monitoreo Efectivo

!!! tip "Consejos de Uso"
    - **Revisa logs críticos** al menos cada hora
    - **Establece filtros** para tus casos de uso
    - **Exporta datos** regularmente para análisis offline
    - **Mantén ventana abierta** para alertas en tiempo real

### Análisis de Incidentes

!!! success "Flujo Recomendado"
    1. **Identifica evento** crítico en logs
    2. **Aplica filtros** para contexto temporal
    3. **Busca patrones** relacionados
    4. **Exporta evidencia** relevante
    5. **Documenta hallazgos** para futuras referencias

### Optimización de Rendimiento

!!! info "Consideraciones"
    - **Limita búsquedas** a rangos de tiempo específicos
    - **Usa filtros** antes de aplicar búsquedas de texto
    - **Exporta datos** en lotes para análisis pesado
    - **Purga logs antiguos** regularmente

## :warning: Solución de Problemas

### Problemas Comunes

=== "Logs no aparecen"
    **Síntomas**: Tabla vacía o sin datos recientes
    
    **Posibles causas**:
    - Filtros muy restrictivos
    - Problemas de conexión WebSocket
    - Fail2ban no está funcionando

    **Soluciones**:
    - Limpia todos los filtros
    - Refresca la página
    - Verifica estado de Fail2ban en servidor

=== "Búsqueda lenta"
    **Síntomas**: Demora en mostrar resultados
    
    **Posibles causas**:
    - Volumen muy alto de logs
    - Búsquedas sin filtros temporales
    - Recursos del servidor limitados

    **Soluciones**:
    - Aplica filtros de fecha primero
    - Usa términos de búsqueda específicos
    - Contacta administrador si persiste

=== "Exportación falla"
    **Síntomas**: Error al descargar datos
    
    **Posibles causas**:
    - Demasiados registros seleccionados
    - Permisos insuficientes
    - Problema temporal del servidor

    **Soluciones**:
    - Reduce rango de fechas
    - Verifica tus permisos de usuario
    - Intenta nuevamente más tarde

!!! warning "Límites del Sistema"
    - **Máximo 10,000 logs** por exportación
    - **Búsquedas limitadas** a 90 días hacia atrás
    - **Actualización en tiempo real** puede pausarse con alto volumen