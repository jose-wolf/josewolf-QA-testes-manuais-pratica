# TC-PRODUCT-STD_USER-001 — Validar informações exibidas nos produtos

**Funcionalidade:** Products  
**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Pré-condição:** Usuário autenticado com `standard_user` e localizado na página **Products**.

**Passos:**
1. Verificar a imagem, o título, a descrição e o preço de cada produto.
2. Validar se as informações apresentadas correspondem corretamente ao mesmo produto.

**Resultado esperado:**  
Todos os produtos devem apresentar imagem, título, descrição e preço de forma legível e coerente entre si, permitindo identificar corretamente cada produto.

**Status:** Falhou

**Observação:**  
Foram encontrados produtos cuja imagem não corresponde ao título e/ou à descrição apresentada, comprometendo a identificação correta do produto pelo usuário.

**Bug relacionado:** BUG-PRODUCT-STD_USER-001 — Inconsistência de informação

****

# TC-PRODUCT-STD_USER-002 — Validar adição e remoção de produtos

**Funcionalidade:** Products
**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Pré-condição:** Usuário autenticado com `standard_user` e localizado na página **Products**.

**Passos:**

1. Selecionar um produto disponível na página **Products**.
2. Clicar no botão **Add to cart**.
3. Verificar se o produto foi adicionado.
4. Clicar no botão **Remove**.
5. Verificar se o produto foi removido.

**Resultado esperado:**
O usuário deve conseguir adicionar um produto e removê-lo corretamente, com a interface refletindo cada ação realizada.

**Status:** Passou

****

# TC-PRODUCT-STD_USER-003 — Validar ordenação dos produtos

**Funcionalidade:** Products
**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Pré-condição:** Usuário autenticado com `standard_user` e localizado na página **Products**.

**Passos:**

1. Localizar o seletor de ordenação na página **Products**.
2. Selecionar a opção **Name (A to Z)**.
3. Verificar se os produtos são ordenados em ordem alfabética crescente.
4. Selecionar a opção **Name (Z to A)**.
5. Verificar se os produtos são ordenados em ordem alfabética decrescente.
6. Selecionar a opção **Price (low to high)**.
7. Verificar se os produtos são ordenados do menor para o maior preço.
8. Selecionar a opção **Price (high to low)**.
9. Verificar se os produtos são ordenados do maior para o menor preço.

**Resultado esperado:**
A lista de produtos deve ser reorganizada corretamente de acordo com cada opção de ordenação selecionada.

**Status:** Passou

****

# TC-PRODUCT-STD_USER-004 — Validar atualização do contador do carrinho

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-004 — Validar atualização do contador do carrinho ao adicionar e remover produtos

**Pré-condição:** Usuário autenticado com `standard_user` e localizado na página **Products**.

**Passos:**

1. Selecionar um produto disponível na página **Products**.
2. Clicar no botão **Add to cart**.
3. Verificar se o contador exibido no ícone do carrinho é atualizado.
4. Adicionar outros produtos ao carrinho.
5. Verificar se o contador aumenta de acordo com a quantidade de produtos adicionados.
6. Remover um produto.
7. Verificar se o contador diminui de acordo com a quantidade de produtos removidos.

**Resultado esperado:**
O contador do carrinho deve refletir corretamente a quantidade de produtos adicionados, sendo atualizado a cada adição ou remoção realizada.

**Status:** Passou

****

# TC-PRODUCT-STD_USER-005 — Validar acesso aos detalhes do produto

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-005 — Validar acesso aos detalhes do produto

**Pré-condição:** Usuário autenticado com `standard_user` e localizado na página **Products**.

**Passos:**

1. Selecionar um produto disponível na página **Products**.
2. Clicar no nome ou na imagem do produto.
3. Verificar se a página de detalhes do produto é exibida.
4. Validar se a imagem, o título, a descrição e o preço apresentados correspondem ao produto selecionado.
5. Retornar para a página **Products**.

**Resultado esperado:**
O usuário deve conseguir acessar a página de detalhes do produto selecionado, visualizar corretamente suas informações e retornar para a página **Products**.

**Status:** Passou
