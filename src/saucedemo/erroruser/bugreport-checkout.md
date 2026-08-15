# Bug Report - Checkout (error_user)

| Campo                    | Descrição                                                                                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bug ID                   | BUG-CHECKOUT-ERROR-001                                                                                                                                                   |
| Requisito Funcional      | RF-05 - Funcionalidade Checkout                                                                                                                                          |
| Relacionado ao Test Case | TC-CHECKOUT-ERROR-002                                                                                                                                                    |
| Título                   | Campo Last Name não permite preenchimento na tela Checkout: Your Information                                                                                             |
| Severidade               | Alta                                                                                                                                                                     |
| Prioridade               | Alta                                                                                                                                                                     |
| Ambiente                 | Ubuntu Linux 24.04.4 \| Firefox / Brave                                                                                                                                  |
| Passos para reproduzir   | 1. Logar com `error_user` <br> 2. Adicionar item ao carrinho <br> 3. Acessar **Checkout** <br> 4. Na tela **Checkout: Your Information**, tentar preencher **Last Name** |
| Resultado obtido         | O campo **Last Name** não aceita preenchimento.                                                                                                                          |
| Resultado esperado       | O campo **Last Name** deve aceitar entrada de texto normalmente.                                                                                                         |
| Impacto                  | Impede o preenchimento completo do formulário e compromete a confiabilidade do fluxo de checkout.                                                                        |
| Evidências               | [Evidência em vídeo:](https://drive.google.com/file/d/19rncfmDKlSpgogVk54UvIQGx7qznXx8g/view?usp=sharing)                                                                                                                                                  |
| Categoria do defeito     | Funcional / UI                                                                                                                                                           |

---

| Campo                    | Descrição                                                                                                                                                                          |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bug ID                   | BUG-CHECKOUT-ERROR-002                                                                                                                                                             |
| Requisito Funcional      | RF-05 - Funcionalidade Checkout                                                                                                                                                    |
| Relacionado ao Test Case | TC-CHECKOUT-ERROR-003                                                                                                                                                              |
| Título                   | Sistema permite avançar no checkout sem preenchimento do Last Name                                                                                                                 |
| Severidade               | Alta                                                                                                                                                                               |
| Prioridade               | Alta                                                                                                                                                                               |
| Ambiente                 | Ubuntu Linux 24.04.4 \| Firefox / Brave                                                                                                                                            |
| Passos para reproduzir   | 1. Logar com `error_user` <br> 2. Adicionar item ao carrinho <br> 3. Acessar **Checkout** <br> 4. Preencher apenas **First Name** e **Postal Code** <br> 5. Clicar em **Continue** |
| Resultado obtido         | O sistema permite avançar para a próxima etapa sem **Last Name** preenchido.                                                                                                       |
| Resultado esperado       | O sistema deve bloquear o avanço e informar que **Last Name** é obrigatório.                                                                                                       |
| Impacto                  | Quebra regra de validação de campos obrigatórios, afetando integridade dos dados da compra.                                                                                        |
| Evidências               | [Evidência em vídeo:](https://drive.google.com/file/d/19rncfmDKlSpgogVk54UvIQGx7qznXx8g/view?usp=sharing)                                                                                                                                                            |
| Categoria do defeito     | Funcional                                                                                                                                                                          |