# ✨ Configuración de Biome en VS Code

Biome es una herramienta moderna para formateo, linting y análisis de código. A continuación te muestro cómo configurarla correctamente en Visual Studio Code para un flujo de trabajo optimizado.

---

## 🛠️ Pasos de instalación

### 1. 📦 Descargar el binario

Descargá el ejecutable de Biome desde su repositorio oficial:

🔗 [Descargar desde GitHub](https://github.com/biomejs/biome/releases)

> Asegurate de descargar la versión correspondiente a tu sistema operativo (por ejemplo, `biome-win32-x64.exe` para Windows).

---

### 2. ⚙️ Agregar a las variables de entorno

1. Mové el ejecutable a una carpeta permanente, por ejemplo: `C:\Herramientas\biome\`.
2. Renombralo como `biome.exe` si es necesario.
3. Agregá esa ruta al **PATH** del sistema:
   - Abrí `Sistema > Configuración avanzada > Variables de entorno`.
   - En `Path`, agregá: `C:\Herramientas\biome\`

> Esto permitirá que VS Code y la terminal reconozcan el comando `biome`.

---

### 3. 📁 biome.json en tu proyecto

Asegurate de tener un archivo `biome.json` en la raíz del proyecto. Podés copiarlo o reemplazarlo con uno actualizado según tu configuración preferida.
o inicializa biome: ``` npx @biomejs/biome init ```

---

## ⚙️ Configuración en VS Code

Abrí el archivo `settings.json` (desde `Ctrl+Shift+P` > `Preferences: Open Settings (JSON)`) y agregá lo siguiente:

```json
{
  "[javascriptreact]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "[json]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "[jsonc]": {
    "editor.defaultFormatter": "biomejs.biome"
  },
  "editor.codeActionsOnSave": {
    "source.organizeImports.biome": "always",
    "source.fixAll.biome": "explicit",
    "source.action.useSortedAttributes.biome": "explicit"
  }
}

