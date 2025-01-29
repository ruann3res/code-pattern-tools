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
## Conventional Commits && Commitlint

### Dicas sobre convention commits

- `build`: Alterações nas configurações de build (vite, webpack, npm, etc).
- `chore`: Alteraçoes que nao modificam codigo nem testes (arquivos de configuracao, ferramentas, bibliotecas ,etc).
- `ci`: Alterações em arquivos de configuração do CI (ex: Github Actions, Travis, Gitlab CI, etc).
- `docs`: Alterações na documentação.
- `feat`: Adição de uma nova funcionalidade.
- `fix`: Correção de bugs.
- `perf`: Alterações de código que melhoram a performance.
- `refactor`: Alterações de código que não corrigem bugs nem adicionam funcionalidades.
- `revert`: Alteraçoes que desfazem alguma coisa (git revert, por exemplo).
- `style`: Alterações que não afetam o significado do código (espaços em branco, formatação, ponto e vírgula, etc).
- `test`: Adição ou modificação de testes.

### Commitlint

- Define regras de como os commits devem ser feitos.
- libs:
- @commitlint/{cli,config-conventional}