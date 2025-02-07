# Developer Preview (Monaco)

Developer preview is based on [Microsofts Monaco Editor](https://microsoft.github.io/monaco-editor/) which is maintained by the Visual Studio Code team.

## Update monaco editor

1. Download Monaco editor with npm: `npm i monaco-editor`.
2. Delete everything except the `min` folder (the minimised code).
3. Copy the `min` folder inside the [`monacoSRC`](/src/modules/previewpane/MonacoPreviewHandler/monacoSRC) folder.
4. Generate the JSON file (see section below)

## languages.json

[`languages.json`](/src/modules/previewpane/MonacoPreviewHandler/languages.json) contains all extensions and Id's for the supported languages of Monaco. The [`FileHandler`](/src/modules/previewpane/MonacoPreviewHandler/FileHandler.cs) class and the installer are using this file.

### Generate languages.json file

After you updated monaco editor or adding a new language you should update the [`languages.json`](/src/modules/previewpane/MonacoPreviewHandler/languages.json) file.

1. Build monaco in debug mode.
2. Open [generateLanguagesJson.html](/src/modules/previewpane/MonacoPreviewHandler/generateLanguagesJson.html) in a browser.
3. Replace the old JSON file.
