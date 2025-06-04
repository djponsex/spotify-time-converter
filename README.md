# 🎧 Spotify Time Converter PRO

<div align="center">
  
  ![Spotify](https://img.shields.io/badge/Spotify-1DB954?style=for-the-badge&logo=spotify&logoColor=white)
  ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
  ![HTML5](https://img.shields.io/badge/HTML5-E34C26?style=for-the-badge&logo=html5&logoColor=white)
  ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
  
  <h3>Convierte tus cortes de tiempo de Spotify al formato JSON de manera rápida y elegante</h3>
  
  [Demo en Vivo](https://djponsex.github.io/spotify-time-converter/pro.html) | [Reportar Bug](https://github.com/djponsex/spotify-time-converter/issues) | [Solicitar Feature](https://github.com/djponsex/spotify-time-converter/issues)

</div>

## 📋 Tabla de Contenidos

- [Acerca del Proyecto](#-acerca-del-proyecto)
- [Características](#-características)
- [Instalación](#-instalación)
- [Uso](#-uso)
- [Formatos](#-formatos)
- [Atajos de Teclado](#-atajos-de-teclado)
- [API](#-api)
- [Contribuir](#-contribuir)
- [Licencia](#-licencia)

## 🎯 Acerca del Proyecto

Spotify Time Converter PRO es una herramienta web diseñada para convertir listas de tiempos y cortes de canciones al formato JSON, ideal para su uso con Shortcuts de iOS, automatizaciones y desarrollo de aplicaciones musicales.

### ¿Por qué usar Spotify Time Converter?

- **🚀 Rápido**: Conversión instantánea sin necesidad de instalación
- **🎨 Intuitivo**: Interfaz inspirada en Spotify con diseño moderno
- **📱 Responsive**: Funciona perfectamente en móvil y desktop
- **🔒 Privado**: Todo el procesamiento se realiza en tu navegador
- **🌐 Sin conexión**: Una vez cargado, funciona offline

## ✨ Características

### 🎯 Funciones Principales

#### 1. **Conversión Dual**
- **JSON Visual**: Incluye emojis y tiempos legibles
  ```json
  {
    "🏁 INICIO ARICA (2:10)": 130000,
    "💃 FIGURA INICIAL (2:25)": 145000
  }
  ```
- **JSON Raw**: Solo datos puros para automatizaciones
  ```json
  {
    "INICIO ARICA": 130000,
    "FIGURA INICIAL": 145000
  }
  ```

#### 2. **📋 Gestión de Datos**
- **Cargar Ejemplo**: Dataset de prueba con 20+ cortes
- **Pegar desde Portapapeles**: Acceso directo al clipboard
- **Importar Archivos**: Soporte para `.txt` y `.json`
- **Limpiar Todo**: Resetea la aplicación instantáneamente

#### 3. **💾 Exportación**
- **Copiar JSON**: Al portapapeles con un click
- **Descargar Archivo**: Guarda en formato `.json`
- **Compartir por URL**: Genera enlaces únicos con los datos codificados

#### 4. **📊 Estadísticas en Tiempo Real**
- Total de cortes procesados
- Duración total de la lista
- Tiempo promedio entre cortes

#### 5. **📜 Historial Persistente**
- Guarda las últimas 10 conversiones
- Acceso rápido a conversiones anteriores
- Persistencia entre sesiones (localStorage)

#### 6. **🔄 Herramientas de Organización**
- **Ordenar por Tiempo**: Reorganiza cronológicamente
- **Validación Automática**: Detecta errores de formato
- **Contador de Caracteres**: Monitoreo en tiempo real

### 🎨 Experiencia de Usuario

- **Diseño Spotify**: Fondo degradado verde característico
- **Modo Oscuro**: Por defecto para reducir fatiga visual
- **Animaciones Suaves**: Transiciones fluidas
- **Notificaciones Visuales**: Feedback instantáneo
- **Responsive Design**: Adaptado para todos los dispositivos

## 🚀 Instalación

### Opción 1: Usar en línea
Simplemente visita: [https://djponsex.github.io/spotify-time-converter/pro.html](https://djponsex.github.io/spotify-time-converter/pro.html)

### Opción 2: Clonar localmente
```bash
# Clonar el repositorio
git clone https://github.com/djponsex/spotify-time-converter.git

# Navegar al directorio
cd spotify-time-converter

# Abrir en el navegador
open pro.html
# O usar un servidor local
python -m http.server 8000
```

## 📖 Uso

### Formato de Entrada

Los cortes deben seguir el formato: `TIEMPO - DESCRIPCIÓN`

```
2:10 - INICIO ARICA
2:25 - FIGURA INICIAL
3:50 - PARTE ROMÁNTICA
4:00 - FINAL PARTE ROMÁNTICA
```

### Pasos Básicos

1. **Pegar o escribir** tus cortes en el área de texto
2. **Click en "Convertir a JSON"**
3. **Seleccionar** entre vista Visual o Raw
4. **Copiar o descargar** el resultado

### Emojis Automáticos

El sistema asigna emojis según palabras clave:

| Palabra Clave | Emoji | Ejemplo |
|--------------|-------|---------|
| INICIO | 🏁 | INICIO ARICA |
| FIGURA | 💃 | FIGURA INICIAL |
| PARTE | 📍 | PRIMERA PARTE |
| FINAL | 💕 | FINAL ROMÁNTICO |
| CANCIÓN | 🎵 | CANCIÓN GILDA |
| CORTE | ✂️ | CORTE RÁPIDO |
| SALIDA | 🚪 | SALIDA ARICA |

## ⌨️ Atajos de Teclado

| Atajo | Acción |
|-------|--------|
| `Ctrl + Enter` | Convertir a JSON |
| `Ctrl + H` | Abrir/Cerrar Historial |
| `Ctrl + C` | Copiar JSON (cuando hay resultados) |

## 🔗 API y Parámetros URL

### Compartir con Datos Precargados

```
https://djponsex.github.io/spotify-time-converter/pro.html?data=BASE64_ENCODED_JSON
```

### Ejemplo de Integración

```javascript
// Codificar datos para compartir
const data = {
  "INICIO": 130000,
  "FIGURA": 145000
};

const encoded = btoa(encodeURIComponent(JSON.stringify(data)));
const shareUrl = `https://djponsex.github.io/spotify-time-converter/pro.html?data=${encoded}`;
```

## 🛠️ Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Animaciones y diseño responsive
- **JavaScript Vanilla**: Sin dependencias externas
- **LocalStorage API**: Persistencia de datos
- **Clipboard API**: Copiar/pegar
- **URL API**: Compartir datos

## 🤝 Contribuir

Las contribuciones son bienvenidas y apreciadas. Para contribuir:

1. Fork el proyecto
2. Crea tu Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push al Branch (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

### Ideas para Contribuir

- [ ] Soporte para más formatos de exportación (CSV, XML)
- [ ] Integración con Spotify Web API
- [ ] Modo oscuro/claro toggle
- [ ] Drag & drop para archivos
- [ ] Editor visual de cortes
- [ ] Exportar a formato de subtítulos
- [ ] Timeline visual interactivo
- [ ] PWA para instalación

## 📝 Licencia

Distribuido bajo la Licencia MIT. Ver `LICENSE` para más información.

## 👤 Autor

**DJ Ponsex**

- GitHub: [@djponsex](https://github.com/djponsex)
- Website: [djponsex.github.io](https://djponsex.github.io)

## 🙏 Agradecimientos

- Diseño inspirado en [Spotify](https://spotify.com)
- Iconos y emojis de [Unicode](https://unicode.org)
- Comunidad de [Shortcuts iOS](https://www.reddit.com/r/shortcuts/)

---

<div align="center">
  Hecho con ❤️ para la comunidad de DJs y productores musicales
</div>
