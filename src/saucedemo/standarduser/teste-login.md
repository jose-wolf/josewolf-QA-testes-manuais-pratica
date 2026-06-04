| Campo             | Descrição                                                                                                  |
|-------------------|------------------------------------------------------------------------------------------------------------|
| Tipo de teste     | Funcional                                                                                                  |
| Subtipo de teste  | Teste de aceitação                                                                                         |
| Objetivo do teste | Realizar login na aplicação                                                                                |
| Pré-condição      | - Ter um usuário cadastrado<br>- Ter uma senha cadastrada                                                  |
| Dados necessários | - Usuário e senha para login<br>- Usuário com acesso: `standard_user`<br>- Senha de acesso: `secret_sauce` |
| Requisito         | RF 1 - Funcionalidade Login  <br/>                                                                         |

***



| ID | TC-001                                                                                                                            |
| ------ |-----------------------------------------------------------------------------------------------------------------------------------|
| Título | Login com credenciais válidas                                                                                                     |
| Pré-condições | O usuário deve possuir cadastro no site                                                                                           |
| Passos | 1. Acessar https://www.saucedemo.com/ <br> 2. Inserir usuário válido <br> 3. Inserir um password válido <br> 4. Clicar em "Login" |
| Resultado esperado | Usuário redirecionado para a página Home<br/>                                                                                          |
| Status | Passou | 


| ID | TC-002                                                                                                                            |
| ------ |-----------------------------------------------------------------------------------------------------------------------------------|
| Título | Login com username inválido                                                                                            |
| Pré-condições | O usuário deve possuir cadastro no site                                                                                           |
| Passos | 1. Acessar https://www.saucedemo.com/ <br> 2. Inserir usuário inválido <br> 3. Inserir um password válido <br> 4. Clicar em "Login" |
| Resultado esperado | - Usuário não deve ser redirecionado para a página Home<br/> - Mensagem de erro deve ser mostrada                                 |
| Status | Passou                                                                                                                            | 


| ID                 | TC-003                                                                                                                              |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Título             | Login com password inválido                                                                                                         |
| Pré-condições      | O usuário deve possuir cadastro no site                                                                                             |
| Passos             | 1. Acessar https://www.saucedemo.com/ <br> 2. Inserir usuário válido <br> 3. Inserir um password inválido <br> 4. Clicar em "Login" |
| Resultado esperado | - Usuário não deve ser redirecionado para a página Home<br/> - Mensagem de erro deve ser mostrada                                   |
| Status             | Passou                                                                                                                              | 


| ID | TC-004                                                                                           |
| ------ |--------------------------------------------------------------------------------------------------|
| Título | Tentativa de login sem preenchimento dos dados                                                   |
| Pré-condições | O usuário deve possuir cadastro no site                                                          |
| Passos | 1. Acessar https://www.saucedemo.com/ <br> 2. Clicar em "Login"                                  |
| Resultado esperado | - Usuário não deve ser redirecionado para a página Home<br/> - Mensagem de erro deve ser mostrada |
| Status | Passou                                                                                           | 

| ID | TC-005                                                                                              |
| ------ |-----------------------------------------------------------------------------------------------------|
| Título | Tentativa de login sem preenchimento do username                                                    |
| Pré-condições | O usuário deve possuir cadastro no site                                                             |
| Passos | 1. Acessar https://www.saucedemo.com/ <br>  2. Inserir um password válido <br> 3. Clicar em "Login" |
| Resultado esperado | - Usuário não deve ser redirecionado para a página Home<br/> - Mensagem de erro deve ser mostrada   |
| Status | Passou                                                                                              | 
                                                                                 | 


| ID | TC-006                                                                                              |
| ------ |-----------------------------------------------------------------------------------------------------|
| Título | Tentativa de login sem preenchimento do password                                                    |
| Pré-condições | O usuário deve possuir cadastro no site                                                             |
| Passos | 1. Acessar https://www.saucedemo.com/ <br>  2. Inserir um username válido <br> 3. Clicar em "Login" |
| Resultado esperado | - Usuário não deve ser redirecionado para a página Home<br/> - Mensagem de erro deve ser mostrada   |
| Status | Passou                                                                                              | 
