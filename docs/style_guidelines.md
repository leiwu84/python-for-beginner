[PEP8](https://peps.python.org/pep-0008/) is the industrial fundamental. You can also check [Style Guides for Google](https://google.github.io/styleguide/pyguide.html), which gives more specifications than PEP8.

## VSCode Setup
Additionally, here is my settings in VSCode. If you have installed these plugins on VS Code, you can directly copy-paste my settings to yours if you like.

- [Python](https://marketplace.visualstudio.com/items?itemName=ms-python.python)
    
    !!! note 
        Pylance (Python language support) is installed automatically)

- [iSort](https://marketplace.visualstudio.com/items?itemName=ms-python.isort)

- [Black Formatter](https://marketplace.visualstudio.com/items?itemName=ms-python.black-formatter)

- [autoDocstring](https://marketplace.visualstudio.com/items?itemName=njpwerner.autodocstring)

Copy-paste the following block to your VSCode `settings.json`.
```json
"[python]": {
    "editor.codeActionsOnSave": {
        "source.organizeImports": "explicit"
    },
    "editor.defaultFormatter": "ms-python.black-formatter",
    "editor.formatOnType": true,
},
"python.analysis.typeCheckingMode": "basic",
"python.analysis.completeFunctionParens": true,
"python.analysis.addImport.exactMatchOnly": true,
"python.analysis.diagnosticSeverityOverrides": {
    "reportOptionalMemberAccess": "none",
    "reportOptionalSubscript": "none",
    "reportOptionalOperand": "none",
    "reportOptionalCall": "none",
    "reportUnusedVariable": "warning",
    "reportUnusedClass": "warning",
    "reportUnusedExpression": "warning",
    "reportUnusedFunction": "warning",
    "reportUnusedImport": "warning",
},
"python.testing.pytestEnabled": true,
"python.testing.pytestArgs": [
    "tests"
],
"python.analysis.autoFormatStrings": true,
```