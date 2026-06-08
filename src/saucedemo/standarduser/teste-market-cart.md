# Test Case - Tela de Carrinho de Compras

| Campo | Descrição |
|--------|--------|
| Tipo de teste | Funcional |
| Subtipo de teste | Teste de aceitação |
| Objetivo do teste | Verificar se o carrinho de compras funciona corretamente durante a navegação e manipulação dos produtos |
| Pré-condição | O usuário deve estar autenticado no sistema |
| Dados necessários | Possuir um usuário cadastrado e ao menos um produto disponível para compra |
| Requisito | RF 3 - Funcionalidade Carrinho de Compras |

## Casos de teste

| ID | TC-009 |
|----|--------|
| Título | Validar exibição dos produtos no carrinho |
| Pré-condições | O usuário deve possuir cadastro no sistema e estar autenticado |
| Passos | 1. Realizar login <br> 2. Adicionar produtos ao carrinho <br> 3. Clicar no ícone do carrinho |
| Resultado esperado | Os produtos adicionados devem ser exibidos corretamente no carrinho com nome, descrição, quantidade e preço |
| Status | Passou |

| ID | TC-010 |
|----|--------|
| Título | Validar remoção de produtos pelo carrinho |
| Pré-condições | O usuário deve possuir cadastro no sistema e estar autenticado |
| Passos | 1. Realizar login <br> 2. Adicionar produtos ao carrinho <br> 3. Acessar o carrinho <br> 4. Clicar em "Remove" |
| Resultado esperado | O produto deve ser removido do carrinho e a quantidade de itens deve ser atualizada corretamente |
| Status | Passou |

| ID | TC-010 |
|----|--------|
| Título | Validar remoção de produtos pelo carrinho |
| Pré-condições | O usuário deve possuir cadastro no sistema e estar autenticado |
| Passos | 1. Realizar login <br> 2. Adicionar produtos ao carrinho <br> 3. Acessar o carrinho <br> 4. Clicar em "Remove" |
| Resultado esperado | O produto deve ser removido do carrinho e a quantidade de itens deve ser atualizada corretamente |
| Status | Passou |

| ID | TC-011 |
|----|--------|
| Título | Validar funcionalidade Continue Shopping |
| Pré-condições | O usuário deve possuir cadastro no sistema e estar autenticado |
| Passos | 1. Realizar login <br> 2. Adicionar produtos ao carrinho <br> 3. Acessar o carrinho <br> 4. Clicar em "Continue Shopping" |
| Resultado esperado | O usuário deve ser redirecionado para a tela de produtos |
| Status | Passou |

| ID | TC-012 |
|----|--------|
| Título | Validar acesso à etapa de checkout |
| Pré-condições | O usuário deve possuir cadastro no sistema e estar autenticado |
| Passos | 1. Realizar login <br> 2. Adicionar produtos ao carrinho <br> 3. Acessar o carrinho <br> 4. Clicar em "Checkout" |
| Resultado esperado | O usuário deve ser redirecionado para a tela de preenchimento dos dados de compra |
| Status | Passou |