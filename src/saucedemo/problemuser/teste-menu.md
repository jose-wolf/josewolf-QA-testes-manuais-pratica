# Test Case - Menu Lateral (problem_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-03 - Funcionalidade Menu Lateral |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Verificar o funcionamento das opções disponíveis no menu lateral |
| Pré-condição        | O usuário deve estar autenticado como `problem_user` |
| Dados Necessários   | Usuário `problem_user` |

## Casos de Teste

| ID | TC-MENU-001 |
|----|--------------|
| Título | Validar redirecionamento da opção About |
| Pré-condições | O usuário deve estar autenticado como `problem_user` |
| Passos | 1. Realizar login com `problem_user` <br> 2. Abrir o menu lateral <br> 3. Clicar em "About" |
| Resultado esperado | O usuário deve ser redirecionado para a página informativa da aplicação |
| Status | Falhou |

| ID | TC-MENU-002 |
|----|--------------|
| Título | Validar funcionalidade Logout |
| Pré-condições | O usuário deve estar autenticado como `problem_user` |
| Passos | 1. Realizar login com `problem_user` <br> 2. Abrir o menu lateral <br> 3. Clicar em "Logout" |
| Resultado esperado | O usuário deve ser desconectado do sistema e redirecionado para a tela de login |
| Status | Passou |

| ID | TC-MENU-003 |
|----|--------------|
| Título | Validar funcionalidade Reset App State |
| Pré-condições | O usuário deve estar autenticado como `problem_user` e possuir produtos adicionados ao carrinho |
| Passos | 1. Realizar login com `problem_user` <br> 2. Adicionar produtos ao carrinho <br> 3. Abrir o menu lateral <br> 4. Clicar em "Reset App State" |
| Resultado esperado | O sistema deve remover os produtos adicionados ao carrinho e restaurar o estado inicial da aplicação |
| Status | Passou com observação |
| Observação | Após executar o Reset App State, o carrinho é limpo corretamente, porém os botões dos produtos permanecem exibindo "Remove" ao invés de retornar para "Add to cart". |