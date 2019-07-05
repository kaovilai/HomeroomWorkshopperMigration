# ReplaceRules Overview

## Pre-requisites
### Install VSCode
Download and install [Visual Studio Code](https://code.visualstudio.com/)
### Install [ReplaceRules](https://github.com/bhughes339/vscode-replacerules) Extension
Go [here](https://marketplace.visualstudio.com/items?itemName=bhughes339.replacerules) to install ReplaceRules

This repository provide the following files
- replacerules.rules.HomeroomWorkshopperMigration.json
  - set of rules and rulesets

In Visual Studio Code, 
1. Open its settings.json file. There may already be other user settings there
2. Paste content of the files above next to each other like so. Don't forget to add `,` between items.
```
    "replacerules.rules": {
        "HWM - Switch Title and add Homeroom Header Template": {
            "find": "^= (.+)",
            "replace": "---\nTitle: $1\nPrevPage: \nNextPage: \n---"
        },
        ...
    },
    "replacerules.rulesets": {
        "HomeroomWorkshopperMigration" : {
            "rules": [
                "HWM - Switch Title and add Homeroom Header Template",
                ...
            ]
        }
    },
```

For specific usage instructions regarding this extension please refer to official [README.md](https://github.com/bhughes339/vscode-replacerules/blob/master/README.md)
