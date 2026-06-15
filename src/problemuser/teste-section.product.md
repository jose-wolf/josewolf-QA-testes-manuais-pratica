# Test Case - Tela de Catálogo de Produtos (problem_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-02 - Funcionalidade da seção Products |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Verificar se os produtos podem ser adicionados e removidos corretamente na tela Products |
| Pré-condição        | O usuário deve estar autenticado como `problem_user` |
| Dados Necessários   | Usuário `problem_user` |

## Casos de Teste

| ID | TC-PRODUTOS-001 |
|----|------------------|
| Título | Validar adição e remoção de produtos na tela Products |
| Pré-condições | O usuário deve estar autenticado como `problem_user` |
| Passos | 1. Realizar login com `problem_user` <br> 2. Adicionar um produto ao carrinho <br> 3. Clicar no botão "Remove" |
| Resultado esperado | O produto deve ser removido do carrinho e o botão deve voltar a exibir "Add to cart" |
| Status | Falhou |

| ID | TC-PRODUTOS-002 |
|----|------------------|
| Título | Validar exibição das imagens dos produtos |
| Pré-condições | O usuário deve estar autenticado como `problem_user` |
| Passos | 1. Realizar login com `problem_user` <br> 2. Acessar a tela Products <br> 3. Verificar as imagens exibidas para cada produto |
| Resultado esperado | Cada produto deve exibir sua imagem correspondente |
| Status | Falhou |