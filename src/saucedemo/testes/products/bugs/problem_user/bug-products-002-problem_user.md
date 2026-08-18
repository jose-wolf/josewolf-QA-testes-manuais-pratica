# BUG-PRODUCT-PROBLEM_USER-002 — Não é possível adicionar determinados produtos ao carrinho

**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Caso de teste relacionado:** TC-PRODUCT-PROBLEM_USER-002

**Categoria:** Funcional

**Severidade:** Alta

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `problem_user`.
3. Acessar a página **Products**.
4. Clicar no botão **Add to cart** de diferentes produtos.
5. Verificar se todos os produtos selecionados são adicionados ao carrinho.

## Resultado obtido

Apenas determinados produtos podem ser adicionados ao carrinho. Ao clicar em **Add to cart** em alguns produtos, a ação não é realizada e o produto não é adicionado.

## Resultado esperado

Todos os produtos disponíveis devem poder ser adicionados ao carrinho quando o usuário clicar no botão **Add to cart**.

## Impacto

O defeito impede que o usuário adicione determinados produtos ao carrinho, comprometendo diretamente o fluxo de compra e podendo impedir a venda dos produtos afetados.

## Evidência

[Vídeo — BUG-PRODUCT-PROBLEM_USER-002]([../evidencias/NOME-DO-VIDEO.webm](https://drive.google.com/file/d/1pEMTJuQl2f-Gitlux6YhetxdOgX75uW3/view?usp=sharing))


## Status

Aberto
