# Dashboard Principal

El Dashboard es el centro de control de Secure Dash, proporcionando una visión completa y en tiempo real del estado de seguridad de tu servidor.

## :bar_chart: Visión General

### Pantalla Principal

![Placeholder: Vista completa del dashboard](assets/dashboard-full-view.png)

El Dashboard está organizado en tres secciones principales:

1. **Métricas Rápidas** - Estadísticas clave del sistema
2. **Gráficos en Tiempo Real** - Visualizaciones dinámicas
3. **Tablas de Datos** - Información detallada y acciones

## :1234: Métricas del Sistema

### Tarjetas de Estadísticas

![Placeholder: Tarjetas de métricas principales](assets/dashboard-metrics.png)

#### Métricas Disponibles

=== "Métricas Principales"
    | Métrica | Descripción | Actualization |
    |---------|-------------|---------------|
    | **Total IPs** | IPs únicas que han interactuado | Tiempo real |
    | **Total Logs** | Eventos totales registrados | Tiempo real |
    | **Logs Info** | Eventos informativos | Tiempo real |
    | **Logs Alerta** | Eventos críticos | Tiempo real |

=== "Indicadores Visuales"
    - **Iconos diferenciados** por tipo de métrica
    - **Colores codificados** según importancia
    - **Animaciones sutiles** para cambios
    - **Tooltips informativos** al pasar el mouse

### Interpretación de Métricas

#### Total de IPs
- **Verde**: Actividad normal
- **Amarillo**: Incremento moderado
- **Rojo**: Actividad anómala alta

#### Logs de Alerta
- **0-10**: Nivel normal de amenazas
- **11-50**: Actividad moderada a vigilar
- **50+**: Alta actividad, requiere atención

!!! info "Actualización Automática"
    Las métricas se actualizan automáticamente cada 5 segundos para mantener información precisa y actual.

## :chart_with_upwards_trend: Gráficos Interactivos

### Gráfico de Tendencias de Actividad

![Placeholder: Gráfico de tendencias en tiempo real](assets/activity-trend-chart.png)

#### Características
- **Datos en tiempo real** con punto verde indicador
- **Eje temporal** muestra los últimos eventos
- **Escala automática** según volumen de datos
- **Hover interactions** para detalles específicos

#### Interpretación
- **Picos altos**: Posibles ataques coordinados
- **Actividad constante**: Escaneos automáticos normales
- **Períodos silenciosos**: Normal durante horas no laborales

### Gráfico de Bans vs Unbans

![Placeholder: Gráfico de bans vs unbans](assets/ban-unban-chart.png)

#### Elementos del Gráfico
- **Línea azul**: Tasa de bloqueos (Ban Rate)
- **Línea verde**: Tasa de desbloqueos (Unban Rate)
- **Eje temporal**: Últimas 10 actualizaciones
- **Leyenda interactiva** para filtrar datos

#### Análisis de Patrones
- **Más bans que unbans**: Sistema funcionando correctamente
- **Picos de bans**: Posibles ataques detectados
- **Unbans frecuentes**: IPs legítimas siendo desbloqueadas

### KPI de Tiempo de Detección

![Placeholder: KPI de tiempo promedio de detección](assets/avg-detection-kpi.png)

#### Niveles de Rendimiento

| Tiempo | Estado | Color | Descripción |
|--------|--------|-------|-------------|
| ≤ 2s | Excelente | Verde | Respuesta muy rápida |
| 2-4s | Bueno | Amarillo | Respuesta normal |
| > 4s | Lento | Rojo | Requiere optimización |

#### Indicadores Visuales
- **Animación de cambio** cuando el valor se actualiza
- **Flecha direccional** indica mejora o deterioro
- **Color dinámico** basado en el rendimiento

## :shield: Top 5 IPs Bloqueadas

### Tabla de IPs Problemáticas

![Placeholder: Tabla de top 5 IPs bloqueadas](assets/top-ips-table.png)

#### Información Mostrada

| Columna | Descripción |
|---------|-------------|
| **IP Address** | Dirección IP problemática |
| **Bans** | Número total de bloqueos |
| **Risk Level** | Nivel de riesgo calculado |

#### Niveles de Riesgo

=== "Alto (High)"
    - **Color**: Rojo
    - **Criterio**: > 10 bans
    - **Acción**: Monitorio continuo

=== "Medio (Medium)"
    - **Color**: Amarillo
    - **Criterio**: 5-10 bans
    - **Acción**: Vigilancia regular

=== "Bajo (Low)"
    - **Color**: Verde
    - **Criterio**: < 5 bans
    - **Acción**: Seguimiento básico

### Acciones Disponibles

- **Clic en IP**: Ver detalles completos
- **Botón de copia**: Copiar IP al portapapeles
- **Enlaces a detalles**: Navegación directa a gestión de IPs

## :bell: Sistema de Alertas

### Alertas en Tiempo Real

![Placeholder: Notificaciones de alerta](assets/security-alerts.png)

#### Tipos de Alertas

=== "Críticas"
    - **Color**: Rojo
    - **Sonido**: Notificación audible
    - **Duración**: 10 segundos
    - **Ejemplo**: IP con 7+ bans en última hora

=== "Advertencias"
    - **Color**: Amarillo
    - **Duración**: 8 segundos
    - **Ejemplo**: Incremento inusual de actividad

=== "Informativas"
    - **Color**: Azul
    - **Duración**: 5 segundos
    - **Ejemplo**: Nuevos logs disponibles

### Gestión de Alertas

#### Configuración Automática
- **Umbrales predefinidos** para diferentes tipos de eventos
- **Filtrado inteligente** para evitar spam de notificaciones
- **Agrupación** de alertas similares

#### Acciones Disponibles
- **Ver detalles**: Clic en la alerta para más información
- **Copiar IP**: Botón directo para copiar direcciones IP
- **Ir a gestión**: Enlaces directos a secciones relevantes

## :arrows_clockwise: Datos en Tiempo Real

### Sistema WebSocket

#### Conexión Activa
- **Indicador verde** en gráficos muestra conexión activa
- **Reconexión automática** si se pierde la conexión
- **Notificación** cuando se restaura la conectividad

#### Frecuencia de Actualización

| Componente | Frecuencia |
|------------|------------|
| **Métricas principales** | 5 segundos |
| **Gráficos** | Tiempo real |
| **Alertas** | Inmediata |
| **Top IPs** | 30 segundos |

### Manejo de Desconexión

#### Indicadores Visuales
- **Punto rojo** en lugar del verde
- **Mensaje de advertencia** en la interfaz
- **Datos en caché** mostrados hasta reconexión

#### Recuperación Automática
- **Reintento cada 5 segundos**
- **Sincronización automática** al reconectar
- **Notificación de éxito** cuando se restaura

## :gear: Personalización del Dashboard

### Preferencias de Usuario

#### Configuraciones Disponibles
- **Tema claro/oscuro** - Botón en header
- **Frecuencia de alertas** - Configuración automática
- **Tamaño de gráficos** - Responsivo automático

#### Configuraciones Persistentes
- **Preferencias guardadas** en el navegador
- **Estado mantenido** entre sesiones
- **Sincronización** entre pestañas

### Optimización para Dispositivos

#### Escritorio (> 1024px)
- **Diseño completo** con todos los elementos
- **Gráficos de tamaño completo**
- **Interacciones hover** mejoradas

#### Tablet (768px - 1024px)
- **Layout adaptado** manteniendo funcionalidad
- **Elementos apilados** verticalmente
- **Touch-friendly** para interacciones táctiles

#### Móvil (< 768px)
- **Vista optimizada** para pantallas pequeñas
- **Navegación simplificada**
- **Elementos esenciales** priorizados

![Placeholder: Vistas responsivas del dashboard](assets/dashboard-responsive.png)

## :bulb: Consejos de Uso

### Mejores Prácticas

!!! tip "Uso Efectivo del Dashboard"
    - **Revisa métricas** al iniciar tu sesión diaria
    - **Monitorea tendencias** durante picos de actividad
    - **Responde a alertas** de manera inmediata
    - **Verifica conectividad** si no ves actualizaciones

### Interpretación de Datos

!!! success "Indicadores Positivos"
    - Métricas estables o con tendencia decreciente
    - Tiempo de detección rápido (< 2s)
    - Pocas alertas críticas
    - Balance adecuado entre bans y unbans

!!! warning "Señales de Alerta"
    - Incremento súbito en total de IPs
    - Tiempo de detección lento (> 4s)
    - Múltiples alertas críticas
    - Picos inusuales en actividad

### Flujo de Trabajo Recomendado

1. **Check inicial** de métricas principales
2. **Revisar alertas** pendientes
3. **Analizar gráficos** de tendencias
4. **Verificar top IPs** problemáticas
5. **Tomar acciones** según sea necesario

## :question: Solución de Problemas

### Problemas Comunes

=== "Datos no se actualizan"
    **Síntomas**: Métricas estáticas, sin punto verde
    
    **Causas posibles**:
    - Conexión WebSocket perdida
    - Problemas de red
    - Servidor no responde

    **Soluciones**:
    - Refresca la página
    - Verifica conexión a internet
    - Contacta al administrador

=== "Gráficos no aparecen"
    **Síntomas**: Espacios en blanco donde deberían estar los gráficos
    
    **Causas posibles**:
    - JavaScript deshabilitado
    - Extensiones del navegador
    - Datos insuficientes

    **Soluciones**:
    - Habilita JavaScript
    - Deshabilita extensiones temporalmente
    - Espera a que se acumulen datos

=== "Alertas no llegan"
    **Síntomas**: No hay notificaciones de eventos
    
    **Causas posibles**:
    - Notificaciones bloqueadas en navegador
    - Filtros muy restrictivos
    - Sistema de alertas deshabilitado

    **Soluciones**:
    - Permite notificaciones en el navegador
        - Verifica configuración de alertas
    - Contacta soporte técnico

!!! info "Nota de Rendimiento"
    El Dashboard está optimizado para mostrar hasta 10,000 eventos simultáneamente. Para volúmenes mayores, algunos elementos pueden mostrar datos agregados.