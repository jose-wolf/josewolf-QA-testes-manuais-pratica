# Test Case - Login 
| Campo               | Descrição                                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Requisito Funcional | RF-01 – Funcionalidade Login                                                                                                                                  |
| Tipo de Teste       | Funcional                                                                                                                                                    |
| Subtipo de Teste    | Teste de Aceitação                                                                                                                                           |
| Objetivo do Teste   | Validar que a tela de login autentica corretamente o usuário `standard_user` e exibe mensagens de erro apropriadas em cenários de credenciais inválidas ou campos obrigatórios não preenchidos |
| Pré-condição        | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                            |
| Dados de Teste      | Username: `standard_user` \| Password: `secret_sauce`                                                                                                        |

---

## Casos de Teste

| Campo              | Descrição                                                                                                                                                                                     |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-LOGIN-001                                                                                                                                                                                  |
| Título             | Login com credenciais válidas                                                                                                                                                                 |
| Pré-condição       | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                                                            |
| Dados de Teste     | Username: `standard_user` \| Password: `secret_sauce`                                                                                                                                        |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Preencher o campo **Username** com `standard_user` <br> 3. Preencher o campo **Password** com `secret_sauce` <br> 4. Clicar em **Login**      |
| Resultado Esperado | O sistema deve autenticar o usuário e redirecionar para a tela **Products**, exibindo a lista de produtos disponíveis                                                                         |
| Status             | Passou                                                                                                                                                                                        |

---

| Campo              | Descrição                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-LOGIN-002                                                                                                                                                                                                     |
| Título             | Login com username inválido                                                                                                                                                                                      |
| Pré-condição       | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                                                                               |
| Dados de Teste     | Username: `invalid_user` \| Password: `secret_sauce`                                                                                                                                                            |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Preencher o campo **Username** com `invalid_user` <br> 3. Preencher o campo **Password** com `secret_sauce` <br> 4. Clicar em **Login**                          |
| Resultado Esperado | O usuário deve permanecer na tela de login e o sistema deve exibir a mensagem: `Epic sadface: Username and password do not match any user in this service`                                                       |
| Status             | Passou                                                                                                                                                                                                           |

---

| Campo              | Descrição                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-LOGIN-003                                                                                                                                                                                                      |
| Título             | Login com password inválido                                                                                                                                                                                       |
| Pré-condição       | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                                                                                |
| Dados de Teste     | Username: `standard_user` \| Password: `senha_invalida`                                                                                                                                                          |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Preencher o campo **Username** com `standard_user` <br> 3. Preencher o campo **Password** com `senha_invalida` <br> 4. Clicar em **Login**                        |
| Resultado Esperado | O usuário deve permanecer na tela de login e o sistema deve exibir a mensagem: `Epic sadface: Username and password do not match any user in this service`                                                        |
| Status             | Passou                                                                                                                                                                                                            |

---

| Campo              | Descrição                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-LOGIN-004                                                                                                                                                         |
| Título             | Tentativa de login sem preenchimento de nenhum campo                                                                                                                 |
| Pré-condição       | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                                   |
| Dados de Teste     | Nenhum dado inserido nos campos                                                                                                                                      |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Clicar em **Login** sem preencher nenhum campo                                                                      |
| Resultado Esperado | O usuário deve permanecer na tela de login e o sistema deve exibir a mensagem: `Epic sadface: Username is required`                                                  |
| Status             | Passou                                                                                                                                                               |

---

| Campo              | Descrição                                                                                                                                                                                  |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-LOGIN-005                                                                                                                                                                               |
| Título             | Tentativa de login sem preenchimento do username                                                                                                                                           |
| Pré-condição       | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                                                         |
| Dados de Teste     | Username: campo vazio \| Password: `secret_sauce`                                                                                                                                         |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Deixar o campo **Username** vazio <br> 3. Preencher o campo **Password** com `secret_sauce` <br> 4. Clicar em **Login**                    |
| Resultado Esperado | O usuário deve permanecer na tela de login e o sistema deve exibir a mensagem: `Epic sadface: Username is required`                                                                        |
| Status             | Passou                                                                                                                                                                                     |

---

| Campo              | Descrição                                                                                                                                                                               |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-LOGIN-006                                                                                                                                                                            |
| Título             | Tentativa de login sem preenchimento do password                                                                                                                                        |
| Pré-condição       | Aplicação disponível em `https://www.saucedemo.com/` e nenhum usuário autenticado                                                                                                      |
| Dados de Teste     | Username: `standard_user` \| Password: campo vazio                                                                                                                                     |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Preencher o campo **Username** com `standard_user` <br> 3. Deixar o campo **Password** vazio <br> 4. Clicar em **Login**               |
| Resultado Esperado | O usuário deve permanecer na tela de login e o sistema deve exibir a mensagem: `Epic sadface: Password is required`                                                                     |
| Status             | Passou                                                                                                                                                                                  |