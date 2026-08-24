
# BUG-PRODUCT-ERROR_USER-003 — Botão Remove não remove produtos adicionados

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
4. Adicionar um dos produtos que permitem a utilização do botão **Add to cart**.
5. Verificar que o botão é alterado para **Remove**.
6. Clicar no botão **Remove**.

## Resultado obtido

Após adicionar o produto, o botão **Remove** é exibido. Entretanto, ao clicar no botão, o produto não é removido do carrinho.

## Resultado esperado

Ao clicar no botão **Remove**, o produto deve ser removido corretamente e a interface deve refletir a alteração realizada.

## Impacto

O defeito impede que o usuário desfaça a adição de um produto diretamente pela página **Products**, prejudicando o gerenciamento dos itens selecionados e o fluxo de compra.

## Evidência

[Vídeo — BUG-PRODUCT-ERROR_USER-003](https://drive.google.com/file/d/1-k5sDQE-3zJ5biS1-G1WDF0oei44YZD6/view?usp=sharing)

## Status

Aberto
