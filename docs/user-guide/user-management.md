 # Gestión de Usuarios

La sección de gestión de usuarios permite a los administradores controlar el acceso al sistema, asignar roles y gestionar permisos de manera granular.

## :busts_in_silhouette: Vista General

!!! warning "Acceso Restringido"
    Esta sección está disponible únicamente para usuarios con rol de **Administrador**.

### Pantalla Principal

![Placeholder: Vista completa de gestión de usuarios](assets/users-management-overview.png)

La gestión de usuarios incluye:

1. **Estadísticas de Usuarios** - Métricas del sistema de acceso
2. **Herramientas de Administración** - Creación y gestión de cuentas
3. **Tabla de Usuarios** - Lista completa con información de acceso
4. **Panel de Edición** - Modificación de roles y permisos

## :bar_chart: Estadísticas del Sistema

### Métricas de Usuarios

![Placeholder: Estadísticas de usuarios del sistema](assets/users-stats.png)

#### Indicadores Principales

| Métrica | Descripción | Interpretación |
|---------|-------------|----------------|
| **Total Usuarios** | Cuentas totales en el sistema | Crecimiento de la plataforma |
| **Usuarios Administradores** | Cuentas con permisos completos | Control de acceso privilegiado |
| **Usuarios Regulares** | Cuentas con permisos básicos | Base de usuarios estándar |
| **Usuarios Activos (30d)** | Actividad reciente | Engagement de la plataforma |

#### Análisis de Roles

=== "Distribución Saludable"
    - **Administradores**: 10-20% del total
    - **Usuarios regulares**: 80-90% del total
    - **Proporción adecuada** según tamaño de organización

=== "Señales de Alerta"
    - **Demasiados administradores**: Riesgo de seguridad
    - **Muy pocos administradores**: Riesgo operacional
    - **Usuarios inactivos altos**: Limpieza necesaria

### Tendencias de Acceso

#### Métricas de Actividad
- **Logins diarios** promedio
- **Tiempo de sesión** medio
- **Funciones más utilizadas** por rol
- **Horarios pico** de actividad

## :hammer_and_wrench: Gestión de Cuentas

### Roles del Sistema

#### Estructura de Permisos

=== "Usuario Regular (USER)"
    **Permisos Incluidos:**
    - ✅ Ver dashboard y métricas
    - ✅ Consultar logs de Fail2ban
    - ✅ Ver lista de IPs bloqueadas
    - ✅ Exportar datos (limitado)
    - ❌ Bloquear/desbloquear IPs
    - ❌ Gestionar otros usuarios
    - ❌ Configurar sistema

=== "Administrador (ADMIN)"
    **Permisos Incluidos:**
    - ✅ **Todos los permisos de Usuario Regular**
    - ✅ Bloquear/desbloquear IPs manualmente
    - ✅ Gestionar usuarios del sistema
    - ✅ Asignar y modificar roles
    - ✅ Configurar políticas de seguridad
    - ✅ Acceder a logs de auditoría
    - ✅ Exportación completa de datos

### Creación de Usuarios

#### Proceso Automático
- **Registro libre** para usuarios regulares
- **Permisos básicos** asignados automáticamente
- **Elevación manual** a administrador

#### Creación Manual (Admins)
1. **Acceso directo** desde panel de administración
2. **Asignación inmediata** de roles
3. **Configuración avanzada** de permisos
4. **Notificación automática** al nuevo usuario

## :table: Tabla de Usuarios

### Estructura de Datos

![Placeholder: Tabla completa de usuarios](assets/users-table-complete.png)

#### Columnas Principales

| Columna | Descripción | Funcionalidad |
|---------|-------------|---------------|
| **Username** | Nombre de usuario único | Identificador principal |
| **Email** | Dirección de correo | Contacto y autenticación |
| **Roles** | Permisos asignados | Badges con códigos de color |
| **Status** | Estado de la cuenta | Activo/Inactivo |
| **Created At** | Fecha de creación | Información histórica |
| **Actions** | Acciones disponibles | Editar, eliminar, detalles |

#### Estados de Cuenta

=== "Activo"
    - **Color**: Verde
    - **Descripción**: Usuario puede acceder normalmente
    - **Funcionalidad**: Todas las funciones habilitadas

=== "Inactivo"
    - **Color**: Gris
    - **Descripción**: Cuenta suspendida temporalmente
    - **Funcionalidad**: Acceso bloqueado

=== "Pendiente"
    - **Color**: Amarillo
    - **Descripción**: Cuenta creada pero no verificada
    - **Funcionalidad**: Acceso limitado hasta verificación

### Badges de Roles

#### Visualización de Permisos

**Usuario Regular:**
- **Badge azul** con texto "Usuario"
- **Icono**: Usuario simple
- **Tooltip**: "Permisos básicos del sistema"

**Administrador:**
- **Badge rojo** con texto "Administrador"
- **Icono**: Escudo con corona
- **Tooltip**: "Acceso completo al sistema"

![Placeholder: Badges de roles de usuario](assets/user-role-badges.png)

## :pencil2: Edición de Usuarios

### Panel de Edición Lateral

![Placeholder: Panel de edición de usuario](assets/user-edit-panel.png)

#### Información Editable

**Datos Básicos:**
- **Nombre de usuario**: Único en el sistema
- **Email**: Verificación automática de formato
- **Estado**: Activo/Inactivo toggle

**Gestión de Roles:**
- **Selector múltiple** de roles disponibles
- **Validación**: Al menos un rol requerido
- **Confirmación**: Para cambios de administrador

#### Validaciones del Sistema

=== "Nombre de Usuario"
    - **Longitud**: 3-20 caracteres
    - **Caracteres permitidos**: Letras, números, guiones, guiones bajos
    - **Unicidad**: Verificación en tiempo real

=== "Email"
    - **Formato válido**: Validación RFC completa
    - **Unicidad**: Un email por cuenta
    - **Verificación**: Opcional para admins

=== "Roles"
    - **Mínimo un rol**: Usuario no puede quedar sin permisos
    - **Confirmación admin**: Cambios requieren confirmación
    - **Auto-asignación**: Usuario regular por defecto

### Proceso de Edición

#### Flujo de Modificación

1. **Seleccionar usuario** en la tabla
2. **Abrir panel** de edición lateral
3. **Modificar campos** necesarios
4. **Validación automática** en tiempo real
5. **Guardar cambios** con confirmación
6. **Notificación** de éxito/error

#### Confirmaciones de Seguridad

**Cambios Críticos que Requieren Confirmación:**
- **Remoción de rol administrador** del propio usuario
- **Desactivación** de cuenta administrador
- **Eliminación** de usuarios con actividad reciente
- **Cambios masivos** de permisos

## :gear: Funciones Administrativas

### Acciones en Lote

![Placeholder: Acciones en lote para usuarios](assets/users-bulk-actions.png)

#### Operaciones Disponibles

=== "Gestión de Estado"
    - **Activar múltiples** usuarios inactivos
    - **Desactivar** usuarios seleccionados
    - **Verificar** cuentas pendientes

=== "Gestión de Roles"
    - **Asignar rol** a múltiples usuarios
    - **Remover permisos** específicos
    - **Estandarizar roles** por departamento

=== "Mantenimiento"
    - **Exportar datos** de usuarios seleccionados
    - **Enviar notificaciones** masivas
    - **Eliminar cuentas** obsoletas

#### Limitaciones de Seguridad

**Restricciones de Protección:**
- **No puede eliminarse** a sí mismo
- **Máximo 50 usuarios** por operación en lote
- **Confirmación obligatoria** para cambios críticos
- **Log de auditoría** completo de cambios

### Gestión de Permisos Avanzada

#### Políticas de Acceso

**Horarios de Acceso:**
- **24/7**: Sin restricciones (por defecto)
- **Horario laboral**: 8 AM - 6 PM días laborales
- **Personalizado**: Definido por administrador

**Restricciones de IP:**
- **Sin restricción**: Acceso desde cualquier IP
- **IP corporativa**: Solo desde redes autorizadas
- **Lista blanca**: IPs específicas permitidas

**Límites de Sesión:**
- **Sesiones concurrentes**: 1-5 sesiones simultáneas
- **Duración máxima**: 1-24 horas
- **Inactividad**: 15 minutos - 8 horas

## :eye: Panel de Detalles de Usuario

### Información Completa

![Placeholder: Panel de detalles completo de usuario](assets/user-details-complete.png)

#### Información Personal

**Datos de Cuenta:**
- **ID único**: Identificador interno del sistema
- **Username**: Nombre de usuario
- **Email**: Dirección de contacto
- **Estado**: Activo/Inactivo con timestamp

**Metadatos del Sistema:**
- **Fecha de creación**: Cuándo se registró
- **Última actividad**: Último login exitoso
- **Total sesiones**: Número de logins históricos
- **IP más frecuente**: Dirección de acceso común

#### Historial de Actividad

**Registro de Accesos:**
- **Logins exitosos**: Fechas y horas
- **Intentos fallidos**: Alertas de seguridad
- **Cambios de perfil**: Modificaciones de datos
- **Acciones realizadas**: Log de actividades importantes

**Análisis de Comportamiento:**
- **Horarios preferidos**: Patrones de uso
- **Secciones más usadas**: Preferencias del usuario
- **Tiempo promedio**: Duración de sesiones
- **Dispositivos utilizados**: Desktop/móvil

#### Configuración Técnica

=== "Sesiones Activas"
    - **Lista de dispositivos** conectados
    - **IP de cada sesión**
    - **Tiempo de actividad** de cada sesión
    - **Forzar logout** remoto disponible

=== "Configuración de Seguridad"
    - **Último cambio** de contraseña
    - **Intentos fallidos** recientes
    - **Alertas de seguridad** configuradas
    - **Verificación 2FA** (cuando esté disponible)

=== "Preferencias de Usuario"
    - **Tema preferido**: Claro/oscuro
    - **Idioma**: Español (por defecto)
    - **Notificaciones**: Push/email habilitadas
    - **Configuración de tabla**: Filas por página

### Acciones Administrativas

#### Herramientas de Gestión

**Gestión de Cuenta:**
- **Resetear contraseña**: Generar nueva temporal
- **Forzar logout**: Cerrar todas las sesiones
- **Suspender cuenta**: Desactivación temporal
- **Eliminar usuario**: Eliminación completa

**Gestión de Datos:**
- **Exportar actividad**: Download de logs del usuario
- **Limpiar sesiones**: Eliminar sesiones vencidas
- **Backup perfil**: Exportar configuración

**Comunicación:**
- **Enviar notificación**: Mensaje directo al usuario
- **Enviar email**: Comunicación formal
- **Programar recordatorio**: Alertas futuras

## :shield: Seguridad y Auditoría

### Log de Auditoría

#### Eventos Registrados

| Evento | Información Registrada | Retención |
|--------|------------------------|-----------|
| **Creación de usuario** | Admin, timestamp, datos iniciales | Permanente |
| **Cambio de roles** | Roles anteriores/nuevos, justificación | Permanente |
| **Modificación de datos** | Campos cambiados, valores anteriores | 1 año |
| **Eliminación** | Datos del usuario, razón, admin responsable | Permanente |
| **Accesos** | IP, timestamp, éxito/fallo | 90 días |

#### Informes de Auditoría

**Reportes Automáticos:**
- **Diario**: Cambios de roles y nuevos usuarios
- **Semanal**: Análisis de actividad y patrones
- **Mensual**: Revisión completa de permisos
- **Anual**: Auditoría de seguridad completa

### Políticas de Seguridad

#### Mejores Prácticas Implementadas

!!! success "Controles de Seguridad"
    - **Principio de menor privilegio**: Permisos mínimos necesarios
    - **Separación de funciones**: Roles claramente definidos
    - **Revisión periódica**: Auditoría regular de permisos
    - **Trazabilidad completa**: Log de todas las acciones

#### Alertas de Seguridad

**Eventos que Generan Alertas:**
- **Creación de administrador**: Notificación inmediata
- **Múltiples fallos de login**: Posible ataque
- **Acceso desde IP nueva**: Verificación adicional
- **Cambios fuera de horario**: Actividad sospechosa

## :bulb: Mejores Prácticas

### Administración Efectiva

!!! tip "Gestión Recomendada"
    - **Revisa usuarios** semanalmente para inactividad
    - **Actualiza roles** según cambios organizacionales
    - **Documenta cambios** críticos de permisos
    - **Mantén respaldos** de configuraciones de usuario

### Principios de Seguridad

!!! warning "Consideraciones Importantes"
    - **Nunca compartas** credenciales de administrador
    - **Revoca acceso** inmediatamente al terminar empleo
    - **Usa cuentas temporales** para contratistas
    - **Documenta justificaciones** para roles administrativos

### Mantenimiento Regular

!!! info "Rutinas Recomendadas"
    - **Limpieza mensual** de cuentas inactivas
    - **Revisión trimestral** de roles asignados
    - **Auditoría semestral** de permisos
    - **Backup anual** de configuraciones

## :warning: Solución de Problemas

### Problemas Comunes

=== "No puedo editar usuario"
    **Síntomas**: Botones deshabilitados o errores

    **Posibles causas**:
    - Permisos insuficientes
    - Usuario editando su propia cuenta
    - Sesión expirada

    **Soluciones**:
    - Verifica rol de administrador
    - Usa otra cuenta admin para editar
    - Refresca sesión

=== "Error al cambiar roles"
    **Síntomas**: Cambios no se guardan

    **Posibles causas**:
    - Intentando remover último admin
    - Validación de formulario falla
    - Problema de conectividad

    **Soluciones**:
    - Mantén al menos un administrador
    - Verifica campos requeridos
    - Reintenta operación

=== "Usuario no puede acceder"
    **Síntomas**: Login falla para usuario creado

    **Posibles causas**:
    - Cuenta inactiva
    - Contraseña no establecida
    - Email no verificado

    **Soluciones**:
    - Activa la cuenta manualmente
    - Resetea contraseña
    - Verifica configuración de email

!!! danger "Situaciones Críticas"
    - **Único administrador**: Nunca elimines el último admin
    - **Bloqueo masivo**: Mantén acceso de emergencia
    - **Compromiso de cuenta**: Suspende inmediatamente
    - **Pérdida de acceso**: Contacta soporte del sistema