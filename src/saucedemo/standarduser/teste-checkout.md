# Test Case - Tela de Checkout: Informações do Usuário

| Campo             | Descrição |
|-------------------|-----------|
| Tipo de teste     | Funcional |
| Subtipo de teste  | Teste de aceitação |
| Objetivo do teste | Verificar se a tela de informações do checkout valida corretamente os campos obrigatórios |
| Pré-condição      | O usuário deve estar autenticado e possuir produto no carrinho |
| Dados necessários | Nome, sobrenome e CEP válidos |
| Requisito         | RF 4 - Funcionalidade Checkout |

| ID | TC-013 |
|----|--------|
| Título | Checkout com dados válidos |
| Pré-condições | O usuário deve estar autenticado e possuir produto no carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" <br> 3. Preencher First Name <br> 4. Preencher Last Name <br> 5. Preencher Postal Code <br> 6. Clicar em "Continue" |
| Resultado esperado | O usuário deve ser redirecionado para a tela de resumo da compra |
| Status | Passou |

| ID | TC-014 |
|----|--------|
| Título | Checkout sem preenchimento do First Name |
| Pré-condições | O usuário deve estar autenticado e possuir produto no carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" <br> 3. Deixar First Name vazio <br> 4. Preencher Last Name <br> 5. Preencher Postal Code <br> 6. Clicar em "Continue" |
| Resultado esperado | O sistema deve impedir o avanço e exibir mensagem de erro informando que o First Name é obrigatório |
| Status | Passou |

| ID | TC-015 |
|----|--------|
| Título | Checkout sem preenchimento do Last Name |
| Pré-condições | O usuário deve estar autenticado e possuir produto no carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" <br> 3. Preencher First Name <br> 4. Deixar Last Name vazio <br> 5. Preencher Postal Code <br> 6. Clicar em "Continue" |
| Resultado esperado | O sistema deve impedir o avanço e exibir mensagem de erro informando que o Last Name é obrigatório |
| Status | Passou |

| ID | TC-016 |
|----|--------|
| Título | Checkout sem preenchimento do Postal Code |
| Pré-condições | O usuário deve estar autenticado e possuir produto no carrinho |
| Passos | 1. Acessar o carrinho <br> 2. Clicar em "Checkout" <br> 3. Preencher First Name <br> 4. Preencher Last Name <br> 5. Deixar Postal Code vazio <br> 6. Clicar em "Continue" |
| Resultado esperado | O sistema deve impedir o avanço e exibir mensagem de erro informando que o Postal Code é obrigatório |
| Status | Passou |