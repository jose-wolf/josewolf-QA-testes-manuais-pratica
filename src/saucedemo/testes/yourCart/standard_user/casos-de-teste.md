# TC-CART-STANDARD_USER-001 — Validar exibição dos produtos no carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-001 — Validar exibição dos produtos no carrinho

**Pré-condição:** Usuário autenticado com `standard_user`, produtos adicionados e tela do carrinho (`/cart.html`) aberta.

**Passos:**

1. Acessar a página do carrinho de compras.
2. Verificar os itens listados na tabela de pedidos (*Sauce Labs Backpack* e *Test.allTheThings() T-Shirt (Red)*).
3. Validar se a coluna **QTY** indica `1` para cada registro.
4. Validar se o nome, a descrição e o preço unitário de cada item correspondem com precisão aos dados apresentados na vitrine de produtos.

**Resultado esperado:**  
Todos os itens selecionados devem ser renderizados com integridade, exibindo quantidade unitária correta, identificadores fiéis ao catálogo e preços formatados ($29.99 e $15.99).

**Status:** Passou

----

# TC-CART-STANDARD_USER-002 — Validar remoção de produtos através do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-002 — Validar remoção de produtos através do carrinho

**Pré-condição:** Usuário autenticado com `standard_user` na página do carrinho (`/cart.html`) contendo ao menos dois itens adicionados.

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Localizar o item *Test.allTheThings() T-Shirt (Red)*.
3. Clicar no botão **Remove** correspondente ao item.
4. Observar a atualização visual da listagem de itens.

**Resultado esperado:**  
O card do produto selecionado deve desaparecer imediatamente da listagem, sem deixar espaços em branco ou desalinhar a interface, mantendo inalterados os demais produtos presentes no carrinho.

**Status:** Passou

----

# TC-CART-STANDARD_USER-003 — Validar navegação de retorno às compras

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-003 — Validar navegação de retorno às compras

**Pré-condição:** Usuário autenticado com `standard_user` na tela do carrinho (`/cart.html`).

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Clicar no botão **Continue Shopping**.
3. Observar a URL carregada e o estado dos produtos listados.

**Resultado esperado:**  
O sistema deve redirecionar o usuário para a vitrine de produtos (`/inventory.html`), mantendo os botões de itens previamente adicionados com o rótulo "Remove" e o badge do carrinho sincronizado.

**Status:** Passou

---

# TC-CART-STANDARD_USER-004 — Validar sincronização do contador do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-004 — Validar sincronização do contador do carrinho

**Pré-condição:** Usuário autenticado com `standard_user` na tela do carrinho (`/cart.html`) contendo ao menos um produto.

**Passos:**

1. Observar o valor numérico exibido no badge do ícone do carrinho no cabeçalho.
2. Clicar no botão **Remove** de um dos produtos.
3. Observar a atualização imediata do badge numérico.

**Resultado esperado:**  
O badge deve decrementar seu valor numérico em sincronia imediata com a exclusão do produto. Caso o carrinho fique vazio, o indicador visual numérico deve desaparecer por completo.

**Status:** Passou

----

# TC-CART-STANDARD_USER-005 — Validar redirecionamento para o fluxo de checkout

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-005 — Validar redirecionamento para o fluxo de checkout

**Pré-condição:** Usuário autenticado com `standard_user` na página do carrinho (`/cart.html`) contendo itens adicionados.

**Passos:**

1. Acessar a página do carrinho de compras (`/cart.html`).
2. Clicar no botão verde **Checkout**.
3. Observar a URL carregada e a renderização da tela subsequente.

**Resultado esperado:**  
O sistema deve redirecionar o usuário com sucesso para a rota `/checkout-step-one.html`, exibindo a tela "Checkout: Your Information" com os campos de entrada (*First Name*, *Last Name* e *Zip/Postal Code*) visíveis e editáveis.

**Status:** Passou