---
title: "Iniciando o Front end"
date: 2020-06-20T16:24:20-03:00
Description: ""
Tags: ["teoria"]
Categories: []
DisableComments: false
---

## O que é back end x front end?

Para entender os conceitos, precisamos entender cliente e servidor:

### Cliente e Servidor

O cliente é a parte que você visualiza no navegador, a página que você está acessando, já o servidor é onde fica os códigos, regras de negócio, os dados e etc.

E eles se comunicam atráves da comunicação HTTP.

### Comunicação HTTP

**HTTP** === Hypertext Transfer Protocol

> HTTP é um protocolo de transferência que possibilita que as pessoas que inserem a URL do seu site na Web possam ver os conteúdos e dados que nele existem.

Então quando você digita na url o site, você está enviando uma chamada para o servidor e o servidor vai enviar para o seu navegador as informações do site atráves das regras de protocolos.

#### E o tal do HTTPS?

O HTTPS é a versão melhorada do HTTP, pois o S vem de segurança. Ou seja, quando um site é configurado com HTTPS ele possui uma "camada extra" de seguranda, pois ele apresenta um certificado do tipo SSL.

> O certificado SSL (sigla para Secure Socket Layer), é um protocolo de segurança padrão na internet. Ele é utilizado em situações que promovem a troca de informações entre dois usuários da rede, o que é comum em ações corriqueiras como compras em lojas virtuais.

Geralmente servidores já oferecem esse tipo de certificado, entretando você pode comprar a parte.

### Back end

É a parte do server-side e ele é responsável pelas regras do negócio

> Regras do negócio: toda a lógica de servir dados para o front end.

### Front end

É a parte client-side e é responsável por solicitar os dados para o servidor.

## HTML

HTML === Hypertext Markup Language

É a apresentação da página que o navegador vai ler.

```html
<html>
  <head>
    <title>Hello World</title>
  </head>
  <body>
    <img src="world.jpg" />
  </body>
</html>
```

## CSS

CSS === Cascading Style Sheet

É uma linguagem de personalização e customização para o HTML.

```css
body {
  margin: 0;
}

img {
  font-family: sans-serif;
}
```

#### Variáveis CSS

```css
:root {
  /*cria-se as variáveis*/
  --color-green: #50fa7b;
  --color-roxo: #7159c1;
}

body {
  /*aplica elas assim*/
  background: var(--color-green);
}
```

#### CSS Grid

```css
/*elemento pai*/
section.cards {
  max-width: 1000px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr; /* define quantas colunas*/
  gap: 30px; /*espaçamento entre os filhos*/
}
```

## JavaScript

É uma linguagem de programação que na sua origem veio para fazer os sites mais dinâmicos. Entretanto hoje em dia, essa linguagem evoluiu tanto que é possível fazer o back-end e o front-end em uma linguagem só.
