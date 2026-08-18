# BUG-PRODUCT-STD_USER-001 — Inconsistência nas informações dos produtos

**Caso de teste relacionado:** TC-PRODUCT-STD_USER-001
**Categoria:** Inconsistência de informações
**Severidade:** Alta
**Prioridade:** Alta
**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `standard_user`.
3. Acessar a página **Products**.
4. Verificar a imagem, o título e a descrição dos produtos exibidos.

## Resultado obtido

Foram encontrados dois produtos cujas imagens não correspondem ao título e/ou à descrição apresentada.

## Resultado esperado

Todos os produtos devem apresentar imagem, título e descrição coerentes entre si, permitindo que o usuário identifique corretamente o produto exibido.

## Impacto

A inconsistência entre imagem, título e descrição pode causar confusão durante a escolha do produto e afetar a decisão de compra do cliente, pois as informações apresentadas não representam corretamente o item exibido.

## Evidência


![BUG-PRODUCTS-STD_USER-001](../../evidencias/standard_user/bug-products-std_user-001-informacoes.png)


## Status

Aberto
