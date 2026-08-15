# Bug Report - Seção Products (error_user)

| Campo                    | Descrição                                                                                                                                                                                             |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Bug ID                   | BUG-PROD-ERROR-001                                                                                                                                                                                    |
| Requisito Funcional      | RF-02 - Funcionalidade da Seção Products                                                                                                                                                              |
| Relacionado ao Test Case | TC-PRODUTOS-001                                                                                                                                                                                       |
| Título                   | Estado inicial dos botões de carrinho inconsistente na tela Products (error_user)                                                                                                                     |
| Severidade               | Média                                                                                                                                                                                                 |
| Prioridade               | Média                                                                                                                                                                                                 |
| Ambiente                 | Ubuntu Linux 24.04.4 \| Firefox / Brave                                                                                                                                                               |
| Passos para reproduzir   | 1. Acessar `https://www.saucedemo.com/` <br> 2. Realizar login com o usuário `error_user` <br> 3. Observar o estado dos botões de todos os produtos (Add to cart / Remove) na tela **Products**       |
| Resultado obtido         | Apenas 3 produtos exibem o botão **Remove** e podem ser manipulados; os demais produtos apresentam comportamento diferente dos outros perfis, permitindo a adição apenas desses 3 itens específicos.  |
| Resultado esperado       | Produtos não adicionados ao carrinho devem exibir **Add to cart** e produtos adicionados devem exibir **Remove**, de forma consistente com o estado real do carrinho, sem limitação a apenas 3 itens. |
| Impacto                  | Limita a experiência de compra do usuário `error_user`, que só consegue interagir adequadamente com parte do catálogo, gerando confusão sobre quais produtos podem ser adicionados.                   |
| Evidências               | [Evidência em vídeo](https://drive.google.com/file/d/1PzF4xUgYQKtP7Wc7oOYZaxoOOFlnoPFd/view?usp=sharing)                                                                                              |
| Categoria do defeito     | Funcional / UI                                                                                                                                                                                        |

---

| Campo                    | Descrição |
|--------------------------|-----------|
| Bug ID                   | BUG-PROD-ERROR-002 |
| Requisito Funcional      | RF-02 - Funcionalidade da Seção Products |
| Relacionado ao Test Case | TC-PRODUTOS-002 |
| Título                   | Botão Remove não atualiza estado visual na tela Products (error_user) |
| Severidade               | Média |
| Prioridade               | Média |
| Ambiente                 | Ubuntu Linux 24.04.4 \| Firefox / Brave |
| Passos para reproduzir   | 1. Realizar login com `error_user` <br> 2. Acessar a tela **Products** <br> 3. Identificar um produto com botão **Remove** <br> 4. Clicar em **Remove** na tela Products <br> 5. Observar o botão e o contador do carrinho |
| Resultado obtido         | Ao clicar em **Remove**, não há alteração visual na tela Products (o botão permanece como **Remove** e o contador do carrinho não é atualizado), embora o produto seja removido corretamente ao verificar o carrinho. |
| Resultado esperado       | Ao clicar em **Remove**, o produto deve ser removido do carrinho, o contador do carrinho deve ser atualizado e o botão na tela Products deve voltar a exibir **Add to cart**, refletindo o estado real do item. |
| Impacto                  | Gera inconsistência entre o estado real do carrinho e o estado exibido na tela Products, podendo levar o usuário a acreditar que o item ainda está no carrinho. |
| Evidências               | [Evidência em vídeo](https://drive.google.com/file/d/1PzF4xUgYQKtP7Wc7oOYZaxoOOFlnoPFd/view?usp=sharing) |
| Categoria do defeito     | Funcional / UI |
