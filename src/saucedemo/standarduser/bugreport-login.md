# Bug-report dos Testes Manuais - saucedemo.com

| Campo                    | Descrição                                                                                             |
|--------------------------|-------------------------------------------------------------------------------------------------------|
| Requisito Funcional      | RF 1                                                                                                  |
| Bug Id                   | bug-001                                                                                               |
| Relacionado ao Test Case | TC-002                                                                                                |
| Título                   | Mensagem de erro está sobreposta ao background                                                        |
| Severidade               | Baixa                                                                                                 |
| Prioridade               | Baixa                                                                                                 |
| Passos para reproduzir   | 1. Acessar https://www.saucedemo.com/ <br> 2. Inserir login/senha inválidos <br> 3. Clicar em "Login" |
| Resultado obtido         | Epic sadface: Username and password do not match any user in this service                             |
| Resultado esperado       | A mensagem de erro deve ser exibida de forma clara, sem sobreposição visual                           |
| Impacto | Não afeta a funcionalidade do sistema, porém compromete a apresentação visual da mensagem de erro |
| Ambiente                 | - Ubuntu linux 24.04.4 <br> - Firefox, Brave  <br>                                                    |
| Evidências               | ![Evidência do Bug](evidencia/TC002 login-bug-ui-ux.png)                                              |                                                                                        |
| Categoria do defeito     | Usabilidade / UI                                                                                      |

bug-001
Tela de Login
Afeta:
- standard_user
- problem_user
- locked_out_user
- performance_glitch_user