# TC-CHECKOUT-ERROR_USER-001 — Validar exibição dos campos de identificação

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-001 - Validar os campos (FirstName, LastName e postal Code)  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela de checkout (`/checkout-step-one.html`).
2. Inspecionar a interface e localizar os campos de entrada de dados.
3. Verificar a visibilidade e o estado dos campos **First Name**, **Last Name** e **Zip/Postal Code**.

**Resultado esperado:**  
Os três campos devem estar visíveis, habilitados para interação e com seus respectivos placeholders legíveis.

**Status:** Passou

---

# TC-CHECKOUT-ERROR_USER-002 — Validar persistência do contador no carrinho

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-002 - Validar contador no cart  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html` com itens adicionados ao carrinho.

**Passos:**
1. Acessar a tela de checkout.
2. Inspecionar o ícone do carrinho no cabeçalho superior direito.
3. Verificar o valor numérico exibido no badge vermelho.

**Resultado esperado:**  
O badge deve permanecer exibindo a quantidade correta de itens selecionados na sessão.

**Status:** Passou

---

# TC-CHECKOUT-ERROR_USER-003 — Validar botão de cancel

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-003 - Validar botão de cancel  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela de checkout (`/checkout-step-one.html`).
2. Clicar no botão branco **Cancel**.
3. Observar a URL e a tela de destino.

**Resultado esperado:**  
O sistema deve cancelar o preenchimento e redirecionar o usuário para `/cart.html`, preservando os itens da sessão.

**Status:** Passou

---

# TC-CHECKOUT-ERROR_USER-004 — Validar avanço com dados válidos

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-004 - Validar botão de continue  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html` com itens no carrinho.

**Passos:**
1. Preencher **First Name**, **Last Name** e **Zip/Postal Code** com dados válidos.
2. Clicar no botão verde **Continue**.
3. Observar o redirecionamento da página.

**Resultado esperado:**  
O formulário deve ser submetido com sucesso e a aplicação deve redirecionar para `/checkout-step-two.html`.

**Status:** Passou

---

# TC-CHECKOUT-ERROR_USER-005 — Validar bloqueio com First Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-005 – Validar mensagem de erro ao submeter formulário com First Name em branco  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Deixar o campo **First Name** completamente vazio.
2. Preencher **Last Name** e **Zip/Postal Code** com dados válidos.
3. Clicar no botão **Continue**.

**Resultado esperado:**  
O avanço deve ser impedido e a mensagem `Error: First Name is required` deve ser renderizada em um banner vermelho.

**Status:** Passou

---

# TC-CHECKOUT-ERROR_USER-006 — Validar bloqueio com Last Name em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-006 – Validar mensagem de erro ao submeter formulário com Last Name em branco  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Preencher o campo **First Name** com valor válido (ex.: `teste`).
2. Deixar o campo **Last Name** completamente vazio.
3. Preencher o campo **Zip/Postal Code** com valor válido (ex.: `10001-0005`).
4. Clicar no botão verde **Continue**.

**Resultado esperado:**  
O sistema deve barrar a submissão, mantendo o usuário na mesma página e exibindo o alerta: `Error: Last Name is required`.

**Resultado obtido:**  
O sistema ignora a ausência do campo obrigatório, não exibe nenhuma mensagem de erro e redireciona o usuário diretamente para a rota `/checkout-step-two.html`.

**Status:** Falhou  
**Bug relacionado:** BUG-CHECKOUT-ERROR_USER-001

---

# TC-CHECKOUT-ERROR_USER-007 — Validar bloqueio com Postal Code em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-007 – Validar mensagem de erro ao submeter formulário com Postal Code em branco  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Preencher os campos **First Name** e **Last Name** com dados válidos.
2. Deixar o campo **Zip/Postal Code** completamente vazio.
3. Clicar no botão **Continue**.

**Resultado esperado:**  
O formulário deve bloquear a transição de rota e exibir a mensagem de validação: `Error: Postal Code is required`.

**Status:** Passou

---

# TC-CHECKOUT-ERROR_USER-008 — Validar mensagem de erro ao submeter formulário com os campos em branco

**Funcionalidade:** Checkout: Your Information  
**Cenário relacionado:** CN-CHECKOUT-008 - Validar mensagem de erro ao submeter formulário com os campos em branco  
**Pré-condição:** Usuário autenticado com `error_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Assegurar que os três campos (**First Name**, **Last Name**, **Zip/Postal Code**) estejam vazios.
3. Clicar no botão **Continue**.

**Resultado esperado:**  
A validação de precedência do formulário deve ser acionada, impedindo o avanço e exibindo a notificação do primeiro campo ausente: `Error: First Name is required`.

**Status:** Passou