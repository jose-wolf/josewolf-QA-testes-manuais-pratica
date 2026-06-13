# Test Case - Carrinho de Compras (problem_user)

| Campo             | Descrição |
|-------------------|-----------|
| Tipo de teste     | Funcional |
| Subtipo de teste  | Teste de aceitação |
| Objetivo do teste | Verificar o funcionamento do carrinho de compras |
| Pré-condição      | O usuário deve estar autenticado como problem_user |
| Dados necessários | Usuário problem_user e produtos adicionados ao carrinho |
| Requisito         | RF 4 - Funcionalidade Carrinho de Compras |

| ID | TC-007 |
|----|--------|
| Título | Validar exibição dos produtos adicionados ao carrinho |
| Pré-condições | Usuário autenticado como problem_user e com produtos adicionados ao carrinho |
| Passos | 1. Adicionar produtos ao carrinho <br> 2. Acessar o carrinho |
| Resultado esperado | Os produtos adicionados devem ser exibidos corretamente no carrinho |
| Status | Passou |

| ID | TC-008 |
|----|--------|
| Título | Validar remoção de produtos pelo carrinho |
| Pré-condições | Usuário autenticado como problem_user e com produtos adicionados ao carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Remove" |
| Resultado esperado | O produto deve ser removido corretamente do carrinho |
| Status | Passou |

| ID | TC-009 |
|----|--------|
| Título | Validar funcionalidade Continue Shopping |
| Pré-condições | Usuário autenticado como problem_user |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Continue Shopping" |
| Resultado esperado | O usuário deve retornar para a tela Products |
| Status | Passou |

| ID | TC-010 |
|----|--------|
| Título | Validar acesso ao Checkout |
| Pré-condições | Usuário autenticado como problem_user e com produtos adicionados ao carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" |
| Resultado esperado | O usuário deve ser redirecionado para a tela Checkout: Your Information |
| Status | Passou |
