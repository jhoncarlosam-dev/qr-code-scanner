# 📷 Lector de Códigos QR desde Imagen

Una aplicación web simple y moderna para leer y decodificar códigos QR desde imágenes. Permite cargar imágenes y detectar automáticamente los códigos QR contenidos en ellas.

## 🎯 Características

- ✅ **Carga de imágenes**: Soporta drag & drop y selección tradicional
- 🔍 **Detección de QR**: Decodifica códigos QR de múltiples formatos
- 👁️ **Vista previa**: Visualiza la imagen antes de escanear
- 🔄 **Detección invertida**: Intenta detectar códigos en imágenes invertidas
- 🛡️ **Seguridad**: Protección contra XSS al mostrar resultados
- 📱 **Responsive**: Interfaz adaptable a dispositivos móviles
- 🎨 **Diseño moderno**: Interfaz limpia y amigable

## 🚀 Cómo Usar

### Instalación
No requiere instalación. Solo necesitas:
1. Descargar o clonar el repositorio
2. Abrir `index.html` en un navegador web moderno

### Uso
1. **Cargar una imagen**:
   - Haz clic en la zona de carga para seleccionar un archivo
   - O arrastra y suelta una imagen directamente

2. **Escanear el QR**:
   - Haz clic en el botón "🔍 Escanear QR"

3. **Ver resultado**:
   - El contenido del código QR se mostrará en la sección de resultados
   - Se indica la ubicación del código en la imagen

## 📋 Requisitos

- Navegador web moderno con soporte para:
  - Canvas API
  - File API
  - FileReader API
- Conexión a Internet (para cargar la librería jsQR desde CDN)

### Navegadores Soportados
- ✅ Chrome/Chromium 60+
- ✅ Firefox 55+
- ✅ Safari 11+
- ✅ Edge 79+

## 🔧 Funcionalidades Técnicas

### Tecnologías Utilizadas
- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos y responsive
- **JavaScript**: Lógica de la aplicación
- **jsQR**: Librería para decodificación de códigos QR (CDN)

### Flujo de Funcionamiento
1. El usuario selecciona una imagen
2. Se crea una vista previa de la imagen
3. Se dibuja la imagen en un canvas HTML
4. Se extraen los datos de píxeles del canvas
5. La librería jsQR analiza los píxeles para encontrar códigos QR
6. Si no encuentra nada, intenta con inversión de colores
7. Se muestra el resultado: contenido del QR, tipo y ubicación

### Seguridad
- **Validación de entrada**: Verifica que se haya seleccionado una imagen
- **Escape HTML**: Previene inyección de código XSS en resultados
- **Procesamiento local**: Los datos se procesan completamente en el navegador

## 📝 Estructura del Archivo

```
index.html          - Archivo principal con HTML, CSS y JavaScript
readme.md          - Este archivo de documentación
```

## 🎨 Interfaz Visual

- **Zona de carga**: Área interactiva para seleccionar/arrastrar imágenes
- **Botón de escaneo**: Dispara el análisis del código QR
- **Sección de resultados**: Muestra el contenido detectado
- **Manejo de errores**: Mensajes claros cuando algo sale mal

## ⚙️ Opciones Avanzadas

### Modos de Detección

El código incluye dos modos de detección de QR:
- `inversionAttempts: "dontInvert"`: Detección estándar
- `inversionAttempts: "attemptBoth"`: Intenta con inversión de colores

Puedes modificar estas opciones en la función `scanQR()` según tus necesidades.

## 🐛 Solución de Problemas

| Problema | Solución |
|----------|----------|
| No se detecta el QR | Verifica que el código esté completo y bien enfocado en la imagen |
| Formato no compatible | Asegúrate de usar formatos soportados: JPG, PNG, GIF, WebP |
| La imagen no se carga | Intenta con una imagen más pequeña o en otro formato |
| Resultados inesperados | Prueba con `inversionAttempts: "attemptBoth"` para imágenes invertidas |

## 📦 Dependencias Externas

- **jsQR (1.4.0)**: Librería de decodificación QR
  - CDN: `https://cdn.jsdelivr.net/npm/jsqr@1.4.0/dist/jsQR.js`
  - Licencia: Apache 2.0

## 💡 Mejoras Futuras

- [ ] Soporte para escaneo desde cámara web en vivo
- [ ] Exportar resultados (copiar al portapapeles, descargar)
- [ ] Historial de códigos escaneados
- [ ] Soporte para múltiples códigos QR en una sola imagen
- [ ] Temas oscuro/claro

## 📄 Licencia

Este proyecto está disponible bajo licencia libre. Úsalo libremente en tus proyectos.

## 👤 Contribuciones

Las contribuciones son bienvenidas. Si encuentras algún bug o tienes sugerencias de mejora, siéntete libre de reportarlas.

---

**Última actualización**: Abril 2026

Hecho con ❤️ para facilitar la lectura de códigos QR
