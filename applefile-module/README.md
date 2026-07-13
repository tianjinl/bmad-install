# Applefile Module

Minimal installable BMad custom module example.

Install from a GitHub repository:

```bash
npx bmad-method install --custom-source https://github.com/xxx/applefile-module
```

Install from this local checkout while developing:

```bash
npx bmad-method install --custom-source ./applefile-module
```

The installer discovers `.claude-plugin/marketplace.json`, installs the listed skill directories, and uses the setup skill's `assets/module.yaml` plus `assets/module-help.csv` as the module registration source.
