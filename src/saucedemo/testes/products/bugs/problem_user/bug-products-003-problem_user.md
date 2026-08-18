# BUG-PRODUCT-PROBLEM_USER-003 — Botão Remove não remove produtos adicionados

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
4. Adicionar um dos produtos que permitem a utilização do botão **Add to cart**.
5. Verificar que o botão é alterado para **Remove**.
6. Clicar no botão **Remove**.

## Resultado obtido

Após adicionar o produto, o botão **Remove** é exibido, porém ao clicar nele o produto não é removido e permanece adicionado ao carrinho.

## Resultado esperado

Ao clicar no botão **Remove**, o produto deve ser removido do carrinho e a interface deve refletir corretamente a remoção realizada.

## Impacto

O defeito impede que o usuário desfaça a adição de um produto diretamente pela página **Products**, prejudicando o gerenciamento do carrinho e podendo interferir no fluxo de compra.

## Evidência

[Vídeo — BUG-PRODUCT-PROBLEM_USER-003](https://drive.google.com/file/d/1pEMTJuQl2f-Gitlux6YhetxdOgX75uW3/view?usp=sharing)


## Status

Aberto
