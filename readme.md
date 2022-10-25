# FinApi - Financeira 💰
Uma API de contas bancárias com regras de negócios a serem seguidas e requisitos, feita com NodeJS e ExpressJS. Testado com Insomnia.

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
