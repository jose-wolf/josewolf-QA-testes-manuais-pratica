# Bug Report - Menu Lateral (problem_user)

| Campo                    | Descrição |
|--------------------------|-----------|
| Requisito Funcional      | RF-03 - Funcionalidade Menu Lateral |
| Bug ID                   | BUG-MENU-001 |
| Relacionado ao Test Case | TC-MENU-001 |
| Título                   | Opção About redireciona para página inexistente |
| Severidade               | Baixa |
| Prioridade               | Média |
| Passos para reproduzir   | 1. Realizar login com `problem_user` <br> 2. Abrir o menu lateral <br> 3. Clicar em "About" |
| Resultado obtido         | O usuário é redirecionado para uma página 404 (Page Not Found) |
| Resultado esperado       | O usuário deve ser redirecionado para a página oficial de informações da aplicação |
| Impacto                  | Impede o acesso ao conteúdo disponibilizado pela opção About |
| Categoria do defeito     | Funcional / Navegação |