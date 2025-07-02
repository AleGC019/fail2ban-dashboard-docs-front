# Primeros Pasos

Esta guía te ayudará a comenzar con Secure Dash desde cero, cubriendo desde el acceso inicial hasta la navegación básica.

## :key: Acceso Inicial

### 1. Acceder a la Aplicación

1. Abre tu navegador web
2. Navega a la URL de Secure Dash
3. Verás la pantalla de autenticación

![Placeholder: Pantalla de login de Secure Dash](assets/login-screen.png)

### 2. Primer Inicio de Sesión

=== "Si tienes cuenta"
    1. Ingresa tu **email o nombre de usuario**
    2. Introduce tu **contraseña**
    3. Haz clic en **"Iniciar Sesión"**

=== "Si necesitas crear cuenta"
    1. Haz clic en **"Crear cuenta"**
    2. Completa el formulario de registro
    3. Acepta los términos y condiciones
    4. Haz clic en **"Registrarse"**

!!! warning "Nota de Seguridad"
    Las cuentas de nuevos usuarios tienen permisos limitados por defecto. Contacta a un administrador para obtener permisos adicionales.

## :eyes: Primera Vista del Dashboard

Una vez autenticado, accederás al dashboard principal:

![Placeholder: Vista general del dashboard](assets/dashboard-overview.png)

### Elementos Principales

1. **Barra Superior**
   - Logo de Secure Dash
   - Breadcrumbs de navegación
   - Avatar y nombre de usuario

2. **Sidebar Izquierdo**
   - Navegación principal
   - Buscador rápido
   - Secciones del sistema

3. **Área Principal**
   - Contenido dinámico
   - Gráficos y métricas
   - Tablas de datos

4. **Área de Notificaciones**
   - Alertas en tiempo real
   - Estado del sistema

## :desktop_computer: Familiarización con la Interfaz

### Navegación Principal

El sidebar contiene las siguientes secciones:

!!! abstract "Secciones Disponibles"
    === "Usuarios Regulares"
        - :bar_chart: **Dashboard** - Métricas y estadísticas
        - :page_facing_up: **Logs de Fail2Ban** - Registro de eventos
        - :shield: **Lista de IPs** - IPs bloqueadas

    === "Administradores"
        - :bar_chart: **Dashboard** - Métricas y estadísticas
        - :page_facing_up: **Logs de Fail2Ban** - Registro de eventos
        - :shield: **Lista de IPs** - IPs bloqueadas
        - :busts_in_silhouette: **Usuarios** - Gestión de usuarios

### Funciones Básicas

#### Búsqueda Rápida
- Ubicada en el sidebar
- Presiona `/` para enfocar
- Busca en todas las secciones

![Placeholder: Función de búsqueda](assets/search-function.png)

#### Cambio de Tema
- Botón en la esquina superior derecha
- Alterna entre tema claro y oscuro
- Preferencia guardada automáticamente

#### Notificaciones
- Aparecen en la esquina inferior derecha
- Colores según importancia:
  - :green_circle: Verde: Información
  - :yellow_circle: Amarillo: Advertencia
  - :red_circle: Rojo: Error/Crítico

## :chart_with_upwards_trend: Explorando el Dashboard

### Métricas Principales

El dashboard muestra cuatro métricas clave:

| Métrica | Descripción |
|---------|-------------|
| **Total IPs** | IPs diferentes que han interactuado |
| **Total Logs** | Número total de eventos registrados |
| **Logs de Información** | Eventos informativos |
| **Logs de Alerta** | Eventos que requieren atención |

![Placeholder: Tarjetas de métricas](assets/metrics-cards.png)

### Gráficos en Tiempo Real

#### Gráfico de Actividad
- Muestra eventos por tiempo
- Actualización automática cada 5 segundos
- Punto verde indica datos en vivo

#### Top 5 IPs Bloqueadas
- Lista de IPs más problemáticas
- Número de bloqueos por IP
- Nivel de riesgo codificado por colores

![Placeholder: Gráficos del dashboard](assets/dashboard-charts.png)

## :gear: Configuración Inicial

### Personalización Básica

1. **Tema de Color**
   - Haz clic en el botón de tema (superior derecha)
   - Selecciona entre claro u oscuro

2. **Preferencias de Tabla**
   - Ajusta filas por página (10, 25, 50)
   - Configura filtros predeterminados

3. **Notificaciones**
   - Las notificaciones push están habilitadas por defecto
   - Se pueden deshabilitar desde configuración del navegador

### Primeras Acciones Recomendadas

!!! tip "Lista de Verificación"
    - [ ] Explora cada sección del sidebar
    - [ ] Revisa las métricas del dashboard
    - [ ] Prueba la función de búsqueda
    - [ ] Examina la tabla de logs
    - [ ] Verifica las IPs bloqueadas
    - [ ] Configura tu tema preferido

## :question: ¿Necesitas Ayuda?

### Recursos de Ayuda

- **[Navegación](navigation.md)** - Aprende más sobre la interfaz
- **[Dashboard](dashboard.md)** - Guía detallada del panel principal
- **[Solución de Problemas](troubleshooting.md)** - Resuelve problemas comunes

### Contacto

Si necesitas ayuda adicional:
- Contacta a tu administrador de sistema
- Revisa la sección de solución de problemas
- Consulta la documentación técnica

!!! success "¡Felicidades!"
    Has completado la configuración inicial de Secure Dash. Ahora estás listo para explorar todas las funcionalidades del sistema.