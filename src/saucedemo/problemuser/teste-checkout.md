# Test Case - Checkout (problem_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-05 - Funcionalidade Checkout |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Verificar o preenchimento das informações obrigatórias do checkout |
| Pré-condição        | O usuário deve estar autenticado como `problem_user` e possuir produtos no carrinho |
| Dados Necessários   | Nome, sobrenome e CEP válidos |

## Casos de Teste

| ID | TC-CHECKOUT-001 |
|----|-------------------|
| Título | Validar preenchimento dos campos obrigatórios do checkout |
| Pré-condições | Usuário autenticado como `problem_user` e com produto no carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" <br> 3. Preencher First Name <br> 4. Preencher Last Name <br> 5. Preencher Postal Code <br> 6. Clicar em "Continue" |
| Resultado esperado | O sistema deve permitir o preenchimento dos campos obrigatórios e redirecionar o usuário para o resumo da compra |
| Status | Falhou |