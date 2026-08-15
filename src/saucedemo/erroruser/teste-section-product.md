# Test Case - Tela de Catálogo de Produtos (error_user)

| Campo               | Descrição                                                                                      |
|---------------------|------------------------------------------------------------------------------------------------|
| Requisito Funcional | RF-02 - Funcionalidade da Seção Products                                                       |
| Tipo de Teste       | Funcional                                                                                      |
| Subtipo de Teste    | Teste de Aceitação                                                                             |
| Objetivo do Teste   | Verificar se a seção Products exibe corretamente os produtos e permite manipulação adequada dos botões de carrinho |
| Pré-condição        | O usuário deve estar autenticado como `error_user`                                            |
| Dados Necessários   | Username: `error_user` \| Password: `secret_sauce`                                            |

---

## Casos de Teste

| Campo              | Descrição                                                                                                                                                                                          |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-PRODUTOS-001                                                                                                                                                                                    |
| Título             | Validar estado inicial dos botões de carrinho na tela Products (error_user)                                                                                                                        |
| Pré-condição       | Usuário autenticado como `error_user` e na tela **Products**                                                                                                                                       |
| Passos             | 1. Acessar `https://www.saucedemo.com/` <br> 2. Realizar login com `error_user` <br> 3. Observar o estado dos botões de todos os produtos (Add to cart / Remove)                                   |
| Resultado esperado | Produtos que ainda não foram adicionados ao carrinho devem exibir o botão **Add to cart**. Produtos já adicionados devem exibir o botão **Remove**, de forma consistente com o estado do carrinho. |
| Status             | Passou                                                                                                                                                                                             |
| Observação         | É possível adicionar apenas 3 produtos fixos.                                                                                                                                                      |

---


| Campo              | Descrição                                                                                                                                                                                                                                                  |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-PRODUTOS-002                                                                                                                                                                                                                                            |
| Título             | Validar comportamento do botão Remove na tela Products (error_user)                                                                                                                                                                                        |
| Pré-condição       | Usuário autenticado como `error_user`, com ao menos um produto exibindo botão **Remove** na tela **Products**                                                                                                                                              |
| Passos             | 1. Realizar login com `error_user` <br> 2. Acessar a tela **Products** <br> 3. Identificar um produto com botão **Remove** <br> 4. Clicar no botão **Remove** na tela Products <br> 5. Observar se há alteração visual do botão ou do contador de carrinho |
| Resultado esperado | Ao clicar em **Remove**, o produto deve ser removido do carrinho, o contador do carrinho deve ser atualizado e o botão na tela Products deve voltar a exibir **Add to cart**.                                                                              |
| Status             | Falhou                                                                                                                                                                                                                                                     |
| Observação         | Na tela Products, o botão **Remove** não apresenta nenhuma mudança visual aparente nem altera o contador, porém o produto é removido ao verificar o carrinho, indicando falha de atualização de estado na UI.                                              |


---

| Campo              | Descrição                                                                                                                                                  |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-PRODUTOS-003                                                                                                                                            |
| Título             | Validar exibição dos nomes dos produtos na tela Products (error_user)                                                                                      |
| Pré-condição       | Usuário autenticado como `error_user` e na tela **Products**                                                                                               |
| Passos             | 1. Realizar login com `error_user` <br> 2. Localizar o produto **Test.allTheThings() T-Shirt (Red)** <br> 3. Verificar os nomes exibidos para cada produto |
| Resultado esperado | Os produtos devem exibir nomes consistentes com o catálogo da aplicação.                                                                                   |
| Status             | Falhou                                                                                                                                                     |
| Observação         | O produto **Test.allTheThings() T-Shirt (Red)** mantém nomenclatura técnica.                                                                               |                                                                             
| Afeta              | `standard_user`,`problem_user`                                                                                                                             |

---

| Campo              | Descrição                                                                                                                                                  |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID                 | TC-PRODUTOS-004                                                                                                                                            |
| Título             | Validar exibição das descrições dos produtos na tela Products (error_user)                                                                                 |
| Pré-condição       | Usuário autenticado como `error_user` e na tela **Products**                                                                                               |
| Passos             | 1. Realizar login com `error_user` <br> 2. Localizar o produto **carry.allTheThings()** <br> 3. Verificar os nomes exibidos para cada produto |
| Resultado esperado | Os produtos devem exibir nomes consistentes com o catálogo da aplicação.                                                                                   |
| Status             | Falhou                                                                                                                                                     |
| Observação         | O produto **carry.allTheThings()** mantém nomenclatura técnica.       
| Afeta              | `standard_user`,`problem_user`                                                                                                                             |

