# BUG-CHECKOUT-PROBLEM_USER-001 — Campo Last Name bloqueado para digitação impede finalização de compra

**Cenário relacionado:** CN-CHECKOUT-004 e CN-CHECKOUT-007  
**Casos de teste relacionados:** TC-CHECKOUT-PROBLEM_USER-004, TC-CHECKOUT-PROBLEM_USER-007  
**Categoria:** Funcional / Bloqueante  
**Severidade:** Crítica (Blocker)  
**Prioridade:** Alta (P0)  
**Ambiente:** Firefox 155 / Ubuntu 24.04

### Descrição:
O campo de texto destinado ao sobrenome (*Last Name*) na tela `/checkout-step-one.html` não registra nenhuma digitação vinda do teclado, tornando impossível preencher o formulário completo. Como consequência direta, o usuário fica impedido de avançar para a tela de revisão e pagamento (`/checkout-step-two.html`).

### Passos para reproduzir:
1. Acessar https://www.saucedemo.com/
2. Autenticar com o usuário `problem_user`.
3. Adicionar qualquer produto ao carrinho e acessar `/cart.html`.
4. Clicar em **Checkout**.
5. Clicar sobre o campo **Last Name** e tentar digitar qualquer texto.
6. Clicar no botão **Continue**.

### Resultado obtido:
Nenhum caractere é inserido no campo de texto e o sistema dispara a mensagem `Error: Last Name is required`, impedindo o fechamento da compra.

### Resultado esperado:
O campo deve aceitar a entrada de dados do usuário e permitir a submissão com sucesso do formulário.

### Impacto de negócio:
Impedimento total de conversão de compras para 100% dos usuários que caem nessa condição (quebra do funil financeiro).

### Evidência:
[Vídeo da falha no Last Name](https://drive.google.com/file/d/1l95_iGKt3S9Wbg6ys2XabznSRSrhBsfJ/view?usp=sharing)

### Status:
Aberto