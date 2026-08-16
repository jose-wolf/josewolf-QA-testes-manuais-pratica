# TC-LOGIN-001 — Login com credenciais válidas

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-001 — Autenticação com credenciais válidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user`
* Password: `secret_sauce`

**Passos:**

1. Acessar: https://www.saucedemo.com/.
2. Informar `standard_user` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário deve ser autenticado com sucesso e redirecionado para a página **Products**.


**Status:**
Passou
****

# TC-LOGIN-002 — Login com username inválido

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `invalid_user`
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `invalid_user` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado e o sistema deve exibir uma mensagem informando que o username e a senha não correspondem a um usuário válido.

**Status: Passou**

**Bug relacionado:** BUG-LOGIN-001 - bug de UI

---

# TC-LOGIN-003 — Login com password inválido

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user`
* Password: `invalid_password`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_user` no campo **Username**.
3. Informar `invalid_password` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado e o sistema deve exibir uma mensagem informando que o username e a senha não correspondem a um usuário válido.

**Status: Passou**

---

# TC-LOGIN-004 — Login com username em uppercase

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `STANDARD_USER`
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `STANDARD_USER` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois o username informado difere do username válido, e o sistema deve exibir uma mensagem de credenciais inválidas.

**Status: Passou**

---

# TC-LOGIN-005 — Login com password em uppercase

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user`
* Password: `SECRET_SAUCE`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_user` no campo **Username**.
3. Informar `SECRET_SAUCE` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois a senha informada difere da senha válida, e o sistema deve exibir uma mensagem de credenciais inválidas.

**Status: Passou**

---

# TC-LOGIN-006 — Login com caractere a mais no username

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user1`
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_user1` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois o username informado contém um caractere adicional, e o sistema deve exibir uma mensagem de credenciais inválidas.

**Status: Passou**

---

# TC-LOGIN-007 — Login com caractere especial a mais no password

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user`
* Password: `secret_sauce!`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_user` no campo **Username**.
3. Informar `secret_sauce!` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois a senha informada contém um caractere especial adicional, e o sistema deve exibir uma mensagem de credenciais inválidas.

**Status: Passou**

---

# TC-LOGIN-008 — Login com caractere a menos no username

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_use`
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_use` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois o username informado está incompleto, e o sistema deve exibir uma mensagem de credenciais inválidas.

**Status: Passou**

---

# TC-LOGIN-009 — Login com caractere a menos no password

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-002 — Autenticação com credenciais inválidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user`
* Password: `secret_sauc`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_user` no campo **Username**.
3. Informar `secret_sauc` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois a senha informada está incompleta, e o sistema deve exibir uma mensagem de credenciais inválidas.

**Status: Passou**

