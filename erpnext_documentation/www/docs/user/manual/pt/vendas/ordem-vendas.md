<!-- add-breadcrumbs -->
# Ordem de Venda

**Uma Ordem de Venda é a confirmação de um pedido do seu cliente.**

Normalmente é um Contracto com o seu Cliente. Uma vez a confirmação da Cotação pelo Cliente voce pode converter a Cotação em uma Ordem de Venda.

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/selling-flow-so.png">

Para acessar Ordens de Venda, va para:
> Home > Vendas > Vendas > Ordem de Venda

## 1. Pre-requisitos
Antes de criar e usar uma Ordem de Venda, é aconselhavel criar os seguintes:

* [Cliente](/docs/user/manual/pt/CRM/cliente)
* [Item](/docs/user/manual/pt/inventario/item)

## 2. Como criar uma Ordem de Venda
1. Va para a lista de Ordem de Venda, clique em Novo.
1. Selecione o Cliente.
1. Defina a 'Data de Entrega' - aplicada em toda a ordem.
1. Com o Tipo de Ordem, voce pode definir se é uma Ordem de Venda, Ordem de Manutenção, ou Online [Shopping Cart](/docs/user/manual/pt/website/shopping-cart) na sua pagina. Por defeito, este valor esta definido para "Vendas".
1. Na "Ordem de Compra do Cliente" voce pode digitar o Numero de Ordem de Compra do Cliente ou outros detalhes no qual podem ser uteis como referencia.
1. Digite os itens e quantidades a serem entregues na tabela de Item. Se o Preço do Item estiver definido para os itens, o campo Preço irá ser preenchido automaticamente. Se não, digite o Preço manual. Voce pode escrever por cima dos Preços do Item preenchidos caso queira trocar o valor.
1. Clique "Salvar" para salvar em rascunho a Ordem de Venda.
1. "Submeter" para submeter a Ordem de Venda no Sistema.

### 2.1 Outras formas de criar uma Ordem de Venda
1. Voce pode tambem criar uma Ordem de Venda apartir de uma Cotação submetida pelo botão Criar no topo a direita.

  <img class="screenshot" alt="Make Sales Order from Quotation" src="{{docs_base_url}}/assets/img/selling/make-SO-from-quote.png">

1. Ou pode criar uma Nova Ordem de Venda e puxar os detalhes aparti de uma Cotação.

  <img class="screenshot" alt="Make Sales Order from Quotation" src="{{docs_base_url}}/assets/img/selling/so-from-quote.gif">

Para permitir por Cliente, por Regra de Preço, ("Cliente A" paga $1.00 por "Item 1" mas "Cliente B" paga $1.25 por "Item 1"), tem uma caixinha 'Permitir Usuario Editar a Lista de Preço numa Transação' em [Configurações de Venda](/docs/user/manual/pt/vendas/configurações-venda). Este permite salvar o preço especifico do item por cliente quando voce muda o preço na Ordem de Venda.

## 3. Funcionalidades

### 3.1 Moeda e Lista de Preço
Voce pode definir a moeda no qual a cotação/ordem de venda sera enviada. Se voce definir uma Lista de Preço, então os preços do item vao ser procurados apartir desta lista. Selecionando 'Ignorar Regra de Preço' irá ignorar as [Regras de Preço](/docs/user/manual/pt/contabilidade/regras-preço) definido em Contabilidade > Regras de Preço.

Para saber mais sobre Listas de Preço, [Clique aqui](/docs/user/manual/pt/inventario/lista-preços).

Para saber como gerir transações em varias moedas, [clique aqui](/docs/user/manual/pt/contabilidade/artigos/gerir-transações-multiplas-moedas).

### 3.1 Definir Armazem Fonte Padrão
Se voce o mesmo stock em varios armazens, definindo um armazem aqui irá fazer com que todos os itens da tabela de itens procurem neste armazem. Voce precisar ter stock disponiveil no 'armazem fonte' que estiver a escolher. Note que esta opção irá subscrever o 'Armazem Padrão' que definiu na tabela Item.

### 3.2 A tabela de Itens

* **Data de Entrega para cada item**: Se existem varios itens e voce digitou uma data de entrega na primeira linha, a data será copiada para todas as outras linhas até aonde estiver vazio. Voce tera de definir estes se não estiver definido no top da Ordem de Venda.

    Uma Ordem de Venda mostra o Valor cobrado, taxa de avaliação, e o lucro na tabela de itens quando voce faz um clique no triangulo invetido para alargar a linha.

    Voce pode tambem adiconar Itens na tabela de Itens fazendo o scan dos codigos de barra se voce tiver um leitor. Saiba como rastrear [aqui](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras)

* **Armazem de Entrega**: Este é o armazem no qual o stock sera levantado para ser entregue ao seu cliente.

* **Drop Ship**: Esta é uma situação aonde voce não guarda itens em armazem mas faz a entrega dos itens directamente ao cliente apartir do seu distribuidor. Para activar o drop shipping para um item selcione o 'Fornecedor entrega ao Cliente'. Quando voce activa isto, a opção do Armazem de Entrega ira desaparecer vendo que não a enviar o item. Selecione o fornecedor no campo 'Fornecedor'.

    Se voce criar uma Ordem de compra apartir desta ordem de venda, ela será criada para o fornecedor que voce selecionar aqui e somente os itens são validos para uma drop shipping.

* **Planeamento**: Para saber mais sobre os campos aqui no plano [clique aqui](/docs/user/manual/pt/inventario/quantidade-projectada).

Os outros campos na tabela de itens são similares como explicados em [Contações](/docs/user/manual/pt/vendas/proforma#33-os-itens-da-tabela).

### 3.3 Lista de Pacotes

Este esta ligado a [Pacote de Produtos](/docs/user/manual/pt/vendas/pacode-de-produtos) e aparece somente quando a transação envolve um pacote de produto.

A tabela “Lista de Pacote” sera actualizada automaticamente quando voce “Salva” a Ordem de Venda. Se algum Item na tua tabela for Pacote de Produto (pacotes), então a “Lista de Pacote” irá conter a lista (detalhada) dos seu Itens.

Sera pedido para selcionar o Armaem de Entrega mesmo para um item de pacote, este armazem sera actualizado depois na Lista de Pacotes do item. Voce pode mudar o Armazem, numero de serie e lote para os itens na lista de pacote no caso os itens no seu pacote de produtos forem diferentes que do armazem.

Aqui esta como a Lista de Pacotes fica:

<img class="screenshot" alt="Packing List" src="{{docs_base_url}}/assets/img/selling/so-packing-list.png">

### 3.4 Impostos e Taxas
Para adicionar impostos a sua Cotação, voce pode selecionar um [Modelo de Impostos de Vendas e Taxas](/docs/user/manual/pt/vendas/modelo-impostos-taxas-vendas) ou adiconar os impostos manualmente na tabela de Impostos de Vendas e Taxas.

O total das taxas e impostos vao ser mostrados na tabela. Clique em Tax Breakup para mostrar todos os componentes e valores.

<img class="screenshot" alt="Taxes in Quotation" src="{{docs_base_url}}/assets/img/selling/sales-order-taxes.png">

#### Regra de Envio
Uma Regra de Envio ajuda a definir o custo do envio de um Item. O custo normalmente irá aumentar com a distancia do envio. Para saber mais, visite a pagina [Regra de Envio](/docs/user/manual/pt/vendas/regra-envio).

Se uma Categoria de Imposto for selecionada, o modelo e a tabel de imposto sera automaticamente preenchida. Para saber mais, visite [esta pagina](/docs/user/manual/pt/contabilidade/categoria-imposto).

### 3.5 Desconto Adicional
Para alem de oferecer desconto por item, voce pode adiconar um desconto para a ordem de venda completa nesta secção. Este desconto pode ser com base no Total Geral  i.e., depois do imposto/taxas ou Total Liquido i.e., antes imposto/taxas. O desconto adicoinar pode ser aplicado como percentagem ou valor.

Leia [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto) para mais detalhes.

### 3.6 Termos de Pagamento
As vezes o pagamento não é feito na totalidade. Dependendo do acordo, metade do pagamento pode ser feito antes do envio e a outra metadad apos recepção dos bens/serviços. Voce pode adicionar modelo de Termos de Pagamento ou adiconar os termos manualmente nesta secção.

Para saber sobre os Termos de Pagamento, [clique aqui](/docs/user/manual/pt/contabilidade/termos-pagamento).

### 3.7 Termos e Condições
Em transações de Vendas/Compras podem ter certos Termos e Condições com base no qual o Fornecedor fornece bens ou serviços ao Cliente. Voce pode aplicar os Termos e Condições a transações que vão aparecer ao imprimir o documento. Para saber sobre Termos e Condições, [clique aqui](/docs/user/manual/pt/configuração/imprimir/termos-e-condições)

### 3.8 Configurações de Impressão
#### Cabeçalho
Voce pode imprimir a sua Cotação/Ordem de Venda com o cabeçalho da sua empresa. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

'Agrupar itens iguais' irá agrupar os itens iguais adiconados varias vezes na tabela. Este pode ser visto quando imprimir.

#### Imprimir Cabeçalho
Cotações podem ter o titulo de “Factura Proforma” ou “Proposta”.
Voce pode fazer isso selecionando **Imprimir Cabeçalho**. Para criar um novo Imprimir Cabeçalho va para: Home > Configurações > Impressão > Imprimir Cabeçalho. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/imprimir-cabeçalhos).

### 3.9 Mais Informações
* **Campanha:** Uma campanha de vendas pode ser associada com a cotação. Um conjunto de cotações podem fazer parte de uma campanha de vendas.
* **Fonte:** O tipo de Fonte da Lead pode ser ligada se a cotação for para uma lead, uma campanha, apartir de um fornecedor, uma exibição,etc,. Selecionando um Cliente existente se for para um cliente.
* **Referencia de Solicitação Entre Empresa**: Se duas ou mais empresa fazem parte da mesma organização ou tem uma relação, voce pode ligar a Ordem de Compra a esta Ordem de Venda. Saiba mais sobre facturas inter-empresas [aqui](/docs/user/manual/pt/contabilidade/facturas-inter-empresa).
* **Projecto**: Se a Ordem de Venda fizer parte de um projecto, voce pode ligar aqui e o Progresso do Projecto ira actualizar.

### 3.10 Cobrança e Status de Entrega

* **Status**: O status de Ordem de Vendas quer seja Rascunho, Em Espera, Para Entregar e Cobrar, Para Cobrar, Para Entregar, Completado, Cancelado ou Fechado.
* **Valor Cobrado e Percentagem Entregue**: A percentagem do valor cobrado e os itens entregues apartir da Ordem de Venda.

### 3.11 Comissão
Se a venda teve lugar por intermedio de uma dos seus Parceiros de Venda, voce pode adicionar os detalhes de comissão aqui. Digite a taxa de comissão e o valor da comissão sera visivel.

### 3.12 Equipes de Venda
**Vendedor:** O ERPNext permite que voce adicione varios Vendedores que tenham trabalhado neste negocio. Voce pode mudar a percentagem de contribuição do Vendedor e rastrear o valor do incentivo que ganharam neste negocio.

<img class="screenshot" alt="Sales Team in Sales Order" src="{{docs_base_url}}/assets/img/selling/so-sales-team.png">

### 3.13 Secção Auto Repetição
Auto repetir Ordens de Venda é como uma subscrição. Defina uma data de inicio e fim para a auto-repetição. Selecione a Auto repetição criada. Para saber mais sobre auto repetição [clique aqui](/docs/user/manual/pt/automação/repetição-automatica).

### 3.14 Depois de Submeter
Ordem de Venda é uma transação que pode ser “Submetida”. Voce poderá fazer mais passos (como criar uma Guia de Remessa) somente depois de “Submeter” a Ordem de Venda.

Assim que “Submeter” a Ordem de Venda, voce pode acionar acções apartir da Ordem de Venda:

* Voce pode Adiconar, Actualizar, Apagar Itens na Ordem de Venda fazendo o clique no botão **Actualizar Itens**. Contudo voce não pode apagar itens que ja tenham sido entregues ou tenham ordem de trabalho atribuidas.

* Status: Uma vez submetido, voce pode por em espera ou Fechar.

* Criar: Apartir de uma Ordem de Venda Submetida, voce pode criar o seguinte:

    * Guia de Remessa - Para dar entrada. Voce pode tambem criar uma Guia de Remessa para os itens selcionados com base na Data de Entrega.
    * Ordem de Trabalho - Para começa a Ordem de Trabalho com as materias primas.
    * Factura de Vendas - Para cobrar a Ordem.
    * Solicitação de Material - Para pedir estocagem de materias se ja não tiver em armazem.
    * Solicitação de Materias Primas - Para pedir materias primas necessarias para o fabrico.
    * Projecto - Para criar um projecto com base em um Ordem de Venda.
    * Subscrição - Para auto repetir uma Ordem de Venda, i.e., tornar uma subscrição.
    * Pedido de Pagamento - Para criar uma Solicitação de Pagamento.
    * Pagamento - Para registar um pagamento contra uma Ordem de Venda.

Estas acções podem ser vistas tambem no topo do Dashboard. Voce pode tambem criar um Registo Contabilistico com base na Ordem de Venda apartir do dashboard.

<img class="screenshot" alt="Actions from Submitted Sales Order" src="{{docs_base_url}}/assets/img/selling/submit-so.png">

### 3.15 Ordem de Vendas com tipo de Ordem 'Manutenção'
Quando o 'Tipo de Ordem' de uma Ordem de Venda for 'Manutenção' siga estes passos:

1. Digite a Moeda, Lista de Preço, e detalhes do Item.
2. Mencione impostos e outras informações.
3. Salve e Submeta o formulario.
4. Uma vez o formulario submetido, o botão Criar irá mostrar estas opções para o Tipo de Ordem Manutenção.

    i) Visita de Manutenção ii) Agendamento de Manutenção.

  ![Ordem de Venda do Tipo Manutenção](/docs/assets/img/selling/so-maintenance.png)

> **Nota 1:**
Ao fazer o clique no botão Acção e selecionando 'Visita de Manutenção' voce pode directamente preencher o formulatio de visita. Os detalhes da Ordem de Venda seram procurados directamente.

> **Nota 2:**
Ao fazer o clique no botão Accão e selecionando 'Agendamento de Manutenção' voce podera preencher os detalhes do agendamento. Os detalhes da Ordem de Venda seram procurados directamente.

> **Nota 3:**
Ao fazer o clique no botão Factura voce pode criar a sua Factura de serviços. Os detalhes da Ordem de Venda seram procurados directamente.

### 4. Topicos Relacionados
1. [Cotação](/docs/user/manual/pt/vendas/proforma)
1. [Fechar Ordem de Vendas](/docs/user/manual/pt/vendas/artigos/fechando-ordens-vendas)
1. [Corrigindo Ordens de Venda depois de Submetida](/docs/user/manual/pt/vendas/artigos/emendando-ordens-de-vendas-depois-de-submetido)
1. [Lista de Escolhas](/docs/user/manual/pt/inventario/lista-de-escolhas#21-criar-a-lista-de-escolha-pela-ordem-de-vendas)

{next}
