<!-- add-breadcrumbs -->
# Solicitação de Material

**Uma Solicitação de Material é um simples documento indentificando a necessidade de um conjunto de Itens (produtos ou serviços) por uma razão em particular.**

Uma Solicitação de Material pode ter varios motivos:

* **Compras**: Se o material sendo pedido é para ser comprado.
* **Transferencia de Material**: Se o material sendo pedido é para ser mudado de armazem.
* **Pedido de Material**: Se o material sendo pedido for requisitado por motivos como fabrico.
* **Fabrico:** Se o material pedido é para ser produzido.
* **Providenciado pelo Cliente**: Se o material pedido é para ser entregue pelo Cliente. Para saber mais sobre isto, viste a pagina [Item Providenciado pelo Cliente](/docs/user/manual/pt/fabrico/artigos/customer-provided-items) .

<img class="screenshot" alt="Material Request" src="{{docs_base_url}}/assets/img/buying/material-request-flowchart.png">

Para acessar a lista de Solicitação de Material, va para:
> Home > Inventario > Transações de Stock > Solicitação de Material

## 1. Como criar uma Solicitação de Material
1. Va para a lista de Solicitação de Material, clique em Novo.
1. Digite a Data necessaria.
1. Selecione um dos motivos listados.
1. Voce pode procurar Itens de uma LDM, Ordem de Venda, ou Pacote de Produtos.
  ![Procura SM apartir de](/docs/assets/img/stock/mr-fetch-from.png)
1. Selecione o Item e defina a quantidade.
1. Selecione o Armazem para os Itens necessarios.
1. Voce pode mudar a Data Necessario até para cada Item na tabela.
1. Salvar e Submeter.

### 1.1 Maneiras Alternativas de criar uma Solicitação de Material
Uma Solicitação de Material pode ser gerado automaticamente:

* Apartir de [Ordem de Vendas](/docs/user/manual/pt/vendas/ordem-vendas).
* Quando a Quantidade Projecta de um Item em Armazem (Warehouses) atinge um certo nivel de stock.
* Apartir do seu [Plano de Produção](/docs/user/manual/pt/fabrico/plano-de-producao) para planificar as suas actividade de fabrico.

Se os seu Itens são itens de inventario, voce deve tambem mencionar o Armazem aonde voce espera estes Itens serem entregues. Isto ajuda a rastrear a [Quantidade Projectada](/docs/user/manual/pt/inventario/quantidade-projectada) para este Item.

> Info: Solicitação de Material não é obrigatorio. Ẽ ideal se voce tem compras
centralizadas no qual pode recolher as informações de varios departamentos.

### 1.2 Estados

Estes são os estados que uma Solicitação de Material pode ter:

* **Rascunho**: Um rascunho é salvo mas ainda não foi submetido no sistema.
* **Submetido**: Documento submetido no sistema.
* **Parado**: Se os materiais não forem mais necessarios a Solicitação de Material pode ser parada.
* **Cancelados**: Os materiais não são necessarios e o pedido é cancelado.
* **Pendente**: A Compra/Fabrico está pendente para completar a Solicitação de Material.
* **Parcialmente Pedido**: Ordens de Compra para alguns Itens apartir de uma Solicitação de Material foram feito e alguns estão pendentes.
* **Pedido**: Todos os Itens na Solicitação de Material foram pedidos via Ordem de Compra.
* **Solicitado**: Os materiais foram solicitados usando um Registo de Solicitação de Material.
* **Transferido**: Os materiais necessarios são transferidos de um Armazem para outro usando a Entrada de Stock.
* **Recebido**: Os materiais foram pedido e foram recebidos no seu Armazem usando o Recibo de Compra.

## 2. Funcionalidades
### 2.1 Tabel de Itens
* **Codigo de Barras**: Voce pode rastrear os Itens usando [Codigo de Barras](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras).

* O Codigo do Item, nome, descrição, Imagem, e Fabricante serao procurados na tabela do Item.

* **Scan Codigo de Barras**: Voce pode adiconar Itens na tabela de Itens fazendo o scan dos Codigos de Barra se voce tiver um leitor. Saiba mais [aqui](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras)

* A UdM, Factor de Conversão, e Valor serao procurados. Voce pode trocar o Armazem no qual o material esta a ser solicitado.

* Detalhes de contabilidade como Conta de Despesas e Dimensão Contabil pode ser definidos para os Itens.

* Quebra de Pagina irá criar uma quebra de pagina antes de imprimir o item.

### 2.2 Configurando Armazens
* **Definir Armaze**: Opcionalmente, voce pode definir o Armazem aonde os Itens soclicitados ficaram. Este sera procurado no campo 'Para Armazem' na linha da tabela do Item.

### 2.3 Mais Informações
No campo 'Solicitado para ', voce pode definir um Referencia de onde a Solicitação de Material foi gerada.

### 2.4 Detalhes de Impressão
#### Cabeçalho
Voce pode imprimr a Solicitação de Material com o cabeçalho da sua Empresa. [Clique aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta) para saber mais.

#### Imprimir Cabeçalhos
Cabeçalhos de Recibo de Compras pode ser alterados ao imprimir o documento. Voce pode fazer selecionando **Imprimir Cabeçalho**. Para criar um novo Imprimir Cabeçalho va para: Home > Configurações > Impressão > Imprimir Cabeçalho. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/imprimir-cabeçalhos).

### 2.5 Termos e Condições
Em transações de Vendas/Compras pode have a necessidade de certos Termos e Condições com base no Fornecedor que presta os serviços ou bens ao Cliente. Voce pode aplicar Termos e Condições a transações e eles vão aparecer ao imprimir o documento. Para saber sobre Termos e Condições, [clique aqui](/docs/user/manual/pt/configuração/imprimir/termos-e-condições)

### 2.6 Depois de Submeter
Voce pode criar os seguintes documentos:

* [Solicitação de Cotação](/docs/user/manual/pt/compras/solicitação-cotação)
* [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
* [Cotação do Fornecedor](/docs/user/manual/pt/compras/cotação-do-fornecedor)

<img class="screenshot" alt="Material Request" src="{{docs_base_url}}/assets/img/stock/material-request.png">


### 2.7 Gerar Solicitação de Material Automaticamente

Solicitação de Material pode ser gerado automaticamente activando a configuração em [Configurações de Stock](/docs/user/manual/pt/inventario/configuracoes-stock#9-requisição-de-material-automatica) e definindo o nivel no [formulario do Item](/docs/user/manual/pt/inventario/item#34-encomenda-automatica). Quando o nivel de stock estiver abaixo de um certa quantidade, configurando uma encomenda irá automaticamente criar uma Solicitação de Material para este Item.

## 3. Video
<div>
  <div class="embed-container">
    <iframe src="https://www.youtube.com/embed/55Gk2j7Q8Zw?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
  </div>
</div>

### 4. Topicos Relacionados
1. [Item](/docs/user/manual/pt/inventario/item)
1. [Auto Criação da Solicitação de Material](/docs/user/manual/pt/inventario/artigos/auto-criacao-solicitacao-material)
1. [Lista de Escolhas](/docs/user/manual/pt/inventario/lista-de-escolhas#23-crie-a-lista-de-escolha-apartir-da-solicitação-de-material)
1. [Solicitação de Cotação](/docs/user/manual/pt/compras/solicitação-cotação)
1. [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
1. [Cotação do Fornecedor](/docs/user/manual/pt/compras/cotação-do-fornecedor)
