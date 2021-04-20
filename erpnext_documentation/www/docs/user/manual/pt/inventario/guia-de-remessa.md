<!-- add-breadcrumbs -->
# Guia de Remessa

**Uma Guia de Remessa é feita quando uma entrega é enviada apartir do Armazem da Empresa para o cliente.**

Uma copia da Guia de Remessa é normalmente enviado com o Transportador. A Guia de Remessa contem a lista de Itens que são usados nos envios e actualiza o inventario. A Guia de remessa é um passo opcional e a Factura de Venda pode ser criado directamente apartir da Ordem de Venda.

Para acessar a lista da Guia de Remessa, va para:
> Home > Inventario > Transações de Stock > Guia de Remessa

![Fluxo de Guia de Remessa](/docs/assets/img/stock/delivery-note-flow.png)


## 1. Pre-requisitos
Antes de criar e utilizadr uma Guia de Remessa, é aconselhado criar os seguintes primeiro:

* [Ordem de Venda](/docs/user/manual/pt/vendas/ordem-vendas)

> Nota: Apartir da versão-13 nós introduzimos o Razão imudavel (immutable ledger) que muda as regras para cancelamento de entradas de stock e postagem para datas atrás de transações de stock no ERPNext. [Aprenda mais aqui](/docs/user/manual/pt/contabilidade/artigos/razão-imudavel-erpnext).

## 2. Como criar uma Guia de Remessa
O registo da Guia de Remessa é similar ao Recibo de Compra. É normalmente criado apartir de uma Ordem de Venda "Submetida" (que não foi enviado) fazendo o clique em Criar > Guia.

Para criar a Guia de Remessa _manual_ (não recomendado), siga estes passos:

1. Va para a lista de Guia de Remessa, clique em Novo.
1. O Cliente e os detalhes de Item podem ser procurados fazendo clique em 'Obter Itens apartir > Ordem de Vendas'.
1. A UDM e Preços serao procurados automaticamente.
1. Salvar e Submeter.

    <img class="screenshot" alt="Delivery Note" src="{{docs_base_url}}/assets/img/stock/delivery-note.png">

Para procurar Itens apartir de um Ordem de Venda, clique em Obter Itens apartir > Ordem de Vendas. Este irá abrir uma janela no qual poderá procurar as Ordens de Venda e selecionar uma.

Você irá verificar que todas as informações sobre Itens não enviados e outros detalhes são transportados das Ordens de Venda se você criar a Guia de Remessa apartir daqui.

Você pode tambem editar a data e hora de postagem, a data e hora corrente são definidas quando você criar a Guia de Remessa.


### 2.1 Statuses

Estes são os statuses em que uma Guia de Remessa pode ter:

* **Rascunho**: Um rascunho é salvo mas ainda não foi submetido no sistema.
* **Para Cobrar**: Ainda por ser cobrado usando uma [Factura de Vendas](/docs/user/manual/pt/contabilidade/factura-vendas).
* **Completado**: Submetido e todos os Itens enviados.
* **Cancelado**: Cancelada a Guia de Remessa.
* **Fechado**: O motivo do Fechar é de gerir um pequeno-fechar. Por exemplo, o seu Cliente pediu 20 qtds mas fechou em 15 qtds. Os restantes 5 não seram enviados ou cobrados.

### 2.2 Entregas Parciais

Quando você cria a Guia de Remessa apartir de um Ordem de Venda, as quantidades podem ser trocadas. Somente se a Ordem de Venda contem 10 Itens a serem entregues e vocẽ somente entragará 5 este semana e os restantes na semana seguinte, então você pode criar 2 Guias de Remessa em duas semanas.


## 3. Acções Relacionadas
### 3.1 Detalhes da Ordem de Compra do Cliente
Você pode digiar o numero da Ordem de Compra do Cliente aqui como Referencia.

### 3.2 Endereço e Contacto
* **Endereço de Envio**: O endereço do Cliente aonde os Itens serao enviados.
* **Pessoa de Contacto**: Se o Cliente for uma Empresa, adicione a pessoa de contacto neste campo.

Para India, os seguintes detalhes pode ser adicionados para GST:

* Customer GSTIN
* Place of Supply
* Billing Address GSTIN
* Company GSTIN
* Company Address Name

[Contactos](/docs/user/manual/pt/CRM/contacto) e [Endereço](/docs/user/manual/pt/CRM/endereço) são guardados separados para que você possa anexar varios Contactos ou Endereços do cliente.

### 3.3 Lista de Preços e Moedas
Você pode definir a moeda no qual a Guia de Remessa será enviada. Normalmente procurado se a Ordem de Venda for definida. Se você definir a Lista de Preços,então os preços de item serao procurados apartir dessa lista. selecionando Ignorar Regra de Preço irá ignorar as Regras de Preço definidos em Contabilidade > Regra de Preços.

Para saber sobre Lista de Preços, [clique aqui](/docs/user/manual/pt/inventario/lista-preços).

Para saber sobre gerir transações em multiplas moedas, [clique aqui](/docs/user/manual/pt/contabilidade/artigos/gerir-transações-multiplas-moedas).

### 3.4 Armazens

* **Definir Armazem Fonte**: Este é aonde os Itens seram fornecidos para ser enviado ao Cliente.
* **Para o Armazem**: Num cenario normal de Vendas, o Item existe no seu Armazem e vai para o Cliente. Contudo, caso queira manter uma amostra de stock, digite o Armazem aqui.

### 3.5 Tabela de Itens
* **Codigo de Barras**: Você pode gerir os Itens usando [Codigo de Barras](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras).

* O Codigo de Item, nome, descrição, Imagem, e Fabricante sera procurado apartir de [Table de Item](/docs/user/manual/pt/inventario/item).

* **Scan Codigo de Barras**: Você pode adicionar Itens numa tabela de Itens fazendo o scan dos Codigos de Barra se você tiver um leitor de Codigo de Barras. Saiba como rastrear [aqui](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras)

* **Desconto e Margem**: Você pode aplicar percentagens de desconto em Itens individuais ou em valor total do Item. Leia [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto) para mais detalhes.

* **Preço**: O Preço é procurado se definido em [Lista de Preço](/docs/user/manual/pt/inventario/preço-item) e o Valor total é calculado.

* **Modelo de Imposto de Item**: Você pode definir um Modelo de Imposto de Item para aplicar um valor de imposto especifico para este Item. Para saber mais,visite [esta pagina](/docs/user/manual/pt/contabilidade/modelo-imposto-item).

* Os detalhes do Peso do Item por unidade e Peso de UDM são procurados se definido na tabela de Item.

* **Armazem e Referencia**: O Armazem pelo qual os Itens são enviados para o Cliente serão visualizados. Tambem, um Ordem de Venda será vista se a Guia de Remessa foi criado: 'Ordens de Venda > Guia de Remessa'.

* **Numero do Lote e Numero de Serie**: Se o seu Item for serializado ou lote, você irá digitar [Numero de Serie](/docs/user/manual/pt/inventario/numero-serie) e [Lote](/docs/user/manual/pt/inventario/lote) na tabela de Itens. Você term permissão para digitar varios Numeros de Serie numa linha (cada em linhas separadas) e você pode digitar o mesmo Numero de Serie como quantidade.

    A 'Qtd disponivel no Armazem de Origem', 'Qtd do Lote Disponivel no Armazem de Origem', e 'Qtds Instalada' serao mostrados. Para saber mais sobre a instalação, visite a pagina [Nota de Instalação](/docs/user/manual/pt/inventario/nota-de-instalacao) .

    **Nota**: O Item tem que ser serializado ou lote para estas funcionalidades funcionarem. Se o Item for serializado uma janela irá aparecer aonde pode digitar os Numeros de Serie.

* Conta de Despesa é a conta no qual o valor será debitado. Activando 'Permitir Taxa de Avaliação Zero' irá permitir submeter a Guia de Remessa mesmo que a Taxa de Avaliação é 0. este pode ser uma amostra de item ou devido a um entendimento mutuo com o seu Fornecedor.

* Dimensões de Contabilidade ajudam a marcar cada transação com Dimensões diferentes sem a necessidade de criar um novo Centro de Custo. você precia criar Dimensões de Contabilidade primeiro, para mais informação, visite [esta pagina](/docs/user/manual/pt/contabilidade/dimensao-contabil).

* **Quebra de Pagina** Irá criar uma Quebra de Pagina mesmo antes deste Item ser impresso.

### 3.6 Rastreando a Inspeção de Qualidade
Se para alguns Itens, for obrigatorio registar as Inspeções de Qualidade (se voce definiu na tabela de Item), voce ira ter que atualizar o campo “Inspeção de Qualidade". O sistema irá somente permitir “Submeter” a Guia de Remessa
se você atualizar a  “Inspeção de Qualidade”.

Depois de activar o Criterio de Inspeção no [Formulario do Item](/docs/user/manual/pt/inventario/item#317-criterio-de-inspecao) para Vendas e anexando o Modelo de Inspeção de Qualidade aquie, Qualidades de Inspeção podem ser registados nas Guias de Remessa.

### 3.7 Impostos e Taxas
Os Impostos e Taxas serao procurados apartir de [Ordem de Vendas](/docs/user/manual/pt/compras/ordem-de-compra).

Visite a pagina [Modelo de Impostos e Taxas de Venda](/docs/user/manual/pt/vendas/modelo-impostos-taxas-vendas) para sabe mais sobre impostos.

O total de impostos e taxas serao mostrados na tabela em baixo.

Para adiconar Impostos automaticamente via Categoria de Imposto, visite [esta pagina](/docs/user/manual/pt/contabilidade/categoria-imposto).

Tenha a certeza de marcar todas os impostos na tabela de Impostos e Taxas para uma avaliação correta.

#### Regra de Envio
A Regra de Envio ajuda definir o custo do Item de envio. O custo sreá normalmente aumentado com a distancia do envio. Para saber mais, visite a pagina [Regra de Envio](/docs/user/manual/pt/vendas/regra-envio).

### 3.8 Desconto Adicional
Qualquer desconto adicional para a ordem completa pode ser definido nesta secção. Este desconto pode ser com base no Total Geral i.e., post tax/charges or Net total i.e., pre tax/charges. O desconto adicional pode ser aplicado como uma percentagem ou um valor.
Leia [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto) para mais detalhes.

### 3.9 Termos e Condições
Nas transações de Vendas/Compras pode ter alguns Termos e Condições com base no qual o Fornecedor da bens ou serviços ao Cliente. Você pode aplicar os Termos e Condições para transações e eles vão aparecer ao imprimir o documento. Para saber mais sobre Termos e Condições, [clique aqui](/docs/user/manual/pt/configuração/imprimir/termos-e-condições)

### 3.10 Informação de Transporte

Se você outsource o transporte de Itens para a sua entrega, os detalhes do transportador podem ser adicionados. Este não é o mesmo como [drop shipping](/docs/user/manual/pt/vendas/artigos/drop-shipping).

* **Transportador**: O Fornecedor que irá transportar o Item para o seu Cliente. A funcionalidade do transportador sera activo na tabela de Fornecedor para selecionar o [Fornecedor](/docs/user/manual/pt/compras/fornecedor) aqui.
* **Motorista**: Você pode adicionar o Motorista aqui que irá conduzir o modo de transporte.

![Nota de Entrega de Transporte](/docs/assets/img/stock/delivery-note-transport.png)

Os seguintes detalhes podem ser registados:

* Distançia em km
* Modo de Transporte quer seja estrada, voo, caminhos de ferro ou maritimo.

Para India, GST:

* GST Transporter ID
* Transport Receipt No
* Vehicle No
    The GST Vehicle Type can be changed

A Data do Recibo de Transporte e Nome do Condutor seram procurados.

### 3.11 Mais Informações

A Guia de Remessa pode ser ligada aos seguines para motivos de rastreamento:

* [Projecto](/docs/user/manual/pt/projectos/projecto)
* [Campanha](/docs/user/manual/pt/CRM/campanha)
* [Fonte](/docs/user/manual/pt/CRM/lead_source)

### 3.11 Configurações de Impressão

#### Cabeçalho
Você pode imprimir a Guia de Remessa com o seu logotipo da empresa. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

'Agrupar itens iguais' irá agrupar os itens iguais adicionados varias vezes na tabela de Itens. Isto pode ser visto ao Imprimir.

#### Imprimir Cabeçalho
Cabeçalho de Recibo de Compras pode tambem ser alterado ao imprimir o documento. Você pode fazer isso selecionando **Imprimir Cabeçalho**. Para criar um novo Imprimir Cabeçalho va para: Home > Configurações > Impressão > Imprimir Cabeçalho. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

Existem caixas adicionais para imprimir a Guia de Remessa sem o valor, este pode ser util quando o Item é de grande valor. Você tambem pode agrupar os itens iguais numa unica linha ao imprimir.

### 3.12 Status
O Status do documento e percentagem de instalação é mostrado aqui. Qualquer instrução adicional para entrega pode ser digitado aqui.

### 3.13 Comissão

Se a venda foi feita via um dos Parceiros de Venda, você pode adicionar os detalhes das comissões aqui. Este é procurado pela Ordem de Venda.

### 3.14  Sales Team
**Vendedor:** O ERPNext permite que voce adicone varios Vendedores que podem ter trabalhado neste negocio.

Este é procurado apartir da Ordem de Vendas, por exemplo:

<img class="screenshot" alt="Sales Team in Sales Order" src="{{docs_base_url}}/assets/img/selling/so-sales-team.png">

### 3.15 Pacotes de Envio ou Itens com Pacote de Produtos

Se você estiver a enviar Itens que tem [Pacote de Produtos](/docs/user/manual/pt/vendas/pacote-de-produtos), o ERPNext irá automaticamente criar uma tabela de "Lista de Escolhas" para si com base nos sub-Itens neste Item.

Se os seus Itens forem serializados, então para o tipo de Pacote de Produtos, você irá ter que actualizar
os Numeros de Serie na tabela "Lista de Escolhas".

### 3.16 Empacotando Itens em caixas, para Envio de Contentor

Se você estiver para fazer uma entrega via contentor ou por peso, então pode usar a Nota Fiscal para dividir a sua Guia de Remessa em unidades mais pequenas. Para saber mais sobre a Nota Fiscal, visite [esta pagina](/docs/user/manual/pt/inventario/nota-fiscal).

Você pode criar varias Notas Fiscais para as Guias de Remessa e o ERPNext fazer com que as quantidades na Nota Fiscal não excedam as quantidades da Guia de Remessa. De notar que pode criar uma Nota Fiscal apartir da Guia de Remessa somente quando a Guia de Remessa estiver em Rascunho.

### 3.17 Depois de Submeter

Quando a Guia de Remessa for submetida, o Registo do Razão de Stock é feito para cada Item e o stock actualizado. Quantidades pendentes na Ordem de Venda são actualizados (caso necessário).

O Dashboard irá mostrar as seguintes opções:

* [Nota de Instalação](/docs/user/manual/pt/inventario/nota-de-instalacao)
* [Devolução de Vendas](/docs/user/manual/pt/inventario/retorno-vendas)
* [Viagem de Entrega](/docs/user/manual/pt/inventario/viagem-de-entrega)
* [Factura de Vendas](/docs/user/manual/pt/contabilidade/factura-vendas)

![Guia de Remessa depois de Submeter](/docs/assets/img/stock/delivery-note-submit.png)

> Dika: Para não permitir a criação de Guias de Remessa sem uma Ordem de Venda:

### 3.18 Devolução de uma Ordem de Venda
Uma vez entregue a Ordem de Venda usando a Guia de Remessa, você pode criar um registo de devolução caso o cliente [Cliente](/docs/user/manual/pt/CRM/cliente) devolva o Item. Para saber mais, visite  a pagina [Devolução de Vendas](/docs/user/manual/pt/inventario/retorno-vendas) .

### 3.19 Pulando a Guia de Remessa

Se você não quer criar uma Guia de Remessa depois de uma Ordem de Venda e queira criar um Factura de Vendas directamente, active a funcionalidade para tal em [Configurações de Venda](/docs/user/manual/pt/vendas/configurações-venda#32-guia-de-remessa-necessaria).


### 4. Topicos Relacionados
1. [Armazem](/docs/user/manual/pt/inventario/armazem)
1. [Erro de Stock na Guia de Remessa](/docs/user/manual/pt/inventario/artigos/erro-stock-guia-de-remessa)
1. [Tranferencia de Material apartir da Guia de Remessa e Recibo de Compra](/docs/user/manual/pt/inventario/artigos/transferencia-material-pela-guia-de-remessa)
1. [Nota de Instalação](/docs/user/manual/pt/inventario/nota-de-instalacao)
1. [Viagem de Entrega](/docs/user/manual/pt/inventario/viagem-de-entrega)