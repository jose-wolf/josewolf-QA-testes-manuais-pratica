# TC-CHECKOUT-VISUAL_USER-001 — Validar exibição dos campos de identificação

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-001 - Validar os campos (FirstName, LastName e postal Code)  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a rota `/checkout-step-one.html`.
2. Inspecionar a presença e os placeholders dos campos **First Name**, **Last Name** e **Zip/Postal Code**.

**Resultado esperado:**  
Os campos devem estar visíveis, desimpedidos e habilitados para digitação.

**Status:** Passou

---

# TC-CHECKOUT-VISUAL_USER-002 — Validar persistência do contador no carrinho

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-002 - Validar contador no cart  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html` com itens adicionados.

**Passos:**
1. Acessar a tela de checkout.
2. Inspecionar o badge numérico no cabeçalho superior direito.

**Resultado esperado:**  
O badge deve refletir a quantidade correta de itens e estar alinhado sobre o canto superior direito do ícone do carrinho.

**Resultado obtido:**  
O badge numérico computa o valor correto (2), porém é renderizado fora da sua posição de ancoragem, deslocado para fora do ícone do carrinho.

**Status:** Passou (Funcional) com apontamento de UI  
**Bug relacionado:** BUG-CHECKOUT-VISUAL_USER-001

---

# TC-CHECKOUT-VISUAL_USER-003 — Validar botão de cancel

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-003 - Validar botão de cancel  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Clicar no botão **Cancel**.
2. Verificar o redirecionamento.

**Resultado esperado:**  
Retorno à rota `/cart.html` preservando os produtos da sessão.

**Status:** Passou

---

# TC-CHECKOUT-VISUAL_USER-004 — Validar avanço com dados válidos

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-004 - Validar botão de continue  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html` com itens no carrinho.

**Passos:**
1. Inserir dados válidos nos três campos de cadastro.
2. Clicar no botão verde **Continue**.

**Resultado esperado:**  
Formulário processado e redirecionamento para `/checkout-step-two.html`.

**Status:** Passou

---

# TC-CHECKOUT-VISUAL_USER-005 — Validar bloqueio com First Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-005 – Validar mensagem de erro ao submeter formulário com First Name em branco  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Deixar o campo **First Name** em branco e preencher os demais campos.
2. Clicar no botão **Continue**.

**Resultado esperado:**  
Exibição do alerta: `Error: First Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-VISUAL_USER-006 — Validar bloqueio com Last Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-006 – Validar mensagem de erro ao submeter formulário com Last Name em branco  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Preencher **First Name** e **Zip/Postal Code**, deixando **Last Name** vazio.
2. Clicar no botão **Continue**.

**Resultado esperado:**  
Exibição do alerta: `Error: Last Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-VISUAL_USER-007 — Validar bloqueio com Postal Code em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-007 – Validar mensagem de erro ao submeter formulário com Postal Code em branco  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Preencher **First Name** e **Last Name**, deixando **Zip/Postal Code** vazio.
2. Clicar no botão **Continue**.

**Resultado esperado:**  
Exibição do alerta: `Error: Postal Code is required`.

**Status:** Passou

---

# TC-CHECKOUT-VISUAL_USER-008 — Validar bloqueio com todos os campos em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-008 - Validar mensagem de erro ao submeter formulário com os campos em branco  
**Pré-condição:** Usuário autenticado com `visual_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Manter todos os campos vazios.
2. Clicar no botão **Continue**.

**Resultado esperado:**  
Validação sequencial exibindo: `Error: First Name is required`.

**Status:** Passou