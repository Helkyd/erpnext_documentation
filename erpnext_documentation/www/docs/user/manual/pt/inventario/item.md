<!-- add-breadcrumbs -->
# Item

**Um Item é um produto ou um serviço oferecido pela sua empresa.**

O termo Item é tambem aplicavel a materia prima ou componentes de produtos ainda por produzir (antes de serem vendidos aos clientes). O ERPNext permite que voce faça a gestão todo o tipo de produtos, materias prima, bens produzidos, variantes de itens e até mesmo de itens como serviços.

O ERPNext está optimizado para gestão minima de itens das suas vendas e compras. Se voce tiver serviços, voce pode criar um Item para cada serrviço que ofereça. Inserindo na tabela de Itens é essencial para a implementação com sucesso do ERPNext.

Para acessar a lista de Itens, va para:
> Home > Inventario > Itens e Preços > Item

## 1. Pre-requisitos
Antes de criar e usar o Item, é aconselhavel que voce crie primeiro:

* [Grupo de Item](/docs/user/manual/pt/inventario/grupo-item)
* [Armazem](/docs/user/manual/pt/inventario/armazem)
* Uma Unida de Medida é necessaria

## 2. Como criar um Item
1. Va para a lista de Itens, clique em novo.
2. Digite um Codigo de Item, o nome será preenchido automaticamente com o Codigo do Item quando fizer um clique no campo Nome do Item.
1. Selecione um Grupo do Item.
1. Digite o Stock de Abertura e o Preço de Venda Padrão.
3. Salvar.
  ![Item Salvo](/docs/assets/img/stock/item-saved.png)

### 2.1 Propriedades do Item

  * **Nome do Item:** Nome do Item é o nome actual do seu produto ou serviço.
  
  * **Codigo do Item:** Codigo do Item é um nome pequeno para denomimar o Item. Se tem poucos Itens, é aconselhavel manter o Nome do Item e Codigo Item igual. Assim ajuda os novos usuarios a reconhecer e actualizar os detalhes dos Itens em todas as transações. No caso de ter uma lista grande de Itens com nomes compridos, é aconselhavel fazer uma codificação. Para entender a Codificação dos Itens veja [Codificação do Item](/docs/user/manual/pt/inventario/artigos/codificacao-item). Voce pode tambem gerar Codigos do item com base na [Serie de Nomes](/docs/user/manual/pt/configuração/configurações/nome-das-series) activando esta funcionalidade aqui [Configurações do Stock](/docs/user/manual/pt/inventario/configuracoes-stock#1-nome-do-item-por).
  
  * **Grupo do Item:** Grupo do Item é usado para categorizar um Item dentro varios criterios como produtos, materia prima, serviços, consumiveis ou todos os Grupos de Item. Crie a sua lista de Grupo do Item padrão em Configuração > Grupo do Item e pre-selecionando a opção enquanto estiver a preenher os detalhes do seu Novo Item [Grupo do Item](/docs/user/manual/pt/inventario/grupo-item). Grupos do Item podem ser materia prima, etc, ou com base no seu negocio.
  
  * **Unidade Medida Padrão:** Esta é a unidade padrão de medida que voce irá usar para os seu produtos. Pode ser Nos, Kgs, Metros, etc. Voce pode guardar todas as UDM que os seus produtos precisam  Configuraçoes > Master Data > UOM. Este pode ser pre-selecionado enquanto estiver a criar um Novo Item. Visite a pagina [UDM](/docs/user/manual/pt/inventario/udm) para mais detalhes

### 2.2 Opções ao criar um Item
* **Desactivo**: Se desactivar um Item, não pode ser usado em qualquer transação.

* **Permitir um Item Alternativo**: Algumas vezes ao fabricar um bem, material especifico pode não estar disponivel. Se voce activar isto, voce pode criar e selecionar um Item alternativo apartir da list de Itens Alternativos. Para sber mais, visite a pagina [Item Alternativo](/docs/user/manual/pt/fabrico/item-alternativo) .

* **Manter Stock:** Se voce estiver a manter o Stock deste Item no seu Inventario, o ERPNext irá criar um razão de Stock para cada transação deste item. Tenha a certeza em não activar esta opção ao criar um Item não-stock (make to order/engineer) ou um serviço.

* **Incluir Item no Fabrico**: Este é para os itens da materia prima que seram usado para cirar bens acabados. Se o Item for um serviço adiconal como  'lavagem' que será usado na LDM, mantenha desactivo.

* **Taxa de Avaliação**: Exitem dois tipo de avaliação de stock para manter. FIFO (primeiro entrou - primeiro a sair) e o Media Movel. Para entender este topico em detalhe visite [Avaliação de Item, FIFO e Media Movel](/docs/user/manual/pt/inventario/artigos/avaliacao-item-fifo-e-media-movel).

* **Taxa de Venda Padrão**: Quando ao *criar* um Item, digitando o valor para este campo irá automaticamente criar um [Preço do Item](/docs/user/manual/pt/inventario/preço-item). Digitando um valor depois do Item ter sido criando não irá criar. Neste caso, o Preço do Item é criado apartir de qualquer transação com o Item. O preço no qual irá ser vendido. Este sera procurado na Ordem de Venda e Facturas de Venda.

* **É um Activo Fixo**: Selecione esta caixa se o item é um Activo da Empresa. Verifique o [Modulo de Activos](/docs/user/manual/pt/activos) para saber mais.

* **Criar Activos Automaticamente ao Comprar**: Se um Item é um Activo da Empresa, selecione esta caixinha se quiser criar activos automaticamente ao fazer a compra deste item pelo [Ciclo de Compras](/docs/user/manual/pt/compras/ordem-de-compra). Verifique a [Pagina dos Activos](/docs/user/manual/pt/activos/activo) para saber mais.

* **Percentagem Permitida**: Esta opção irá estar disponiveil somente cria e salva um Item. Esta é a percentagem pelo qual poderá cobrar a mais ou entragar a mais este item. Se não for definido, irá selecionar apartir das [Configurações de Stock](/docs/user/manual/pt/inventario/configuracoes-stock#3-limite-de-percentagem).

* **Carregar uma Imagem**: Para carregar um imagem para o icone que irá aparecer em todas as transações, salve o formulario preenchido parcialmente. Somente depois o seu ficheiro salvo que o botão 'Alterar' irá aparecer no Icone de Imagem. Clique em Alterar, depois clique em Carregar, e carregue a imagem.

Para India:

* **HSN/SAC**: Harmonized System of Nomenclature (HSN) and Service Accounting Code (SAC) for GST. These numbers are defined by the government and different Items fall under different codes. New HSN codes can be added if not present in the list.
* **Is nil rated or exempted**: For an Item that is under GST, but no tax is applied to it. Eg: Cereals.
* **Is Non GST**: For an item that is not covered under GST. Eg: petrol.

## 3. Funcionalidades

### 3.1 Marca e Descrição

* **Marca**: Se voce tem mais que uma marca salve em Vendas > Marcas e pre-selecione ao preenher um Novo Item.
* **Descrição**: Descrição do item. O texto do Codigo do Item será usado por defeito.
  ![Marca do Item e descrição](/docs/assets/img/stock/item-brand-description.png)

### 3.2 Codigos de Barra

Codigos de Barra podem ser gravados nos Itens para facilmente fazer o scan e adiconar em transações. Na tabela de Codigos de Barra voce pode adicionar Itens [scan do Codigo de Barras](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras). Existem dois tipos de Codigos de Barra no ERPNext:

* **EAN**: O Numero Europeu do Artigo é de 13 digitos. EAN é usado internacionalmente e reconhecido pelos varios sistemas POS.
* **UPC**: O Codigo do Produto Universal é um numero de 12 digitos. UPS é geralmente usado somente no USA e Canada.

### 3.3 Inventario

* **Dias de Vida no Armario**: Este é para o produto [Lote](/docs/user/manual/pt/inventario/lote). O numero de dias pelo qual o lote do produto depois deixara de ser usado. Por exemplo, medicamentos.
* **Fim de Vida**: Para um unico item/produto, a data que depois ficará completamente fora de uso. Isto é, o item ficara inutilizado para transações e fabrico. Por exemplo, voce usa cristais de plastico para fabricar itens nos proximos 5 anos que depois irá usar as miçangas de plastico.
* **Garantia**: Para rastrear o periodo de garantia, é necessario que o Item seja serializado. Quando o Item for entregue, a data de entrega e periodo de expiração é salvo na tabela de Numero de Serie. Pelo Numero de Serie, voce pode rastrear o status da garantia.

  O periodo de garantia é um tempo no qual o produto comprado pode ser devolvido ou trocado.

  <img class="screenshot" alt="Item Warranty" src="{{docs_base_url}}/assets/img/stock/item-inventory.png">

* **UDM do Peso**: A Unidade de Medida para o Item. Este pode ser Nos, Kilo, etc. O Peso da UDM pode ser usado internamente pode ser diferente da UDM de compra.
* **Peso por Unidade**: O peso actual por unidade do item. Eg: 1 kilo de biscoitos ou 10 biscoitos por pacote.
* **Tipo de Solicitação de Material Padrão**: Quando voce cria uma nova Solicitação de Material para este item, o campo definido aqui será selecionado na nova Solicitação de Material. Este é tambem conhecido como um 'indent'.
* **Metodo de Avaliação**: Selecione o Metodo de Avaliação FIFO ou Media Movel. Para saber mais sobre os Metodos de Avaliação, [clique aqui](/docs/user/manual/pt/inventario/artigos/avaliacao-item-fifo-e-media-movel).

### 3.4 Encomenda Automatica
Quando o stock de um item está abaixo de uma certa quantia, voce pode definir um pedido automatico na secção 'Auto Encomenda'. Este deve ser activado em [Configurações de Stock](/docs/user/manual/pt/inventario/configuracoes-stock#9-requisição-de-material-automatica). Este irá criar uma [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material) para o Item. O usuario com o papel de Gestor de Compras e Gestor de Stock será **notificado** quando a Solicitação de Material for criada.

* **Check in (grupo)**: Em qual dos Grupos de Armazem deve verificar a quantidade de item.
* **Pedido para**: Em que armazem guardar o pedido/solicitação de Stock.
* **Nivel de pedido (Re-order)**: Quanto esta quantidade é alcançada, o pedido/solicitação sera activada. O nivel de pedido pode ser determinado com base na hora e na media do consumo diario. Por exemplo, voce pode definir o nivel de pedido para uma Motherboard aos 10. Somente quando a Motherboards tiver 10 no stock, o sistema irá automaticamente criar uma Solicitação de Material na sua conta do ERPNext. 
* **Qtd de pedido (Re-order)**: O numero de unidade a serem pedidas para que a soma do custo do pedido e o custo sejam o minimo. A quantidade de pedido é feita com base na 'Qtd Minima do Pedido' especificado pelo fornecedor e muitos outros factores.

  Por exemplo, se o nivel de ordem for de 100 itens, a quantidade de pedido pode não ser necessaria mente de 100 itens. A quantidade do peidod pode ser maior ou igual ao nivel de pedido. Pode depender do tempo de entrega, desconto, tranporte e da media diario de consumo.

* **Tipo de Solicitação de Material**: O tipo de [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material) pelo qual o stock sera pedido. Este depende se voce compra o Item, fabrica ou transfere entre armazens.

  <img alt="Item Reorder" class="screenshot" src="{{docs_base_url}}/assets/img/stock/item-reorder.png">

> **Nota**: A Solicitação de Material é criada as 12 horas dependendo do nivel de pedido definido.

### 3.5 Varias Unidades de Medida
Voce pode adiconar UDM alternativas para um Item. Se a UDM padrão no qual voce vende for numeros (NoS) mas voce recebe em kilos, voce pode definir UDM adicional com o factor de conversão apropriado. Por exemplo, 500 Nos de parafusos = 1 Kilo, então selecione Kilogram/Litre como UDM e defina o factor de conversão como 500. Para saber mais sobre vendas em diferentes UDM, visite [esta pagina](/docs/user/manual/pt/vendas/artigos/vendendo-em-UDM-diferente).

### 3.6 Numeros de Serie

Com os Numeros de Serie, voce pode rastrear garantias e devoluções. Caso algum Item individual for chamado de volta pelo fornecedor o numero do sistema irá ajudar a procurar. A numeração do sistema tambem gere as datas de expiração.

De notar que se voce vende os seu itens aos milhares, e se os itens são muito pequenos como esferograficas ou borrachas, voce precisa de dar um numero de serie.

No ERPNext, voce tem que mencionar o Numero de Serie em alguns registo de conta. Se o seu produto não for de consumo grande, se não tem garantias e não tem changes de ser chamado de volta pelo fornecedor, envite criar numeros de serie.

<img alt="Serial No modal" class="screenshot" src="{{docs_base_url}}/assets/img/stock/serial_no_modal.gif">

### 3.7 Lotes

Um conjunto de Itens pode ser fabricado em Lotes. Este é util para mover os lotes e associar uma data de expiração com um certo lote.

* **Tem Numero de Lote**: Opções de numero de Lote, data de expiração, e amostra de retenção de stock sera mostrado ao selecionar esta caixa. Voce não pode activar isto se ja existe uma transação para este item. Se estiver desactivo, voce vai ter que digitar o numero de serie manual para cada transação.

* **Numero de Serie para Lotes**: O Prefixo que será aplicado aos numeros de lote. Se voce definir 5x1SCR, então o primeiro lote será 5x1SCR00001 na primeira transação/produção.

* **Criar um Novo Lote Automaticamente**: Se o numero do lote for mencionado em transações, então eles vão ser automaticamente criados de acordo o formato AAAA.00001. Se voce quer criar sempre manualmente um numero de lote para este item, deixe em branco este campo. Esta configuração irá passar por cima do 'Prefixo de Nome de Series' nas configurações do Stock. Numeros de Lote pode ser gerados automaticamente se voce fabrica os itens ou podem ser inserido manualmente se veem de um fabricante externo.

* **Tem Data de Expiração**: Se voce selecionar este, o numero de lote será criado de acordo a data de expiração. A data de expiração pode ser definida na tabela dos 'Lotes'.

* **Reter Amostra**: Para reter um numero pequeno da amostra do stock do item. Voce precisa definir um Armazem para Retenção de Amostra nas Configurações de Stock. Para saber mais, [clique aqui](/docs/user/manual/pt/inventario/reter-amostra-stock).

* **Tem Numero de Serie**: Este é similar aos Lotes de Serie, será criado quando fizer uma transação/fabrico. Se voce definir o Numero de Serie como AA, então a primeira transação o numero de serie sera criado como AA00001.

> Dika: Ao digitar o Codigo do Item na tabela de Itens, se a tabela requer detalhes de inventario, então dependendo da escolha em ser lote ou serie, voce pode digitar o Numero de Serie ou Lote aqui mesmo.

<img alt="Batch No modal" class="screenshot" src="{{docs_base_url}}/assets/img/stock/batch_no_modal.png">

> **Nota**: Uma vez que marque um item como Serializado ou Lote ou nenhum, ja não vai poder trocar depois de fazer um Registo de Stock.

Para saber mais, visita a pagina [Reconciliação de Stock](/docs/user/manual/pt/inventario/reconciliacao-de-stock) .

### 3.8 Variantes
Uma Variante do Item é uma versão diferente de um Item. Para aprender mais sobre gerir variantes [Variantes de Item](/docs/user/manual/pt/inventario/variantes-item).

### 3.9 Padroẽs do Item

Nesta secção, voce pode definir as transações relacionadas com a Empresa para este Item.

* **Armazem Padrão:** Este é o Armazem que é automaticamente selecionado nas transaçóes com este item.
* **Lista de Preço Padrão:** Quer seja Lista de Venda ou Compra. Voce pode definir as contas padrão de compras e vendas
* **Fornecedor**: Se o fornecedor padrão for definido, este fornecedor será selecionar para novas transações de compra.
* **Conta de Despensas Padrão:** É uma conta no qual o custo do Item será debitado.
* **Conta de Rendimento Padrão:** É uma conta no qual o rendimento pela venda do Item será creditada.
* **Centro de Custo Padrão:** É usado para gerir despesas para este Item.

  ![Padrões do Item](/docs/assets/img/stock/item-defaults.png)

> Dika: Voce pode adiconar mais linhas para varias empresas.

### 3.10 Compra, Detalhes de Reabastecimento

* **Unidade de Medida de Compra Padrão**: A UDM padrão que será usado para as transações de Compras.
* **Qtd Minima de Ordem**: A quantidade minima necessari para transações de compra como Ordens de Compra. Se definido, o sistema não irá deixar que prosiga com a transação de compra se a quantidade do item na transação de compra for menor que a quantidade definida neste campo.
* **Stock de Segurança**: “Stock de Segurança” é usado no relatorio “Itemwise Recommended Reorder Level”. Com base no Stock de Segurança, media do consumo diario e tempo de entrega, o sistema sugere a Nivel de Ordem para um item.

  Nivel de Pedido = Stock de Segurança + (Media do Consumo Diario * Tempo de Entrega)
* **Ultimo Preço de Compra**: O preço no qual foi feita a ultima compra para este item usando [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra) sera mostrado aqui.
* **É um Item de Compra:** Se não selecionado, voce não poderá usar este item para transações de compra.
* **É um Item dado pelo Cliente:** Selecionado se o Item é dado por um cliente e recebido pelo **Registo de Stock > Recepção de Material**. Se selecionado, o campo **Cliente** é Obrigadorio como o cliente padrão para **Solicitação de Material**. Para saber mais visite [esta pagina](/docs/user/manual/pt/fabrico/artigos/customer-provided-items).
* **Dias de Tempo de Entrega:** Dias de tempo de entrega é o numero de dias entre a ordem do Item e a mesmo alcançar o Armazem.

  <img class="screenshot" alt="Purchase details" src="{{docs_base_url}}/assets/img/stock/item-purchase-details.png">

### 3.11 Detalhes do Fornecedor

* **Entregue pelo Fornecedor (Drop Ship)**: Se o item for entregue directamente pelo fornecedor ao clisnte, selecione este caixinha. Leia mais [aqui](/docs/user/manual/pt/vendas/artigos/drop-shipping).
* **Codigos do Fornecedor:** Rastreie o Codigo do Item definido pelos Fornecedores para este Item. Nas Transções de Compras, ao selecionar o Item, o Numero da Peça do Fornecedor sera procurado bem como o referencia do Fornecedor. Pode ser mais [aqui](/docs/user/manual/pt/compras/artigos/maintaining-suppliers-part-no-in-item).

  ![Detalhes do Item do Fornecedor](/docs/assets/img/stock/item-supplier.png)

### 3.12 Detalhes de Transações Estrangeiras (Foreign Trade Details)
Se voce estiver a pegar o item de um outro país, voce pode definir os detalhes aqui.

* **País de Origem**: O país pelo qual voce busca o item.
* **Numero de Tarifa da Alfandega**: Voce pode criar um Numreo de Tarifa da Alfandega com uma descrição e usar como referencia aqui para partilhar com agencias das Alfandegas. Mais tarde poderá ser usado para adicionado nas Guia de Remessa.

### 3.13 Detalhes de Vendas

* **Unidade de Medida de Venda Padrão**: A UDM padrão que será usada para as transações de vendas.
* **Desconto Maximo (%)**: Voce pode definir o desconto maximo em % a ser aplicado num item. Eg: se voce definir 20%, voce não pode vender este item com um desconto maior que 20%.
* **É um Item de Venda**: Se não selecionado, voce não poderá usar este item nas transações de vendas.

  ![Detalhes do Item de Vendas](/docs/assets/img/stock/item-sales.png)

### 3.14 Remunerações Diferidas e Despesas Diferidas
Voce pode activar  deferred revenue or expense pelo formulario do item. Umva vez activa a caixa, voe irá ver opções para definir a Conta de Despesa Diferida e o numero de meses pelo o qual a remuneração/desconto é diferido. 

Por exemplo, considere um ano de adessão ao ginasio, voce paga o valor adiantado uma unica vez mas o serviços são dados durante o ano. Para o dono do ginsasio, este é uma remuneração diferida e o para cliente, é um despesa diferida.

  ![Remuneração Diferida](/docs/assets/img/stock/deferred-revenue.png)

Verifique as paginas em [Remuneração Diferida](/docs/user/manual/pt/contabilidade/receita-diferida) para mais detalhes.

### 3.15 Detalhes do Cliente

O Cliente pode identificar um Item com um Codigo de Item diferente. Este é similar ao [Codigo do Fornecedor](/docs/user/manual/pt/inventario/item#311-detalhes-do-fornecedor). 

* **Nome do Cliente**: Selecione um cliente aqui.
* **Grupo do Cliente**: Este ira procurar com base no Cliente que selecionou no campo anterior.
* **Codigo de Ref:** Um cliente pode identificar este item com um numero diferente. Voce pode rastrear o Codigo do Item atribuido pelo Cliente para este item. Quando voce cria uma Ordem de Vendas, o Codigo de Referencia do Cliente para este Item ficara visivel.

### 3.16 Imposto de Item

Estas configurações são necessarias osmente se um Item em particular tiver uma taxa de imposto diferente que a taxa definida na Conta de imposto padrão.

Voce precisa criar um novo 'Modelo de Imposto de Item' ou escolher um existente. Por exemplo, se voce tiver uma Conta de Imposto, “VAT 14%” e este Item em particular esta isento do imposto, entao voce seleciona “VAT 14%” na primeira coluna, e define “0” como o valor da taxa na segunda coluna. Visite a pagina[Modelo de Imposto de Item](/docs/user/manual/pt/contabilidade/modelo-imposto-item) para mais detalhes.

![Modelo de Imposto de Item](/docs/assets/img/stock/item-tax-template.png)

Voce pode tambem definir a [Categoria do Imposto](/docs/user/manual/pt/contabilidade/categoria-imposto) para este Item.


### 3.17 Criterio de Inspeção

* **Inspeção Necessaria antes da Compra**: Se uma inspeção for obrigatoria antes do item for comprado, i.e., antes de voce gerar o Recibo de Compra, selecione esta caixa.
* **Inpeção Necessaria antes da Entrega**: Se a inspeção é necessaria na altura da entrega pelo seu Fornecedor for obrigatoria para este Item, selecione a caixinha. Isto é, antes de voce gerar a Guia de Remessa. 
* **Modelo de Inspeção de Qualidade**: Se a Inspeção da Qualidade for preparada para este Item, então este modelo de criterio sera automaticamente actualizado na tabela de Inspeção de Quadlidade. Exemplos de Criterios são: Peso, Largura, Termino, etc.

Inspeção de Qualidade pode ser feito com o Visão Rapida e voce não precisa ir a uma pagina diferente para actualizar os detalhes de inspeção no ERPNext.

Para saber mais sobre Inspeção de Qualidade, [clique aqui](/docs/user/manual/pt/inventario/inspecao-de-qualidade).

### 3.18 Fabricando

* **LDM Padrão**: A [Lista de Materiais](/docs/user/manual/pt/fabrico/lista-de-materiais) padrão usado para fabricar este Item.
* **Fornecer Materia Prima para Compra**: Se voce subcontractou a venda, voce pode escolher a materia prima para fabrico do item usando a UDM padrão deles.
* **Fabricante:** Selecione o Fabricante que produziu este item.
* **Numero de Peça do Fabricante:** Digite o numero da peça do fabricante que o fabricante atribuiu a este item.

  ![Fabrico do Item](/docs/assets/img/stock/item-manufacturing.png)

* Os detalhes do fabricante aparecem depois de voce criar um 'Fabricante do Item' no dashboard e selecionou esse registo como padrão. Aqui, acrescente os detalhes para:
  * Codigo do Item
  * Diogite o nome do Fabricante
  * Digite o numero da peça o fabricante usou para identificar este item
  * Selecione 'É Padrão' para mostrar o fabricante e o numero da peça no registo do Item

  ![Fabricante do Item](/docs/assets/img/stock/item-manufacturer.png)

### 3.19  Website

* **Mostrar na Pagina**: Escolha se quiser mostra este Item na sua pagina. Uma vez selecionado, opções adicionais ficaram visiveis para configurar o item na sua pagina. Para visualizar o item na pagina clique em 'Ver na Pagina' em cima no lado esquedo em baixo da imagem do item. Visite [Modulo Website](/docs/user/manual/pt/website) para saber mais.

  <img class="screenshot" alt="Manufaturing details" src="{{docs_base_url}}/assets/img/stock/item-manufacturing-website.png">

* **Weightage**: Itens com maior peso serao mostrados primeiro na pagina. O limite para o numero que pode digitar aqui é muito alto. 

* **Slideshow**: Um slideshow pode ser mostrado no top da pagina. Visite a pagina [Homepage](/docs/user/manual/pt/website/homepage) no Modulo Website para saber mais.
* **Imagem**: Voce pode anexar uma imagem em vez de um Slideshow. 
* **Armazem da Pagina**: Selecione um existente ou crie um novo armazem para transações via pagina. Este Armazem será diferente dos seus outros Armazens. Stock para qualquer transação onlin será deduzida apartir dos Armazens definidos na sua pagina.
* **Grupos de Item do Website**: Aqui nesta table voce pode selecionar existente ou criar um novo [Grupos de Item](/docs/user/manual/pt/inventario/grupo-item) para classificar itens na sua pagina.
* **Set Meta Tags**: Meta tags ajudam com o SEO. Veja [Web Page](/docs/user/manual/pt/website/web-page) para saber como adicionar.

Visite [Fabrico](/docs/user/manual/pt/fabrico) e [Website](/docs/user/manual/pt/website) para entender estes topicos em detalhe.

### 3.20 Especificações da Pagina
Este secção é para configurar outros detalhes sobre o item.

* **Copiar apartir do Grupo de Item:** O detalhes 'Especificações da Pagina' seram procurados como definidos num Grupo de Itens especificos e escolhidos com base na secção anterior (2.17).
* **Especificações da Pagina**: Titulo e descrição para o item. Por exemplo, 'Garantia: 1 Ano'.
* **Descrição da Pagina**: Este irá aparecer na pagina do item.
* **Conteudo da Pagina**: (*Criando na v12*) Voce pode criar estilo adicional, etc., use Bootstrap 4  marcador para mostra na pagina do item.

### 3.21 Hub de Detalhes de Publicação

O hub é um mercado online livre aonde Fornecedores e Clientes pode transacionar. Se ambas parte estão no ERPNext, as transações são rapidas. Voce pode visitar o hub em : https://hubmarket.org.

* **Publicar no Hub**: Escolha se voce quer publicar o seu item no https://hubmarket.org/. É um mercado livre. Se o seu fornecedor/cliente estiver a usar o ERPNext, as transações são rapidas. Por exemplo, ao criar uma Ordem de Compra no seu lado, uma Ordem de Venda será criada no lado do Fornecedor.
* **Armazem do Hub**: Este é um Armazem separado para manter o stock das transações do seu hub.
* **Syncronizar com o Hub**: Sincronizar item e outros detalhes com o hub quando transações acontecem.

## 4. Video

<div>
  <div class='embed-container'>
    <iframe src='https://www.youtube.com/embed/FcOsV-e8ymE?end=192' frameborder='0' allowfullscreen>
    </iframe>
  </div>
</div>

### 5. Topicos Relacionados
1. [Preço do Item](/docs/user/manual/pt/inventario/preço-item)
1. [Codificação do Item](/docs/user/manual/pt/inventario/artigos/codificacao-item)
1. [Variantes do Item](/docs/user/manual/pt/inventario/variantes-item)
1. [Grupo do Item](/docs/user/manual/pt/inventario/grupo-item)
1. [Atributos do Item](/docs/user/manual/pt/inventario/atributo-item)
1. [Avaliação do Item FIFO e Media Movel](/docs/user/manual/pt/inventario/artigos//avaliacao-item-fifo-e-media-movel)
1. [Transações de Avaliação do Item](/docs/user/manual/pt/inventario/artigos/transacoes-de-avaliacao-item)
1. [Manter o Campo Stock Congelado na Ficha do Item](/docs/user/manual/pt/inventario/artigos/maintain-stock-field-frozen-in-item-master)
1. [Gerir Bens Produzidos Rejeitados](/docs/user/manual/pt/inventario/artigos/managing-rejected-finished-goods-items)
1. [Devolver Itens Rejeitados](/docs/user/manual/pt/inventario/artigos/return-rejected-item)
1. [Rastrear Itens usando Codigo de Barras](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras)
1. [Criando Depreciação para Item](/docs/user/manual/pt/inventario/artigos/creating-depreciation-for-item)
1. [Nome do Numero do Serie](/docs/user/manual/pt/inventario/artigos/serial-no-naming)
1. [Registo do Saldo de Abertura do Stock para Itens com Serie e Lote](/docs/user/manual/pt/inventario/artigos/abertura-balanco-stock-para-itens-serializados-e-lotes)
1. [Numero de Serie](/docs/user/manual/pt/inventario/numero-serie)
