# Test Case - Tela de Resumo da Compra

| Campo             | Descrição |
|-------------------|-----------|
| Tipo de teste     | Funcional |
| Subtipo de teste  | Teste de aceitação |
| Objetivo do teste | Verificar se a tela de resumo da compra exibe corretamente os produtos, informações de pagamento, envio e valores da compra |
| Pré-condição      | O usuário deve estar autenticado, possuir produto no carrinho e ter preenchido os dados do checkout |
| Dados necessários | Produto adicionado ao carrinho e dados válidos no checkout |
| Requisito         | RF 5 - Funcionalidade Resumo da Compra |

| ID | TC-017 |
|----|--------|
| Título | Validar exibição do resumo da compra |
| Pré-condições | O usuário deve estar autenticado, possuir produtos no carrinho e ter preenchido os dados do checkout |
| Passos | 1. Adicionar produtos ao carrinho <br> 2. Acessar o carrinho <br> 3. Clicar em "Checkout" <br> 4. Preencher os dados obrigatórios <br> 5. Clicar em "Continue" |
| Resultado esperado | O sistema deve exibir a tela Checkout Overview com os produtos selecionados, quantidade, descrição, preço, informações de pagamento, envio e valores da compra |
| Status | Passou |

| ID | TC-018 |
|----|--------|
| Título | Validar cálculo do valor total da compra |
| Pré-condições | O usuário deve estar na tela Checkout Overview |
| Passos | 1. Verificar o valor dos produtos exibidos <br> 2. Verificar o valor do imposto <br> 3. Verificar o valor total da compra |
| Resultado esperado | O valor total deve corresponder à soma do valor dos produtos mais o imposto informado pelo sistema |
| Status | Passou |