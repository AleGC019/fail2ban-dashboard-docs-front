# Autenticación

Secure Dash utiliza un sistema de autenticación robusto que garantiza la seguridad de acceso al dashboard.

## :lock: Sistema de Login

### Pantalla de Autenticación

La pantalla principal de autenticación ofrece una interfaz moderna y segura:

![Placeholder: Pantalla completa de autenticación](assets/auth-full-screen.png)

#### Características Visuales
- **Diseño responsivo** que se adapta a cualquier dispositivo
- **Imagen hero** con testimonios de usuarios
- **Formularios dinámicos** con validación en tiempo real
- **Tema adaptativo** (claro/oscuro)

### Opciones de Acceso

=== "Iniciar Sesión"
    Para usuarios existentes que ya tienen una cuenta en el sistema.

=== "Crear Cuenta"
    Para nuevos usuarios que necesitan registrarse por primera vez.

## :pencil2: Registro de Nueva Cuenta

### Formulario de Registro

![Placeholder: Formulario de registro](assets/register-form.png)

#### Campos Requeridos

| Campo | Requisitos | Ejemplo |
|-------|------------|---------|
| **Nombre de Usuario** | 3-20 caracteres, solo letras, números, guiones y guiones bajos | `usuario123` |
| **Email** | Dirección email válida | `usuario@empresa.com` |
| **Contraseña** | Mínimo 8 caracteres, mayúscula, minúscula y número | `MiPassword123` |
| **Confirmar Contraseña** | Debe coincidir con la contraseña | `MiPassword123` |
| **Términos y Condiciones** | Debe aceptarse | ☑️ |

#### Validaciones en Tiempo Real

El formulario valida automáticamente:

!!! check "Validaciones Activas"
    - **Nombre de usuario**: Disponibilidad y formato
    - **Email**: Formato válido y unicidad
    - **Contraseña**: Fortaleza y criterios de seguridad
    - **Confirmación**: Coincidencia exacta

### Proceso de Registro

1. **Completar Formulario**
   - Llena todos los campos requeridos
   - Acepta términos y condiciones

2. **Validación Automática**
   - El sistema verifica los datos en tiempo real
   - Se muestran mensajes de error si es necesario

3. **Envío y Confirmación**
   - Haz clic en "Registrarse"
   - Recibirás confirmación de cuenta creada

4. **Redirección Automática**
   - El sistema te redirige al login
   - Ya puedes iniciar sesión con tus credenciales

!!! warning "Permisos Iniciales"
    Las cuentas nuevas tienen permisos de **Usuario Regular** por defecto. Para obtener permisos de administrador, contacta a un administrador existente.

## :key: Inicio de Sesión

### Formulario de Login

![Placeholder: Formulario de login](assets/login-form.png)

#### Métodos de Autenticación

Puedes iniciar sesión usando:

=== "Email"
    ```
    usuario@empresa.com
    ```

=== "Nombre de Usuario"
    ```
    usuario123
    ```

#### Opciones Adicionales

- **"Recordarme"**: Mantiene la sesión activa por más tiempo
- **Mostrar/Ocultar contraseña**: Toggle para verificar tu contraseña

### Proceso de Login

1. **Ingresar Credenciales**
   - Email o nombre de usuario
   - Contraseña

2. **Validación del Sistema**
   - Verificación de credenciales
   - Validación de estado de cuenta

3. **Redirección Exitosa**
   - Acceso automático al dashboard
   - Notificación de login exitoso

## :shield: Seguridad

### Características de Seguridad

!!! abstract "Medidas de Protección"
    - **Encriptación de contraseñas** con algoritmos seguros
    - **Tokens de sesión** con expiración automática
    - **Validación del lado del servidor** para todos los datos
    - **Protección CSRF** contra ataques de falsificación

### Políticas de Contraseña

Las contraseñas deben cumplir con:

- **Longitud mínima**: 8 caracteres
- **Mayúscula**: Al menos una letra mayúscula
- **Minúscula**: Al menos una letra minúscula  
- **Número**: Al menos un dígito
- **Caracteres especiales**: Recomendados pero no obligatorios

### Gestión de Sesiones

#### Duración de Sesión

| Opción | Duración |
|--------|----------|
| **Sesión normal** | 8 horas |
| **"Recordarme"** | 30 días |
| **Inactividad** | 2 horas (logout automático) |

#### Cierre de Sesión

Para cerrar sesión de forma segura:

1. Haz clic en tu avatar (esquina superior derecha)
2. Selecciona "Cerrar Sesión"
3. Serás redirigido a la pantalla de login

![Placeholder: Menú de usuario](assets/user-menu.png)

## :warning: Solución de Problemas

### Problemas Comunes

=== "No puedo iniciar sesión"
    **Posibles causas:**
    - Credenciales incorrectas
    - Cuenta bloqueada o inactiva
    - Problemas de conectividad

    **Soluciones:**
    - Verifica usuario/email y contraseña
    - Contacta al administrador
    - Intenta desde otro navegador

=== "Error al registrarse"
    **Posibles causas:**
    - Email ya registrado
    - Nombre de usuario en uso
    - Contraseña no cumple requisitos

    **Soluciones:**
    - Usa un email diferente
    - Elige otro nombre de usuario
    - Revisa los requisitos de contraseña

=== "Sesión expirada"
    **Causa:**
    - Tiempo de inactividad excedido
    - Token de sesión vencido

    **Solución:**
    - Inicia sesión nuevamente
    - Activa "Recordarme" para sesiones más largas

### Mensajes de Error

| Error | Significado | Acción |
|-------|-------------|--------|
| `Credenciales inválidas` | Usuario/contraseña incorrectos | Verificar datos |
| `Usuario no encontrado` | Email/usuario no existe | Verificar o registrarse |
| `Sesión expirada` | Token vencido | Iniciar sesión nuevamente |
| `Acceso denegado` | Sin permisos suficientes | Contactar administrador |

## :bulb: Consejos de Seguridad

!!! tip "Mejores Prácticas"
    - **Usa contraseñas únicas** para cada servicio
    - **No compartas credenciales** con otros usuarios
    - **Cierra sesión** cuando uses computadoras compartidas
    - **Mantén actualizado** tu navegador web
    - **Verifica la URL** antes de ingresar credenciales

!!! danger "Nunca hagas esto"
    - No uses contraseñas simples o comunes
    - No guardes contraseñas en navegadores públicos
    - No accedas desde redes WiFi públicas no seguras
    - No compartas tu cuenta con otros usuarios