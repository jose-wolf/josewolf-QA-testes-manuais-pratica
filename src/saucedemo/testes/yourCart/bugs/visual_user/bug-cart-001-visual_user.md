# BUG-CART-VISUAL_USER-001 — Divergência de preços unitários entre vitrine e carrinho de compras

**Cenário relacionado:** CN-CART-001 — Validar os produtos exibidos  
**Caso de teste relacionado:** TC-CART-VISUAL_USER-001  
**Categoria:** Integridade de Dados / Negócio  
**Severidade:** Alta  
**Prioridade:** Alta  
**Ambiente:** Firefox 155 / Ubuntu 24.04

### Passos para reproduzir:
1. Acessar https://www.saucedemo.com/
2. Autenticar com o usuário `visual_user`.
3. Na vitrine (`/inventory.html`), verificar o preço da *Sauce Labs Backpack* ($66.44) e clicar em *Add to cart*.
4. Clicar no ícone do carrinho no cabeçalho superior direito.
5. Inspecionar o valor unitário da *Sauce Labs Backpack* na listagem de `/cart.html`.

### Resultado obtido:
O carrinho renderiza o item com valor unitário de $29.99, divergindo dos $66.44 anunciados na vitrine.

### Resultado esperado:
O carrinho deve manter paridade estrita com o valor anunciado na vitrine ($66.44) ou a vitrine deve apresentar os valores nominais padrão ($29.99) de ponta a ponta.

### Impacto:
Dano financeiro direto e quebra de conformidade jurídica com órgãos de proteção ao consumidor devido à cobrança divergente do preço ofertado ao usuário.

### Evidência:
[Evidência em Vídeo](https://drive.google.com/file/d/1Yp3uIGuQVBFT3lAZu1lCRQQtetq7kYXU/view?usp=sharing)

### Status:
Aberto