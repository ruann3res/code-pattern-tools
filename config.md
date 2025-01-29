# Tools

## Editorconfig

- [Editorconfig](https://editorconfig.org/)
- Serve para manter a consistência de estilo de código entre diferentes editores e IDEs.

## Eslint

- [Eslint](https://eslint.org/)
- Define regras de estilo de código e ajuda a identificar e corrigir problemas no código.
- libs:
- - @typescript-eslint/eslint-plugin,
- - @typescript-eslint/parser,
- - eslint,
- - eslint-config-airbnb,
- - eslint-import-resolver-typescript,
- - eslint-plugin-import,
- - eslint-plugin-jsx-a11y,
- - eslint-plugin-react,
- - eslint-plugin-react-hooks
- Todas as configurações estão no arquivo .eslintrc.js

#### Config vscode settings.json

```json
{
// Rest of the settings.json file

// ESLint Settings
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": "always",
    "source.fixAll": "always",
    "source.addMissingImports":"always",
    "source.sortMembers": "always",
    "source.organizeImports": "always"
  },
}

```

## Prettier

- Diferente do eslint que serve para reforcar o code style, o prettier serve para formatar o código e deixa-lo mais `bonito`.
- libs:
- - prettier
- - eslint-config-prettier
- - eslint-plugin-prettier

## Husky e Lint-staged

- [Husky](https://typicode.github.io/husky/)
- [Lint-staged](https://github.com/lint-staged/lint-staged)
- Husky serve para rodar scripts no git hooks, como por exemplo, rodar os testes antes de commitar.
- Lint-staged serve para rodar scripts apenas nos arquivos que estão staged no git.