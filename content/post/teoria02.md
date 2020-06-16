---
title: "Objetos e Vetores"
date: 2020-06-16T17:02:02-03:00
Description: ""
Tags: ["teoria"]
DisableComments: false
Draft: false
---

### Objetos

Podem ser considerados como uma coleção de propriedade e funcionalidades.

```
const aluno01 = {
    nome: "Amanda",
    idade: 24
}
```

E para acessar as propriedades, nesse caso, usa-se:

```
aluno01.nome
```

### Vetores

Vetores ou como conhecidos, os arrays são o agrupamento desses objetos. É eu colocar vários objetos, dentro de um objeto maior.

```
const alunos = [
    {
        nome: "Amanda",
        idade: 24
    },
    {
        nome: "Gabriel"
        idade: 22
    }
]
```

E para acessar os objetos desse vetores, usa-se o valor da posição que ele se encontra. 

```
alunos[0].nome
alunos[1].idade
```

> _Lembrando que os indíces começam no valor 0._