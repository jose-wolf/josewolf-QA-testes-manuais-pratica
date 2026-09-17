# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-001 — Validar exibição dos campos de identificação

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-001 - Validar os campos (FirstName, LastName e postal Code)  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Inspecionar a presença e o estado dos campos **First Name**, **Last Name** e **Zip/Postal Code**.

**Resultado esperado:**  
Os campos devem estar visíveis, desimpedidos e habilitados para digitação.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-002 — Validar persistência do contador no carrinho

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-002 - Validar contador no cart  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html` com itens no carrinho.

**Passos:**
1. Acessar a tela de checkout.
2. Inspecionar o badge vermelho no ícone do carrinho no canto superior direito.

**Resultado esperado:**  
O badge deve refletir a quantidade exata de itens adicionados.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-003 — Validar botão de cancel

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-003 - Validar botão de cancel  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Clicar no botão **Cancel**.
2. Observar o redirecionamento.

**Resultado esperado:**  
O usuário deve retornar à rota `/cart.html` preservando os itens da sessão.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-004 — Validar avanço com dados válidos

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-004 - Validar botão de continue  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html` com produtos no carrinho.

**Passos:**
1. Inserir dados válidos nos campos **First Name**, **Last Name** e **Zip/Postal Code**.
2. Clicar no botão verde **Continue**.
3. Acompanhar a transição e a latência de rede no console DevTools.

**Resultado esperado:**  
O sistema deve processar o formulário com tempo de resposta estável e redirecionar para `/checkout-step-two.html`.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-005 — Validar bloqueio com First Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-005 – Validar mensagem de erro ao submeter formulário com First Name em branco  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Deixar o campo **First Name** vazio e preencher os demais campos.
2. Clicar em **Continue**.

**Resultado esperado:**  
Exibição do banner de erro com a mensagem: `Error: First Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-006 — Validar bloqueio com Last Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-006 – Validar mensagem de erro ao submeter formulário com Last Name em branco  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Preencher **First Name** e **Zip/Postal Code**, deixando **Last Name** vazio.
2. Clicar em **Continue**.

**Resultado esperado:**  
Exibição do banner de erro com a mensagem: `Error: Last Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-007 — Validar bloqueio com Postal Code em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-007 – Validar mensagem de erro ao submeter formulário com Postal Code em branco  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Preencher **First Name** e **Last Name**, deixando **Zip/Postal Code** vazio.
2. Clicar em **Continue**.

**Resultado esperado:**  
Exibição do banner de erro com a mensagem: `Error: Postal Code is required`.

**Status:** Passou

---

# TC-CHECKOUT-PERFORMANCE_GLITCH_USER-008 — Validar bloqueio com todos os campos em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-008 - Validar mensagem de erro ao submeter formulário com os campos em branco  
**Pré-condição:** Usuário autenticado com `performance_glitch_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Manter todos os campos vazios.
2. Clicar em **Continue**.

**Resultado esperado:**  
Validação por precedência acionada, exibindo: `Error: First Name is required`.

**Status:** Passou