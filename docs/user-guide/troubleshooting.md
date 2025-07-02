# Solución de Problemas

Esta guía te ayudará a resolver los problemas más comunes que puedes encontrar al usar Secure Dash.

## :computer: Problemas de Acceso

### Problemas de Autenticación

=== "No puedo iniciar sesión"
    **Síntomas**:
    - Mensaje "Credenciales inválidas"
    - Página de login se recarga
    - No hay redirección al dashboard

    **Soluciones paso a paso**:
    
    1. **Verificar credenciales**:
       ```
       ✓ Email o usuario correcto
       ✓ Contraseña exacta (case-sensitive)
       ✓ Sin espacios adicionales
       ```

    2. **Limpiar caché del navegador**:
       - Chrome: `Ctrl/Cmd + Shift + Delete`
       - Firefox: `Ctrl/Cmd + Shift + Delete`
       - Safari: `Cmd + Option + E`

    3. **Probar navegador diferente**:
       - Chrome, Firefox, Safari, Edge
       - Modo incógnito/privado

    4. **Verificar conectividad**:
       - Revisar conexión a internet
       - Probar otros sitios web
       - Verificar firewall/proxy

=== "Sesión se cierra automáticamente"
    **Síntomas**:
    - Redirección inesperada al login
    - Mensaje "Sesión expirada"
    - Pérdida de estado durante uso

    **Causas y soluciones**:

    | Causa | Tiempo | Solución |
    |-------|--------|----------|
    | **Inactividad** | 2 horas | Usar la aplicación regularmente |
    | **Sesión normal** | 8 horas | Activar "Recordarme" |
    | **Token vencido** | Variable | Reiniciar sesión |

=== "Pantalla de login no carga"
    **Síntomas**:
    - Página en blanco
    - Error de conexión
    - Carga infinita

    **Diagnóstico**:
    
    1. **Verificar URL**:
       ```
       ✓ URL correcta del servidor
       ✓ HTTPS habilitado
       ✓ Puerto correcto
       ```

    2. **Revisar red**:
       ```bash
       # Probar conectividad básica
       ping [servidor-secure-dash]
       ```

    3. **Estado del servidor**:
       - Contactar administrador
       - Verificar mantenimiento programado

## :link: Problemas de Conectividad

### Desconexión de WebSocket

=== "Indicadores de desconexión"
    **Síntomas visuales**:
    - Punto rojo en gráficos (en lugar de verde)
    - Mensaje "Conexión perdida"
    - Datos no se actualizan
    - Alertas no llegan

    ![Placeholder: Indicadores de desconexión](assets/disconnection-indicators.png)

=== "Soluciones de reconexión"
    **Acciones automáticas**:
    - Reintento cada 5 segundos
    - Reconexión automática
    - Sincronización al restaurar

    **Acciones manuales**:
    1. **Refresco suave**: `F5` o `Ctrl/Cmd + R`
    2. **Refresco completo**: `Ctrl/Cmd + Shift + R`
    3. **Cerrar y reabrir pestaña**
    4. **Reiniciar navegador**

### Problemas de Red

=== "Conexión lenta"
    **Síntomas**:
    - Carga lenta de datos
    - Timeout en operaciones
    - Gráficos no se actualizan

    **Optimizaciones**:
    
    !!! tip "Mejoras de rendimiento"
        - Cerrar pestañas innecesarias
        - Deshabilitar extensiones
        - Usar conexión ethernet
        - Verificar ancho de banda

=== "Firewall/Proxy"
    **Puertos requeridos**:
    ```
    HTTP:  Puerto 80
    HTTPS: Puerto 443
    WebSocket: Puerto 443 (WSS)
    ```

    **Configuración de proxy**:
    - Permitir dominio de Secure Dash
    - Habilitar WebSocket connections
    - Configurar bypass para APIs

## :desktop_computer: Problemas de Interfaz

### Elementos No Cargan

=== "Dashboard vacío"
    **Síntomas**:
    - Métricas muestran 0
    - Gráficos no aparecen
    - Tablas vacías

    **Diagnóstico**:
    
    1. **Verificar permisos**:
       ```
       ✓ Usuario tiene acceso a datos
       ✓ Rol correcto asignado
       ✓ Sin restricciones de IP
       ```

    2. **Revisar datos del servidor**:
       ```
       ✓ Fail2ban está funcionando
       ✓ Logs se están generando
       ✓ Base de datos accesible
       ```

=== "Tablas no cargan"
    **Síntomas**:
    - Spinner de carga infinito
    - Error "No se pudieron cargar datos"
    - Tabla muestra estado vacío

    **Soluciones por orden**:
    
    1. **Refresco de página**: `F5`
    2. **Cambiar filtros**: Resetear todos los filtros
    3. **Verificar permisos**: Contactar administrador
    4. **Reportar problema**: Incluir screenshots

=== "Gráficos distorsionados"
    **Síntomas**:
    - Elementos superpuestos
    - Texto cortado
    - Escalas incorrectas

    **Soluciones**:
    ```
    1. Cambiar zoom del navegador (100%)
    2. Redimensionar ventana
    3. Cambiar orientación (móvil)
    4. Actualizar navegador
    ```

### Problemas de Responsive

=== "Móvil"
    **Problemas comunes**:
    - Sidebar no se abre
    - Botones muy pequeños
    - Texto ilegible

    **Soluciones**:
    - Orientación horizontal recomendada
    - Zoom adecuado del navegador
    - Usar navegador móvil actualizado

=== "Tablet"
    **Problemas comunes**:
    - Layout desorganizado
    - Elementos superpuestos
    - Touch no funciona

    **Soluciones**:
    - Verificar orientación
    - Limpiar caché del navegador
    - Actualizar sistema operativo

## :chart_with_upwards_trend: Problemas de Datos

### Datos Inconsistentes

=== "Métricas no coinciden"
    **Síntomas**:
    - Dashboard vs tablas diferentes
    - Números no actualizados
    - Datos desactualizados

    **Explicaciones comunes**:
    
    | Diferencia | Causa | Solución |
    |------------|-------|----------|
    | **Tiempo de caché** | Cache del navegador | Refresco forzado |
    | **Filtros activos** | Filtros en tablas | Resetear filtros |
    | **Sincronización** | Delay de WebSocket | Esperar 30 segundos |

=== "Alertas no llegan"
    **Verificaciones**:
    
    1. **Permisos del navegador**:
       ```
       Chrome: Configuración > Privacidad > Notificaciones
       Firefox: Preferencias > Privacidad > Notificaciones
       Safari: Preferencias > Sitios web > Notificaciones
       ```

    2. **Configuración del sistema**:
       - Windows: Centro de actividades
       - macOS: Preferencias del sistema
       - Linux: Configuración de notificaciones

### Exportación de Datos

=== "Download no funciona"
    **Síntomas**:
    - Botón no responde
    - Archivo no se descarga
    - Error en consola

    **Soluciones**:
    
    1. **Verificar bloqueadores**:
       - Deshabilitar ad-blockers
       - Permitir pop-ups
       - Revisar descargas del navegador

    2. **Permisos de archivo**:
       - Verificar carpeta de descargas
       - Espacio en disco suficiente
       - Permisos de escritura

## :bust_in_silhouette: Problemas de Usuarios (Admin)

### Gestión de Usuarios

=== "No puedo crear usuarios"
    **Verificaciones**:
    ```
    ✓ Permisos de administrador
    ✓ Formulario completo
    ✓ Email único
    ✓ Contraseña cumple requisitos
    ```

=== "Usuario no puede acceder"
    **Pasos de diagnóstico**:
    
    1. **Verificar estado del usuario**:
       - Estado activo
       - Rol asignado
       - Sin bloqueo temporal

    2. **Resetear credenciales**:
       - Cambiar contraseña temporal
       - Verificar email correcto
       - Confirmar activación

## :wrench: Herramientas de Diagnóstico

### Consola del Navegador

#### Acceder a la Consola
```
Chrome/Firefox: F12 → Console
Safari: Cmd + Option + C
Edge: F12 → Console
```

#### Errores Comunes
```javascript
// Error de conexión WebSocket
WebSocket connection failed

// Error de autenticación
401 Unauthorized

// Error de red
Network Error / Failed to fetch

// Error de JavaScript
TypeError: Cannot read property
```

### Información del Sistema

#### Datos para Soporte
Cuando contactes soporte, incluye:

```
- Navegador y versión
- Sistema operativo
- URL completa
- Hora exacta del problema
- Screenshots del error
- Logs de consola (si disponibles)
```

#### Recopilar Información
```javascript
// En consola del navegador
console.log('User Agent:', navigator.userAgent);
console.log('URL:', window.location.href);
console.log('Timestamp:', new Date().toISOString());
```

## :sos: Contacto de Soporte

### Canales de Ayuda

=== "Autoservicio"
    - Esta documentación
    - Preguntas frecuentes
    - Videos tutoriales
    - Foros de usuarios

=== "Soporte Técnico"
    - Email: soporte@secure-dash.com
    - Ticket system
    - Chat en vivo (horario laboral)
    - Teléfono de emergencia

### Información Requerida

!!! warning "Antes de Contactar Soporte"
    Prepara la siguiente información:
    
    - **Descripción detallada** del problema
    - **Pasos para reproducir** el error
    - **Screenshots** o videos del problema
    - **Información del navegador** y sistema
    - **Hora exacta** cuando ocurrió
    - **Frecuencia** del problema

### Niveles de Urgencia

| Nivel | Descripción | Tiempo de Respuesta |
|-------|-------------|-------------------|
| **Crítico** | Sistema no funciona | 2 horas |
| **Alto** | Funcionalidad importante afectada | 4 horas |
| **Medio** | Problema menor con workaround | 24 horas |
| **Bajo** | Consulta general | 48 horas |

## :books: Recursos Adicionales

### Documentación Relacionada

- [Navegación](navigation.md) - Problemas de interfaz
- [Dashboard](dashboard.md) - Métricas y gráficos
- [Autenticación](authentication.md) - Problemas de login
- [IPs Bloqueadas](banned-ips.md) - Gestión de IPs

### Enlaces Útiles

- **Estado del servicio**: https://status.secure-dash.com
- **Actualizaciones**: https://updates.secure-dash.com
- **Comunidad**: https://community.secure-dash.com
- **GitHub Issues**: https://github.com/secure-dash/issues

!!! success "Problema Resuelto"
    Si lograste resolver tu problema, considera documentar la solución para ayudar a otros usuarios en el futuro.

!!! info "Mejora Continua"
    Tu feedback nos ayuda a mejorar Secure Dash. No dudes en reportar problemas o sugerir mejoras.