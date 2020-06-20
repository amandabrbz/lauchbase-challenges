---
title: "Variáveis e Escopo"
date: 2020-06-17T23:50:00-03:00
Description: ""
Tags: ["teoria"]
Categories: []
DisableComments: false
---

## Variáveis

Atualmente temos 3 tipos de variáveis e que são necessários o entendimento do seu tipo na hora da criação da variável.

**const** == recebe valores que serão FIXOS e não poderão ser alterados ao decorrer do programa.

**let** == recebe valores que servirão apenas para aquele escopo do código, ou seja, não podem ser acessados globalmente, mas podem sofrer alteraçnoes dentro do escopo previsto.

**var** == recebe valores que podem ser acessados em qualquer escopo, portanto podem sofrer alterações ao decorrer do programa.

### Escopo

Se refere ao bloco de código contido naquele método/função/condição

```js
//+ inicio do escopo
function calculaMedia(alunos) {
  //+ inicio do escopo

  let soma = 0;
  for (let = i; i < alunos.lenght; i++) {
    //+ inicio do escopo
    soma = soma + alunos[i].nota;
    //fecha escopo
  }

  return soma;
  //fecha escopo
}
//continua escopo
```
