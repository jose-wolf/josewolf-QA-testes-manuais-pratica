# Test Case - Tela de Catálogo de Produtos (problem_user)

| Campo             | Descrição                                                                              |
|-------------------|----------------------------------------------------------------------------------------|
| Tipo de teste     | Funcional                                                                              |
| Subtipo de teste  | Teste de aceitação                                                                     |
| Objetivo do teste | Verificar se os produtos podem ser adicionados e removidos corretamente na tela Products |
| Pré-condição      | O usuário deve estar autenticado como problem_user                                     |
| Dados necessários | Usuário problem_user                                                                   |
| Requisito         | RF 2 - Funcionalidade Products                                                         |

| ID | TC-001 |
|----|--------|
| Título | Validar adição e remoção de produtos na tela Products |
| Pré-condições | O usuário deve estar autenticado como problem_user |
| Passos | 1. Realizar login com problem_user <br> 2. Adicionar um produto ao carrinho <br> 3. Clicar no botão "Remove" |
| Resultado esperado | O produto deve ser removido do carrinho e o botão deve voltar a exibir "Add to cart" |
| Status | Falhou |

| ID | TC-002                                                                                                                     |
|----|----------------------------------------------------------------------------------------------------------------------------|
| Título | Validar exibição das imagens dos produtos                                                                                  |
| Pré-condições | O usuário deve estar autenticado como problem_user                                                                         |
| Passos | 1. Realizar login com problem_user <br> 2. Acessar a tela Products <br> 3. Verificar as imagens exibidas para cada produto |
| Resultado esperado | Cada produto deve exibir sua imagem correspondente                                                                         |
| Status | Falhou                                                                                                                     |
