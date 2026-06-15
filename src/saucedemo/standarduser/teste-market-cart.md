# Test Case - Tela de Carrinho de Compras

| Campo               | Descrição                                                                                                                                         |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Requisito Funcional | RF-03 – Funcionalidade Carrinho de Compras                                                                                                       |
| Tipo de Teste       | Funcional                                                                                                                                         |
| Subtipo de Teste    | Teste de Aceitação                                                                                                                                |
| Objetivo do Teste   | Verificar se o carrinho de compras exibe corretamente os produtos adicionados e se as ações de remoção, continuidade de compra e checkout funcionam conforme esperado |
| Pré-condição        | Usuário `standard_user` autenticado e com ao menos um produto adicionado ao carrinho                                                              |
| Dados de Teste      | Username: `standard_user` \| Password: `secret_sauce`                                                                                             |

---

## Casos de Teste

| Campo              | Descrição                                                                                                                                                                                                 |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CART-001                                                                                                                                                                                               |
| Título             | Validar exibição dos produtos no carrinho                                                                                                                                                                 |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto adicionado ao carrinho                                                                                                                      |
| Passos             | 1. Acessar `https://www.saucedemo.com/` e realizar login com `standard_user` <br> 2. Adicionar um produto ao carrinho usando **Add to cart** <br> 3. Clicar no ícone do carrinho                          |
| Resultado Esperado | O carrinho deve exibir corretamente o nome, a descrição, a quantidade e o preço de cada produto adicionado                                                                                                |
| Status             | Passou                                                                                                                                                                                                    |

---

| Campo              | Descrição                                                                                                                                                                                                                 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CART-002                                                                                                                                                                                                               |
| Título             | Validar remoção de produto pelo carrinho                                                                                                                                                                                  |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto no carrinho                                                                                                                                                 |
| Passos             | 1. Acessar `https://www.saucedemo.com/` e realizar login com `standard_user` <br> 2. Adicionar um produto ao carrinho usando **Add to cart** <br> 3. Clicar no ícone do carrinho <br> 4. Clicar em **Remove** no produto  |
| Resultado Esperado | O produto deve ser removido do carrinho e o contador do ícone do carrinho deve ser atualizado para refletir a quantidade correta de itens                                                                                  |
| Status             | Passou                                                                                                                                                                                                                    |

---

| Campo              | Descrição                                                                                                                                                                                                                        |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CART-003                                                                                                                                                                                                                      |
| Título             | Validar funcionalidade Continue Shopping                                                                                                                                                                                         |
| Pré-condição       | Usuário `standard_user` autenticado e na tela do carrinho                                                                                                                                                                        |
| Passos             | 1. Acessar `https://www.saucedemo.com/` e realizar login com `standard_user` <br> 2. Adicionar um produto ao carrinho usando **Add to cart** <br> 3. Clicar no ícone do carrinho <br> 4. Clicar em **Continue Shopping**         |
| Resultado Esperado | O usuário deve ser redirecionado para a tela **Products**                                                                                                                                                                        |
| Status             | Passou                                                                                                                                                                                                                           |

---

| Campo              | Descrição                                                                                                                                                                                                           |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-CART-004                                                                                                                                                                                                         |
| Título             | Validar acesso à etapa de checkout pelo carrinho                                                                                                                                                                    |
| Pré-condição       | Usuário `standard_user` autenticado e com ao menos um produto no carrinho                                                                                                                                           |
| Passos             | 1. Acessar `https://www.saucedemo.com/` e realizar login com `standard_user` <br> 2. Adicionar um produto ao carrinho usando **Add to cart** <br> 3. Clicar no ícone do carrinho <br> 4. Clicar em **Checkout**     |
| Resultado Esperado | O usuário deve ser redirecionado para a tela de checkout com o formulário de informações do comprador                                                                                                               |
| Status             | Passou                                                                                                                                                                                                             |