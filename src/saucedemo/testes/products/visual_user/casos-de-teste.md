# TC-PRODUCT-VISUAL_USER-001 — Validar informações exibidas nos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Pré-condição:** Usuário autenticado com `visual_user` e localizado na página **Products**.

**Passos:**

1. Verificar os produtos apresentados na página **Products**.
2. Validar a imagem exibida em cada produto.
3. Validar o título e a descrição apresentados.
4. Verificar o preço dos produtos.
5. Comparar as informações apresentadas entre os diferentes elementos de cada produto.
6. Verificar se os cards mantêm uma apresentação visual consistente.

**Resultado esperado:**  
Todos os produtos devem apresentar imagem, título, descrição e preço corretos e coerentes entre si, mantendo uma apresentação visual consistente.

**Status:** Falhou

**Observação:**  
Foram identificadas diversas inconsistências nas informações e na apresentação dos produtos.

Entre os comportamentos observados estão:

- imagem que não corresponde ao produto apresentado;
- descrição com conteúdo inconsistente, como `carry.allTheThings()`;
- valores de produtos inconsistentes;
- formatação de preço inconsistente, como `$84.3`;
- diferenças na disposição e apresentação visual dos elementos dos produtos.

As inconsistências afetam diferentes produtos exibidos na página **Products**.

****

# TC-PRODUCT-VISUAL_USER-002 — Validar adição e remoção de produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Pré-condição:** Usuário autenticado com `visual_user` e localizado na página **Products**.

**Passos:**

1. Selecionar diferentes produtos disponíveis na página **Products**.
2. Clicar no botão **Add to cart**.
3. Verificar se o produto é adicionado corretamente.
4. Clicar no botão **Remove**.
5. Verificar se o produto é removido corretamente.
6. Repetir o processo com diferentes produtos.

**Resultado esperado:**  
Os produtos devem ser adicionados e removidos corretamente através dos respectivos botões.

**Status:** Passou

**Observação:**  
A funcionalidade de adicionar e remover produtos funciona corretamente. Entretanto, os botões apresentados nos cards dos produtos não mantêm um alinhamento visual consistente, sendo exibidos em posições diferentes entre os produtos.

****

# TC-PRODUCT-VISUAL_USER-003 — Validar ordenação dos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Pré-condição:** Usuário autenticado com `visual_user` e localizado na página **Products**.

**Passos:**

1. Localizar o seletor de ordenação na página **Products**.
2. Selecionar diferentes opções de ordenação disponíveis.
3. Verificar a posição dos produtos após cada alteração.
4. Quando necessário, acessar a página de detalhes dos produtos para comparar as informações apresentadas.
5. Retornar à página **Products** e continuar a validação da ordenação.

**Resultado esperado:**  
Os produtos devem ser reorganizados corretamente de acordo com a opção de ordenação selecionada, e as informações exibidas na página **Products** devem permitir identificar visualmente essa ordenação.

**Status:** Passou

**Observação:**  
A funcionalidade de ordenação é aplicada corretamente. Entretanto, as informações exibidas na página **Products**, principalmente os preços, apresentam inconsistências que fazem a ordenação parecer incorreta visualmente.

Ao acessar individualmente os produtos e comparar os valores apresentados na página de detalhes, é possível confirmar que a ordem dos produtos corresponde ao critério selecionado.

A inconsistência está relacionada aos dados exibidos na listagem de produtos e não à funcionalidade de ordenação.

****

# TC-PRODUCT-VISUAL_USER-004 — Validar atualização do contador do carrinho

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-004 — Validar atualização do contador do carrinho ao adicionar e remover produtos

**Pré-condição:** Usuário autenticado com `visual_user` e localizado na página **Products**.

**Passos:**

1. Adicionar um produto ao carrinho.
2. Verificar se o contador do carrinho é atualizado.
3. Adicionar outros produtos e validar o incremento do contador.
4. Remover um produto adicionado.
5. Verificar se o contador é decrementado corretamente.
6. Repetir o processo com diferentes produtos.

**Resultado esperado:**  
O contador do carrinho deve aumentar e diminuir corretamente de acordo com a quantidade de produtos adicionados ou removidos.

**Status:** Passou

****

