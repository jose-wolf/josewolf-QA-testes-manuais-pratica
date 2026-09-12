# TC-CART-PERFORMANCE_GLITCH_USER-001 — Validar exibição dos produtos no carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-001 — Validar exibição dos produtos no carrinho

**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela do carrinho (`/cart.html`) contendo itens adicionados.

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Verificar os produtos listados (*Sauce Labs Backpack* e *Sauce Labs Bike Light*).
3. Validar se a coluna **QTY** registra `1` para cada produto.
4. Comparar títulos, descrições e valores unitários com os dados originais da vitrine.

**Resultado esperado:**  
Os produtos selecionados devem ser renderizados com integridade, exibindo quantidade unitária correta, descrições consistentes e preços formatados.

**Status:** Passou

---

# TC-CART-PERFORMANCE_GLITCH_USER-002 — Validar remoção de produtos através do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-002 — Validar remoção de produtos através do carrinho

**Pré-condição:** Usuário autenticado com `performance_glitch_user` na página do carrinho (`/cart.html`) contendo ao menos dois itens.

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Localizar um dos produtos listados (ex.: *Sauce Labs Bike Light*).
3. Clicar no botão vermelho **Remove**.
4. Observar a atualização da listagem e a fluidez da resposta.

**Resultado esperado:**  
O card do produto deve ser removido imediatamente do DOM, sem retenções ou travamentos de interface (*freezes*), preservando os itens restantes.

**Status:** Passou

---

# TC-CART-PERFORMANCE_GLITCH_USER-003 — Validar navegação de retorno às compras

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-003 — Validar navegação de retorno às compras

**Pré-condição:** Usuário autenticado com `performance_glitch_user` na página do carrinho (`/cart.html`).

**Passos:**

1. Acessar a tela do carrinho (`/cart.html`).
2. Abrir o DevTools (`F12`) na aba **Rede**.
3. Clicar no botão **Continue Shopping**.
4. Monitorar o tempo de resposta e o redirecionamento.

**Resultado esperado:**  
O sistema deve redirecionar para `/inventory.html` , preservando os itens e o estado do carrinho.

**Resultado obtido:**  
O redirecionamento ocorreu funcionalmente, porém a requisição de rota levou 8,45 segundos para ser concluída (SLA violado).

**Status:** Passou com observação
**Bug relacionado:** BUG-CART-PERFORMANCE_GLITCH_USER-001

---

# TC-CART-PERFORMANCE_GLITCH_USER-004 — Validar sincronização do contador do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-004 — Validar sincronização do contador do carrinho

**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela do carrinho com badge ativo.

**Passos:**

1. Verificar o valor numérico inicial do badge no ícone do carrinho no cabeçalho.
2. Clicar no botão **Remove** de um dos itens.
3. Observar a atualização do badge numérico.

**Resultado esperado:**  
O contador deve decrementar imediatamente de forma síncrona com a exclusão do produto, refletindo a nova quantidade sem atraso.

**Status:** Passou

---

# TC-CART-PERFORMANCE_GLITCH_USER-005 — Validar redirecionamento para o fluxo de checkout

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-005 — Validar redirecionamento para o fluxo de checkout

**Pré-condição:** Usuário autenticado com `performance_glitch_user` na página do carrinho (`/cart.html`) contendo ao menos um produto.

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Clicar no botão verde **Checkout**.
3. Observar a resposta da interface e o redirecionamento de tela.

**Resultado esperado:**  
O sistema deve redirecionar com sucesso para a rota `/checkout-step-one.html`, exibindo a etapa "Checkout: Your Information" com os campos de entrada cadastrais disponíveis para preenchimento.

**Status:** Passou