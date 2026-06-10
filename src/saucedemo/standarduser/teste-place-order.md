# Test Case - Finalização da Compra

| Campo             | Descrição |
|-------------------|-----------|
| Tipo de teste     | Funcional |
| Subtipo de teste  | Teste de aceitação |
| Objetivo do teste | Verificar se o sistema conclui a compra corretamente e exibe a confirmação ao usuário |
| Pré-condição      | O usuário deve estar autenticado e estar na tela Checkout Overview |
| Dados necessários | Produto adicionado ao carrinho e dados válidos no checkout |
| Requisito         | RF 6 - Funcionalidade Finalização da Compra |


| ID | TC-020 |
|----|--------|
| Título | Validar finalização da compra |
| Pré-condições | O usuário deve estar na tela Checkout Overview |
| Passos | 1. Prosseguir até a tela Checkout Overview <br> 2. Clicar em "Finish" |
| Resultado esperado | O sistema deve concluir a compra e exibir a tela Checkout Complete com mensagem de confirmação |
| Status | Passou |

| ID | TC-021 |
|----|--------|
| Título | Validar limpeza do carrinho após finalização da compra |
| Pré-condições | O usuário deve ter concluído uma compra com sucesso |
| Passos | 1. Finalizar uma compra com sucesso <br> 2. Verificar o ícone do carrinho |
| Resultado esperado | O carrinho deve estar vazio e não deve exibir quantidade de itens pendentes |
| Status | Passou |

| ID | TC-022 |
|----|--------|
| Título | Validar retorno para a página inicial após conclusão da compra |
| Pré-condições | O usuário deve estar na tela Checkout Complete |
| Passos | 1. Finalizar a compra <br> 2. Clicar em "Back Home" |
| Resultado esperado | O usuário deve ser redirecionado para a tela Products |
| Status | Passou |
