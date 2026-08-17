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

****

# TC-LOGIN-010 — Login com campos vazios

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-003 — Validação dos campos obrigatórios

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: campo vazio
* Password: campo vazio

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Manter o campo **Username** vazio.
3. Manter o campo **Password** vazio.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado e o sistema deve informar que o campo **Username** é obrigatório.

**Status: Passou**

---

# TC-LOGIN-011 — Login com username vazio e password válido

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-003 — Validação dos campos obrigatórios

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: campo vazio
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Manter o campo **Username** vazio.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado e o sistema deve informar que o campo **Username** é obrigatório.

**Status: Passou**

---

# TC-LOGIN-012 — Login com username válido e password vazio

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-003 — Validação dos campos obrigatórios

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `standard_user`
* Password: campo vazio

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `standard_user` no campo **Username**.
3. Manter o campo **Password** vazio.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado e o sistema deve informar que o campo **Password** é obrigatório.

**Status: Passou**

****

# TC-LOGIN-013 — Login com performance_glitch_user

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-005 — Autenticação de usuário com comportamento de performance

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `performance_glitch_user`
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `performance_glitch_user` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.
5. Aguardar o carregamento da página **Products**.

**Resultado esperado:**
O usuário deve ser autenticado com sucesso e redirecionado para a página **Products**.

**Status:** Passou

**Observação:**
Foi identificado um delay perceptível durante a autenticação e o carregamento da página **Products**. O usuário consegue acessar o sistema  após o atraso.

---

# TC-LOGIN-014 — Login com locked_out_user

**Funcionalidade:** Login
**Cenário relacionado:** CN-LOGIN-004 — Validação de acesso de usuário bloqueado

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

* Username: `locked_out_user`
* Password: `secret_sauce`

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar `locked_out_user` no campo **Username**.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.

**Resultado esperado:**
O usuário não deve ser autenticado, pois sua conta está bloqueada, e o sistema deve exibir uma mensagem informando que o acesso desse usuário está bloqueado.

**Status:** Passou

****

# TC-LOGIN-015 — Login com demais usuários válidos

**Funcionalidade:** Login  
**Cenário relacionado:** CN-LOGIN-001 — Autenticação com credenciais válidas

**Pré-condição:** Aplicação disponível e usuário não autenticado.

**Dados de teste:**

| Username | Password | Status |
|---|---|---|
| `problem_user` | `secret_sauce` | Passou |
| `error_user` | `secret_sauce` | Passou |
| `visual_user` | `secret_sauce` | Passou |

**Passos:**

1. Acessar `https://www.saucedemo.com/`.
2. Informar um dos usernames listados nos dados de teste.
3. Informar `secret_sauce` no campo **Password**.
4. Clicar no botão **Login**.
5. Repetir o teste para cada usuário listado.

**Resultado esperado:**  
Cada usuário deve ser autenticado com sucesso e redirecionado para a página **Products**.

**Status:** Passou