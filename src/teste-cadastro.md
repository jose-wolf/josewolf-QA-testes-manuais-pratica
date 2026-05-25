# Validando tela de Login

* **ID**: TC-001
* **Título**: Login com credenciais válidas.
* **Pré-condição**: Usuário cadastrado com o username "standard_user" e senha "secret_sauce" 
* **Passos**:
  * Acessar https://www.saucedemo.com/
  * Inserir um username validado
  * Iserir um password validado
  * Clicar em "Login"
*  **Resultado esperado**: O usuários deve ser redirecionado para o site de produtos
* **Status**: Passou

***

* **ID**: TC-002
* **Título**: Login com username inválido.
* **Pré-condição**: Usuário não cadastrado com o username "standard_user1" e senha "secret_sauce"
* **Passos**:
    * Acessar https://www.saucedemo.com/
    * Inserir um username inválido
    * Iserir um password validado
    * Clicar em "Login"
*  **Resultado esperado**: O usuários não deve ser redirecionado para o site de produtos. E uma mensagem
deve ser mostrada.
* **Status**: Passou

***

* **ID**: TC-003
* **Título**: Login com senha inválida.
* **Pré-condição**: Usuário não cadastrado com o username "standard_user" e senha "secret_sauce1"
* **Passos**:
    * Acessar https://www.saucedemo.com/
    * Inserir um username válido
    * Iserir um password inválido
    * Clicar em "Login"
*  **Resultado esperado**: O usuários não deve ser redirecionado para o site de produtos. E uma mensagem
   deve ser mostrada.
* **Status**: Passou

***

* **ID**: TC-004
* **Título**: Login sem campo preenchido.
* **Pré-condição**: Usuário não preencheu os campos username e password.
* **Passos**:
    * Acessar https://www.saucedemo.com/
    * Username não preenchido
    * Password não preenchido
    * Clicar em "Login"
*  **Resultado esperado**: O usuários não deve ser redirecionado para o site de produtos. E uma mensagem
   deve ser mostrada.
* **Status**: Passou