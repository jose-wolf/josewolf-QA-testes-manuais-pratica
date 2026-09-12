# TC-CART-PROBLEM_USER-001 — Validar exibição dos produtos no carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-001 — Validar exibição dos produtos no carrinho

**Pré-condição:** Usuário autenticado com `problem_user` na tela do carrinho (`/cart.html`) com itens adicionados.

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Verificar os itens listados (*Sauce Labs Backpack*, *Sauce Labs Bike Light* e *Sauce Labs Onesie*).
3. Validar se a coluna **QTY** indica `1` para cada item.
4. Validar se os nomes, descrições e valores unitários ($29.99, $9.99 e $7.99) correspondem aos dados do catálogo.

**Resultado esperado:**  
Todos os itens selecionados devem ser renderizados corretamente com suas respectivas descrições, quantidades unitárias e valores monetários preservados.

**Status:** Passou

---

# TC-CART-PROBLEM_USER-002 — Validar remoção de produtos através do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-002 — Validar remoção de produtos através do carrinho

**Pré-condição:** Usuário autenticado com `problem_user` na tela do carrinho (`/cart.html`) contendo múltiplos itens.

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Localizar o item *Sauce Labs Onesie*.
3. Clicar no botão vermelho **Remove** correspondente ao item.
4. Observar a atualização da listagem de itens.

**Resultado esperado:**  
O card do produto selecionado deve ser excluído da visualização imediatamente, mantendo a integridade visual e a listagem dos produtos restantes (*Backpack* e *Bike Light*).

**Status:** Passou

---

# TC-CART-PROBLEM_USER-003 — Validar navegação de retorno às compras

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-003 — Validar navegação de retorno às compras

**Pré-condição:** Usuário autenticado com `problem_user` na tela do carrinho (`/cart.html`).

**Passos:**

1. Acessar a tela do carrinho de compras (`/cart.html`).
2. Clicar no botão **Continue Shopping**.
3. Observar a rota carregada e a persistência dos produtos.

**Resultado esperado:**  
O sistema deve redirecionar o usuário para a vitrine de produtos (`/inventory.html`), preservando os itens previamente adicionados com o rótulo "Remove" e mantendo o badge do carrinho sincronizado com o total de itens restantes (2).

**Status:** Passou

---
# TC-CART-PROBLEM_USER-004 — Validar sincronização do contador do carrinho

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-004 — Validar sincronização do contador do carrinho

**Pré-condição:** Usuário autenticado com `problem_user` na tela do carrinho (`/cart.html`) com o badge indicando 3 itens.

**Passos:**

1. Observar o número indicado no badge do ícone do carrinho no cabeçalho (valor inicial: 3).
2. Acionar a exclusão de um produto através do botão **Remove**.
3. Observar a atualização imediata do valor numérico no badge.

**Resultado esperado:**  
O badge deve decrementar de forma instantânea e sincronizada com a remoção do item, reduzindo a contagem exibida de 3 para 2.

**Status:** Passou

---

# TC-CART-PROBLEM_USER-005 — Validar o botão "Checkout"

**Funcionalidade:** Cart

**Cenário relacionado:** CN-CART-005 — Validar o botão "Checkout"

**Pré-condição:** Usuário autenticado com `problem_user` na tela do carrinho (`/cart.html`) contendo ao menos um item.

**Passos:**

1. Acessar a página do carrinho de compras (`/cart.html`).
2. Clicar no botão verde **Checkout**.
3. Observar a rota carregada e a renderização da tela subsequente.

**Resultado esperado:**  
O sistema deve redirecionar o usuário com sucesso para a rota `/checkout-step-one.html`, exibindo o formulário "Checkout: Your Information".

**Status:** Passou