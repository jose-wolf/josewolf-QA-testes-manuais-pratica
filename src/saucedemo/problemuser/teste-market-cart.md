# Test Case - Carrinho de Compras (problem_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-04 - Funcionalidade Carrinho de Compras |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Verificar o funcionamento do carrinho de compras |
| Pré-condição        | O usuário deve estar autenticado como `problem_user` |
| Dados Necessários   | Usuário `problem_user` e produtos adicionados ao carrinho |

## Casos de Teste

| ID | TC-CARRINHO-001 |
|----|------------------|
| Título | Validar exibição dos produtos adicionados ao carrinho |
| Pré-condições | Usuário autenticado como `problem_user` e com produtos adicionados ao carrinho |
| Passos | 1. Adicionar produtos ao carrinho <br> 2. Acessar o carrinho |
| Resultado esperado | Os produtos adicionados devem ser exibidos corretamente no carrinho |
| Status | Passou |

| ID | TC-CARRINHO-002 |
|----|------------------|
| Título | Validar remoção de produtos pelo carrinho |
| Pré-condições | Usuário autenticado como `problem_user` e com produtos adicionados ao carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Remove" |
| Resultado esperado | O produto deve ser removido corretamente do carrinho |
| Status | Passou |

| ID | TC-CARRINHO-003 |
|----|------------------|
| Título | Validar funcionalidade Continue Shopping |
| Pré-condições | Usuário autenticado como `problem_user` |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Continue Shopping" |
| Resultado esperado | O usuário deve retornar para a tela Products |
| Status | Passou |

| ID | TC-CARRINHO-004 |
|----|------------------|
| Título | Validar acesso ao Checkout |
| Pré-condições | Usuário autenticado como `problem_user` e com produtos adicionados ao carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" |
| Resultado esperado | O usuário deve ser redirecionado para a tela Checkout: Your Information |
| Status | Passou |