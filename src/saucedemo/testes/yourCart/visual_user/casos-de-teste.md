# TC-CART-VISUAL_USER-001 — Validar exibição dos produtos no carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-001 — Validar os produtos exibidos

**Pré-condição:** Usuário autenticado com `visual_user` na tela do catálogo (`/inventory.html`).

**Passos:**
1. Acessar a vitrine de produtos (`/inventory.html`).
2. Adicionar ao carrinho os itens *Sauce Labs Backpack* ($66.44), *Sauce Labs Bike Light* ($57.15) e *Sauce Labs Onesie* ($66.36).
3. Acessar a tela do carrinho clicando no ícone superior direito (`/cart.html`).
4. Confrontar os dados cadastrais e valores unitários renderizados com os valores visualizados na vitrine.

**Resultado esperado:**  
Os produtos listados no carrinho devem refletir com precisão os dados cadastrais e os respectivos valores monetários visualizados e confirmados na vitrine.

**Resultado obtido:**  
Os produtos são renderizados, porém com valores divergentes dos informados na vitrine: a *Backpack* passou de $66.44 para $29.99, a *Bike Light* de $57.15 para $9.99, e o *Onesie* de $66.36 para $7.99.

**Status:** Falhou  
**Bug relacionado:** BUG-CART-VISUAL_USER-001

---

# TC-CART-VISUAL_USER-002 — Validar botão de remover o produto

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-002 — Validar botão de remover o produto

**Pré-condição:** Usuário autenticado com `visual_user` na tela do carrinho (`/cart.html`) com múltiplos produtos adicionados.

**Passos:**
1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Localizar um dos produtos adicionados (ex.: *Sauce Labs Onesie*).
3. Clicar no botão vermelho **Remove**.
4. Observar a atualização visual da listagem de produtos.

**Resultado esperado:**  
O card do produto selecionado deve desaparecer imediatamente da listagem, mantendo os produtos restantes inalterados e a interface estável.

**Status:** Passou

---

# TC-CART-VISUAL_USER-003 — Validar botão de voltar para a página de produtos

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-003 — Validar botão de voltar para a página de produtos

**Pré-condição:** Usuário autenticado com `visual_user` na tela do carrinho (`/cart.html`).

**Passos:**
1. Acessar a página do carrinho de compras (`/cart.html`).
2. Clicar no botão cinza **Continue Shopping** no canto inferior esquerdo.
3. Observar a URL e os elementos carregados na tela.

**Resultado esperado:**  
O sistema deve redirecionar o navegador para `/inventory.html`, preservando o catálogo de produtos e os itens previamente salvos na sessão.

**Status:** Passou

---

# TC-CART-VISUAL_USER-004 — Validar sincronização do contador do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-004 — Validar contador do carrinho

**Pré-condição:** Usuário autenticado com `visual_user` na tela do carrinho (`/cart.html`) com múltiplos itens adicionados.

**Passos:**
1. Observar o número inicial exibido no badge do carrinho no topo direito da tela.
2. Clicar no botão vermelho **Remove** de um dos produtos.
3. Observar a atualização visual do contador no cabeçalho.

**Resultado esperado:**  
O badge deve decrementar seu valor numérico imediatamente em sincronia com a exclusão do produto, atualizando a contagem restante.

**Status:** Passou

---

# TC-CART-VISUAL_USER-005 — Validar o botão "Checkout"

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-005 — Validar o botão "checkout"

**Pré-condição:** Usuário autenticado com `visual_user` na tela do carrinho (`/cart.html`) contendo itens adicionados.

**Passos:**
1. Acessar a página do carrinho de compras (`/cart.html`).
2. Localizar o botão verde **Checkout** (posicionado de forma anômala no topo superior direito).
3. Clicar no botão **Checkout**.
4. Observar o redirecionamento e a integridade da navegação.

**Resultado esperado:**  
O sistema deve redirecionar o usuário com sucesso para a rota `/checkout-step-one.html`, mantendo o botão em conformidade com o design system no rodapé da página.

**Resultado obtido:**  
O redirecionamento funcional para `/checkout-step-one.html` ocorre com sucesso, porém o botão apresenta grave anomalia de layout, renderizado no topo da página acima do cabeçalho.

**Status:** Passou com observação  
**Bug relacionado:** BUG-CART-VISUAL_USER-002