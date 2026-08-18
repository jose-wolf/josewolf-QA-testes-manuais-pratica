# BUG-PRODUCT-PROBLEM_USER-004 — Ordenação dos produtos não é aplicada

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Caso de teste relacionado:** TC-PRODUCT-PROBLEM_USER-003

**Categoria:** Funcional

**Severidade:** Média

**Prioridade:** Média

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `problem_user`.
3. Acessar a página **Products**.
4. Abrir o seletor de ordenação.
5. Selecionar uma opção diferente da ordenação atual.
6. Observar a disposição dos produtos.
7. Repetir o teste utilizando as demais opções de ordenação.

## Resultado obtido

O seletor apresenta as opções de ordenação disponíveis, porém a opção selecionada não é aplicada corretamente e a lista de produtos permanece na ordenação original.

## Resultado esperado

Ao selecionar uma opção de ordenação, a lista de produtos deve ser reorganizada de acordo com o critério escolhido.

## Impacto

O defeito impede que o usuário organize os produtos conforme sua preferência, dificultando a localização e comparação de itens por nome ou preço.

## Evidência

[Vídeo — BUG-PRODUCT-PROBLEM_USER-004](https://drive.google.com/file/d/1-weYuktfqMenluxRQQH553XXXXxMVtEu/view?usp=sharing)

## Status

Aberto
