<!-- add-breadcrumbs -->
#Pacote de Produtos

**Um Pacote de Produto é um ficheiro mestre aonde voce pode listar os itens existentes que estão agrupados e vendidos como um conjunto (ou pacote).** 

Por exemplo, quando voce vende um telefone, voce precisa ter a certeza que o carregador, cabo, e injector do sim são entregues e que o nivel de stock destes itens são deduzidos. 
Para endereçar este cenario, voce criar um Pacote de Produtos para o item principal, i.e. telefone. Depois lista itens a serem entregues i.e. telefone + carregador + cabo + injector do sim como são chamados de "Filho dos Itens".

Um Pacote de Produtos pode ser visto como uma "Lista-de-Materiais" no lado das vendas. 

De seguinda são os passos para configurar um Pacote de Produtos e usar nas transações de vendas.

Para acessar Pacote de Produtos, va para:
> Home > Vendas > Itens e Preços > Pacote de Produtos

## 1. Pre-requisitos
Antes de criar e usar um Pacote de Produto, é aconselhavel que voce crie os seguintes:

* [Item](/docs/user/manual/pt/inventario/item)

## 2. Como criar um Pacote de Produtos
1. Va para a lista de Pacote de Produtos, clique em Novo.
2. Selecione o Item principal (Pai), crie um se não estiver ja criado. Tenha a certeza de ter Actualizar Stock não activo ao criar um Item principal (Pai). eg: Conjunto de Jantar.
1. Digite o preço para o parente do item, este será procurado ao criar a transação.
1. Voce pode digitar uma descrição para uso interno.
3. Digite os produtos para fazerem parte do pactoe na tabela de Itens e digite as quantidades.
4. Salve.
<img class="screenshot" alt="Product Bundle" src="{{docs_base_url}}/assets/img/selling/product-bundle.png">

### 2.1 Selecionando o Item Principal (Pai)

No Pacote de Produtos, tem duas secções. O "Item Principal" e a lista de itens a ser entregue (Child Items).

O "Item Principal" deve ser visto como um navio ou item virtual e não como um produto fisico.
O "Item Principal" deve ser um <b>item de não stock</b>. Para criar um <b>item de não stock</b> voce desmarcar "Manter Stocks" no Formulario do Item.
Este é um item de não stock porque não tem em armazem somente os "Itens filhos". 
Se voce quiser manter stock para Itens Principais, voce deve criar uma Lista de Material (LDM) 
e empacotar usando Transações de Entrada de Stock.

### 2.2 Selecionado Itens de Filho

Na tabel de Itens, voce irá listar todos os itens filho do qual nós mantemos o stock e são entregues ao cliente.
Lembre-se: O "Item Principal" é somente virtual, então o seu produto principal (um telefone no exemplo aqui) tambem de ser ser listado na Lista de Itens filhos dos Itens (ou Pacote).

## 3. Funcionalidades
### 3.1 Pacote de Produtos numa Transaçãode Vendas

Ao fazer transações de Vendas (Factura de Vendas, Ordem de Vendas, Guia de Remessa) o Item Principal irá ser selecionado na tabela principal do item.

<img class="screenshot" alt="Product Bundle" src="{{docs_base_url}}/assets/img/selling/product-bundle.gif">

Na seleção de um Item Principal na tabel de itens, os itens filho serao procurados na tabela de Pacote de Produtos da transação. Se o iten filho tiver numero de serie, voce irá poder especificar o Numero de Serie
na tabela de pacote. Ao submeter a transação, o sistema irá deduzir o nivel de stock dos itens filho apartir do armazem especificado na tabela de Pacote de Produtos.

<div class="well"><b>Utilizando Pacote de Produtos para Gerir Ofertas/Esquemas:</b>
<br>
Este foi descoberto quando um cliente ao negociar produtos de nutrição pediu a funcionalidade para gerir ofertas como "Compre Um Leve mais Um". Para gerir o mesmo, ele criou um item não stock que foi usado como Item Principal. Na descrição do item, ele inseriu os detalhes da oferta com a imagem do item mostrando a oferta. O produto em venda foi selecionado no Pacote de Produtos aonde a quantidade foi dois. Assim sendo sempre que eles vendem uma quantidade do item principal dentro da oferta, o sistema deduz duas quantidades do produto no Armazem.</div>

### 4. Topicos Relacionados
1. [Item](/docs/user/manual/pt/inventario/item)

{next}
