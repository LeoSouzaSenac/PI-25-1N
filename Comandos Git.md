# Comandos Básicos de Git/GitHub para Projetos em Grupo

Este guia ensina o essencial para colaborar em grupo usando Git e GitHub.  
Ideal para iniciantes que nunca usaram controle de versão.

---

## 1. Configuração Inicial (executar apenas uma vez)

Define seu nome e e-mail nos commits.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
````

> **Dica:** Use o mesmo e-mail da sua conta GitHub.

Verifique sua configuração:

```bash
git config --list
```

---

## 2. Clonar um repositório do GitHub

Cria uma cópia local de um projeto hospedado no GitHub.

```bash
git clone https://github.com/usuario/repositorio.git
```

---

## 3. Verificar o status do repositório

Mostra quais arquivos foram modificados, adicionados ou estão prontos para commit.

```bash
git status
```

---

## 4. Adicionar arquivos para commit

Adiciona arquivos que você quer salvar na próxima versão do projeto.

```bash
git add nome_do_arquivo
# ou para adicionar todos os arquivos modificados:
git add .
```

---

## 5. Salvar mudanças (commit)

Grava as mudanças feitas com uma mensagem descritiva.

```bash
git commit -m "Mensagem clara sobre o que foi feito"
```

> 💡 **Boas mensagens de commit:** use verbos no imperativo, como:
>
> * `adiciona funcionalidade de login`
> * `corrige bug no formulário`
> * `atualiza layout da home`

---

## 6. Enviar mudanças para o GitHub

Envia seus commits locais para o repositório remoto.

```bash
git push
```

---

## 7. Atualizar seu repositório local com as mudanças do grupo

Baixa e aplica mudanças feitas por outras pessoas.

```bash
git pull
```

> Sempre execute `git pull` antes de começar a trabalhar!

---

## 8. Trabalhar com branches (opcional, mas recomendado)

### O que é uma branch?

Uma branch é uma “linha paralela” de desenvolvimento. Você pode fazer mudanças sem interferir diretamente na versão principal (geralmente chamada `main` ou `master`).

### Criar uma nova branch:

```bash
git checkout -b nome-da-branch
```

### Trocar de branch:

```bash
git checkout nome-da-branch
```

### Enviar a branch para o GitHub:

```bash
git push -u origin nome-da-branch
```

---

## Como nomear branches

Use nomes curtos e descritivos, sempre em minúsculas e separados por hífens.
Se quiser, use prefixos para organizar melhor:

| Tipo                  | Exemplo                |
| --------------------- | ---------------------- |
| Funcionalidade nova   | `cadastro-cliente`     |
| Correção de erro      | `corrige-login`        |
| Refatoração de código | `melhora-performance`  |

---

## 9. Resolver conflitos (básico)

Conflitos acontecem quando duas pessoas alteram a mesma parte do código.

1. Ao rodar `git pull`, o Git avisará que há conflito.
2. Abra o(s) arquivo(s) marcados e **escolha qual parte manter**.
3. Após resolver:

```bash
git add .
git commit -m "resolve conflito no arquivo X"
git push
```

> As partes conflitantes estarão entre `<<<<<<<`, `=======` e `>>>>>>>`.

---

## 10. Ver histórico de commits

Mostra um resumo de todos os commits feitos.

```bash
git log --oneline
```

---

## 11. Alterar usuário ou email (caso precise trocar)

Útil se estiver em outro computador ou com configurações erradas.

```bash
git config --global user.name "Novo Nome"
git config --global user.email "novo@email.com"
```

---

## ✅ Dicas Finais para Trabalhar em Equipe

* Faça `git pull` **antes** de começar a trabalhar
* Faça `git add`, `git commit` e `git push` **sempre que terminar uma tarefa**
* Comunique-se com o grupo antes de editar arquivos compartilhados
* Use branches com nomes claros para evitar conflitos
* Escreva mensagens de commit que expliquem **o que foi feito**
* Nunca edite diretamente a `main`, use branches!

Perfeito! Aqui está uma **versão revisada** dos exercícios, **sem conflitos** e com o passo de **criar o próprio repositório no GitHub** incluído logo no início.

---

# 🧪 Exercícios Práticos com Git/GitHub
---


## ✅ Exercício 1 – Criar repositório no GitHub e clonar

**Objetivo:** Criar um repositório e começar a usá-lo localmente

### Passos:

1. Acesse [github.com](https://github.com) e crie um novo repositório chamado `meu-projeto-git` (sem README).
2. Copie o link HTTPS do repositório (ex: `https://github.com/seu-usuario/meu-projeto-git.git`)
3. No terminal, escolha uma pasta e clone o repositório:

   ```bash
   git clone https://github.com/seu-usuario/meu-projeto-git.git
   ```
4. Entre na pasta clonada:

   ```bash
   cd meu-projeto-git
   ```

---

## ✅ Exercício 2 – Criar arquivo e fazer commit

**Objetivo:** Criar um arquivo e registrar a mudança

### Passos:

1. Crie um arquivo de texto no seu repositório clonado. Se quiser, pode criar via terminal:

   ```bash
   echo "Anotações" > anotacoes.txt
   ```
2. Veja o status:

   ```bash
   git status
   ```
3. Altere o arquivo, escrevendo um breve resumo do porque você escolheu o curso. Use git status novamente e veja a diferença.
   
4. Adicione o arquivo:

   ```bash
   git add anotacoes.md
   ```
5. Faça o commit:

   ```bash
   git commit -m "adiciona arquivo de anotações"
   ```
6. Envie para o GitHub:

   ```bash
   git push
   ```

---

## ✅ Exercício 3 – Criar e usar uma branch

**Objetivo:** Criar uma nova branch e trabalhar nela

### Passos:

1. Crie uma nova branch:

   ```bash
   git checkout -b minha-branch
   ```
2. Crie um novo arquivo:

   ```bash
   echo "console.log('Aprendendo Git')" > script.js
   ```
3. Adicione e faça commit:

   ```bash
   git add script.js
   git commit -m "adiciona script inicial"
   ```
4. Envie a branch para o GitHub:

   ```bash
   git push -u origin minha-branch
   ```

---

## ✅ Exercício 4 – Ver o histórico de commits

**Objetivo:** Visualizar os commits feitos até agora

### Passos:

1. Execute:

   ```bash
   git log --oneline
   ```
2. Experimente também:

   ```bash
   git log --graph --all --decorate
   ```

---



