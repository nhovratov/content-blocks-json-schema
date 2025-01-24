# JSON Schema for TYPO3 CMS Content Blocks

This repository contains [JSON schemas](https://json-schema.org/) for Content Elements, Page Types and Record Types
from the [Content Blocks extension](https://github.com/nhovratov/content-blocks). Using them in your IDE allows for
auto-completion and validation of your EditorInterface.yaml files.

## Setup

### PhpStorm

1. Open PhpStorm and switch to *File > Preferences > Languages & Frameworks > Schemas and DTDs > JSON Schema Mappings*
2. Add new entry for Content Elements
    - **Schema file or URL**: `https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/content-element.schema.json`
    - **File path Pattern for version 0.8.2 or lower**: `**/ContentBlocks/ContentElements/*/EditorInterface.yaml`
    - **File path Pattern for version 1.0.0 or higher**: `**/ContentBlocks/ContentElements/*/config.yaml`
3. Add new entry for Page Types
   - **Schema file or URL**: `https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/page-type.schema.json`
   - **File path Pattern for version 0.8.2 or lower**: `**/ContentBlocks/PageTypes/*/EditorInterface.yaml`
   - **File path Pattern for version 1.0.0 or higher**: `**/ContentBlocks/PageTypes/*/config.yaml`
4. Add new entry for Record Types
   - **Schema file or URL**: `https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/record-type.schema.json`
   - **File path Pattern for version 0.8.2 or lower**: `**/ContentBlocks/RecordTypes/*/EditorInterface.yaml`
   - **File path Pattern for version 1.0.0 or higher**: `**/ContentBlocks/RecordTypes/*/config.yaml`

### Visual Studio Code

1. Install the plugin "redhat.vscode-yaml"
2. Open the settings and search for "*yaml schemas*" and open the `settings.json`.
3. Add the following config

```
"yaml.schemas": {
    "https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/content-element.schema.json" : ["**/ContentBlocks/ContentElements/*/EditorInterface.yaml"],
    "https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/page-type.schema.json" : ["**/ContentBlocks/PageTypes/*/EditorInterface.yaml"],
    "https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/record-type.schema.json" : ["**/ContentBlocks/RecordTypes/*/EditorInterface.yaml"]
}
```

A basic configuration.json looks like this
```json
{
    "explorer.confirmDelete": false,
    "window.zoomLevel": 1,
    "security.workspace.trust.untrustedFiles": "open",
    "yaml.schemas": {
       "https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/content-element.schema.json" : ["**/ContentBlocks/ContentElements/*/EditorInterface.yaml"],
       "https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/page-type.schema.json" : ["**/ContentBlocks/PageTypes/*/EditorInterface.yaml"],
       "https://raw.githubusercontent.com/nhovratov/content-blocks-json-schema/main/record-type.schema.json" : ["**/ContentBlocks/RecordTypes/*/EditorInterface.yaml"]
    }
}
```
