# TC-PRODUCT-ERROR_USER-001 — Validar informações exibidas nos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-001 — Validar as informações exibidas nos produtos

**Pré-condição:** Usuário autenticado com `error_user` e localizado na página **Products**.

**Passos:**

1. Verificar a imagem, o título, a descrição e o preço de cada produto.
2. Validar se as informações apresentadas correspondem corretamente ao mesmo produto.
3. Comparar título e descrição dos produtos exibidos.

**Resultado esperado:**  
Todos os produtos devem apresentar imagem, título, descrição e preço de forma legível e coerente entre si, permitindo que o usuário identifique corretamente cada produto.

**Status:** Falhou

**Observação:**  
Foram identificadas inconsistências no título e/ou na descrição de determinados produtos, fazendo com que as informações apresentadas não representem corretamente o produto exibido.

**Bug relacionado:** BUG-PRODUCT-ERROR_USER-001 — Inconsistência nas informações dos produtos

****

# TC-PRODUCT-ERROR_USER-002 — Validar adição e remoção de produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-002 — Validar adição e remoção de produtos

**Pré-condição:** Usuário autenticado com `error_user` e localizado na página **Products**.

**Passos:**

1. Tentar adicionar diferentes produtos disponíveis utilizando o botão **Add to cart**.
2. Verificar se cada produto selecionado é adicionado corretamente.
3. Clicar no botão **Remove** dos produtos adicionados.
4. Verificar se os produtos são removidos corretamente.

**Resultado esperado:**  
Todos os produtos disponíveis devem poder ser adicionados ao carrinho e removidos posteriormente através dos respectivos botões.

**Status:** Falhou

**Observação:**  
Apenas determinados produtos podem ser adicionados ao carrinho. Após a adição, o botão **Remove** é exibido, porém não permite remover os produtos adicionados.

**Bugs relacionados:**
- BUG-PRODUCT-ERROR_USER-002 — Não é possível adicionar determinados produtos ao carrinho
- BUG-PRODUCT-ERROR_USER-003 — Botão Remove não remove produtos adicionados

****

# TC-PRODUCT-ERROR_USER-003 — Validar ordenação dos produtos

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-003 — Validar ordenação dos produtos

**Pré-condição:** Usuário autenticado com `error_user` e localizado na página **Products**.

**Passos:**

1. Localizar o seletor de ordenação na página **Products**.
2. Abrir o seletor de ordenação.
3. Selecionar uma opção diferente da ordenação atual.
4. Verificar se os produtos são reorganizados conforme a opção selecionada.
5. Repetir o teste utilizando diferentes opções de ordenação.

**Resultado esperado:**  
O sistema deve permitir selecionar qualquer opção de ordenação disponível e reorganizar corretamente a lista de produtos de acordo com o critério escolhido, sem apresentar erros.

**Status:** Falhou

**Observação:**  
Durante a utilização do seletor de ordenação, o sistema apresenta a mensagem:

`Sorting is broken! This error has been reported to Backtrace.`

O comportamento impede o funcionamento correto da ordenação dos produtos.

**Bug relacionado:** BUG-PRODUCT-GLOBAL-001 — Erro ao utilizar a ordenação dos produtos

# TC-PRODUCT-ERROR_USER-004 — Validar atualização do contador do carrinho

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-004 — Validar atualização do contador do carrinho ao adicionar e remover produtos

**Pré-condição:** Usuário autenticado com `error_user` e localizado na página **Products**.

**Passos:**

1. Adicionar produtos disponíveis ao carrinho.
2. Verificar se o contador do carrinho aumenta conforme os produtos são adicionados.
3. Remover um produto adicionado.
4. Verificar se o contador diminui após a remoção.
5. Repetir o processo com diferentes produtos.

**Resultado esperado:**  
O contador do carrinho deve aumentar e diminuir corretamente de acordo com a quantidade de produtos adicionados ou removidos.

**Status:** Bloqueado

**Observação:**  
Não foi possível concluir a validação completa do contador do carrinho, pois apenas determinados produtos podem ser adicionados e o botão **Remove** não permite remover os produtos adicionados.

**Bugs relacionados:**
- BUG-PRODUCT-ERROR_USER-002 — Não é possível adicionar determinados produtos ao carrinho
- BUG-PRODUCT-ERROR_USER-003 — Botão Remove não remove produtos adicionados

****

# TC-PRODUCT-ERROR_USER-005 — Validar acesso aos detalhes do produto

**Funcionalidade:** Products

**Cenário relacionado:** CN-PRODUCT-005 — Validar acesso aos detalhes do produto

**Pré-condição:** Usuário autenticado com `error_user` e localizado na página **Products**.

**Passos:**

1. Selecionar um produto disponível na página **Products**.
2. Clicar no nome ou na imagem do produto.
3. Verificar se a página de detalhes do produto é exibida.
4. Validar a imagem, o título, a descrição e o preço apresentados.
5. Retornar para a página **Products**.
6. Repetir a validação com os demais produtos.

**Resultado esperado:**  
Todos os produtos devem abrir corretamente suas respectivas páginas de detalhes e apresentar imagem, título, descrição e preço coerentes com o produto selecionado.

**Status:** Falhou

**Observação:**  
A imagem, o título e o preço dos produtos são apresentados corretamente. Entretanto, a descrição de todos os produtos não é carregada e, em seu lugar, o sistema apresenta a mensagem:

`A description should be here, but it failed to render! This error has been reported to Backtrace.`

**Bug relacionado:** BUG-PRODUCT-ERROR_USER-005 — Descrição dos produtos não é renderizada na página de detalhes