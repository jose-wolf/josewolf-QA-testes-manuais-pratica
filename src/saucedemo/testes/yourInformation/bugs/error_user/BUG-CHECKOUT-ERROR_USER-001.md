# BUG-CHECKOUT-ERROR_USER-001 — Formulário de checkout permite avanço sem o preenchimento do campo obrigatório Last Name

**Cenário relacionado:** CN-CHECKOUT-006  
**Caso de teste relacionado:** TC-CHECKOUT-ERROR_USER-006  
**Categoria:** Regra de Negócio / Integridade de Dados  
**Severidade:** Alta  
**Prioridade:** Alta  
**Ambiente:** Firefox 155 / Ubuntu 24.04

### Descrição:
A validação de campos obrigatórios falha na tela `/checkout-step-one.html`. Ao submeter o formulário com o campo *Last Name* vazio e os demais preenchidos, o sistema não aciona o bloqueio nem exibe mensagem de erro, avançando diretamente para a tela de visão geral do pedido (`/checkout-step-two.html`).

### Passos para reproduzir:
1. Acessar https://www.saucedemo.com/
2. Autenticar com o perfil `error_user`.
3. Adicionar itens e navegar até `/checkout-step-one.html`.
4. Inserir `teste` no campo **First Name**.
5. Manter o campo **Last Name** completamente vazio.
6. Inserir `10001-0005` no campo **Zip/Postal Code**.
7. Clicar no botão **Continue**.

### Resultado obtido:
A aplicação avança para `/checkout-step-two.html` sem exigir o preenchimento do sobrenome.

### Resultado esperado:
O avanço deve ser impedido e a mensagem `Error: Last Name is required` deve ser exibida em destaque.

### Impacto:
Envio de cadastros incompletos para a base de pedidos e risco de inconsistência com operadoras de pagamento ou notas fiscais.

### Evidência:
[Vídeo do avanço sem Last Name](https://drive.google.com/file/d/1AAW9ta5JTD9hvCzosDNoPydoWHmMYVY2/view?usp=sharing)

### Status:
Aberto