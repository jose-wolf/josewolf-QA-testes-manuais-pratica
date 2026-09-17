# TC-CHECKOUT-STANDARD_USER-001 — Validar exibição dos campos de identificação

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-001 - Validar os campos (FirstName, LastName e postal Code)

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela de checkout (`/checkout-step-one.html`).
2. Inspecionar a interface e localizar as entradas de dados.
3. Verificar a presença dos campos de texto **First Name**, **Last Name** e **Zip/Postal Code**.
4. Validar se os placeholders descritivos são renderizados corretamente em cada campo.

**Resultado esperado:**  
Os três campos devem estar visíveis, desimpedidos, habilitados para edição e com seus respectivos textos de placeholder legíveis.

**Status:** Passou

---

# TC-CHECKOUT-STANDARD_USER-002 — Validar persistência do contador do carrinho

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-002 - Validar contador no cart

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html` com itens previamente adicionados.

**Passos:**
1. Adicionar produtos ao carrinho na vitrine (ex.: 2 itens) e prosseguir para o checkout.
2. Na rota `/checkout-step-one.html`, inspecionar o ícone do carrinho no cabeçalho superior direito.
3. Conferir o número exibido no badge numérico vermelho.

**Resultado esperado:**  
O badge deve permanecer visível e sincronizado, exibindo o número exato de itens contidos no carrinho durante toda a permanência na tela.

**Status:** Passou

---

# TC-CHECKOUT-STANDARD_USER-003 — Validar cancelamento e retorno ao carrinho

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-003 - Validar botão de cancel

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela de checkout (`/checkout-step-one.html`).
2. Localizar o botão branco **Cancel** no canto inferior esquerdo.
3. Clicar no botão **Cancel**.
4. Observar o redirecionamento e os dados da página carregada.

**Resultado esperado:**  
O sistema deve cancelar o fluxo de compra e redirecionar o usuário para `/cart.html`, preservando todos os produtos e quantidades no carrinho.

**Status:** Passou

---

# TC-CHECKOUT-STANDARD_USER-004 — Validar avanço com dados válidos

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-004 - Validar botão de continue

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html` com itens adicionados ao carrinho.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Inserir um nome válido no campo **First Name** (ex.: `José`).
3. Inserir um sobrenome válido no campo **Last Name** (ex.: `Silva`).
4. Inserir um código postal válido no campo **Zip/Postal Code** (ex.: `87000-000`).
5. Clicar no botão verde **Continue**.

**Resultado esperado:**  
O sistema deve aceitar os dados cadastrais e redirecionar o navegador para a visão geral do pedido na rota `/checkout-step-two.html`.

**Status:** Passou

> **Observação:** O formulário não valida tipo de dados nem limita caracteres: os campos *First Name* e *Last Name* aceitam entradas exclusivamente numéricas, e o campo *Zip/Postal Code* aceita strings e não tem limite mínimo de caracteres. Em produção, isso representa risco de quebra de contrato com APIs de frete e motores antifraude.

---

# TC-CHECKOUT-STANDARD_USER-005 — Validar bloqueio com First Name em branco

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-005 – Validar mensagem de erro ao submeter formulário com First Name em branco

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Deixar o campo **First Name** completamente vazio.
3. Preencher o campo **Last Name** com valor válido (ex.: `Silva`).
4. Preencher o campo **Zip/Postal Code** com valor válido (ex.: `87000-000`).
5. Clicar no botão **Continue**.

**Resultado esperado:**  
O avanço deve ser bloqueado, mantendo o usuário na rota `/checkout-step-one.html` com a exibição do banner vermelho contendo a mensagem: `Error: First Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-STANDARD_USER-006 — Validar bloqueio com Last Name em branco

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-006 – Validar mensagem de erro ao submeter formulário com Last Name em branco

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Preencher o campo **First Name** com valor válido (ex.: `José`).
3. Deixar o campo **Last Name** completamente vazio.
4. Preencher o campo **Zip/Postal Code** com valor válido (ex.: `87000-000`).
5. Clicar no botão **Continue**.

**Resultado esperado:**  
O avanço deve ser bloqueado e o sistema deve exibir a mensagem de erro: `Error: Last Name is required`.

**Status:** Passou

---

# TC-CHECKOUT-STANDARD_USER-007 — Validar bloqueio com Postal Code em branco

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-007 – Validar mensagem de erro ao submeter formulário com Postal Code em branco

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Preencher o campo **First Name** com valor válido (ex.: `José`).
3. Preencher o campo **Last Name** com valor válido (ex.: `Silva`).
4. Deixar o campo **Zip/Postal Code** completamente vazio.
5. Clicar no botão **Continue**.

**Resultado esperado:**  
O avanço deve ser bloqueado e o sistema deve exibir a mensagem de erro: `Error: Postal Code is required`.

**Status:** Passou

---

# TC-CHECKOUT-STANDARD_USER-008 — Validar mensagem de erro ao submeter formulário com todos os campos em branco

**Funcionalidade:** Checkout: Your Information

**Cenário relacionado:** CN-CHECKOUT-008 - Validar mensagem de erro ao submeter formulário com os campos em branco

**Pré-condição:** Usuário autenticado com `standard_user` na tela `/checkout-step-one.html`.

**Passos:**
1. Acessar a tela `/checkout-step-one.html`.
2. Assegurar que os três campos (**First Name**, **Last Name**, **Zip/Postal Code**) estejam vazios.
3. Clicar no botão **Continue**.

**Resultado esperado:**  
O sistema deve impedir a transição de rota e acionar a validação de precedência do primeiro campo da árvore DOM, exibindo a mensagem: `Error: First Name is required`.

**Status:** Passou