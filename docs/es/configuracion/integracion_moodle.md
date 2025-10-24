# Integración con Moodle

## Configuración básica de SEB en Moodle

### 🎥 Videotutorial de integración con Moodle

Antes de comenzar, te recomendamos ver este videotutorial que muestra el proceso completo de integración de SEB con Moodle:

[![Tutorial de integración SEB con Moodle](https://img.youtube.com/vi/clRh0efdSJo/0.jpg)](https://www.youtube.com/watch?v=clRh0efdSJo)

### 📋 Requisitos previos
- Moodle 3.5 o superior instalado
- Permisos de administrador en el sitio Moodle
- Navegador SEB instalado en los equipos de los estudiantes
- Módulo de actividad "Cuestionario" activado en Moodle

## 🔧 Configuración en Moodle

### 1. Habilitar SEB en el cuestionario

1. **Crear/Editar un cuestionario**:
    - Ve a la sección del curso donde quieras añadir el examen
    - Haz clic en "Añadir una actividad o recurso"
    - Selecciona "Cuestionario" y haz clic en "Agregar"

2. **Configurar SEB**:
    - En la página de configuración del cuestionario, desplázate hasta la sección **Safe Exam Browser**
    - Selecciona **"Sí"** en la opción **"Requerir Safe Exam Browser"**
    - Elige el tipo de configuración:
      - **Configuración del navegador**: Usa las opciones básicas de Moodle
      - **Archivo de configuración SEB**: Carga un archivo de configuración personalizado

### 2. Opciones de configuración recomendadas

#### 🔒 Opciones de seguridad básicas
 - **Bloquear salida del navegador**: Impide que los estudiantes cierren SEB durante el examen
 - **Deshabilitar atajos de teclado**: Evita el uso de combinaciones como Alt+Tab o Ctrl+W
 - **Modo pantalla completa**: Obliga a mostrar el examen en pantalla completa
 - **Bloquear capturas de pantalla**: Impide que los estudiantes capturen el contenido

#### 🌐 Configuración de red
 - **Permitir sitios web específicos**: Lista blanca de URLs permitidas
 - **Bloquear descargas**: Evita la descarga de archivos durante el examen
 - **Permitir recursos locales**: Útil para exámenes con archivos locales

### 3. Configuración avanzada

Puedes personalizar aún más la configuración mediante un archivo XML. Aquí tienes un ejemplo con las opciones más importantes:

## ⚙️ Configuración XML recomendada

```xml
<?xml version="1.0" encoding="UTF-8"?>
<plist version="1.0">
<dict>
    <!-- Navegación -->
    <key>allowBrowsingBackForward</key>
    <false/>
    <key>allowReloading</key>
    <false/>
    <key>newWindow</key>
    <false/>
    <key>enableSpellCheck</key>
    <false/>
    
    <!-- Ventana del navegador -->
    <key>browserViewMode</key>
    <integer>1</integer> <!-- 1 = Pantalla completa -->
    <key>hideToolbar</key>
    <true/>
    
    <!-- Seguridad -->
    <key>quitURL</key>
    <string>about:blank</string>
    <key>quitURLConfirm</key>
    <true/>
    
    <!-- Contenido web -->
    <key>enablePlugIns</key>
    <false/>
    <key>enableJava</key>
    <false/>
    <key>enableJavaScript</key>
    <true/>
    <key>enableCookies</key>
    <true/>
    
    <!-- Teclado -->
    <key>enableKeychain</key>
    <false/>
    <key>enableInputManagers</key>
    <false/>
</dict>
</plist>
```

### 📝 Explicación de las opciones clave

| Opción | Valor | Descripción |
|--------|-------|-------------|
| `browserViewMode` | 1 | Pantalla completa (2 = Ventana, 3 = Sin bordes) |
| `allowReloading` | false | Impide recargar la página durante el examen |
| `enablePlugIns` | false | Desactiva todos los plugins del navegador |
| `enableJavaScript` | true | Necesario para el funcionamiento de Moodle |
| `quitURL` | about:blank | Página que se muestra al salir de SEB |
| `enableKeychain` | false | Desactiva el acceso al llavero de contraseñas |
```

## 🛠️ Solución de problemas comunes

### 1. Los estudiantes no pueden iniciar el examen
- **Síntoma**: SEB no se inicia o muestra un error al abrir el examen
- **Solución**:
  - Verifica que la URL del sitio Moodle esté correctamente configurada en SEB
  - Comprueba que el certificado SSL sea válido y esté correctamente instalado
  - Asegúrate de que los estudiantes tengan instalada la versión correcta de SEB

### 2. Problemas con las restricciones
- **Síntoma**: Las restricciones no se aplican correctamente
- **Solución**:
  - Verifica que el archivo de configuración SEB esté correctamente formateado
  - Comprueba que no haya configuraciones contradictorias en el archivo XML
  - Asegúrate de que el navegador SEB esté actualizado a la última versión

### 3. Errores de conexión
- **Síntoma**: Pérdida de conexión durante el examen
- **Solución**:
  - Verifica la estabilidad de la conexión de red
  - Asegúrate de que los puertos necesarios (80, 443) estén abiertos en el firewall
  - Configura un tiempo de espera adecuado en la configuración del cuestionario

## 📌 Consejos adicionales

1. **Pruebas previas**:
   - Siempre realiza pruebas con un usuario de prueba antes del examen real
   - Verifica que todas las restricciones funcionen como se espera

2. **Comunicación con los estudiantes**:
   - Proporciona instrucciones claras sobre cómo instalar y usar SEB
   - Realiza una sesión de prueba con los estudiantes antes del examen real

3. **Copia de seguridad**:
   - Guarda una copia de la configuración SEB utilizada
   - Ten un plan B en caso de fallos técnicos

## 🔗 Recursos adicionales

- [📚 Documentación oficial de SEB](https://safeexambrowser.org/)
- [🎓 Guía completa de integración con Moodle](https://docs.moodle.org/all/es/Safe_Exam_Browser)
- [💬 Foro de soporte de SEB](https://safeexambrowser.org/support_forum/index.html)
- [📥 Descargar la última versión de SEB](https://safeexambrowser.org/download_en.html)

## 📞 Soporte

Si necesitas ayuda adicional, no dudes en contactar con el soporte técnico de tu centro o consultar los foros oficiales de Moodle y SEB.
