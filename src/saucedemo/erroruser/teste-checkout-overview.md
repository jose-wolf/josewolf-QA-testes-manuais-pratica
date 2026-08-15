# Test Case - Checkout: Overview (error_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-05 - Funcionalidade Checkout |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Validar a exibição correta das informações no checkout overview e a finalização da compra |
| Pré-condição        | Usuário autenticado como `error_user`, com itens no carrinho e dados de checkout preenchidos |
| Dados Necessários   | Username: `error_user` \| Password: `secret_sauce` |

---

## Casos de Teste

| Campo              | Descrição |
|--------------------|-----------|
| ID                 | TC-CHECKOUT-OVERVIEW-ERROR-001 |
| Título             | Validar exibição das informações dos produtos e resumo da compra |
| Pré-condição       | Usuário na tela **Checkout: Overview** |
| Passos             | 1. Realizar login com `error_user` <br> 2. Adicionar produtos ao carrinho <br> 3. Acessar carrinho e clicar em **Checkout** <br> 4. Preencher dados obrigatórios e clicar em **Continue** <br> 5. Validar itens, quantidade, descrição, preços, pagamento, envio e total na tela **Checkout: Overview** |
| Resultado esperado | A tela deve exibir corretamente todas as informações dos produtos e o resumo financeiro da compra |
| Status             | Passou |
| Observação         | Informações exibidas corretamente nesta etapa |

---

| Campo              | Descrição |
|--------------------|-----------|
| ID                 | TC-CHECKOUT-OVERVIEW-ERROR-002 |
| Título             | Validar finalização da compra ao clicar em Finish |
| Pré-condição       | Usuário na tela **Checkout: Overview** com dados válidos |
| Passos             | 1. Estar na tela **Checkout: Overview** <br> 2. Clicar no botão **Finish** |
| Resultado esperado | O sistema deve finalizar a compra e redirecionar para a tela **Checkout: Complete!** com mensagem de sucesso |
| Status             | Falhou |
| Observação         | Ao clicar em **Finish**, a compra não foi concluída conforme esperado |