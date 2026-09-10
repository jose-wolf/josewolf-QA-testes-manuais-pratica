# BUG-PRODUCT-PERFORMANCE_GLITCH_USER-002 — Lentidão ao sair do detalhamento do produto

**Cenário relacionado:** CN-PRODUCT-005 — Validar acesso aos detalhes do produto

**Caso de teste relacionado:** TC-PRODUCT-PERFORMANCE_GLITCH_USER-005 — Validar acesso aos detalhes do produto

**Categoria:** Performance / Tempo de Resposta

**Severidade:** Média  
**Prioridade:** Média

**Ambiente:** Firefox 153.0.4 / Ubuntu 24.04.4

## Passos para reproduzir

1. Acessar `https://www.saucedemo.com/`.
2. Realizar login com as credenciais do usuário `performance_glitch_user`.
3. Na página de produtos (`/inventory.html`), abrir as ferramentas de desenvolvedor (`F12`) na aba **Rede** (*Network*).
4. Clicar no título ou na imagem de qualquer item (ex.: *Sauce Labs Backpack*).
5. Observar o tempo de transição até a renderização completa da página individual (`/inventory-item.html`).

## Resultado obtido

O sistema apresenta um atraso de aproximadamente 5 segundos para realizar a transição e exibir a página de detalhes do produto selecionado, retendo a requisição antes de renderizar os elementos da interface.

## Resultado esperado

A navegação para a página de detalhes deve ocorrer em até 1 a 2 segundos [source: 1], garantindo agilidade na visualização das informações do produto.

## Impacto

Prejudica a navegação no catálogo. A demora ao clicar para ver mais detalhes sobre um produto causa frustração e interrompe o fluxo natural de compras do usuário.

## Evidência

[BUG-PRODUCT-PERFORMANCE_GLITCH_USER-002](https://drive.google.com/file/d/12fnYYeauPcdfbJ0wiSGdo6nIOcx3foH0/view?usp=sharing)

## Status

Aberto