# BUG-PRODUCT-ERROR_USER-001 — Inconsistência nas informações dos produtos

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Caso de teste relacionado:** TC-PRODUCT-ERROR_USER-001

**Categoria:** Inconsistência de informações

**Severidade:** Média

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `error_user`.
3. Acessar a página **Products**.
4. Verificar o título e a descrição dos produtos exibidos.
5. Comparar as informações apresentadas com o produto correspondente.

## Resultado obtido

Foram identificadas inconsistências no título e/ou na descrição de determinados produtos, fazendo com que as informações apresentadas não representem corretamente o item exibido.

## Resultado esperado

Todos os produtos devem apresentar título e descrição coerentes com o item correspondente, permitindo que o usuário identifique corretamente o produto.

## Impacto

Informações inconsistentes podem causar confusão durante a escolha dos produtos e prejudicar a decisão de compra do usuário.

## Evidência

![BUG-PRODUCT-ERROR_USER-001](../evidencias/NOME-DA-EVIDENCIA.png)

## Status

Aberto

---

# BUG-PRODUCT-ERROR_USER-002 — Não é possível adicionar determinados produtos ao carrinho

**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Caso de teste relacionado:** TC-PRODUCT-ERROR_USER-002

**Categoria:** Funcional

**Severidade:** Alta

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `error_user`.
3. Acessar a página **Products**.
4. Tentar adicionar diferentes produtos utilizando o botão **Add to cart**.
5. Observar o comportamento apresentado.

## Resultado obtido

Apenas determinados produtos podem ser adicionados ao carrinho. Ao clicar em **Add to cart** em alguns dos produtos disponíveis, a ação não é realizada.

## Resultado esperado

Todos os produtos disponíveis devem poder ser adicionados ao carrinho através do botão **Add to cart**.

## Impacto

O defeito impede a inclusão de determinados produtos no carrinho, comprometendo diretamente o fluxo de compra e podendo impedir a venda dos produtos afetados.

## Evidência

[Vídeo — BUG-PRODUCT-ERROR_USER-002](https://drive.google.com/file/d/1-k5sDQE-3zJ5biS1-G1WDF0oei44YZD6/view?usp=sharing)

## Status

Aberto
