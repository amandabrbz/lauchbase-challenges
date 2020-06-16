---
title: "Starter JavaScript"
date: 2020-06-15T21:27:44-03:00
Description: "!!!"
Tags: []
Categories: []
DisableComments: true
Draft: false
---

### Cálculo de IMC

Crie um programa para calcular o IMC e nível de obesidade de uma pessoa.
Comece criando constantes para armazenar o nome, peso, altura e sexo de uma pessoa, por exemplo:

**Joana** tem **66** kg e mede **1.40** cm

A partir desses dados armazene em uma constante chamada imc o cálculo do índice de massa corporal definido pela fórmula abaixo:

**peso / (altura \* altura);**

Baseado no valor obtido através desse cálculo exiba as seguintes mensagens:

* SE o IMC maior ou igual a 30: Carlos você está acima do peso;
* SE o IMC menor que 29.9: Carlos você não está acima do peso;


```sh
const paciente = "Fernanda";
const peso = 90;
const altura = 1.75;

var imc = peso / (altura * altura);

if (imc >= 30) {
    console.log(`${paciente} está acima do peso`);
} else {
    console.log(`${paciente} não está acima do peso`);
}

//não está acima
```

### Cálculo de aposentadoria
Crie um programa para calcular a aposentadoria de uma pessoa.

*Obs.: Esse cálculo é fictício, dentro da aposentadoria existem muitos outros fatores para serem levados em conta :)*

Comece criando constantes para armazenar nome, sexo, idade e contribuicao(em anos).

O tempo de contribuição mínimo para homens é de 35 anos e, para mulheres, 30 anos;
**Utilizando a regra 85-95, a soma da idade com o tempo de contribuição do homem precisa ser de no mínimo 95 anos, enquanto a mulher precisa ter no mínimo 85 anos na soma;**

Com base nas regras acima imprima na tela as mensagens:

* SE a pessoa estiver aposentada: Silvana, você pode se aposentar!

* SE a pessoa NÃO estiver aposentada: Silvana, você ainda não pode se aposentar!
```sh
const pessoa = "Marcio";
const sexo = "M";
const idade = 70;
const anosContribuicao = 12;

var apto = idade + anosContribuicao;

if (apto >= 85 && sexo === "F") {
console.log(`${pessoa}, você pode se aposentar!`);
} else if (apto >= 95 && sexo === "M") {
console.log(`${pessoa}, você pode se aposentar!`);
} else {
console.log(`${pessoa}, você ainda não pode se aposentar!`);
}
```
