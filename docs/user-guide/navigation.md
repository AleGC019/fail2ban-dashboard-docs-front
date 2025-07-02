# Navegación

Aprende a navegar eficientemente por todas las secciones de Secure Dash y aprovecha al máximo la interfaz de usuario.

## :compass: Estructura General

### Layout Principal

Secure Dash utiliza un diseño moderno de sidebar que se adapta a diferentes tamaños de pantalla:

![Placeholder: Layout general de la aplicación](assets/main-layout.png)

#### Componentes Principales

1. **Header Superior** - Navegación y usuario
2. **Sidebar Izquierdo** - Menú principal
3. **Área de Contenido** - Información principal
4. **Notificaciones** - Alertas en tiempo real

## :hamburger: Sidebar y Menú Principal

### Estructura del Sidebar

![Placeholder: Sidebar completo](assets/sidebar-full.png)

#### Secciones del Menú

=== "Todos los Usuarios"
    **Secciones Generales**
    
    - :bar_chart: **Dashboard** - Panel principal con métricas
    - :page_facing_up: **Fail2Ban Logs** - Registros del sistema
    - :shield: **Lista de IPs** - IPs bloqueadas

=== "Solo Administradores"
    **Administración**
    
    - :busts_in_silhouette: **Usuarios** - Gestión de usuarios del sistema

### Elementos Interactivos

#### Logo y Branding
- **Logo de Secure Dash** en la parte superior
- Actúa como botón de inicio
- Siempre visible y accesible

#### Buscador Integrado
- Búsqueda global en el sidebar
- Atajo de teclado: presiona `/`
- Busca en contenido y navegación

![Placeholder: Función de búsqueda en sidebar](assets/sidebar-search.png)

### Estados Visuales

#### Navegación Activa
Los elementos del menú muestran diferentes estados:

- **Activo**: Gradiente azul y texto resaltado
- **Hover**: Gradiente sutil al pasar el mouse
- **Inactivo**: Texto gris y sin fondo

#### Indicadores de Carga
- Animación de pulso durante la navegación
- Feedback visual instantáneo
- Mantiene al usuario informado

## :arrow_up: Header Superior

### Elementos del Header

![Placeholder: Header con todos los elementos](assets/header-complete.png)

#### Componentes Principales

1. **Botón de Sidebar** (móvil)
   - Aparece solo en dispositivos móviles
   - Abre/cierra el menú lateral

2. **Breadcrumbs**
   - Muestra tu ubicación actual
   - Incluye ícono de escudo
   - Navegación jerárquica

3. **Área de Usuario**
   - Avatar del usuario
   - Nombre de bienvenida
   - Acceso a configuración

### Breadcrumbs Dinámicos

Los breadcrumbs se actualizan automáticamente según tu ubicación:

| Página | Breadcrumb |
|--------|------------|
| `/app` | :shield: → Fail2ban Logs |
| `/app/dashboard` | :shield: → Dashboard |
| `/app/banned-ips` | :shield: → Lista De Ips |
| `/app/users` | :shield: → Gestión De Usuarios |

## :iphone: Navegación Responsiva

### Dispositivos Móviles

En pantallas pequeñas (< 768px):

- **Sidebar colapsado** por defecto
- **Botón hamburguesa** en el header
- **Navegación táctil** optimizada
- **Contenido adaptado** al espacio disponible

![Placeholder: Vista móvil con menú colapsado](assets/mobile-navigation.png)

### Tablets

En pantallas medianas (768px - 1024px):

- **Sidebar visible** pero más compacto
- **Iconos prominentes** para fácil acceso
- **Gestos táctiles** soportados

### Escritorio

En pantallas grandes (> 1024px):

- **Sidebar completo** siempre visible
- **Hover effects** mejorados
- **Navegación con teclado** optimizada

## :keyboard: Atajos de Teclado

### Navegación Global

| Atajo | Acción |
|-------|--------|
| `/` | Enfocar búsqueda |
| `Escape` | Cerrar modales/hojas |
| `Tab` | Navegación secuencial |
| `Shift + Tab` | Navegación reversa |

### Navegación por Secciones

| Atajo | Destino |
|-------|---------|
| `Alt + D` | Dashboard |
| `Alt + L` | Logs |
| `Alt + I` | IPs Bloqueadas |
| `Alt + U` | Usuarios (admin) |

!!! tip "Consejo de Navegación"
    Los atajos de teclado mejoran significativamente la velocidad de navegación para usuarios frecuentes.

## :gear: Personalización

### Preferencias de Interfaz

#### Tema de Colores
- **Botón de tema** en esquina superior derecha
- Alterna entre claro y oscuro
- Preferencia guardada automáticamente

![Placeholder: Selector de tema](assets/theme-selector.png)

#### Tamaño de Sidebar
- **Auto-colapso** en pantallas pequeñas
- **Expansión manual** disponible
- **Estado recordado** por sesión

### Configuración de Tabla

Para todas las tablas del sistema:

- **Filas por página**: 10, 25, 50
- **Orden de columnas**: Personalizable
- **Filtros**: Persistentes durante la sesión

## :mag: Función de Búsqueda

### Búsqueda Global

#### Activación
- Haz clic en el campo de búsqueda del sidebar
- Presiona `/` desde cualquier página
- Comienza a escribir inmediatamente

#### Capacidades
- **Búsqueda en tiempo real** mientras escribes
- **Resultados contextuales** por sección
- **Navegación directa** a resultados

![Placeholder: Resultados de búsqueda](assets/search-results.png)

### Búsquedas Específicas

Cada sección tiene su propia búsqueda avanzada:

- **Logs**: Por mensaje, nivel, fecha
- **IPs**: Por dirección, país, amenaza
- **Usuarios**: Por nombre, email, rol

## :link: Enlaces y Navegación

### Tipos de Enlaces

#### Enlaces Internos
- **Navegación instantánea** sin recarga
- **Estado preservado** durante navegación
- **Historial del navegador** mantenido

#### Enlaces Externos
- **Indicadores visuales** para enlaces externos
- **Apertura en nueva pestaña** (donde apropiado)
- **Confirmación** antes de salir del sistema

### Navegación por Pestañas

Secure Dash soporta navegación multi-pestaña:

- **Estado independiente** por pestaña
- **Sincronización automática** de datos
- **Notificaciones** en todas las pestañas activas

## :warning: Indicadores de Estado

### Estados de Conexión

La aplicación muestra indicadores visuales para:

#### Conectado
- **Punto verde** en gráficos en tiempo real
- **Actualizaciones automáticas** funcionando
- **WebSocket activo**

#### Desconectado
- **Advertencia visible** en interfaz
- **Reintento automático** de conexión
- **Datos en caché** mostrados

#### Sincronizando
- **Indicador de carga** en header
- **Animaciones sutiles** durante actualización
- **Feedback inmediato** al usuario

![Placeholder: Indicadores de estado de conexión](assets/connection-status.png)

## :bulb: Mejores Prácticas

### Navegación Eficiente

!!! tip "Consejos de Navegación"
    - **Usa atajos de teclado** para navegación rápida
    - **Aprovecha breadcrumbs** para orientación
    - **Mantén múltiples pestañas** para comparar datos
    - **Usa búsqueda global** para acceso directo

### Organización del Trabajo

!!! success "Flujo Recomendado"
    1. **Inicia en Dashboard** para visión general
    2. **Revisa alertas** en notificaciones
    3. **Profundiza en logs** según necesidad
    4. **Gestiona IPs** cuando sea necesario
    5. **Administra usuarios** (solo admins)

### Solución de Problemas de Navegación

| Problema | Solución |
|----------|----------|
| Sidebar no aparece | Refresca la página |
| Navegación lenta | Verifica conexión a internet |
| Enlaces no funcionan | Limpia caché del navegador |
| Breadcrumbs incorrectos | Navega usando el menú principal |

!!! warning "Nota Importante"
    Si experimentas problemas persistentes de navegación, contacta al administrador del sistema o revisa la [sección de solución de problemas](troubleshooting.md).