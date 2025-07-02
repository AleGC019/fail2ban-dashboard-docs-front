# Gestión de IPs Bloqueadas

La sección de IPs Bloqueadas te permite monitorear, analizar y gestionar todas las direcciones IP que han sido bloqueadas por Fail2ban.

## :shield: Vista General

### Pantalla Principal

![Placeholder: Vista completa de IPs bloqueadas](assets/banned-ips-overview.png)

La gestión de IPs bloqueadas incluye:

1. **Estadísticas de Bloqueos** - Métricas del sistema de seguridad
2. **Herramientas de Gestión** - Bloqueo manual y filtros
3. **Tabla de IPs** - Lista detallada con información de amenazas
4. **Panel de Detalles** - Análisis profundo por IP

## :bar_chart: Estadísticas de Seguridad

### Métricas Principales

![Placeholder: Estadísticas de IPs bloqueadas](assets/banned-ips-stats.png)

#### Indicadores Clave

| Métrica | Descripción | Interpretación |
|---------|-------------|----------------|
| **IPs Bloqueadas Hoy** | Nuevos bloqueos en 24h | Actividad diaria de amenazas |
| **Total IPs Activas** | IPs actualmente bloqueadas | Estado actual de seguridad |
| **Top País Origen** | País con más IPs bloqueadas | Origen geográfico principal |
| **Promedio Duración** | Tiempo promedio de bloqueo | Efectividad de políticas |

#### Análisis de Tendencias

=== "Tendencia Positiva"
    - **Disminución** en nuevos bloqueos
    - **Aumento** en duración promedio de bloqueos
    - **Diversificación** geográfica de amenazas

=== "Tendencia Negativa"
    - **Incremento súbito** en bloqueos diarios
    - **Concentración** de ataques desde un país
    - **Duración muy corta** de bloqueos (evasión)

=== "Requiere Atención"
    - **Picos inusuales** en actividad
    - **Nuevos países** en top de amenazas
    - **Patrones repetitivos** de mismo origen

## :hammer_and_wrench: Herramientas de Gestión

### Bloqueo Manual de IPs

![Placeholder: Formulario de bloqueo manual](assets/manual-ban-form.png)

#### Proceso de Bloqueo

1. **Acceso a la Función**
   - Botón "Bloquear IP" en la esquina superior derecha
   - Solo disponible para administradores

2. **Formulario de Bloqueo**
   - **Campo IP**: Dirección IPv4 o IPv6
   - **Validación en tiempo real** del formato
   - **Verificación** de duplicados

3. **Confirmación y Ejecución**
   - **Diálogo de confirmación** antes del bloqueo
   - **Feedback inmediato** del resultado
   - **Actualización automática** de la tabla

#### Validaciones del Sistema

=== "Formatos Soportados"
    ```
    IPv4: 192.168.1.100
    IPv6: 2001:0db8:85a3:0000:0000:8a2e:0370:7334
    ```

=== "Verificaciones"
    - **IP ya bloqueada**: Notificación si existe
    - **IP inválida**: Error en formato
    - **IP local**: Advertencia especial para redes internas

### Desbloqueo de IPs

#### Proceso de Desbloqueo

![Placeholder: Botón de desbloqueo en tabla](assets/unban-button.png)

1. **Localizar IP** en la tabla
2. **Clic en botón "Desbloquear"** (icono de candado abierto)
3. **Confirmar acción** en diálogo
4. **Verificar resultado** en notificación

#### Consideraciones de Seguridad
- **Solo administradores** pueden desbloquear
- **Log de auditoría** registra la acción
- **Re-bloqueo automático** si la IP reincide

## :mag: Filtros y Búsqueda

### Filtros Avanzados

![Placeholder: Barra de filtros de IPs](assets/ip-filters-bar.png)

#### Filtro por Tiempo de Bloqueo

**Opciones Disponibles:**
- **Última hora**: IPs bloqueadas recientemente
- **Últimas 6 horas**: Actividad del turno actual
- **Últimas 24 horas**: Actividad diaria completa
- **Última semana**: Análisis semanal
- **Personalizado**: Rango específico de fechas

#### Filtro por Jail

**Servicios Monitoreados:**
- **sshd**: Ataques de SSH (por defecto)
- **apache**: Ataques web HTTP
- **nginx**: Ataques web con Nginx
- **postfix**: Ataques de email
- **custom**: Jails personalizados

#### Aplicación de Filtros

=== "Filtro Simple"
    - **Un filtro activo** por vez
    - **Aplicación inmediata** al seleccionar
    - **Indicador visual** del filtro activo

=== "Filtro Combinado"
    - **Múltiples criterios** simultáneos
    - **Filtrado incremental** para refinar
    - **URL actualizada** para compartir vista

### Búsqueda por IP

#### Búsqueda Directa
- **Campo de texto** para dirección IP exacta
- **Autocompletado** con IPs recientes
- **Validación** de formato en tiempo real

#### Búsqueda por Rango
```
Ejemplos de búsqueda:
• 192.168.1.* - Busca toda la subred
• 10.0.0.1-10.0.0.100 - Rango específico
• 192.168.*.* - Red clase B completa
```

## :table: Tabla de IPs Bloqueadas

### Estructura de Datos

![Placeholder: Tabla completa de IPs bloqueadas](assets/banned-ips-table.png)

#### Columnas Principales

| Columna | Descripción | Funcionalidad |
|---------|-------------|---------------|
| **IP Address** | Dirección IP bloqueada | Clic para detalles completos |
| **Ban Time** | Momento del bloqueo | Ordenable, formato relativo |
| **Jail** | Servicio que detectó la amenaza | Filtrable por tipo |
| **Threat Level** | Nivel de riesgo calculado | Badge codificado por color |
| **Country** | País de origen | Bandera e ISO code |
| **Actions** | Acciones disponibles | Desbloquear, detalles |

#### Niveles de Amenaza

=== "Critical (Crítico)"
    - **Color**: Rojo oscuro
    - **Criterios**: Múltiples bloqueos, listas negras conocidas
    - **Acción**: Bloqueo permanente recomendado

=== "High (Alto)"
    - **Color**: Rojo
    - **Criterios**: Ataques coordinados, actividad maliciosa clara
    - **Acción**: Monitoreo continuo

=== "Medium (Medio)"
    - **Color**: Amarillo
    - **Criterios**: Actividad sospechosa, escaneos
    - **Acción**: Vigilancia regular

=== "Low (Bajo)"
    - **Color**: Verde
    - **Criterios**: Errores menores, actividad mínima
    - **Acción**: Seguimiento básico

### Información Geográfica

#### Visualización de País
- **Banderas** de países para identificación rápida
- **Código ISO** del país (US, CN, RU, etc.)
- **Tooltip** con nombre completo del país

#### Análisis Geográfico
- **Top 5 países** con más amenazas
- **Distribución global** de ataques
- **Patrones regionales** de actividad maliciosa

## :eye: Panel de Detalles Detallado

### Información Completa de IP

![Placeholder: Panel de detalles completo de IP](assets/ip-details-panel.png)

#### Información Básica

**Datos de Red:**
- **Dirección IP**: Completa con formato
- **Tipo**: IPv4 o IPv6
- **ISP/Organización**: Proveedor de internet
- **ASN**: Número de sistema autónomo

**Geolocalización:**
- **País**: Con bandera y código
- **Región/Estado**: División administrativa
- **Ciudad**: Ubicación específica
- **Coordenadas**: Latitud y longitud

#### Información de Seguridad

**Análisis de Amenazas:**
- **Nivel de riesgo**: Calculado algorítmicamente
- **Tipo de ataque**: Categorización automática
- **Frecuencia**: Número de intentos
- **Duración**: Tiempo activo atacando

**Historial de Actividad:**
- **Primera detección**: Timestamp inicial
- **Último intento**: Actividad más reciente
- **Total intentos**: Suma de todos los eventos
- **Servicios atacados**: Lista de jails afectados

#### Contexto Adicional

=== "Información Técnica"
    - **TTL de conexión**
    - **User-Agent** (cuando aplique)
    - **Protocolos utilizados**
    - **Puertos atacados**

=== "Inteligencia de Amenazas"
    - **Listas negras** donde aparece la IP
    - **Reputación** en servicios externos
    - **Categorización** de amenaza
    - **Confianza** del análisis

=== "Recomendaciones"
    - **Acciones sugeridas** por el sistema
    - **Tiempo de bloqueo** recomendado
    - **Monitoreo adicional** requerido
    - **Escalación** a autoridades si aplica

### Navegación en Detalles

#### Controles del Panel
- **Cerrar**: Botón X o tecla Escape
- **Copiar IP**: Botón para portapapeles
- **Desbloquear**: Acción directa (solo admins)
- **Reporte**: Generar reporte específico de la IP

#### Acciones Avanzadas

**Para Administradores:**
- **Bloqueo permanente**: Añadir a lista negra
- **Whitelisting**: Añadir a lista blanca
- **Investigación**: Marcar para análisis profundo
- **Reporte externo**: Enviar a servicios de inteligencia

## :gear: Funciones Administrativas

### Gestión en Lote

![Placeholder: Acciones en lote para IPs](assets/bulk-ip-actions.png)

#### Operaciones Disponibles

=== "Selección Múltiple"
    - **Checkboxes** individuales por IP
    - **Seleccionar todo** en página actual
    - **Selección por criterios** (país, nivel, etc.)

=== "Acciones en Lote"
    - **Desbloqueo masivo** de IPs seleccionadas
    - **Exportación** de datos seleccionados
    - **Cambio de nivel** de amenaza
    - **Añadir a listas** (blanca/negra)

#### Consideraciones de Seguridad
- **Confirmación obligatoria** para acciones masivas
- **Límite máximo** de 100 IPs por operación
- **Log de auditoría** detallado de cambios
- **Rollback** disponible para correcciones

### Configuración Avanzada

#### Políticas de Bloqueo

**Duración Automática:**
- **Primera ofensa**: 10 minutos
- **Reincidencia**: 1 hora exponencial
- **Amenaza alta**: 24 horas mínimo
- **Crítica**: Bloqueo permanente

**Umbrales de Detección:**
- **Intentos fallidos**: 3-5 según servicio
- **Ventana de tiempo**: 10 minutos
- **Persistencia**: Reinicio automático de contador

#### Integración con Servicios

**Fuentes de Inteligencia:**
- **AbuseIPDB**: Verificación de reputación
- **VirusTotal**: Análisis de amenazas
- **MaxMind**: Geolocalización precisa
- **Shodan**: Información de dispositivos

## :arrows_clockwise: Monitoreo en Tiempo Real

### Actualizaciones Automáticas

#### Sistema de Notificaciones
- **Nuevos bloqueos** aparecen automáticamente
- **Toast notifications** para IPs críticas
- **Contador en tiempo real** de estadísticas
- **Indicador visual** de actividad reciente

#### Configuración de Alertas

**Umbrales Personalizables:**
- **Número de IPs** bloqueadas por hora
- **Países nuevos** detectados
- **Niveles de amenaza** específicos
- **Servicios atacados** críticos

### Panel de Actividad

#### Vista de Stream en Vivo
- **Feed continuo** de nuevos bloqueos
- **Información básica** por evento
- **Acceso rápido** a detalles completos
- **Filtros aplicables** al stream

## :bulb: Mejores Prácticas

### Análisis de Amenazas

!!! tip "Flujo de Investigación"
    1. **Identifica patrones** en países de origen
    2. **Analiza horarios** de mayor actividad
    3. **Correlaciona servicios** más atacados
    4. **Investiga IPs recurrentes** en detalles
    5. **Ajusta políticas** según hallazgos

### Mantenimiento Preventivo

!!! success "Rutinas Recomendadas"
    - **Revisión semanal** de top amenazas
    - **Limpieza mensual** de IPs obsoletas
    - **Análisis trimestral** de efectividad
    - **Actualización semestral** de políticas

### Gestión de Falsos Positivos

!!! warning "Identificación y Corrección"
    - **Revisa IPs corporativas** bloqueadas
    - **Verifica servicios legítimos** afectados
    - **Documenta excepciones** necesarias
    - **Ajusta reglas** para evitar recurrencia

## :question: Solución de Problemas

### Problemas Comunes

=== "No puedo desbloquear IP"
    **Síntomas**: Botón no disponible o error

    **Posibles causas**:
    - Permisos insuficientes
    - IP ya desbloqueada
    - Problema de conectividad

    **Soluciones**:
    - Verifica permisos de administrador
    - Refresca la tabla
    - Contacta soporte técnico

=== "Bloqueo manual falla"
    **Síntomas**: Error al intentar bloquear IP

    **Posibles causas**:
    - Formato de IP incorrecto
    - IP ya bloqueada
    - Fail2ban no responde

    **Soluciones**:
    - Verifica formato de IP
    - Consulta tabla de IPs existentes
    - Revisa estado del servicio

=== "Datos de geolocalización incorrectos"
    **Síntomas**: País o ubicación errónea

    **Posibles causas**:
    - Base de datos desactualizada
    - IP usando VPN/Proxy
    - Error en servicio de geolocalización

    **Soluciones**:
    - Actualiza base de datos GeoIP
    - Marca IP como proxy/VPN
    - Reporta error a administrador

!!! info "Límites y Consideraciones"
    - **Máximo 50,000 IPs** en tabla simultáneamente
    - **Geolocalización** puede tener precisión limitada
    - **Desbloqueo automático** según políticas configuradas
    - **Retención de datos** por 90 días por defecto