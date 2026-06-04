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
| Resutado esperado        | Epic sadface: Username and password do not match any user in this service                             |
| Impacto                  | Afeta 0% dos usuários, porém o texto está ocupando mais espaço que necessário                         |
| Ambiente                 | - Ubuntu linux 24.04.4 <br> - Firefox, Brave  <br>                                                    |
| Evidências               | ![Evidência do Bug](evidencia/TC002 login-bug-ui-ux.png)                                               |                                                                                        |
| Categoria do defeito     | Usabilidade / UI                                                                                                                  |

