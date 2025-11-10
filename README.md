# front-end

Projeto desenvolvido em Next.js.

## 🚀 Como rodar o projeto

Instale as dependências:
bash
npm install

## Redação de Commits (Conventional Commits)

Este projeto utiliza **Conventional Commits** com validação automática via **Husky** e **CommitLint**.

### Formato dos Commits

Os commits devem seguir o padrão:

```
<tipo>[escopo opcional]: <descrição>

[corpo opcional]

[rodapé opcional]
```

### Tipos Permitidos

- `feat` → nova funcionalidade
- `fix` → correção de bug
- `docs` → documentação
- `style` → formatação (não afeta código)
- `refactor` → refatoração de código
- `test` → adição/correção de testes
- `chore` → tarefas de build, configurações, etc.
- `perf` → melhorias de performance
- `ci` → mudanças em CI/CD
- `build` → mudanças no sistema de build

### Exemplos de Commits Válidos

```bash
feat: adiciona endpoint para buscar usuários
fix: corrige validação de email no login
docs: atualiza README com instruções de deploy
test: adiciona testes para middleware de autenticação
refactor: simplifica lógica de validação de dados
chore: atualiza dependências do projeto
```

### Com Escopo (Opcional)

```bash
feat(auth): implementa login com JWT
fix(api): corrige erro 500 no endpoint /users
docs(readme): adiciona seção sobre commits
```

### Validação Automática

- **Pre-commit Hook** → roda `npm test` antes de cada commit
- **Commit-msg Hook** → valida formato do commit com CommitLint
- Commits que não seguem o padrão são **rejeitados automaticamente**
- Se os **testes falharem**, o commit também será **rejeitado**

### Comandos Úteis

Se o commit for rejeitado, corrija a mensagem:

```bash
git commit --amend -m "feat: nova mensagem no formato correto"
```
