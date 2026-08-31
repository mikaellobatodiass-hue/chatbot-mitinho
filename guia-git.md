# Guia Git

## 🧩 Visão geral

Este guia mostra de forma simples como criar branch, alterar arquivos e enviar mudanças para o repositório.

Ele é útil para qualquer pessoa que queira colaborar no projeto sem bagunçar a branch principal.

---

## 1. Criar uma branch

Use uma branch separada para cada tarefa ou alteração.

### Comando

```bash
git switch -c feature/minha-alteracao
```

Também funciona assim:

```bash
git checkout -b feature/minha-alteracao
```

### Exemplo

```bash
git switch -c feature/atualizar-documentacao
```

---

## 2. Fazer alterações

Depois de criar a branch, edite os arquivos necessários.

### Verificar o estado do projeto

```bash
git status
```

### Adicionar as mudanças

```bash
git add .
```

### Fazer o commit

```bash
git commit -m "Atualiza documentação do projeto"
```

---

## 3. Enviar para o GitHub

Se a branch ainda não existir no repositório remoto:

```bash
git push -u origin feature/minha-alteracao
```

Se a branch já estiver no GitHub:

```bash
git push
```

---

## 4. Atualizar a branch principal

Se quiser integrar as mudanças com a branch principal, faça assim:

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

- revisar as alterações;
- manter o projeto organizado;
- evitar conflitos;
- reduzir erros antes de publicar.

---

## 6. Permissões do GitHub

Para criar branch e enviar mudanças, a pessoa precisa ter acesso ao repositório.

Se não tiver permissão, ela não consegue:

- criar branch;
- fazer push;
- abrir Pull Request.

### Como liberar acesso

1. abrir o repositório no GitHub;
2. ir em Settings;
3. entrar em Collaborators;
4. adicionar a pessoa;
5. definir a permissão como Write ou superior.

---

## 7. Fluxo rápido

```bash
git switch -c feature/nova-tarefa
# editar arquivos
git status
git add .
git commit -m "Descreve a alteração"
git push -u origin feature/nova-tarefa
```

---

## ✅ Conclusão

O mais importante é entender que a pessoa precisa ter acesso ao GitHub para colaborar. Sem permissão, ela não consegue enviar alterações. Com acesso, o processo é simples e organizado.

> Em resumo: branch + alteração + commit + push + Pull Request.
