# Comandos Básicos de Git/GitHub para Projetos em Grupo

Este guia ensina o essencial para colaborar em grupo usando Git e GitHub.  
Ideal para iniciantes que nunca usaram controle de versão.

---

## 1. Configuração Inicial (executar apenas uma vez)

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
````

> **Dica:** Use o mesmo e-mail da sua conta GitHub.

Verifique a configuração:

```bash
git config --list
```

---

## 2. Clonar um repositório do GitHub

```bash
git clone https://github.com/usuario/repositorio.git
```

> Isso cria uma cópia local do projeto para você trabalhar.

---

## 3. Verificar o status do repositório

```bash
git status
```

> Mostra arquivos modificados, não rastreados, etc.

---

## 4. Adicionar arquivos para commit

```bash
git add nome_do_arquivo
# ou para adicionar tudo:
git add .
```

---

## 5. Salvar mudanças (commit)

```bash
git commit -m "Mensagem clara sobre o que foi feito"
```

---

## 6. Enviar mudanças para o GitHub

```bash
git push
```

---

## 7. Atualizar seu repositório local com as mudanças do grupo

```bash
git pull
```

> Sempre execute `git pull` antes de começar a trabalhar!

---

## 8. Trabalhar com branches (opcional, mas recomendado)

Criar uma nova branch:

```bash
git checkout -b nome-da-branch
```

Trocar de branch:

```bash
git checkout nome-da-branch
```

Enviar a branch para o GitHub:

```bash
git push -u origin nome-da-branch
```

---

## 9. Resolver conflitos (básico)

1. Ao rodar `git pull`, pode aparecer um **conflito**.
2. Abra o arquivo indicado e **escolha qual código manter**.
3. Após corrigir:

   ```bash
   git add .
   git commit -m "Resolvido conflito"
   git push
   ```

---

## 10. Ver histórico de commits

```bash
git log --oneline
```

---

## 11. Alterar usuário ou email (caso precise trocar)

```bash
git config --global user.name "Novo Nome"
git config --global user.email "novo@email.com"
```

---

## Dicas Finais

✅ Faça `git pull` antes de começar
✅ Faça `git add`, `git commit` e `git push` ao terminar
✅ Comunique-se com o grupo antes de alterar arquivos compartilhados
✅ Use branches para evitar conflitos
