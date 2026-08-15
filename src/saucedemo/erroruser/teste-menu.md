# Test Case - Menu Lateral (error_user)

| Campo             | Descrição |
|-------------------|-----------|
| Tipo de teste     | Funcional |
| Subtipo de teste  | Teste de aceitação |
| Objetivo do teste | Verificar o funcionamento das opções disponíveis no menu lateral |
| Pré-condição      | O usuário deve estar autenticado como `error_user` |
| Dados necessários | Usuário `error_user` |
| Requisito         | RF-03 - Funcionalidade Menu Lateral |

| ID | TC-MENU-001 |
|----|-----------------|
| Título | Validar redirecionamento da opção About |
| Pré-condições | O usuário deve estar autenticado como `error_user` |
| Passos | 1. Realizar login com `error_user` <br> 2. Abrir o menu lateral <br> 3. Clicar em **About** |
| Resultado esperado | O usuário deve ser redirecionado para a página informativa da aplicação |
| Status | Passou |

| ID | TC-MENU-002 |
|----|-----------------|
| Título | Validar funcionalidade Logout |
| Pré-condições | O usuário deve estar autenticado como `error_user` |
| Passos | 1. Realizar login com `error_user` <br> 2. Abrir o menu lateral <br> 3. Clicar em **Logout** |
| Resultado esperado | O usuário deve ser desconectado do sistema e redirecionado para a tela de login |
| Status | Passou |

| ID | TC-MENU-003 |
|----|-----------------|
| Título | Validar funcionalidade Reset App State |
| Pré-condições | O usuário deve estar autenticado como `error_user` e possuir produtos adicionados ao carrinho |
| Passos | 1. Realizar login com `error_user` <br> 2. Adicionar produtos ao carrinho <br> 3. Abrir o menu lateral <br> 4. Clicar em **Reset App State** |
| Resultado esperado | O sistema deve remover os produtos adicionados ao carrinho e restaurar o estado inicial da aplicação |
| Status | Passou |
| Observação | O menu lateral apresentou todas as opções funcionando corretamente durante os testes com o usuário `error_user`. |