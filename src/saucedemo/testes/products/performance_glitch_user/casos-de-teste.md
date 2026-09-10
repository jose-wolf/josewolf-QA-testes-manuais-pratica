# TC-PRODUCT-PERFORMANCE_GLITCH_USER-001 — Validar informações exibidas nos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Pré-condição:** Usuário autenticado com `performance_glitch_user` e localizado na página **Products** (`/inventory.html`).

**Passos:**

1. Observar a listagem de produtos na página.
2. Verificar se a imagem de cada item é carregada de acordo com o produto correspondente.
3. Verificar a exibição do título de cada produto.
4. Verificar se a descrição de cada item está presente e legível.
5. Verificar se o preço de cada item é apresentado no formato correto ($XX.YY).

**Resultado esperado:**  
Todos os produtos devem apresentar imagens corretas, títulos descritivos, textos informativos e preços devidamente formatados, sem elementos ausentes ou quebrados.

**Status:** Passou

---

# TC-PRODUCT-PERFORMANCE_GLITCH_USER-002 — Validar adição e remoção de produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Pré-condição:** Usuário autenticado com `performance_glitch_user` e localizado na página **Products** (`/inventory.html`).

**Passos:**

1. Localizar um item na lista de produtos (ex.: *Sauce Labs Backpack*).
2. Clicar no botão **Add to cart**.
3. Verificar a alteração visual e o texto do botão.
4. Clicar no mesmo botão, agora exibindo **Remove**.
5. Verificar se o botão retorna ao estado inicial.

**Resultado esperado:**  
Ao clicar em **Add to cart**, o botão deve mudar imediatamente para **Remove**. Ao clicar em **Remove**, o botão deve voltar ao estado inicial exibindo **Add to cart**, sem apresentar falhas de interface ou travamentos.

**Status:** Passou

---

# TC-PRODUCT-PERFORMANCE_GLITCH_USER-003 — Validar ordenação dos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Pré-condição:** Usuário autenticado com `performance_glitch_user` e localizado na página **Products** (`/inventory.html`).

**Passos:**

1. Localizar o seletor de ordenação no canto superior direito da listagem.
2. Selecionar a opção **Name (Z to A)** e validar a ordenação.
3. Selecionar a opção **Price (low to high)** e validar a ordenação.
4. Selecionar a opção **Price (high to low)** e validar a ordenação.
5. Selecionar a opção **Name (A to Z)** e validar a ordenação.

**Resultado esperado:**  
A listagem deve reordenar os itens corretamente de acordo com cada filtro selecionado, mantendo a consistência dos dados de cada produto.

**Status:** Passou

**Observação:**  
A funcionalidade de ordenação atende aos critérios funcionais e classifica os produtos corretamente em todas as opções. Entretanto, foi identificado um atraso (delay) perceptível na renderização da tela ao alternar entre os filtros de ordenação.

---

# TC-PRODUCT-PERFORMANCE_GLITCH_USER-004 — Validar atualização do contador do carrinho ao adicionar e remover produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-004 — Validar atualização do contador do carrinho ao adicionar e remover produtos

**Pré-condição:** Usuário autenticado com `performance_glitch_user` e localizado na página **Products** (`/inventory.html`).

**Passos:**

1. Localizar um item na listagem e clicar no botão **Add to cart**.
2. Verificar a exibição e o valor numérico do contador (badge) no ícone do carrinho de compras.
3. Clicar no botão **Add to cart** de um segundo item diferente.
4. Verificar se o contador do carrinho incrementa para `2`.
5. Clicar no botão **Remove** de um dos produtos adicionados.
6. Verificar se o contador do carrinho decrementa para `1`.

**Resultado esperado:**  
O ícone do carrinho no cabeçalho deve atualizar o contador numérico de forma imediata tanto na adição quanto na remoção de itens, refletindo fielmente a quantidade de produtos selecionados.

**Status:** Passou

---

# TC-PRODUCT-PERFORMANCE_GLITCH_USER-005 — Validar acesso aos detalhes do produto

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-005 — Validar acesso aos detalhes do produto

**Pré-condição:** Usuário autenticado com `performance_glitch_user` e localizado na página **Products** (`/inventory.html`).

**Passos:**

1. Localizar um item na listagem (ex.: *Sauce Labs Backpack*).
2. Clicar no título ou na imagem do produto.
3. Aguardar o carregamento da tela de detalhes (`/inventory-item.html`).
4. Validar a exibição das informações do produto (imagem, título, descrição, preço e botão de ação).
5. Clicar no botão **Back to products**.

**Resultado esperado:**  
O sistema deve redirecionar o usuário para a página individual do produto, apresentando todas as informações completas e corretas, além de permitir o retorno ao catálogo.

**Status:** Passou

**Observação:**  
A navegação e os dados do produto são apresentados corretamente. Entretanto, foi identificado um atraso (*delay*) perceptível no carregamento da página de detalhes após o clique no item.
