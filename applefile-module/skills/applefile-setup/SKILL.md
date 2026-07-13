---
name: applefile-setup
description: Sets up Applefile Module in a BMad project.
---

# Applefile Setup

## Overview

Installs and configures the Applefile Module. Module identity and configuration questions come from `./assets/module.yaml`; help/menu entries come from `./assets/module-help.csv`.

## On Activation

1. Read `./assets/module.yaml`.
2. Ask for each prompted variable, using defaults when the user accepts them.
3. Write answers to a temporary JSON file.
4. Run:

```bash
python3 ./scripts/merge-config.py --config-path "{project-root}/_bmad/config.yaml" --user-config-path "{project-root}/_bmad/config.user.yaml" --module-yaml ./assets/module.yaml --answers {temp-file}
python3 ./scripts/merge-help-csv.py --target "{project-root}/_bmad/module-help.csv" --source ./assets/module-help.csv --legacy-dir "{project-root}/_bmad" --module-code af
```

5. Show the module greeting from `./assets/module.yaml`.
