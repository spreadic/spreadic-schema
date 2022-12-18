# Spreadic Data Definition Validation

Welcome to Spreadic!

This repository contains the schema of the data definition used in Spreadic. This allows common IDEs like VSCode to be capable to not only validate the correctness of Spreadic data definition before pushing to their own repository, but also auto-suggest along the editing journey as the practitioners interact with the definition files.

# Pre-Requisite
It's assumed that VSCode has been installed as the IDE.

You also need to get [VS Code Extension for YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml) installed.

# Setup

When you start a project in VSCode, you can simply create a file `.vscode/settings.json` with the below content:

```json
{    
  "yaml.schemas": {
    "https://raw.githubusercontent.com/spreadic/spreadic-schema/main/schemas/data_definition.json": [
      "models/**/*.yml",
      "models/**/*.yaml"
    ]
  },
}
```

After that, the YAML files (with `yml` or `yaml` file extension) in the given project will be automatically validated.

If you want to recommend other team members in the same project to enable the above, you can also checkin the file `.vscode/settings.json`. In addition, you may also create `.vscode/extensions.json` with the following to recommend others to install [VS Code Extension for YAML](https://marketplace.visualstudio.com/items?itemName=redhat.vscode-yaml).

```json
{
  "recommendations": [
    "redhat.vscode-yaml"
  ]
}
```

The content of the two files can also be found in `.vscode` folder in this repository.
