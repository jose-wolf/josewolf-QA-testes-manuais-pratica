# BUG-PRODUCT-VISUAL_USER-001 — Imagem exibida não corresponde ao produto

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Caso de teste relacionado:** TC-PRODUCT-VISUAL_USER-001

**Categoria:** Inconsistência de informações

**Severidade:** Média

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `visual_user`.
3. Acessar a página **Products**.
4. Observar as imagens apresentadas nos produtos.
5. Comparar a imagem exibida com o título e as demais informações do produto.

## Resultado obtido

Determinados produtos apresentam imagens que não correspondem ao item identificado pelo título.

Por exemplo, o produto **Sauce Labs Backpack** é apresentado com uma imagem que não representa uma mochila.

## Resultado esperado

Cada produto deve apresentar uma imagem correspondente ao item identificado pelo título e pelas demais informações exibidas.

## Impacto

A utilização de imagens incorretas pode dificultar a identificação dos produtos e causar confusão durante a escolha dos itens, prejudicando a experiência e a decisão de compra do usuário.

## Evidência

![BUG-PRODUCT-VISUAL_USER-001](../../evidencias/visual_user/bug-products-visual_user-001.png)

## Status

Aberto