# Test Case - Carrinho de Compras (error_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-04 - Funcionalidade Carrinho de Compras |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Validar a exibição correta dos itens no carrinho e a disponibilidade das ações principais de navegação e checkout |
| Pré-condição        | Usuário autenticado como `error_user` com ao menos 1 produto adicionado ao carrinho |
| Dados Necessários   | Username: `error_user` \| Password: `secret_sauce` |

---

## Casos de Teste

| Campo              | Descrição |
|--------------------|-----------|
| ID                 | TC-CARRINHO-001 |
| Título             | Validar exibição e ações disponíveis na tela Your Cart |
| Pré-condição       | Usuário autenticado como `error_user` e com item previamente adicionado ao carrinho |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Realizar login com `error_user` <br> 3. Adicionar o produto **Sauce Labs Bike Light** <br> 4. Clicar no ícone do carrinho <br> 5. Verificar a tela **Your Cart** |
| Resultado esperado | O item adicionado deve ser exibido corretamente com nome, descrição, quantidade e preço; os botões **Remove**, **Continue Shopping** e **Checkout** devem estar visíveis e habilitados. |
| Status             | Passou |
| Observação         | Execução concluída sem falhas; tela do carrinho apresentou comportamento esperado. |