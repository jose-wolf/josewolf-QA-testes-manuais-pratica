# Bug Report - Checkout (problem_user)

| Campo                    | Descrição |
|--------------------------|-----------|
| Requisito Funcional      | RF-05 - Funcionalidade Checkout |
| Bug ID                   | BUG-CHECKOUT-001 |
| Relacionado ao Test Case | TC-CHECKOUT-001 |
| Título                   | Campo Last Name não permite digitação corretamente |
| Severidade               | Alta |
| Prioridade               | Alta |
| Passos para reproduzir   | 1. Realizar login com `problem_user` <br> 2. Adicionar produto ao carrinho <br> 3. Acessar o carrinho <br> 4. Clicar em "Checkout" <br> 5. Preencher o campo First Name <br> 6. Tentar preencher o campo Last Name |
| Resultado obtido         | O campo Last Name não permite inserir texto corretamente e, ao digitar, o caractere informado substitui o valor do campo First Name |
| Resultado esperado       | O campo Last Name deve permitir a digitação normalmente, sem alterar o conteúdo de outros campos |
| Impacto                  | Impede o preenchimento correto dos dados obrigatórios do checkout e bloqueia o avanço do fluxo de compra |
| Ambiente                 | Ubuntu Linux 24.04.4 <br> Firefox <br> Brave |
| Evidências               | [Vídeo da reprodução do defeito](https://drive.google.com/file/d/1ArUxTIAsQXgXXEBp7RobDg0zaXfzTMHQ/view?usp=sharing) |
| Categoria do defeito     | Funcional |

