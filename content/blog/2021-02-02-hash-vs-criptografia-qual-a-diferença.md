---
title: Hash vs Criptografia - Qual a diferença?
slug: hash-vs-criptografia
images:
  - /media/criptografia.jpg
date: 2021-02-02T22:05:29.892Z
description: >-
  Qual a diferença entre Hash e Criptografia?


  Muitas pessoas na área de tecnologia falam sobre esses conceitos, mas muitos não sabem a diferença e suas utilidades.


  A ideia do artigo que apresentar os conceitos de forma simples.
categories:
  - Tecnologia
tags:
  - criptografia
  - segurança
---
Neste final de semana, 10 de junho de 2018 (sim, este artigo foi escrito a quase 2 anos atrás), participei de um evento de programação chamado PHPSC (https://www.phpsc.com.br/), que foi um momento de muito aprendizado e diversão, além de ter conhecido ótimas pessoas.

Dentre as palestras, uma me chamou atenção, que foi a do Vinicius Campitelli (@vcampitelli) sobre o Libsodium, uma biblioteca de criptografia, que a partir do PHP 7.2 é implementada no core da linguagem. Esta biblioteca possui várias vantagens, devido a ser moderna, fácil de usar para encriptar e decriptar, construir hash de password, entre outras funções. Não vou entrar em detalhes sobre essa biblioteca, mas quem tiver mais curiosidade, pode dar uma olhada sobre ela clicando [aqui](https://paragonie.com/book/pecl-libsodium/read/00-intro.md).

É muito comum na área de tecnologia ouvirmos pessoas comentando sobre conceitos como criptografia e hash, porém muitas pessoas - mesmo profissionais da área - não sabem exatamente a diferença. Além disso, outras pessoas que não são da área acabam escutando esses conceitos e não possuem ideia do que significa. A ideia deste simples artigo é explicar de uma maneira simples o que é cada um.

### Criptografia

Criptografia é a prática de possuir regras usadas para codificar e descodificar uma informação, buscando a segurança de que só pessoas com conhecimento da regra tenham permissão de codificar ou descodificar.

#### Exemplo

Renan quer mandar uma mensagem secreta para Eduarda. Então os dois definem que a mensagem irá ser codificada alterando cada letra 2 caracteres na frente no alfabeto (A vira C, M vira O, etc.).

Mensagem: FelizNatal

Mensagem Codificada: Hgnkbpcvcn

Considerando que somente Renan e Eduarda possuem conhecimento das regras, somente os dois conseguem codificar e descodificar a informação e saber a mensagem.

### Hash

Hash é a prática de mapear dados grandes que possuem tamanho variável para pequenos dados de tamanho fixo. A principal função do hash é resumir dados e comparação de dados.

#### Exemplo

Renan possui a responsabilidade de imprimir um contrato (um arquivo word de uma página) cada vez que ele é alterado, pois ele é um modelo para advogados da sua empresa. Renan então gerou um hash dos dados desse word e ao invés de ficar analisando manualmente se foi alterado algo no arquivo word ou não, ele somente gera um novo hash e verifica se é idêntico ao anterior.

Hash Arquivo Word: 9f76d

Hash Arquivo Word após alteração: 8de3x

Então se o arquivo word não for alterado, ele sempre terá o mesmo hash (resumo), porém após possuir alguma alteração e gerar um novo hash, este será diferente do anterior.

### Conclusão

Esses 2 conceitos são muito usados na área de tecnologia principalmente relacionada a segurança. Se você não é da área de tecnologia é interessante saber o que é cada um de forma simples, para que comece a entender o papo do pessoal da área de tecnologia. Se você é da área de tecnologia ou tem interesse pela área, acho interessante estudar mais a fundo sobre os dois conceitos, tipos de criptografias e hash, entre outras coisas.

### Referências
<https://viniciuscampitelli.com/slides/libsodium-php/#/2/1>