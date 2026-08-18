# TC-PRODUCT-PROBLEM_USER-001 — Validar informações exibidas nos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Pré-condição:** Usuário autenticado com `problem_user` e localizado na página **Products**.

**Passos:**

1. Verificar a imagem, o título, a descrição e o preço de cada produto.
2. Validar se as informações apresentadas correspondem corretamente ao mesmo produto.

**Resultado esperado:**  
Todos os produtos devem apresentar imagem, título, descrição e preço coerentes entre si, permitindo identificar corretamente cada produto.

**Status:** Falhou

**Observação:**  
As imagens exibidas não correspondem aos produtos apresentados. Os produtos exibem a mesma imagem de um cachorro, enquanto seus títulos e descrições representam produtos diferentes.

**Bug relacionado:** BUG-PRODUCT-PROBLEM_USER-001 — Imagens dos produtos não correspondem às informações apresentadas

****

# TC-PRODUCT-PROBLEM_USER-002 — Validar adição e remoção de produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Pré-condição:** Usuário autenticado com `problem_user` e localizado na página **Products**.

**Passos:**

1. Tentar adicionar cada produto disponível utilizando o botão **Add to cart**.
2. Verificar se cada produto selecionado é adicionado corretamente.
3. Clicar no botão **Remove** dos produtos adicionados.
4. Verificar se os produtos são removidos corretamente.

**Resultado esperado:**  
Todos os produtos disponíveis devem poder ser adicionados ao carrinho e removidos posteriormente através dos respectivos botões.

**Status:** Falhou

**Observação:**  
Apenas determinados produtos podem ser adicionados ao carrinho. Após a adição, o botão **Remove** é exibido, porém não remove o produto quando acionado.

**Bugs relacionados:**
- BUG-PRODUCT-PROBLEM_USER-002 — Não é possível adicionar determinados produtos ao carrinho
- BUG-PRODUCT-PROBLEM_USER-003 — Botão Remove não remove produtos adicionados

****

# TC-PRODUCT-PROBLEM_USER-003 — Validar ordenação dos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Pré-condição:** Usuário autenticado com `problem_user` e localizado na página **Products**.

**Passos:**

1. Localizar o seletor de ordenação na página **Products**.
2. Selecionar uma opção diferente da ordenação atual.
3. Verificar se a opção selecionada é aplicada.
4. Verificar se a lista de produtos é reorganizada conforme a ordenação escolhida.
5. Repetir o teste com as demais opções disponíveis.

**Resultado esperado:**  
A opção selecionada deve ser aplicada e a lista de produtos deve ser reorganizada corretamente conforme o critério de ordenação escolhido.

**Status:** Falhou

**Observação:**  
O seletor apresenta as opções de ordenação, porém a opção escolhida não é aplicada corretamente e os produtos permanecem na ordenação original.

**Bug relacionado:** BUG-PRODUCT-PROBLEM_USER-004 — Ordenação dos produtos não é aplicada

****

# TC-PRODUCT-PROBLEM_USER-004 — Validar atualização do contador do carrinho

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-004 — Validar atualização do contador do carrinho ao adicionar e remover produtos

**Pré-condição:** Usuário autenticado com `problem_user` e localizado na página **Products**.

**Passos:**

1. Adicionar produtos disponíveis ao carrinho.
2. Verificar se o contador do carrinho aumenta conforme os produtos são adicionados.
3. Remover um produto adicionado.
4. Verificar se o contador diminui após a remoção.
5. Repetir o processo com diferentes produtos.

**Resultado esperado:**  
O contador do carrinho deve aumentar e diminuir corretamente conforme produtos são adicionados ou removidos.

**Status:** Bloqueado

**Observação:**  
Não foi possível concluir a validação do contador do carrinho, pois apenas determinados produtos podem ser adicionados e o botão **Remove** não permite remover os produtos adicionados.

**Bugs relacionados:**
- BUG-PRODUCT-PROBLEM_USER-002 — Não é possível adicionar determinados produtos ao carrinho
- BUG-PRODUCT-PROBLEM_USER-003 — Botão Remove não remove produtos adicionados

****

# TC-PRODUCT-PROBLEM_USER-005 — Validar acesso aos detalhes do produto

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-005 — Validar acesso aos detalhes do produto

**Pré-condição:** Usuário autenticado com `problem_user` e localizado na página **Products**.

**Passos:**

1. Selecionar diferentes produtos disponíveis na página **Products**.
2. Observar a imagem, o título, a descrição e o preço apresentados na listagem.
3. Clicar no nome ou na imagem de cada produto.
4. Verificar a página de detalhes apresentada.
5. Comparar as informações da página de detalhes com as informações exibidas anteriormente na página **Products**.
6. Repetir a validação com diferentes produtos.

**Resultado esperado:**
Ao acessar os detalhes de um produto, a imagem, o título, a descrição e o preço devem permanecer coerentes com as informações apresentadas anteriormente na página **Products**.

**Status:** Falhou

**Observação:**
Foram identificadas inconsistências entre as informações exibidas na página **Products** e as respectivas páginas de detalhes. Principalmente as imagens dos produtos apresentam alterações ao acessar seus detalhes, fazendo com que o mesmo produto seja representado de formas diferentes entre as telas.

**Bug relacionado:** BUG-PRODUCT-PROBLEM_USER-005 — Informações dos produtos divergem entre a listagem e a página de detalhes
