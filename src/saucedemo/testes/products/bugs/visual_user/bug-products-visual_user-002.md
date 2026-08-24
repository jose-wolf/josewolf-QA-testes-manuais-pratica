# BUG-PRODUCT-VISUAL_USER-002 — Descrições dos produtos apresentam informações inconsistentes

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
4. Observar as descrições apresentadas nos produtos.
5. Comparar o conteúdo da descrição com o produto correspondente.

## Resultado obtido

Determinados produtos apresentam descrições com conteúdo inconsistente ou que não representa corretamente o item exibido.

Foi observado, por exemplo, conteúdo como:

`carry.allTheThings()`

em uma descrição de produto, indicando que a informação apresentada não corresponde adequadamente ao item.

## Resultado esperado

Cada produto deve apresentar uma descrição coerente com o item exibido, contendo informações claras e apropriadas para sua identificação.

## Impacto

Descrições incorretas ou inconsistentes podem causar confusão durante a avaliação dos produtos e dificultar a compreensão das características do item, prejudicando a decisão de compra do usuário.

## Evidência

![BUG-PRODUCT-VISUAL_USER-002](../../evidencias/visual_user/bug-products-visual_user-001.png)

## Status

Aberto