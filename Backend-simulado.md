# Projeto Integrador: Sistema de Biblioteca (Padrão MVC Simplificado)

## Introdução

Este projeto tem o objetivo de simular um sistema de biblioteca onde usuários podem pegar livros emprestados, renovar empréstimos, devolver livros, além de permitir o cadastro e gerenciamento de usuários e livros.

Vocês irão trabalhar com TypeScript, utilizando Programação Orientada a Objetos (POO) e arrays para armazenar os dados, simulando um banco de dados.

---

## Estrutura do Projeto

### 1. Models (Entidades)

- Aqui vocês devem criar as classes que representam os dados do sistema.
- Cada classe deve conter os atributos que representam suas informações.
- Podem ter métodos que façam sentido apenas para o próprio objeto (exemplo: alterar quantidade de livros, renovar um empréstimo, validar senha do usuário).
- **Não** coloquem aqui regras que envolvam várias entidades ou manipulações de listas.

**Exemplos:**

- `Usuario`
  - Atributos: `id`, `nome`, `email`, `senha` (privado)
  - Métodos: validar senha, alterar senha.

- `Livro`
  - Atributos: `id`, `titulo`, `autor`, `preco`, `quantidade`
  - Métodos: alterar quantidade (aumentar ou diminuir).

- `Emprestimo`
  - Atributos: `id`, `usuarioId`, `livroId`, `dataEmprestimo`, `dataDevolucao`, `renovado` (boolean)
  - Métodos: renovar empréstimo (só pode renovar uma vez, adiciona 7 dias à data de devolução).

---

### 2. Services (Regras de Negócio e Manipulação de Dados)

- Nesta camada ficam as regras do sistema, toda a lógica de negócio.
- Vocês vão criar arrays para armazenar os dados (simulando um banco de dados).
- Devem implementar os métodos para:
  - Criar, listar, buscar por id, atualizar e remover usuários e livros (CRUD).
  - Emprestar livros (verificar se o livro está disponível, diminuir a quantidade, criar o empréstimo).
  - Devolver livros (aumentar a quantidade e remover o empréstimo).
  - Renovar empréstimos (permitir apenas uma renovação por empréstimo).
  - Listar empréstimos por usuário e listar todos os empréstimos.

**Exemplos:**

- `UsuarioService`
- `LivroService`
- `EmprestimoService`

---

## Observações Importantes

- **IDs**: Usem números inteiros para identificar usuários, livros e empréstimos. Eles ajudam a relacionar os dados.
- **Separação de responsabilidades**: 
  - **Model:** apenas dados e métodos simples ligados ao próprio objeto.
  - **Service:** toda a lógica que envolve várias entidades ou manipulação dos arrays.
- **Tratamento de erros**: Para este momento, apenas usem `if` e mensagens no console para informar problemas (exemplo: “Livro indisponível”, “Usuário não encontrado”, etc). Não precisam usar `try/catch` ainda.

---

## Exemplo de fluxo simplificado

1. Criar usuário.
2. Criar livro.
3. Emprestar livro para usuário (se disponível).
4. Renovar empréstimo (se ainda não renovado).
5. Devolver livro.
6. Listar dados para verificar se tudo está correto.

---

## Banco de Dados (simulado)

Vocês já possuem um banco de dados em SQL com as tabelas e relacionamentos. Agora, no TypeScript, vocês vão simular esse banco usando arrays de objetos.

Cada `Service` vai manter um array privado com as instâncias das classes correspondentes.

---

## Dicas finais

- Organize seu código em pastas: `models` para as entidades e `services` para as regras.
- Use nomes claros para métodos e variáveis.
- Teste seu código sempre, criando dados e simulando operações.
- Comentem o código para facilitar a compreensão.
