---
title: "Praticando Vetores e Objetos"
date: 2020-06-16T17:04:06-03:00
Description: ""
Tags: ["pratica"]
Categories: []
DisableComments: false
Draft: false
---

### Construção e impressão de objetos

Crie um programa que armazena dados da empresa Rocketseat dentro de um objeto chamado `empresa`. Os dados a serem armazenados são:

- Nome: Rocketseat
- Cor: Roxo
- Foco: Programação
- Endereço:

  - Rua: Rua Guilherme Gembala
  - Número: 260

Imprima em tela utilizando `console.log` o nome da empresa e seu endereço no seguinte formato:

_A empresa Rocketseat está localizada em Rua Guilherme Gembala, 260_

### Resultado

```js
const empresa = {
  nome: "RocketSeat",
  cor: "roxo",
  foco: "programação",
  endereco: {
    rua: "Rua: Rua Guilherme Gembala",
    numero: 260,
  },
};

console.log(
  `A ${empresa.nome} que possui como tema a cor ${empresa.cor} e foco em ${empresa.foco}, está localizada na ${empresa.endereco.rua} no número ${empresa.endereco.numero}.`
);

//A RocketSeat que possui como tema a cor roxo e foco em programação, está localizada na Rua: Rua Guilherme Gembala no número 260.
```

### Vetores e objetos

Crie um programa com um objeto para armazenar dados de um programador como `nome`, `idade` e `tecnologias` que trabalha.

Um programador pode trabalhar com várias tecnologias, por isso armazene essas tecnologias em um array.

As tecnologias também devem ser objetos contendo `nome` e `especialidade`, use as tecnologias abaixo:

```js
{ nome: 'C++', especialidade: 'Desktop' }
{ nome: 'Python', especialidade: 'Data Science' }
{ nome: 'JavaScript', especialidade: 'Web/Mobile' }
```

Por exemplo:

```js
const objeto = {
  propriedade: [
    { nome: "C++", especialidade: "Desktop" },
    { nome: "JavaScript", especialidade: "Web/Mobile" },
  ],
};
```

Imprima em tela o nome e especialidade da primeira tecnologia que o usuário utiliza no seguinte formato:

```
O usuário Carlos tem 32 anos e usa a tecnologia C++ com especialidade em Desktop
```

### Resultado

```js
const programadoras = [
  {
    dev: "Amanda",
    idade: 24,
    linguagem: [
      {
        principal: "JavaScript",
        foco: "Web development",
      },
      {
        principal: "Go",
        foco: "aprendizado",
      },
    ],
  },
  {
    dev: "Erika",
    idade: 30,
    linguagem: {
      principal: "Go",
      foco: "backend development",
    },
  },
];

console.log(
  `A programadora ${programadoras[0].dev} tem ${programadoras[0].idade} anos e usa o ${programadoras[0].linguagem[0].principal} com foco em ${programadoras[0].linguagem[1].foco}`
); //A programadora Amanda tem 24 anos e usa o JavaScript com foco em Web development
```
