# GitHub - Como criar branch e fazer alterações

Este arquivo explica de forma simples como colaborar no projeto usando Git e GitHub.

## 1. Como criar uma branch

Uma branch é uma cópia do projeto para que você possa fazer alterações sem mexer na branch principal.

### Comando para criar e entrar na branch

```bash
git checkout -b feature/minha-alteracao
```

Ou, em versões mais novas do Git:

```bash
git switch -c feature/minha-alteracao
```

Exemplo:

```bash
git switch -c feature/atualizar-documentacao
```

---

## 2. Como fazer uma alteração

Depois de criar a branch, você pode editar arquivos, textos, documentação ou qualquer parte do projeto.

### Verificar status

```bash
git status
```

### Adicionar as alterações

```bash
git add .
```

### Fazer o commit

```bash
git commit -m "Atualiza documentação do projeto"
```

---

## 3. Como enviar para o GitHub

Se a branch ainda não existe no GitHub:

```bash
git push -u origin feature/minha-alteracao
```

Se a branch já existe no GitHub:

```bash
git push
```

---

## 4. Se outra pessoa quiser alterar algo

A pessoa precisa ter acesso ao repositório no GitHub. Se não tiver permissão, ela não consegue criar branch nem fazer push.

Para isso, o dono do repositório precisa:

- abrir o GitHub;
- entrar no repositório;
- ir em Settings;
- entrar em Collaborators;
- adicionar a pessoa;
- definir a permissão como Write ou maior.

Sem esse acesso, a pessoa não consegue colaborar diretamente.

---

## 5. Fluxo recomendado para qualquer alteração

```bash
git switch -c feature/nova-tarefa
# editar arquivos
git status
git add .
git commit -m "Descreve a alteração"
git push -u origin feature/nova-tarefa
```

Depois disso, no GitHub, é possível abrir um Pull Request para revisar e aprovar a alteração.

---

## 6. Se quiser atualizar sua branch com a main

Antes de finalizar, pode ser útil atualizar a branch com a versão principal:

```bash
git checkout main
git pull origin main
git checkout feature/minha-alteracao
git merge main
```

---

## 7. Resumo prático

- cria branch: `git switch -c feature/nome`
- edita arquivos
- salva alterações: `git add .`
- cria commit: `git commit -m "mensagem"`
- envia para o GitHub: `git push -u origin feature/nome`
- abre Pull Request no GitHub

> Em resumo: qualquer pessoa com acesso ao repositório pode criar branch e alterar o projeto. O que define isso não é o ERP, e sim a permissão no GitHub.
