# TC-CHECKOUT-PROBLEM_USER-001 — Validar exibição dos campos de identificação

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-001 - Validar os campos (FirstName, LastName e postal Code)  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela de checkout (`/checkout-step-one.html`).
2. Inspecionar a interface e localizar as entradas de dados.
3. Verificar a presença visual dos campos **First Name**, **Last Name** e **Zip/Postal Code**.

**Resultado esperado:**  
Os três campos devem estar renderizados na tela e visíveis ao usuário.

**Status:** Passou

---

# TC-CHECKOUT-PROBLEM_USER-002 — Validar persistência do contador do carrinho

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-002 - Validar contador no cart  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html` com itens no carrinho.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Observar o badge vermelho do carrinho no cabeçalho superior direito.

**Resultado esperado:**  
O badge deve permanecer exibindo a quantidade correta de itens selecionados.

**Status:** Passou

---

# TC-CHECKOUT-PROBLEM_USER-003 — Validar cancelamento e retorno ao carrinho

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-003 - Validar botão de cancel  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Clicar no botão **Cancel**.
3. Observar a URL e a tela de destino.

**Resultado esperado:**  
O usuário deve ser redirecionado de volta para `/cart.html`.

**Status:** Passou

---

# TC-CHECKOUT-PROBLEM_USER-004 — Validar avanço com dados válidos

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-004 - Validar botão de continue  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html` com itens no carrinho.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Digitar `teste` no campo **First Name**.
3. Tentar digitar no campo **Last Name**.
4. Inserir código postal no campo **Zip/Postal Code**.
5. Clicar no botão **Continue**.

**Resultado esperado:**  
O formulário deve aceitar o preenchimento de todos os campos e redirecionar para `/checkout-step-two.html`.

**Resultado obtido:**  
O campo **Last Name** rejeita qualquer inserção de texto pelo teclado, permanecendo em branco. Ao clicar em **Continue**, o sistema exibe a mensagem de validação `Error: Last Name is required`, impedindo o avanço.

**Status:** Bloqueado
**Bug relacionado:** BUG-CHECKOUT-PROBLEM_USER-001

---

# TC-CHECKOUT-PROBLEM_USER-005 — Validar bloqueio com First Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-005 – Validar mensagem de erro ao submeter formulário com First Name em branco  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Deixar o campo **First Name** em branco.
3. Preencher o campo **Zip/Postal Code**.
4. Clicar no botão **Continue**.

**Resultado esperado:**  
O avanço deve ser bloqueado com a mensagem: `Error: First Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-PROBLEM_USER-006 — Validar bloqueio com Last Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-006 – Validar mensagem de erro ao submeter formulário com Last Name em branco  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Preencher o campo **First Name**.
3. Deixar o campo **Last Name** vazio (ou tentar digitar sem sucesso).
4. Preencher o campo **Zip/Postal Code**.
5. Clicar no botão **Continue**.

**Resultado esperado:**  
O sistema deve acusar a ausência do sobrenome exibindo: `Error: Last Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-PROBLEM_USER-007 — Validar bloqueio com Postal Code em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-007 – Validar mensagem de erro ao submeter formulário com Postal Code em branco  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Preencher o campo **First Name**.
3. Tentar preencher o campo **Last Name**.
4. Deixar o campo **Zip/Postal Code** vazio.
5. Clicar em **Continue**.

**Resultado esperado:**  
Com *First Name* e *Last Name* preenchidos e *Postal Code* vazio, o sistema deve exibir: `Error: Postal Code is required`.

**Resultado obtido:**  
Não foi possível executar o cenário de forma isolada, pois o campo **Last Name** não aceita entrada de dados, forçando a precedência do erro `Error: Last Name is required`.

**Status:** Bloqueado  
**Bug impeditivo:** BUG-CHECKOUT-PROBLEM_USER-001

---

# TC-CHECKOUT-PROBLEM_USER-008 — Validar bloqueio com todos os campos em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-008 - Validar mensagem de erro ao submeter formulário com os campos em branco  
**Pré-condição:** Usuário autenticado com `problem_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Manter todos os campos vazios.
2. Clicar no botão **Continue**.

**Resultado esperado:**  
O sistema deve validar sequencialmente o primeiro campo ausente e exibir: `Error: First Name is required`.

**Status:** Passou