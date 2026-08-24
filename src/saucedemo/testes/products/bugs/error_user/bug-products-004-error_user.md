# BUG-PRODUCT-ERROR_USER-004 — Erro ao utilizar a ordenação dos produtos

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Caso de teste relacionado:** TC-PRODUCT-ERROR_USER-003

**Categoria:** Funcional

**Severidade:** Média

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `error_user`.
3. Acessar a página **Products**.
4. Abrir o seletor de ordenação dos produtos.
5. Selecionar uma opção de ordenação diferente da atual.
6. Observar o comportamento apresentado pelo sistema.

## Resultado obtido

Ao utilizar o seletor de ordenação com o usuário `error_user`, o sistema apresenta a mensagem:

`Sorting is broken! This error has been reported to Backtrace.`

A opção selecionada não é aplicada corretamente e a funcionalidade de ordenação apresenta erro.

## Resultado esperado

O sistema deve permitir selecionar qualquer opção de ordenação disponível e reorganizar corretamente a lista de produtos de acordo com o critério escolhido, sem apresentar mensagens de erro.

## Impacto

O defeito impede que o usuário `error_user` organize os produtos por nome ou preço, prejudicando a localização e a comparação dos itens disponíveis.

## Evidência

[Vídeo — BUG-PRODUCT-ERROR_USER-004](https://drive.google.com/file/d/1YPeM6VssdSVjbPW7eGTCLIcshhUSXFAM/view?usp=sharing)

## Status

Aberto