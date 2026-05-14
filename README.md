<div align="center">

# 🏆 Overlay de Logros — Beta

### Overlay de escritorio para PC integrado con RetroAchievements

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat-square&logo=python)
![Platform](https://img.shields.io/badge/Plataforma-Windows-0078D4?style=flat-square&logo=windows)
![License](https://img.shields.io/badge/Licencia-MIT-green?style=flat-square)
![Status](https://img.shields.io/badge/Estado-Beta-orange?style=flat-square)
![RetroAchievements](https://img.shields.io/badge/API-RetroAchievements-cc2200?style=flat-square)

Muestra tus logros de [RetroAchievements.org](https://retroachievements.org) directamente en pantalla mientras juegas,  
con cronómetro, contador de progreso y traducción automática al español.

</div>

---

## 📸 Capturas de pantalla

### Overlay principal
Muestra hasta 4 logros activos con temporizador, contador o modo solo-visualización.

![Overlay principal](assets/screenshot_overlay.png)

### Panel de selección de logros
Busca y selecciona logros con sus íconos y descripciones, resaltando los activos con ✔.

![Selección de logros](assets/screenshot_seleccion.png)

### Menú de configuración
Acceso rápido a cuenta, juegos, idioma, apariencia y teclas rápidas.

![Menú](assets/screenshot_menu.png)

---

## ✨ Características

| Función | Descripción |
|---|---|
| 🔗 **Integración con RA** | Conecta tu cuenta de RetroAchievements con usuario + API Key |
| 🔍 **Búsqueda por consola** | Filtra juegos por consola y nombre desde el overlay |
| 🏆 **Hasta 4 logros activos** | Muestra simultáneamente hasta 4 logros con sus íconos de badge |
| ⏱️ **Temporizador** | Cronómetro por logro con play, pausa y reset |
| 🔢 **Contador** | Contador con meta configurable (ej: 342 / 1,000 kills) |
| ⊘ **Solo mostrar** | Muestra el logro sin ningún tracker, como referencia visual |
| 🌐 **Español / English** | Traduce títulos y descripciones al español automáticamente |
| 🎨 **Temas y colores** | 5 temas incluidos + personalización total de colores y opacidad |
| 💾 **Presets de apariencia** | Guarda y carga tus combinaciones de colores favoritas |
| ⌨️ **Teclas globales** | Hotkeys configurables que funcionan en cualquier aplicación |
| 🖼️ **Imagen de juego y avatar** | Muestra el ícono del juego y tu foto de perfil de RA |
| 📦 **Sin instalación** | Distribuible como `.exe` autónomo generado con PyInstaller |
| 💾 **Auto-guardado** | Toda la configuración se guarda automáticamente |

---

## 🚀 Inicio rápido

**Requisitos:**
```
Python 3.8 o superior
```
> **Nota:** Para que las teclas globales funcionen correctamente,  
> ejecuta el overlay como **Administrador**.

---

## ⚙️ Configuración inicial

### 1. Cuenta de RetroAchievements
1. Abre el menú con `F3` → **👤 Cuenta**
2. Ingresa tu **nombre de usuario** de RetroAchievements
3. Ingresa tu **API Key** (la encuentras en [retroachievements.org/settings](https://retroachievements.org/settings))

### 2. Seleccionar un juego
1. Menú → **🔍 Buscar juego en RetroAchievements**
2. Elige la consola en el desplegable
3. Escribe el nombre del juego y haz clic en **Buscar**
4. Selecciona el juego de la lista

### 3. Agregar logros
1. Menú → **🏆 Seleccionar / editar logros**
2. Haz clic en los logros que quieras rastrear (máximo 4)
3. Haz clic en **Siguiente →**
4. Elige el tipo de seguimiento por cada logro:
   - **⊘ Solo mostrar** — visible sin tracker
   - **⏱ Temporizador** — cronómetro
   - **🔢 Contador** — con meta numérica opcional
5. Haz clic en **Guardar y aplicar**

---

## ⌨️ Teclas rápidas

| Tecla | Función |
|---|---|
| `F1` | Iniciar / Pausar todos los temporizadores |
| `F2` | Reiniciar todo |
| `F3` | Abrir / cerrar menú de configuración |
| `Esc` | Cerrar el overlay |

> Todas las teclas son configurables desde el menú → **⌨ Configurar teclas rápidas**

---

## 🌐 Sistema de idioma

El overlay incluye traducción automática al español de los títulos y descripciones de logros  
usando Google Translate (sin API key, solo requiere conexión a internet).

- **Español** — al guardar un logro, su nombre y descripción se traducen automáticamente
- **English** — los datos se muestran tal como aparecen en RetroAchievements

Para cambiar el idioma: Menú → **🌐 Idioma**

---

## 🎨 Personalización

### Colores y opacidad
Menú → **🎨 Colores y opacidad**  
Personaliza fondo, borde, texto, texto secundario, acento y transparencia de la ventana.

### Temas incluidos
| Tema | Estilo |
|---|---|
| 🟫 Oscuro madera | Por defecto (marrón oscuro + dorado) |
| ⬛ Noche | Negro puro + blanco |
| 🟦 Azul acero | Azul oscuro + cian |
| 🟩 Bosque | Verde oscuro + lima |
| 🟥 Rojo rubí | Rojo oscuro + coral |

### Presets
Guarda tu combinación actual con **💾 Guardar apariencia** y recupérala después con **📂 Cargar apariencia guardada**.

---

## 🛠️ Stack técnico

- **Python 3.8+** + **tkinter** — interfaz gráfica nativa
- **requests** — llamadas a la API de RetroAchievements
- **Pillow (PIL)** — carga de íconos de badge y avatar
- **keyboard** — hotkeys globales
- **PyInstaller** — compilación a `.exe`
- **Google Translate (libre)** — traducción automática sin API key

---

## 📁 Estructura del proyecto

```
overlay_de_logros/

├── LEEME.txt             # Instrucciones en español
├── overlay_config.json   # Configuración guardada (auto-generado)
├── overlay_presets.json  # Presets de apariencia (auto-generado)
└── badge_cache/          # Caché de imágenes de badges (auto-generado)
```

---

## 🔑 API de RetroAchievements

Este proyecto usa la [API pública de RetroAchievements](https://api.docs.retroachievements.org/).  
Tu API Key se guarda **solo en tu equipo** en `overlay_config.json` y nunca se envía a ningún servidor externo.

Endpoints utilizados:
- `API_GetGameList.php` — lista de juegos por consola
- `API_GetGameExtended.php` — logros de un juego
- `API_GetUserSummary.php` — perfil del usuario

---

## 🐛 Problemas conocidos (Beta)

- Las teclas globales requieren ejecutar como Administrador en Windows
- La traducción automática requiere conexión a internet activa
- Algunas fuentes del sistema pueden no mostrar todos los emojis correctamente
- En monitores de escala >100% puede verse ligeramente desenfocado (limitación de tkinter)

---

## 📋 Changelog

### v3.4 — Beta actual
- ✅ Imágenes de badges visibles en el panel de selección de logros
- ✅ Sistema de idioma Español / English con traducción automática
- ✅ Botón ✕ por logro para quitarlo individualmente
- ✅ Menú "Quitar todos los logros"
- ✅ Modo "⊘ Solo mostrar" para logros sin tracker
- ✅ Corrección de descarga de imágenes (User-Agent correcto)
- ✅ Avatar de perfil en el panel de cuenta

---

## 📄 Licencia

Distribuido bajo licencia MIT. Consulta `LICENSE` para más información.

---

<div align="center">

Hecho con ❤️ para la comunidad de RetroAchievements  
[retroachievements.org](https://retroachievements.org)

</div>
