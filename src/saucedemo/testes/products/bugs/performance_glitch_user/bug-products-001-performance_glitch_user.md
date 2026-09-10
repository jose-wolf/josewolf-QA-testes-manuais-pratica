# BUG-PRODUCT-PERFORMANCE_GLITCH_USER-001 — Lentidão excessiva ao alterar a ordenação dos produtos

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Caso de teste relacionado:** TC-PRODUCT-PERFORMANCE_GLITCH_USER-003 — Validar ordenação dos produtos

**Categoria:** Performance / Tempo de Resposta

**Severidade:** Média  
**Prioridade:** Média

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com o usuário `performance_glitch_user`.
3. Abrir as ferramentas de desenvolvedor (`F12`) na aba **Rede** (*Network*).
4. Na página de produtos (`/inventory.html`), clicar no menu suspenso de ordenação.
5. Selecionar qualquer opção de ordenação diferente da padrão (ex.: *Price (low to high)*).

## Resultado obtido

O sistema apresenta um atraso de resposta perceptível de aproximadamente 5 segundos para reordenar a listagem na tela, retendo as requisições no navegador antes da nova renderização dos itens.

## Resultado esperado

A reordenação da lista de produtos deve ocorrer de forma imediata (em menos de 1 segundo), visto que se trata de uma manipulação de elementos da interface.

## Impacto

Prejudica a navegabilidade e fluidez da loja. A espera excessiva ao aplicar filtros pode levar o cliente a crer que o filtro falhou ou que a página travou.

## Evidência

![BUG-PRODUCT-PERFORMANCE_GLITCH_USER-001](../../evidencias/products/bug-producd-001-performance_glitch_user.jpg)

## Status

Aberto