---
title: "Começando na programação:"
date: 2020-06-16T13:47:35-03:00
Description: ""
Tags: ["teoria"]
DisableComments: false
Draft: false
---

## Iniciando na programação

Programação nada mais é do que ensinar ao computar a executar tarefas, através dos comados. Esses comandos podem ser chamados de ALGORITMOS, que são instruções, contendo regras, para executar as tarefas.

### Tipos de variáveis

Do tipo **string**:

```
const nome = "Amanda"
const nome = 'Bruna Carolina'
```

Do tipo **number**:

````
const idade = 17
const peso = 17.6
````

Do tipo **boolean**:

```
const verdade = true
const falso = false
const indefinido = null
```

### Operadores de comparação

Maior: `>` ou maior e igual:  `>=`

```
idade 18 > 17
```

Menor: `<` ou menor e igual: `<=`

```
idade 15 < 18
```

Igual: `==` ou igual e do mesmo tipo: `===`

```
17 == "17" || 17 === 17
```

Diferente:  `!` ou diferente e diferente de tipo: `!==`

### Operadores lógicos

`&&` **E**: as duas condições devem ser verdadeiras

```
(afirmacao1 && afirmacao2) ? true : false
```

`||` **OU**: apenas uma das afirmações deve ser verdadeira

```
(afirmacao1 || afirmacao2) return true
```

`!` **Não**: nega uma afirmação

### Operadores matemáticos

`+` soma

`-` subtração

`*` multiplicação

`/` divisão

`%` resto da divisão

**Obs:** Para executar um arquivo .js, não há necessidade de criar um arquivo html com a importação do script na página, pode rodar no terminal o arquivo:

```
node nome-do-arquivo.js
```