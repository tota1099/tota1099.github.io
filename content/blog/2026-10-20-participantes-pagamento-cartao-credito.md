---
title: Participantes em um pagamento online com cartão de crédito
slug: participantes-pagamento-cartao-credito
date: 2026-10-20T10:00:00-03:00
description: "Resumo em uma frase, até 160 caracteres. É o que aparece no Google."
categories:
  - Tecnologia
  - Pagamentos
tags:
  - pagamentos
  - ecommerce
---

Milhares de pessoas efetuam compras onlines todos os dias utilizando seus cartões de crédito. Seja na amazon, mercado livre ou outro ecommerce, virou rotina o consumo online de produtos, principalmente devido as facilidades nesse modelo de compra: entrega rápida, avaliações de quem já comprou, entre outros benefícios da compra online.

Mas por que já parou para pensar que essa simples compra, que parece ter sido feita sozinha pelo comprador, colocando seu cartão de crédito no site, pode envolver dezenas de participantes? Sempre pensamos no vinculo comprador -> banco -> lojista, mas essa estrutura não é tão simples quanto parece.

O objetivo desse artigo é explicar quais os participantes envolvidos em uma compra online com cartão de crédito; desde a confeção do cartão, até o dinheiro caindo na conta do lojista.

## O começo: efetuando a compra

Uma pessoa quer comprar uma camiseta de futebol do seu time do coração: a seleção brasileira! Como de costume, ela digita no google "Camiseta seleção brasileira" e abre 2 ou 3 abas com as principais lojas com esse produto. Da uma olhada nas fotos, descrições, avaliações dos clientes, frete e preço; e decide comprar o produto na loja 1, que além de mais barata, irá entregar em até 2 dias úteis! A pessoa então clica para comprar, seleciona cartão de crédito como meio de pagamento, preenche seus dados e finaliza a compra! Pronto, em até 2 dias, estará vestindo a camiseta da seleção que tanto queria!

```mermaid
flowchart LR
    A["🧑 Cliente"] -->|usa| B["💳 Cartão de crédito"]
    B -->|paga no| C["🛒 E-commerce"]
    C -->|repassa o pedido ao| D["🏪 Lojista"]
    D -->|entrega a camiseta ao| A
```

Olhando esse processo, parece muito simples e ter envolvimento de somente **3 participantes**: cliente, Lojista e E-commerce.

Mas como o cliente possui um cartão de crédito? Quem lhe da crédito? Quem lhe entregou o cartão? Quem confeccionou o cartão? Vamos descobrir isso no próximo tópico.

## O cartão de crédito

O cliente utilizou um cartão de crédito para efetuar a compra no e-commerce: mas como o cliente possui um cartão de crédito?

Tudo começa com o emissor, ou seja, quem emite o cartão: um cartão de crédito pode ser emitido por um banco ou por uma instituição de pagamento emissora de instrumento pós-pago.

- Exemplos de bancos são: Banco do Brasil, Santander, Caixa Econômica Federal, Bradesco.
- Exemplos de Instituições de Pagamento: Mercado Pago, Picpay, Nubank.

Para simplificar, não vou adicionar esses participantes no artigo em detalhes, mas para essas instituições poderem emitir os cartões, dependem de outros participantes como:

- Banco Central: autoriza e supervisiona o emissor.
- Bandeira (Visa, Mastercard, Elo): licencia o emissor a participar do arranjo de pagamento.

Uma vez que temos o cartão, alguém tem que decidir dar crédito ao cliente. Porém, nesse processo, podemos ter até 4 empresas diferentes:

- Marca do cartão: quem aparece para o cliente. Pode ser uma fintech, um varejista ou o próprio banco.
- Emissor: a instituição autorizada pelo banco central e licenciada pela bandeira.
- Credor: a instituição financeira que de fato concede o financiamento ao cliente.
- Quem financia (funding): de onde vem o dinheiro emprestado. Pode ser o caixa do próprio banco, captação via CDB, etc.

Para esses participantes decidirem dar crédito para uma pessoa, eles fazem uma análise com os órgãos de proteção ao crédito, como o Serasa; e o Sistema de Informações de Créditos (SCR) do banco central, que mostra o endividamento do cliente no sistema financeiro inteiro.
