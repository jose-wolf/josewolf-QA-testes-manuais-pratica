# Test Case - Filtros de Produtos (problem_user)

| Campo               | Descrição |
|---------------------|-----------|
| Requisito Funcional | RF-02 - Funcionalidade Products |
| Tipo de Teste       | Funcional |
| Subtipo de Teste    | Teste de Aceitação |
| Objetivo do Teste   | Verificar se os filtros de ordenação funcionam corretamente na tela Products |
| Pré-condição        | O usuário deve estar autenticado como `problem_user` |
| Dados Necessários   | Usuário `problem_user` |

## Casos de Teste

| ID | TC-FILTROS-001 |
|----|------------------|
| Título | Validar funcionamento dos filtros de ordenação na tela Products |
| Pré-condições | O usuário deve estar autenticado como `problem_user` |
| Passos | 1. Realizar login com `problem_user` <br> 2. Acessar a tela Products <br> 3. Selecionar cada opção de filtro disponível |
| Resultado esperado | Os produtos devem ser reordenados corretamente conforme a opção selecionada |
| Status | Falhou |