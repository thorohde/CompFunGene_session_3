# CompFunGene Session 3

## 1. Conecting Positron to Github Copilot:

This might be the hardest task we want to solve today. 

1.1 Open the Command Palette with `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS).
1.2 Enter `Posit Assistant: Configure AI Providers`.
1.3. Open `Providers.json` and add:
```
"copilot": {
  "enabled": true
}:
```
Your `Providers.json` file should look something like this:  

```{json}
{
  "$schema": "https://assistant.posit.co/schemas/providers.schema.json",
  "version": 1,
  "providers": {
    "openai": {
      "baseUrl": "https://api.openai.com/v1"
    }, 
    "copilot": {
      "enabled": true
    }
  }
}
```

1.4 Disable automatic MCP startup: 
1.5 Open Positron's Command Palette (`Ctrl+Shift+P`) and select `Preferences: Open User Settings (JSON)`, click on `open Settings (JSON)`.
Add this setting to your `settings.json`:

```
{
  "chat.mcp.autostart": "never"
}
```

Your `Settings.json` file should look something like this:  

```
{
    "[r]": {
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "Posit.air-vscode"
    },

    "files.associations": {
        "renv.lock": "json"
    },
    "workbench.colorTheme": "Default Positron Dark",
    "window.autoDetectColorScheme": true,
    "workbench.keybindings.rstudioKeybindings": true,
    "authentication.openai-api.baseUrl": "https://api.openai.com/v1",
    "editor.wordBasedSuggestions": "off", 
    "editor.suggest.matchOnWordStartOnly": true,
    "editor.suggest.showModules": false,
    "editor.suggest.showSnippets": false,
    "python.languageServer": "None",
    "telemetry.telemetryLevel": "all",
    "git.openRepositoryInParentFolders": "never",
    "packages.warnMissingInEditor": false,
    "ai.mcp.enabled": true,
    "packages.confirmMissingOnRun": false,
    "chat.disableAIFeatures": false, 
    "chat.mcp.autostart": "never"
}
```
