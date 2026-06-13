# Test Case - Checkout (problem_user)

| Campo             | Descrição |
|-------------------|-----------|
| Tipo de teste     | Funcional |
| Subtipo de teste  | Teste de aceitação |
| Objetivo do teste | Verificar o preenchimento das informações obrigatórias do checkout |
| Pré-condição      | O usuário deve estar autenticado como problem_user e possuir produtos no carrinho |
| Dados necessários | Nome, sobrenome e CEP válidos |
| Requisito         | RF 5 - Funcionalidade Checkout |

| ID | TC-011 |
|----|--------|
| Título | Validar preenchimento dos campos obrigatórios do checkout |
| Pré-condições | Usuário autenticado como problem_user e com produto no carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" <br> 3. Preencher First Name <br> 4. Preencher Last Name <br> 5. Preencher Postal Code <br> 6. Clicar em "Continue" |
| Resultado esperado | O sistema deve permitir o preenchimento dos campos obrigatórios e redirecionar o usuário para o resumo da compra |
| Status | Falhou |