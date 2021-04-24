<!-- add-breadcrumbs -->
# Recibo de Compra

**Recibo de Compras são feitas quando voce aceita Itens do seu Fornecedor normalmente contra uma Ordem de Compra.**

Voce pode tambem aceitar Recibos de Compra directamente sem a necessida de uma Ordem de Compra. Para fazer isso, defina Ordem de Compra
Necessaria como “Não” nas configurações de Compra.

Para acessar a lista de Recibo de Compra, va para:
> Home > Inventario > Transações de Stock > Recibo de Compra

![Fluxo de Recibo de Compra](/docs/assets/img/stock/purchase-receipt-flow.png)

## 1. Pre-requisitos
Antes de criar e usar um Recibo de Compra, é aconselhavel que crie os seguintes antes:

* [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)

> Nota: Apartir da versão-13 para frente nós introduzimos razão imutavel que muda as regras para cancelamente dos registo de stock e postagem de datas anteriores de transações de stock no ERPNext. [Aprenda mais aqui](/docs/user/manual/pt/contabilidade/artigos/razão-imudavel-erpnext).


## 2. Como criar um Recibo de Compra
Um Recibo de Compra é normalmente criado para uma [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra). Na Ordem de Compra, clique em Criar > Recibo de Compra.

Para criar uma Ordem de Compra _manualmente_ (não recomendado), siga estes passos:

1. Va para a lista de Recibo de Compra, clique em Novo.
1. O nome do Fornecedor e Itens podem ser procurados apartir da Ordem de Compra fazendo o clique em 'Obter Itens apartir > Ordem de Compra'.
1. Voce pode definir os Armazens Aceites para todos os itens neste Recibo de Compra. Este é procurado se for definido na Ordem de Compra.
1. Caso qualquer Item estiver defeituoso, defina o Armazem Rejeitado aonde este Itens serão guardados.
1. Selecione o Item e digite a quantidade na tabela dos Itens.
1. O preço sera procurado e o valor será automaticamente.
1. Voce pode expandir a linha do item e mudar o Armazem de Aceitação para um Item.
1. Salve e Submeta.

    <img class="screenshot" alt="Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-receipt.png">

Voce pode tambem adiconar uma 'Guia de Remessa do Fornecedor' para o Recibo de Compra se o seu Fornecedor adicionou algumas notas.
Usando a caixinha 'Editar Data e Hora de Postagem' voce pode editar a hora e data de postagem do Recibo de Compra. Por defeito, a data e hora são definidos quando voce clique no botão Novo.

É Retorno: Selecione esta caixinha se voce estiver a devolver Itens que não foram aceites no seu Armazem.

### 2.1 Estados

Estes são os status um Recibo de Compra pode ter:

* **Rascunho**: Um rascunho é salvo mas ainda não foi submetido no sistema.
* **Para Combrar**: Ainda por ser combrado usando uma [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra).
* **Completado**: Submetido e todos os Itens recebidos.
* **Cancelado**: Cancelado o Recibo de Compra.
* **Fechado**: O motivo do Fecho é para gerir fechos pequenos. Por exemplo, voce solicitou 20 qtds, mas fechou em 15 qtds. Os restantes 5 não seram recebidos ou cobrados.

## 3. Funcionalidades
### 3.1 Moeda e Lista de Preço
A moeda do Recibo de Compra é mostrado nesta secção, é procurado apartir de uma Ordem de Compra. Os preços do item serao procurados pela lista de Preços criada. Selecionando em Ignorar Regra de Preço será ignorado as Regras de Preço definidos em Contabilidades > Regra de Preço.

Vendo que os itens recebidos afectam o valor do seu inventario, é importante converter na sua moeda base se fez a solicitação foi feita numa outra Moeda. Voce ira precisar actualizar a Taxa de Conversão de Moedas se necessario.

Para saber sobre Listas de Preço, [clique aqui](/docs/user/manual/pt/inventario/lista-preços).

### 3.2 Detalhes de Armazem
Os seguintes Armazens definidos serao definidos em todos o Itens na tabela de Itens do Recibo de Compra. Voce pode mudar os Armazens dos Itens individuais via tabela.

* **Armazens Aceite**: Este é o Armazem no qual voce irá aceitar e guardar os Itens recebidos. Normalmente, este é o armazem 'Armazem'.
* **Armazens Rejeitados:** Este é o Armazem no qual voce irá guardar todos os Itens que estavam defeituosos ou não tem a qualidade requerida.

#### Subcontratação

* **Materias Primas Consumidas**: Caso estiver a subcontractar, selecione 'Sim' para consumir as Materias Primas apartir do vendedor. Para saber mais sobre subcontratação, [clique aqui](/docs/user/manual/pt/fabrico/subcontratação).

### 3.3 Tabela de Itens

* **Codigo de Barras**: Voce pode rastrear Itens usando [Codigo de Barra](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras).

* **Scan Codigo de Barras**: Voce pode adiconar Itens na tabela de Itens fazendo o scan dos seus condigos de barra se voce tiver um leitor de codigos de barra. Saiba mais como rastrear [aqui](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras)

* O Codigo do Item, nome, descrição, Imagem, e Fabrico irá ser procurado apartir da tabela do Item.

* **Recebido e Aceite**: Defina o recebido, aceite e quantidade rejeitada. A UdM sera procurada apartir da tabela Item. Voce irá precisar actualizar o “Factor de Conversor de UDM” se a sua Ordem de Compra para um Item na qual a Unidade de Medida (UDM) é diferente que voce tem em Stock (UDM Stock).

    ![Tabela de Recibo de Compra dos Itens](/docs/assets/img/stock/purchase-receipt-item.png)

* **Preço**: O Preço é procurado se definido na [Lista de Preços](/docs/user/manual/pt/inventario/lista-preços) e o Total geral é calculado.

* **Modelo de Imposto do Item**: Voce pode definir o Modelo de Imposto de Item para aplicar um valor especifico do valor do Imposto para este Item em particular. Para saber mais, visite [esta pagina](/docs/user/manual/pt/contabilidade/modelo-imposto-item).

* Os detalhes do Peso do Item por unidade e UDM do Peso são procurados se definidos na tabela do Item.

* **Referencia e Armazem**: Voce pode definir os Armazens aceites ou rejeitados e tambem adicionar a Inspeção de Qualidade, veja a proxima secção.

* **Nº de Serie, Nº do Lote, e LDM**: Se o seu Item for serializado ou tem lotes, voce irá que digitar um Numero de Serie
e Lotes na tabel do Item. Voce pode digitar varios Numeros de Serie
numa linha (em linhas separadas) e voce deve digitar os mesmos Numeros
de Serie de acordo as quantidades.

    Tem campos diferentes para digitar Numreos de Serie para ambos Itens aceites e rejectados aqui. Um Numero de Lote pode tambem ser definido se estiver a guardar lotes de plastico medico por exemplo.

    Selecionando 'Permitir Taxa de Avaliação Zero' irá permitir submeter o Recibo de Compra mesmo que a Taxa de Avaliação do Item seja 0. Este pode ser uma amostra do item ou devido a um entendimento mutuo como o seu Fornecedor.

* Voce pode ligar uma LDM aqui se o Item esta a ser [subcontratado](/docs/user/manual/pt/fabrico/subcontratação). Ligando a LDM aqui irá afectar o Razão do Stock, i.e. a materia prima do stock irá ser reduzida apartir do Armazem do Fornecedor.

    **Nota**: O Item tem que ser serializado ou ter lotes para esta funcionalidade funcionar. Se o Item for serializado uma janela irá aparecer aonde voce pode digitar os Numeros de Series.

* Dimensões Contabeis ajudam a marcar cada transação com diferentes dimensões sem a necessidade de criar um novo Centro de Custo. Voce precisa criar primeiro Dimensões Contabei, para saer mais, visite [esta pagina](/docs/user/manual/pt/contabilidade/dimensao-contabil).

* Quebra de Pagina irá criar uma quebra de pagina antes de imprimir este item.

### 3.4 Restreando a Inspeção de Qualidade
Se para alguns Itens, for obrigatorio registar a Inspeção de Qualidade (se voce definiu na tabela do Item), voce irá precisar actualizar o campo “Inspeção de Qualidade". O sistema irá somente permitir “Submeter” o
Recibo de Compra se voce actualizar a “Inspeção de Qualidade”.

Depois de activar o Criteio de Inspeção no [Formulario do Item](/docs/user/manual/pt/inventario/item#317-criterio-de-inspeção) para Compra e anexando o Modelo de Inspeção de Qualidade aqui, Inspeção de Qualidade pode ser gravado nos Recibos de Compra.

Para saber mais, visite a pagina [Inspeção de Qualidade](/docs/user/manual/pt/inventario/inspecao-de-qualidade) .

![Inspeção de Qualidade](/docs/assets/img/stock/quality-inspection.png)


### 3.5 Materias Primas Consumidas
* Na tabela **Itens Consumidos** contem as Materias Primas consumidas pelo Fornecedor de formas a receber os Produtos Acabados.
* O Botão **Obter Stock Corrente** ira procurar o stock corrente dos Itens Consumidos pelo Armazem do Fornecedor.
    <img class="screenshot" alt="Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-receipt-consumed-items.png">

### 3.6 Impostos e Avaliações
Os Impostos e Taxa sao procurados pela [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra).

Visite a pagina [Impostos de Compra e Modelo de Taxas](/docs/user/manual/pt/compras/modelo-impostos-taxas-compra) para saber mais sobre impostos.

O total dos Impostos e taxas sera mostrado em baixo da tabela.

Para adicionar impostos automaticamente via Categoria de Impostos, visite [esta pagina](/docs/user/manual/pt/contabilidade/categoria-imposto).

Tenha a certeza de marcar todos os impostos na tabela de Impostos e Taxas correctamente para uma Avaliação correcta.

#### Regras de Envio
Uma Rgra de Envio ajuda a definir os custo do Envio dos Itens. O custo normalmente irá aumentar com a distancia do envio. Para saber mais, visite a pagina[Regras de Envio](/docs/user/manual/pt/vendas/regra-envio).


### 3.7 Disconto Adicional
Qualquer desconto adicional para a Ordem completa pode ser definida nestea secção.
Leia [Aplicar Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto) para mais detalhes.

### 3.8 Mais Informação
O Status do Recibo de Compra é mostrado aqui no topo. Os varios estados são: Rascunho, Para Cobrar, Completado, Cancelado, e Fechado. Esta secção tambem mostra % Valor Cobrado, i.e. o valor da percentagem no qual [Factura de Venda](/docs/user/manual/pt/contabilidade/factura-venda) são criados.

### 3.9 Configurações de Impressão

#### Cabeçalho
Voce pode imprimir o Recibo de Compra com o cabeçalho da sua Empresa. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

'Agrupar Itens iguais' irá agrupar os itens iguais adiconados varias vezes na tabela de itens. Pode ser visto ao Imprimir.

#### Imprimir Cabeçalho
Cabeçalhos de Recibo de Compra podem ser trocados ao imprimir o documento. Voce pode fazer isso ao selecionar **Imprimir Cabeçalho**. Para criar um novo Imprimir Cabeçalho va para: Home > Configurações > Impressão > Imprimir Cabeçalho. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/imprimir-cabeçalhos).

### 3.10 Depois de Submeter

Um Registo do Razão do Stock é criado para cada Item adicionado no Armazem pela
“Quantidade Aceite” se tiver rejeições, um Registo do Razão de Stock é feito
para cada Rejeição. As “Quantidades Pendentes” são actualizadas na Ordem de Compra.

Depois de submeter o Recibo de Compra, o seguinte é criado:

* [Devolução de Compras](/docs/user/manual/pt/inventario/retorno-compras)
* [Registo de Stock](/docs/user/manual/pt/inventario/entrada-stock)
* [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra)
* [Reter Amostra de Stock](/docs/user/manual/pt/inventario/reter-amostra-stock)

![Submeter Recibo de Compra](/docs/assets/img/stock/purchase-receipt-submit.png)

### 3.11 Devolução de um Ordem de Compra
Uma vez que recebeu a Ordem de Compra usnado um Recibo de Compra, voce pode criar um registo de devolução no caso do Item deve ser devolvido ao [Fornecedor](/docs/user/manual/pt/compras/fornecedor). Para saber mais, visite a pagina [Devolução de Compras](/docs/user/manual/pt/inventario/retorno-compras).

### 3.12 Pulando o Recibo de Compra

Se voce não quer criar um Recibo de Compra depois de uma Ordem de Compra e quiser criar directamente uma Factura de Compra, active a funcionalidade para tal em [Configurações de Compra](/docs/user/manual/pt/compras/configuração-compras#23-recibo-de-compras-obrigatorio).

* * *

#### Alterando o valor dos Itens apos Recibo de Compra:

Algumas vezes, algumas despesas que adicionados ao total das compras dos Itens são conhecidos somente depois.
Exemplo practico é, se voce estiver a importar Itens, voce
irá ter Despesas de Alfandega, etc somente quando o seu “Clearing Agent” enviar
a Factura. Se voce quiser atribuir este custo aos Itens comoprados, voce
tera de usar o [Voucher de Custo de Entrega](/docs/user/manual/pt/inventario/landed-cost-voucher). O porque "Custo de Entrega"? Porque representa os impostos que voce pagou quando chegou até si.

## 4. Topicos Relacionados
1. [Guia de Remessa](/docs/user/manual/pt/inventario/guia-de-remessa)
1. [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
1. [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra)
1. [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
1. [Voucher de Custo de Entrega](/docs/user/manual/pt/inventario/landed-cost-voucher)
