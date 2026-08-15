# Test Case - Checkout: Your Information (error_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-05 - Funcionalidade Checkout |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Validar navegação, preenchimento e regras de obrigatoriedade dos campos no checkout |
| Pré-condição        | Usuário autenticado como `error_user`, com ao menos 1 item no carrinho |
| Dados Necessários   | Username: `error_user` \| Password: `secret_sauce` |

---

## Casos de Teste

| Campo              | Descrição |
|--------------------|-----------|
| ID                 | TC-CHECKOUT-ERROR-001 |
| Título             | Validar retorno para sessão anterior via botão Cancel |
| Pré-condição       | Usuário na tela **Checkout: Your Information** |
| Passos             | 1. Acessar Checkout: Your Information <br> 2. Clicar em **Cancel** |
| Resultado esperado | O sistema deve retornar para a sessão anterior (carrinho) |
| Status             | Passou |

---

| Campo              | Descrição |
|--------------------|-----------|
| ID                 | TC-CHECKOUT-ERROR-002 |
| Título             | Validar preenchimento do campo Last Name |
| Pré-condição       | Usuário na tela **Checkout: Your Information** |
| Passos             | 1. Preencher **First Name** <br> 2. Tentar preencher **Last Name** <br> 3. Preencher **Postal Code** |
| Resultado esperado | O campo **Last Name** deve aceitar digitação normalmente |
| Status             | Falhou |
| Observação         | Não foi possível preencher o campo **Last Name**. |

---

| Campo              | Descrição |
|--------------------|-----------|
| ID                 | TC-CHECKOUT-ERROR-003 |
| Título             | Validar bloqueio do avanço sem Last Name preenchido |
| Pré-condição       | Usuário na tela **Checkout: Your Information** |
| Passos             | 1. Preencher **First Name** <br> 2. Deixar **Last Name** em branco <br> 3. Preencher **Postal Code** <br> 4. Clicar em **Continue** |
| Resultado esperado | O sistema deve impedir o avanço e exibir validação de campo obrigatório para **Last Name** |
| Status             | Falhou |
| Observação         | O sistema permitiu avançar mesmo sem **Last Name** preenchido. |