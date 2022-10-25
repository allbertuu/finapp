# FinApi - Financeira 💰
Uma API de contas bancárias com regras de negócios a serem seguidas e requisitos, feita com NodeJS e ExpressJS. Testado com Insomnia.  
Projeto simples para botar em prática meus estudos em NodeJS.

## Como usar
1. É preciso utilizar uma ferramenta de design e testes de APIs, como o [Insomnia](https://insomnia.rest/products/insomnia) ou [Postman](https://www.postman.com/).
2. Será preciso passar o CPF no header da requisição para acessar determinadas rotas (middleware). De chave: `cpf`, e valor relacionado ao número do CPF. (não possue validador de CPF)


## Documentação da API

#### Retorna os dados (JSON) da conta ligada ao CPF (via header da requisição)

```http
  GET /account
```
#### Cria uma conta com o `cpf` e o `name` recebidos via body da requisição

```http
  POST /account
```

#### Atualiza o `name`, via body da requisição, da conta através do CPF indicado (via header da requisição)

```http
  PUT /account
```

#### Remove a conta através do CPF indicado (via header da requisição)

```http
  DELETE /account
```

#### Retorna um array (extrato) das transações da conta do CPF indicado (via header da requisição)

```http
  GET /statement
```

#### Retorna um array (extrato) das transações, no período indicado, da conta do CPF passado (via header da requisição)

```http
  GET /statement/date?date=2022-10-25
```

| Parâmetro   | Tipo       | Descrição                                   |
| :---------- | :--------- | :------------------------------------------ |
| `date`      | `query` | **Obrigatório**. A data que você quer saber, em padrão EUA |

#### Realiza um saque de valor descrito no `amount`, recebido via body da requisição, na conta do CPF indicado (via header da requisição)

```http
  POST /withdraw
```

#### Realiza um depósito de valor descrito no `amount` e com uma descrição sobre o depósito na `description`, recebidos via body da requisição, na conta do CPF indicado (via header da requisição)

```http
  POST /deposit
```

## Requisitos

- [x] Deve ser possível criar uma conta  
- [x] Deve ser possível buscar o extrato bancário do cliente
- [x] Deve ser possível realizar um depósito
- [x] Deve ser possível realizar um saque
- [x] Deve ser possível buscar o extrato bancário do cliente por data
- [x] Deve ser possível atualizar dados da conta do cliente
- [x] Deve ser possível obter dados da conta do cliente
- [x] Deve ser possível deletar uma conta

## Regras de negócio

- [x] Não deve ser possível cadastrar uma conta com CPF já existente
- [x] Não deve ser possível fazer depósito em uma conta não existente
- [x] Não deve ser possível buscar extrato em uma conta não existente
- [x] Não deve ser possível fazer saque em uma conta não existente
- [x] Não deve ser possível excluir uma conta não existente
- [x] Não deve ser possível fazer saque quando o saldo for insuficiente

## Aprendizados 📚
- Criar meu próprio Middleware e entender o significado e uso do mesmo.
- Testar a API usando o Insomnia.
- Aplicar uma lógica de acesso e excessões que contemplem regras de negócio.
- Utilizar e tratar dados vindos de query, route, e body params.
