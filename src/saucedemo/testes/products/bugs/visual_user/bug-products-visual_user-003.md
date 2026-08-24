# BUG-PRODUCT-VISUAL_USER-003 — Preços dos produtos apresentam valores inconsistentes

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Caso de teste relacionado:** TC-PRODUCT-VISUAL_USER-001

**Categoria:** Inconsistência de informações

**Severidade:** Alta

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `visual_user`.
3. Acessar a página **Products**.
4. Observar os preços apresentados nos diferentes produtos.
5. Selecionar um produto e acessar sua página de detalhes.
6. Comparar o preço exibido na listagem com o preço apresentado nos detalhes do produto.
7. Repetir a validação com diferentes produtos.

## Resultado obtido

Determinados produtos apresentam preços inconsistentes na página **Products**.

Também foram observadas diferenças entre o valor apresentado na listagem e o valor exibido na página de detalhes do mesmo produto.

Além disso, alguns preços apresentam formatação inconsistente, como:

`$84.3`

em vez de manter o mesmo padrão de casas decimais utilizado nos demais produtos.

## Resultado esperado

O preço de cada produto deve permanecer consistente entre a página **Products** e sua respectiva página de detalhes.

Os valores também devem seguir um padrão uniforme de formatação monetária.

## Impacto

A apresentação de preços incorretos ou inconsistentes pode induzir o usuário a interpretar de forma errada o valor de um produto e comprometer diretamente sua decisão de compra.

A inconsistência também prejudica funcionalidades que dependem visualmente dessas informações, como a validação da ordenação por preço.

## Evidência

[Vídeo — BUG-PRODUCT-VISUAL_USER-003](https://drive.google.com/file/d/1mKcfuSjQB9KLvFbwhiiUc5mkWhGTkKiq/view?usp=sharing)

## Status

Aberto