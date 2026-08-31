# Fluxo de trabalho no GitHub

Este guia explica de forma prática como criar branches, realizar alterações e enviar mudanças para o repositório.

## 1. Criar uma branch

Use uma branch separada para cada tarefa ou alteração.

```bash
git switch -c feature/minha-alteracao
```

Ou, se preferir:

```bash
git checkout -b feature/minha-alteracao
```

Exemplo:

```bash
git switch -c feature/atualizar-documentacao
```

---

## 2. Fazer alterações no projeto

Depois de criar a branch, edite os arquivos necessários.

Verifique o estado:

```bash
git status
```

Adicione as alterações:

```bash
git add .
```

Crie o commit:

```bash
git commit -m "Atualiza documentação do projeto"
```

---

## 3. Enviar para o GitHub

Se a branch ainda não existir no remoto:

```bash
git push -u origin feature/minha-alteracao
```

Se a branch já estiver no GitHub:

```bash
git push
```

---

## 4. Atualizar a branch principal

Para integrar as mudanças com a versão principal, use:

```bash
git checkout main
git pull origin main
git checkout feature/minha-alteracao
git merge main
```

---

## 5. Abrir Pull Request

Depois que a branch estiver no GitHub, abra um Pull Request para revisão antes do merge.

Isso ajuda a:

- revisar alterações antes de publicar;
- manter o histórico organizado;
- evitar conflitos de trabalho em equipe;
- manter a branch principal mais estável.

---

## 6. Permissões no GitHub

Qualquer pessoa pode criar uma branch e alterar o projeto se tiver acesso ao repositório.

Se a pessoa não tiver permissão, ela não conseguirá:

- criar branch;
- fazer push;
- abrir Pull Request.

Para conceder acesso:

1. entrar no repositório;
2. abrir Settings;
3. acessar Collaborators;
4. adicionar a pessoa;
5. definir permissão como Write ou superior.

---

## 7. Resumo prático

```bash
git switch -c feature/nova-tarefa
# editar arquivos
git status
git add .
git commit -m "Descreve a alteração"
git push -u origin feature/nova-tarefa
```

> Conclusão: não é o ERP que define isso, e sim a permissão no GitHub. Com acesso, a pessoa pode criar branch, alterar arquivos e enviar as mudanças normalmente.
