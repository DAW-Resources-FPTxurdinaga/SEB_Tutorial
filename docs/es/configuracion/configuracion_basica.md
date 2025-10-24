# 3. Configuración de Safe Exam Browser

## 3.1. Introducción a la configuración de SEB

SEB se configura mediante archivos `.seb` encriptados que controlan su comportamiento durante los exámenes. Es fundamental utilizar la herramienta de configuración oficial (`SebWindowsConfig.exe` en Windows) para crear estos archivos.

!!! warning "Importante"
    Siempre establece una contraseña de administrador en tus configuraciones para prevenir modificaciones no autorizadas.

## 3.2. Guía paso a paso de configuración

### Paso 1: Abrir la Herramienta de Configuración

#### En Windows:
1. Busca "SEB Config Tool" en el menú Inicio.
2. O ejecuta directamente `SebWindowsConfig.exe` desde la carpeta de instalación (normalmente en `C:\Program Files\SafeExamBrowser\`).

### Paso 2: Configuración Básica (Pestaña General)

1. **URL de Inicio**:
    - Ingresa la URL completa del examen (ej: `https://tu-lms.com/examen1`).
    - Asegúrate de incluir `https://` para conexiones seguras.

2. **Contraseña de Administrador**:
    - Establece una contraseña fuerte (mínimo 8 caracteres, mayúsculas, minúsculas, números y símbolos).
    - Esta contraseña será necesaria para modificar la configuración.

3. **Permitir Salir de SEB**:
    - **Recomendado**: Desactiva esta opción para evitar que los estudiantes cierren el navegador.
    - Si la activas, establece una "Contraseña para Salir" diferente a la de administrador.

4. **Modo de Examen**:
    - Selecciona "Usar archivo de configuración SEB para iniciar un examen".
    - Esto permite configuraciones específicas para cada examen.

### Paso 3: Configuración de Interfaz de Usuario

1. **Modo Pantalla Completa**:
    - Activa para maximizar el área de trabajo y minimizar distracciones.
   
2. **Barra de Tareas**:
    - Desactiva para evitar accesos no deseados.
   
3. **Recarga de Página**:
    - Configura según necesidad:
      - "Permitir con advertencia" para evitar cierres accidentales.
      - O desactiva para mayor seguridad.

### Paso 4: Configuración del Navegador

1. **Bloqueo de Navegación**:
    - Activa "Bloquear enlaces a nuevas ventanas".
    - Desactiva navegación atrás/adelante.
   
2. **Opciones de Visualización**:
    - Oculta la barra de direcciones.
    - Desactiva el corrector ortográfico si no es necesario.

### Paso 5: Control de Aplicaciones

1. **Monitorización de Procesos**:
    - Activa "Monitorizar Procesos".
   
2. **Aplicaciones Permitidas**:
    - Añade aplicaciones permitidas (ej: calculadora de Windows).
   
3. **Aplicaciones Bloqueadas**:
    - Añade navegadores (Chrome, Firefox, Edge).
    - Incluye aplicaciones de mensajería o captura de pantalla.

### Paso 6: Configuración de Red

1. **Filtro de URLs**:
    - Activa "Filtro de URLs".
    - Configura reglas:
     ```
     block:*
     allow:tu-lms.com/*
     ```
    - Ajusta los dominios según tu plataforma de exámenes.

### Paso 7: Configuración de Seguridad Avanzada

1. **Modo Kiosco**:
    - Selecciona "Crear Nuevo Escritorio".
    - Aísla completamente la sesión de examen.
   
2. **Protección contra Capturas**:
    - Desactiva la posibilidad de capturas de pantalla.
   
3. **Bloqueo de Accesos**:
    - Desactiva actualizaciones automáticas de Windows.
    - Bloquea el uso de máquinas virtuales.

### Paso 8: Bloqueo de Teclas

1. **Teclas a Bloquear**:
    - Alt+Tab
    - Ctrl+Alt+Supr
    - Impr Pant / PrintScreen
    - Tecla de Windows
    - Clic derecho

2. **Personalización de Atajos**:
    - Desactiva o reasigna combinaciones de teclas según necesidades.

### Paso 9: Configuración para el LMS

1. **Clave de Examen del Navegador**:
    - Genera una clave única para el examen.
    - Cópiala al configurar el examen en tu LMS (Moodle, etc.).
   
2. **Verificación de Configuración**:
    - SEB verificará esta clave al iniciar el examen.
    - Asegura que los estudiantes usen la configuración correcta.

## 3.3. Guardar la Configuración

1. **Guardar como Plantilla**:
    - Útil para exámenes futuros.
    - Usa la extensión `.seb`.
   
2. **Protección con Contraseña**:
    - Asegúrate de que el archivo esté encriptado.
    - Verifica que pida contraseña al abrirlo.

3. **Pruebas de Validación**:
    - Prueba el archivo en un equipo de prueba.
    - Verifica todas las restricciones.

## 3.4. Distribución del Archivo de Configuración

1. **Métodos de Distribución**:
    - Sube el archivo a tu plataforma educativa.
    - O envíalo por correo electrónico a los estudiantes.
   
2. **Instrucciones para Estudiantes**:
    - Explica cómo abrir el archivo con SEB.
    - Proporciona soporte técnico si es necesario.

## 3.5. Solución de Problemas Comunes

### Problemas de Inicio
- **SEB no inicia**:
   - Verifica que el archivo `.seb` no esté dañado.
   - Revisa los permisos del sistema.
  
- **Error de Contraseña**:
   - Asegúrate de usar la contraseña correcta.
   - Verifica mayúsculas y caracteres especiales.

### Problemas de Conexión
- **URL no carga**:
   - Comprueba la conexión a internet.
   - Verifica que la URL esté escrita correctamente.
   - Asegúrate de que el dominio esté en la lista de permitidos.

### Problemas de Rendimiento
- **Lentitud**:
   - Cierra otras aplicaciones.
   - Verifica los requisitos del sistema.

## 3.6. Consejos para una Configuración Segura

### Mejores Prácticas
1. **Contraseñas Fuertes**:
    - Usa una combinación de letras, números y símbolos.
    - No compartas contraseñas por correo electrónico.

2. **Pruebas Previas**:
    - Realiza pruebas con antelación.
    - Verifica todas las restricciones.

3. **Copia de Seguridad**:
    - Guarda una copia de la configuración.
    - Documenta los cambios realizados.

### Seguridad Adicional
- **Actualizaciones**:
   - Mantén SEB actualizado.
   - Revisa las actualizaciones de seguridad.
  
- **Monitoreo**:
   - Supervisa la actividad durante los exámenes.
   - Registra incidentes para futuras mejoras.

## 3.7. Recursos Adicionales

### Enlaces Útiles
- [Documentación Oficial de SEB](https://safeexambrowser.org/)
- [Guía de Configuración para Windows](https://safeexambrowser.org/windows/win_usermanual_en.html)
- [Foro de Soporte](https://safeexambrowser.org/forum/)

### Soporte Técnico
- Contacta con el servicio técnico de tu institución.
- Proporciona detalles del problema para una solución más rápida.

---

En el próximo capítulo, veremos cómo integrar SEB con plataformas de aprendizaje como Moodle, Blackboard y Canvas, y cómo gestionar exámenes en línea de manera efectiva.
