# 🧪 CENÁRIOS DE TESTE – E-COMMERCE

---

## 🧩 Cenário 1 – Adicionar Produto ao Carrinho

### 🎯 Objetivo
Verificar se o usuário consegue adicionar produtos ao carrinho e se o carrinho atualiza as informações corretamente.

### 📌 Pré-condições
- Acesso à página inicial com produtos disponíveis.

### 🧪 Passos de Execução
1. Abrir a página inicial do e-commerce.
2. Escolher um produto visível na lista.
3. Clicar no botão “Adicionar” do produto escolhido.
4. Abrir o carrinho para visualizar os itens adicionados.

### 🔢 Dados de Entrada
- Quantidade inicial: 1
- Valor do produto selecionado

### ✅ Resultado Esperado
- O produto aparece no carrinho com o nome correto.
- O preço do produto está correto.
- A quantidade inicial é 1.
- O botão “Finalizar” está **ativo** *(corrigi isso: antes estava como “inativo”, o que não faz sentido se já tem produto no carrinho, a menos que você queira deixar o botão bloqueado propositalmente)*.

### 📊 Status do Teste
- [x] Passou  
- [ ] Falhou

---

## 🧩 Cenário 2 – Remover Produto do Carrinho

### 🎯 Objetivo
Verificar se o usuário consegue remover produtos do carrinho e se o carrinho atualiza as informações corretamente.

### 📌 Pré-condições
- O usuário já adicionou pelo menos 2 itens ao carrinho.
- O usuário está na tela do carrinho.

### 🧪 Passos de Execução
1. Acessar o carrinho de compras.
2. Verificar que existem ao menos 2 produtos.
3. Clicar no botão “-” ao lado do produto.
4. Verificar se a quantidade está sendo atualizada corretamente.
5. Repetir até remover todos os produtos do carrinho.

### 🔢 Dados de Entrada
- 2 produtos adicionados
- 2 produtos removidos

### ✅ Resultado Esperado
- O produto é removido do carrinho.
- O total do carrinho é atualizado corretamente.
- Ao remover todos os itens, aparece a mensagem: “Seu carrinho está vazio” e o botão “Ver Produtos”.

### 📊 Status do Teste
- [x] Passou  
- [ ] Falhou

---

## 🧩 Cenário 3 – Alterar Quantidade de um Produto no Carrinho

### 🎯 Objetivo
Verificar se o usuário consegue alterar a quantidade de um produto no carrinho e se o total é atualizado corretamente.

### 📌 Pré-condições
- O usuário já adicionou ao menos um produto ao carrinho.
- O usuário está na tela do carrinho.

### 🧪 Passos de Execução
1. Clicar no botão “Adicionar” de um produto.
2. Acessar o carrinho de compras no canto superior direito.
3. Verificar que há um produto listado.
4. Clicar no botão “+” ao lado do produto para aumentar a quantidade.
5. Clicar no botão “–” para reduzir a quantidade (até o mínimo permitido).
6. Observar a atualização da quantidade e do valor total do carrinho.

### 🔢 Dados de Entrada
- Quantidade inicial: 1  
- Produto 1: R$ 2.599,00  
- Produto 2: R$ 899,99  
- Quantidade final: 2 produtos diferentes  
- Preço total esperado: R$ 3.498,99

### ✅ Resultado Esperado
- A quantidade do produto é atualizada corretamente.
- O valor total do carrinho é recalculado automaticamente.
- Se a quantidade chegar a 0, o produto é removido.
- Se o carrinho ficar vazio, deve exibir a mensagem: “Seu carrinho está vazio”.

### 📊 Status do Teste
- [x] Passou  
- [ ] Falhou

---

## 🧩 Cenário 4 – Verificar Funcionamento do Botão “Ver Produtos”

### 🎯 Objetivo
Verificar se o botão “Ver Produtos” carrega corretamente a página inicial com a lista de produtos.

### 📌 Pré-condições
- O usuário já adicionou um produto ao carrinho.
- O usuário está na tela do carrinho.
- O carrinho está vazio após a remoção do produto.

### 🧪 Passos de Execução
1. Clicar no botão “Adicionar” de um produto.
2. Clicar no ícone do carrinho.
3. Remover o produto adicionado.
4. Clicar no botão “Ver Produtos”.

### 🔢 Dados de Entrada
- Produto adicionado e removido do carrinho.
- Clique no botão “Ver Produtos”.

### ✅ Resultado Esperado
- O botão “Ver Produtos” é exibido quando o carrinho está vazio.
- Ao clicar, o usuário é redirecionado para a tela inicial.
- A lista de produtos é carregada normalmente.

### 📊 Status do Teste
- [x] Passou  
- [ ] Falhou

---

### 🧩 Cenário 5 – Verificar estado do botão "Finalizar"

### 🎯 Objetivo
Verificar se o usuário consegue finalizar a compra com sucesso após adicionar itens ao carrinho.

### 📌 Pré-condições
- O usuário adicionou pelo menos um item ao carrinho.
- O usuário está na tela do carrinho.
- O botão “Finalizar” está ativo.

### 🧪 Passos de Execução
1. Adicionar 1 ou mais produtos ao carrinho.
2. Acessar o carrinho de compras.
3. Verificar se o botão “Finalizar” está habilitado.
4. Clicar no botão “Finalizar”.
5. Observar se é exibida uma mensagem de confirmação e se há redirecionamento.

### 🔢 Dados de Entrada
- Produto(s) adicionados ao carrinho.
- Total do pedido calculado corretamente.

### ✅ Resultado Esperado
- O botão “Finalizar” deveria executar a ação de finalização de compra.
- Exibir uma mensagem como: “Compra realizada com sucesso!”.
- Redirecionar o usuário para a tela inicial ou de confirmação.

### 📊 Status do Teste
- [ ] Passou  
- [x] Falhou


