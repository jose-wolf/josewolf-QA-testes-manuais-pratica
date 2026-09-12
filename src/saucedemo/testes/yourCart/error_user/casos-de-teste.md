# TC-CART-ERROR_USER-001 — Validar exibição dos produtos no carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-001 — Validar os produtos exibidos

**Pré-condição:** Usuário autenticado com `error_user` na tela do carrinho (`/cart.html`) contendo itens adicionados.

**Passos:**
1. Acessar a página do carrinho de compras (`/cart.html`).
2. Verificar os produtos listados (*Sauce Labs Backpack*, *Sauce Labs Onesie* e *Sauce Labs Bike Light*).
3. Validar se a coluna **QTY** exibe `1` para cada item.
4. Validar se os nomes, descrições e preços unitários ( $29.99, $7.99 e $9.99) correspondem aos dados do catálogo.

**Resultado esperado:**  
Todos os itens selecionados devem ser renderizados com integridade, exibindo quantidade unitária correta, identificadores fiéis à vitrine e preços formatados.

**Status:** Passou

---

# TC-CART-ERROR_USER-002 — Validar botão de remover o produto

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-002 — Validar botão de remover o produto

**Pré-condição:** Usuário autenticado com `error_user` na tela do carrinho (`/cart.html`) contendo itens adicionados.

**Passos:**
1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Localizar um dos produtos da lista (ex.: *Sauce Labs Bike Light*).
3. Clicar no botão vermelho **Remove**.
4. Observar a atualização visual da listagem.

**Resultado esperado:**  
O card do produto selecionado deve desaparecer imediatamente da listagem, sem quebras de layout e mantendo os demais itens intactos.

**Status:** Passou

---

# TC-CART-ERROR_USER-003 — Validar botão de voltar para a página de produtos

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-003 — Validar botão de voltar para a página de produtos

**Pré-condição:** Usuário autenticado com `error_user` na tela do carrinho (`/cart.html`).

**Passos:**
1. Acessar a página do carrinho de compras (`/cart.html`).
2. Clicar no botão **Continue Shopping**.
3. Observar o redirecionamento e a integridade da vitrine.

**Resultado esperado:**  
O sistema deve redirecionar o navegador para `/inventory.html`, preservando o estado dos botões ("Remove") dos itens previamente adicionados.

**Status:** Passou

---

# TC-CART-ERROR_USER-004 — Validar contador do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-004 — Validar contador do carrinho

**Pré-condição:** Usuário autenticado com `error_user` na tela do carrinho com badge ativo.

**Passos:**
1. Observar o número inicial exibido no ícone do carrinho no cabeçalho.
2. Clicar no botão **Remove** de um dos produtos.
3. Verificar a atualização do contador no topo direito.

**Resultado esperado:**  
O badge deve decrementar seu valor numérico instantaneamente em sincronia com a remoção do item.

**Status:** Passou

---

# TC-CART-ERROR_USER-005 — Validar o botão "Checkout"

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-005 — Validar o botão "checkout"

**Pré-condição:** Usuário autenticado com `error_user` na tela do carrinho (`/cart.html`) contendo ao menos um item.

**Passos:**
1. Acessar a página do carrinho de compras (`/cart.html`).
2. Clicar no botão verde **Checkout**.
3. Observar a URL carregada e a renderização da tela subsequente.

**Resultado esperado:**  
O sistema deve redirecionar o usuário com sucesso para a rota `/checkout-step-one.html`, exibindo a tela "Checkout: Your Information".

**Status:** Passou