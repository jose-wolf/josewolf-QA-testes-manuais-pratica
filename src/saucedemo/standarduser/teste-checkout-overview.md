# Test Case - Tela de Resumo da Compra

| Campo               | Descrição                                                                                                                                                              |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Requisito Funcional | RF-05 – Funcionalidade Resumo da Compra                                                                                                                               |
| Tipo de Teste       | Funcional                                                                                                                                                              |
| Subtipo de Teste    | Teste de Aceitação                                                                                                                                                     |
| Objetivo do Teste   | Verificar se a tela de resumo da compra exibe corretamente os produtos, informações de pagamento, envio e valores, e se o cálculo do total está de acordo com os itens |
| Pré-condição        | Usuário `standard_user` autenticado, com ao menos um produto no carrinho e dados do checkout preenchidos                                                               |
| Dados de Teste      | Username: `standard_user` \| Password: `secret_sauce` \| Produto adicionado ao carrinho \| First Name: `José` \| Last Name: `Silva` \| Postal Code: `12345`            |

---

## Casos de Teste

| Campo              | Descrição                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-OVERVIEW-001                                                                                                                                                                                                                                                                   |
| Título             | Validar exibição do resumo da compra na tela Checkout Overview                                                                                                                                                                                                               |
| Pré-condição       | Usuário `standard_user` autenticado, com ao menos um produto no carrinho e dados de checkout preenchidos                                                                                                                                                                     |
| Dados de Teste     | Produto adicionado ao carrinho \| First Name: `José` \| Last Name: `Silva` \| Postal Code: `12345`                                                                                                                                                                          |
| Passos             | 1. Acessar `https://www.saucedemo.com/` e realizar login com `standard_user` <br> 2. Adicionar ao menos um produto ao carrinho usando **Add to cart** <br> 3. Acessar o carrinho e clicar em **Checkout** <br> 4. Preencher os dados obrigatórios <br> 5. Clicar em **Continue** |
| Resultado Esperado | A tela **Checkout: Overview** deve exibir corretamente: nome do produto, descrição, quantidade, preço unitário, informações de pagamento, informações de envio e o valor total da compra                                                                                      |
| Status             | Passou                                                                                                                                                                                                                                                                       |

---

| Campo              | Descrição                                                                                                                                                                                   |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-OVERVIEW-002                                                                                                                                                                                  |
| Título             | Validar cálculo do valor total na tela Checkout Overview                                                                                                                                    |
| Pré-condição       | Usuário `standard_user` autenticado e na tela **Checkout: Overview**                                                                                                                        |
| Passos             | 1. Prosseguir até a tela **Checkout: Overview** <br> 2. Verificar o valor exibido em **Item total** <br> 3. Verificar o valor exibido em **Tax** <br> 4. Verificar o valor exibido em **Total** |
| Resultado Esperado | O valor exibido em **Total** deve corresponder exatamente à soma do valor de **Item total** com o valor de **Tax** informados pelo sistema                                                  |
| Status             | Passou                                                                                                                                                                                      |