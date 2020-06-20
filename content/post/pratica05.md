---
title: "Pratica - Operações bancárias"
date: 2020-06-20T14:09:38-03:00
Description: ""
Tags: ["pratica"]
Categories: []
DisableComments: false
---

Crie um programa para realizar operações bancárias na conta de um usuário.

Comece criando um objeto com o nome do usuário, suas transações e saldo.

As transações (transactions) devem iniciar como um array vazio `[]` e o saldo (balance) em `0` (zero).

```js
const user = {
  name: "Mariana",
  transactions: [],
  balance: 0,
};
```

### Adicionar transações

Crie uma função `createTransaction` para adicionar uma nova transação no array de transações de um usuário, essa função deve receber como parâmetro um objeto de transação que tem o seguinte formato:

```js
{
  type: 'credit',
  value: 50.5
}
```

O `type` pode ser `credit` para créditos e `debit` para débitos da conta do usuário.

Quanto uma transação for do tipo `credit` ela deve também somar o valor do crédito no saldo (balance) do usuário.

Se for uma transação do tipo `debit` ela deve subtrair o valor do débito no saldo (balance) do usuário.

_Dica.: Você pode usar o método `user.transactions.push(transaction)` para adicionar um novo item no array de transações._

### Relatórios

- Crie uma função chamada `getHigherTransactionByType` que recebe como parâmetro o tipo de transação `credit/debit`, percorre as transações do usuário e retorna o **objeto** da transação de maior valor com aquele tipo:

```js
getHigherTransactionByType("credit"); // { type: 'credit', value: 120 }
```

- Crie uma função chamada `getAverageTransactionValue` que retorna o valor médio das transações de um usuário independente do seu tipo:

```js
getAverageTransactionValue(); // 83.3
```

- Crie uma função chamada `getTransactionsCount` que retorna o número de transações de cada tipo `credit/debit`, o retorno da função deve ser um objeto e seguir exatamente como o modelo apresentado abaixo:

```js
getTransactionsCount(); // { credit: 5, debit: 3 }
```

### Exemplo de resultado final do projeto:

```js
createTransaction({ type: "credit", value: 50 });
createTransaction({ type: "credit", value: 120 });
createTransaction({ type: "debit", value: 80 });
createTransaction({ type: "debit", value: 30 });

console.log(user.balance); // 60

getHigherTransactionByType("credit"); // { type: 'credit', value: 120 }
getHigherTransactionByType("debit"); // { type: 'debit', value: 80 }

getAverageTransactionValue(); // 70

getTransactionsCount(); // { credit: 2, debit: 2 }
```

## Resultado

```js
const user = {
  name: "Mariana",
  transactions: [],
  balance: 0,
};

//cria uma função para adicionar uma nova transação
//passa transaction como uma nova variavel
function createTransaction(transaction) {
  // encaminha para o array onde adicionar a transaction
  user.transactions.push(transaction);

  //condicao para classificar a transaction como credito
  if (transaction.type === "credit") {
    user.balance = user.balance - transaction.value;
  } else {
    user.balance = user.balance + transaction.value;
  }
}

function getHigherTransactionByType(transactionType) {
  //valor de comparação
  let higherValue = 0;
  //variavel qualquer
  let higherTransaction;

  //para cada transação do usuario
  for (transaction of user.transactions) {
    // vai comparar a transação passada com a do array e ver se é maior que 0
    if (
      transaction.type == transactionType &&
      transaction.value > higherValue
    ) {
      //variavel qualquer recebe e a transação maior
      higherTransaction = transaction;
    }
  }

  //retorna a maior transaçao
  return higherTransaction;
}

function getAverageTransactionValue() {
  //cria uma variavel inicial
  let soma = 0;

  //percorre o array de transações
  for (transaction of user.transactions) {
    //faz a soma com o valor da transação
    soma = soma + transaction.value;
  }

  //retorna a operação
  return soma / user.transactions.length;
}

function getTransactionsCount() {
  //objeto para contar as transações
  const numberTransaction = {
    debit: 0,
    credit: 0,
  };

  //percorre o array de transações
  for (let transaction of user.transactions) {
    //para cada operação
    if (transaction.type === "credit") {
      //adiciona 1
      numberTransaction.credit++;
    } else {
      //adiciona 1
      numberTransaction.debit++;
    }
  }

  //retorna o objeto atualizado
  return numberTransaction;
}

//adicionando transações
createTransaction({ type: "credit", value: 250 });
createTransaction({ type: "debit", value: 250 });
createTransaction({ type: "debit", value: 650 });
createTransaction({ type: "debit", value: 750 });

//imprimindo maiores transações
console.log(getHigherTransactionByType("debit"));
//média de transações
console.log(getAverageTransactionValue().toFixed(2));
//count de transações
console.log(getTransactionsCount());
```