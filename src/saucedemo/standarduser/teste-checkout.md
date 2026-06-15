# Test Case - Tela de Checkout: Informações do Usuário

| Campo               | Descrição                                                                                                                              |
|---------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Requisito Funcional | RF-04 – Funcionalidade Checkout                                                                                                       |
| Tipo de Teste       | Funcional                                                                                                                              |
| Subtipo de Teste    | Teste de Aceitação                                                                                                                     |
| Objetivo do Teste   | Verificar se a tela de checkout valida corretamente os campos obrigatórios e avança o fluxo apenas quando os dados estão preenchidos   |
| Pré-condição        | Usuário `standard_user` autenticado e com ao menos um produto no carrinho                                                              |
| Dados de Teste      | First Name: `José` \| Last Name: `Silva` \| Postal Code: `12345`                                                                       |

---

## Casos de Teste

| Campo              | Descrição                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CHECKOUT-001                                                                                                                                                                                                           |
| Título             | Checkout com todos os dados válidos                                                                                                                                                                                  |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto no carrinho                                                                                                                                            |
| Dados de Teste     | First Name: `José` \| Last Name: `Silva` \| Postal Code: `12345`                                                                                                                                                     |
| Passos             | 1. Acessar o carrinho <br> 2. Clicar em **Checkout** <br> 3. Preencher o campo **First Name** com `José` <br> 4. Preencher o campo **Last Name** com `Silva` <br> 5. Preencher o campo **Postal Code** com `12345` <br> 6. Clicar em **Continue** |
| Resultado Esperado | O usuário deve ser redirecionado para a tela **Checkout: Overview**                                                                                                                                                  |
| Status             | Passou                                                                                                                                                                                                               |

---

| Campo              | Descrição                                                                                                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CHECKOUT-002                                                                                                                                                                                                             |
| Título             | Checkout sem preenchimento do First Name                                                                                                                                                                               |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto no carrinho                                                                                                                                              |
| Dados de Teste     | First Name: campo vazio \| Last Name: `Silva` \| Postal Code: `12345`                                                                                                                                                 |
| Passos             | 1. Acessar o carrinho <br> 2. Clicar em **Checkout** <br> 3. Deixar o campo **First Name** vazio <br> 4. Preencher o campo **Last Name** com `Silva` <br> 5. Preencher o campo **Postal Code** com `12345` <br> 6. Clicar em **Continue** |
| Resultado Esperado | O sistema deve impedir o avanço e exibir a mensagem de erro: `Error: First Name is required`                                                                                                                          |
| Status             | Passou                                                                                                                                                                                                                 |

---

| Campo              | Descrição                                                                                                                                                                                                            |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CHECKOUT-003                                                                                                                                                                                                           |
| Título             | Checkout sem preenchimento do Last Name                                                                                                                                                                              |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto no carrinho                                                                                                                                            |
| Dados de Teste     | First Name: `José` \| Last Name: campo vazio \| Postal Code: `12345`                                                                                                                                                |
| Passos             | 1. Acessar o carrinho <br> 2. Clicar em **Checkout** <br> 3. Preencher o campo **First Name** com `José` <br> 4. Deixar o campo **Last Name** vazio <br> 5. Preencher o campo **Postal Code** com `12345` <br> 6. Clicar em **Continue** |
| Resultado Esperado | O sistema deve impedir o avanço e exibir a mensagem de erro: `Error: Last Name is required`                                                                                                                         |
| Status             | Passou                                                                                                                                                                                                               |

---

| Campo              | Descrição                                                                 |
|--------------------|---------------------------------------------------------------------------|
| ID                 | TC-CHECKOUT-004                                                           |
| Título             | Checkout sem preenchimento do Postal Code                                 |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto no carrinho |
| Dados de Teste     | First Name: `José` \| Last Name: `Silva` \| Postal Code: campo vazio      |
| Passos             | 1. Acessar o carrinho <br> 2. Clicar em **Checkout** <br>                 


