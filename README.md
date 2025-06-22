
## Configuración para Biome en VS Code

Para que Visual Studio Code utilice **Biome** como formateador y aplicador de acciones automáticas al guardar archivos, agregá lo siguiente en tu archivo `settings.json` de VS Code:

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
