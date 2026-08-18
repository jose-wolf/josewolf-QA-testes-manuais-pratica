# BUG-PRODUCT-PROBLEM_USER-005 — Informações dos produtos divergem entre a listagem e a página de detalhes

**Cenário relacionado:** CN-PRODUCT-005 — Validar acesso aos detalhes do produto

**Caso de teste relacionado:** TC-PRODUCT-PROBLEM_USER-005

**Categoria:** Inconsistência de informações

**Severidade:** Média

**Prioridade:** Alta

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `problem_user`.
3. Acessar a página **Products**.
4. Observar a imagem e as informações de um produto.
5. Clicar no nome ou na imagem do produto para acessar seus detalhes.
6. Comparar as informações apresentadas nas duas telas.
7. Repetir o procedimento com diferentes produtos.

## Resultado obtido

As informações apresentadas na página **Products** não permanecem consistentes ao acessar os detalhes dos produtos. Principalmente as imagens sofrem alterações: produtos exibidos com uma determinada imagem na listagem passam a apresentar outra imagem em suas respectivas páginas de detalhes.

O comportamento não é uniforme entre os produtos, fazendo com que a representação de um mesmo item varie conforme a página acessada.

## Resultado esperado

A imagem, o título, a descrição e o preço de cada produto devem permanecer coerentes entre a página **Products** e sua respectiva página de detalhes.

## Impacto

A inconsistência pode causar confusão e reduzir a confiança do usuário nas informações apresentadas, pois o produto visualizado na listagem pode parecer diferente quando seus detalhes são acessados. Isso pode afetar a avaliação do item e a decisão de compra.

## Evidência

[Vídeo — BUG-PRODUCT-PROBLEM_USER-005](https://drive.google.com/file/d/1EtUdP1Zpgu1m9yf_6-AYvR5gs-ZcPkh5/view?usp=sharing)

## Status

Aberto
