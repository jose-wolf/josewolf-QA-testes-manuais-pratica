
| Campo                    | Descrição                                                                                                                         |
| ------------------------ |-----------------------------------------------------------------------------------------------------------------------------------|
| Requisito Funcional      | RF 2                                                                                                                              |
| Bug Id                   | bug-002                                                                                                                           |
| Relacionado ao Test Case | TC-003                                                                                                                            |
| Título                   | Descrição do produto exibe texto técnico ao usuário                                                                               |
| Severidade               | Baixa                                                                                                                             |
| Prioridade               | Baixa                                                                                                                             |
| Passos para reproduzir   | 1. Acessar https://www.saucedemo.com/ <br> 2. Realizar login com usuário válido <br> 3. Localizar o produto "Sauce Labs Backpack" |
| Resultado obtido         | A descrição do produto exibe o texto técnico "carry.allTheThings()" ao usuário final                                              |
| Resultado esperado       | A descrição deve apresentar apenas texto compreensível e adequado ao usuário final                                                |
| Impacto                  | Não afeta a funcionalidade do sistema, porém compromete a qualidade visual e a experiência do usuário                             |
| Ambiente                 | - Ubuntu Linux 24.04.4 <br> - Firefox, Brave                                                                                      |
| Evidências               | ![Evidência do Bug](./evidencia/TC003 descricao-do-produto.png)                                                                   |

***

| Campo                    | Descrição                                                                                                                                       |
| ------------------------ |-------------------------------------------------------------------------------------------------------------------------------------------------|
| Requisito Funcional      | RF 2                                                                                                                                            |
| Bug Id                   | bug-003                                                                                                                                         |
| Relacionado ao Test Case | TC-003                                                                                                                                          |
| Título                   | Nome do produto exibe nomenclatura técnica ao usuário                                                                                           |
| Severidade               | Baixa                                                                                                                                           |
| Prioridade               | Baixa                                                                                                                                           |
| Passos para reproduzir   | 1. Acessar https://www.saucedemo.com/ <br> 2. Realizar login com usuário válido <br> 3. Localizar o produto "Test.allTheThings() T-Shirt (Red)" |
| Resultado obtido         | O produto é exibido com nomenclatura técnica "Test.allTheThings() T-Shirt (Red)"                                                                |
| Resultado esperado       | O produto deve apresentar nomenclatura comercial adequada ao usuário final                                                                      |
| Impacto                  | Não afeta a funcionalidade do sistema, porém reduz a clareza da interface e a experiência do usuário                                            |
| Ambiente                 | - Ubuntu Linux 24.04.4 <br> - Firefox, Brave                                                                                                    |
| Evidências               | ![Evidência do Bug](./evidencia/TC003 bug-title--produto.png)                                                                                   |
