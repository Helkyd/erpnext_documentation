<!-- add-breadcrumbs -->
# Proforma

**Uma Proforma é um custo estimado de um produtos/serviços que voce está a vender ao seu cliente futuro/presente.** 

Durante uma venda, um cliente pode pedir uma nota sobre os produtos
ou serviços que voce pretende oferecer com os preços e outros termos.
Isto é muitos nomes como "Proposta", Estimada", "Factura Proforma" ou **Cotação**.

Para acessar a Lista de Proformas, va para:
> Home > Vendas > Vendas > Cotação

Um fluxo de tipo de Vendas é como:

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/selling-flow-quo.png">

Uma Proforma contem detalhes sobre:

  * O recepiente da Proforma
  * Os Itens e quantidade que esta a oferecer.
  * Os preços no qual são oferecidos.
  * Os Impostos aplicados.
  * Outras taxas (como entrega, seguro) se aplicavel.
  * A validade do contracto.
  * O tempo de Entrega.
  * Outras Condições.

> Dica: Imagens ficam melhor em Cotações. Tenha a certeza que os seu itens tenham imagens anexadas.


## 1. Pre-requisitos
Antes de criar e usar Proformas, é aconselhavel criar os seguintes primeiro:

* [Cliente](/docs/user/manual/pt/CRM/cliente)
* [Lead](/docs/user/manual/pt/CRM/lead)
* [Item](/docs/user/manual/pt/inventario/item)

## 2. Como criar uma Proforma
1. Va pra a lista de Proformas, clique em Novo.
2. Selecione se a Proforma for para um Cliente ou Lead apartir do campo 'Proforma Para'.
3. Digite o nome do Cliente/Lead.
1. Digite a data de Validade no qual o valor da cotação será invalida.
1. Tipo de Ordem pode ser Vendas, Manutenção ou Carrinho de Compras. Carrinho de compras é para a sua Pagina e não deve ser criado por aqui.
4. Adicone os Itens e suas quantidades na tabela de itens, os preços vao ser porocurados automaticamente do Preço do Item. Voce pode tambem procurar itens apartir de uma Oportunidade fazendo o clique em Obter Itens Apartir > Oportunidade.
5. Adicone Impostos adiconais e taxas caso necessario.
6. Salve.

Voce pode tambem criar uma Proforma apartir de uma Oportunidade como mostra.

<img class="screenshot" alt="Make Quotation from Opportunity" src="{{docs_base_url}}/assets/img/selling/make-quote-from-opp.png">

## 3. Funcionalidade

### 3.1 Endereço e Contacto
Nesta secção existem quatro campos:

* **Endereço do Cliente:** Este é o endereço de Cobrança do cliente.
* **Endereço de Envio:** O Endereço aonde os itens vão ser entregues.
* **Pessoa de Contacto:** Se o seu cliente for uma empresa, então voce pode adiconar a pessoa a contactar neste campo.
* **Territorio:** Região aonde o cliente pertence. O padrão é Todos os Territorios. 

### 3.2 Moeda e Lista de Preço
Voce pode definir a moeda no qual a proforma/ordem de venda será enviada. Se voce definir uma Lista de Preços, então os preços dos itens vão ser procurados por ai. Selecionado Ignorar Regra de Preço irá ignorar as Regras de Preço definidas em Contabilidade > Regras de Preço.

Para saber sobre Listas de Preço, [clique aqui](/docs/user/manual/pt/inventario/lista-preços).

Para saber sobre gerir transações em varias moedas, [clique aqui](/docs/user/manual//pt/contabilidade/artigos/gerir-transações-multiplas-moedas).

### 3.3 Os Itens da Tabela
Esta tabela pode ser expandida fazendo o clique no triangulo invertido presente a direita da tabela.

* Ao selecionar o Codigo do Item, o seguinte sera automaticamente procurado: nome do ite, descrição, qualquer imagem se definida, quantidade padrão será 1, os preços. Voce pode adiconar descontos na secção de Descontos e Margens. 
* **Dentro de Desconto e Margem** voce pode adiconar margem extra para lucros ou dar um desconto. Ambos podem ser definidos com base em valor ou percentagem. O preço final será mostrado na secção de Preços. Voce pode atribuir um Modelo de Imposto do Item criado especificamente para o item.
* **Peso do Item** será procurado se definido na tabela de Item.
* Em **Armazem e Referencia**, o armazem será procurados apartir da tabela de Item, este é o armazem aonde voce tem o stock presente.
* Em **Planeamento** voce pode ver a quantidade Projectada e a quantidada actual presente. Para saber mais sobre estes campos, [clique aqui](/docs/user/manual/pt/inventario/quantidade-projectada). Se voce fizer o clique no botão 'Balanço de Stock', irá levar-lhe ao doctype aonde voce pode gerar um relatorio de stock para o item.
* **Carrinho de Compras**, notas adicionais são geradas nas transações da Pagina. Notes sobre o item vao ser procuradas aqui quando adiconados pelo carrinho de compras. Por exempo: fazer comida muito picante. *Introduzido na v12*
* **Quebra de Pagina** Ira criar uma Quebra de pagina antes do item ser impresso.

* Voce pode adionar linhas em cima/em baixo, duplicar, mover ou apagar linhas na tabela.

* Dica: Voce pode tambem descarregar a tabela de itens em formato CSV e Carregar em outra transação.

A quantidade total, preço e peso liquido de todos os itens vão ser motrados na tabela. O preço mostrado é antes do imposto.

### 3.4 Impostos e Taxas
Para adiconar impostos a sua Proforma, voce pode selecionar um [Modelo de Imposto de Vendas e Taxas](/docs/user/manual/pt/vendas/modelo-impostos-taxas-vendas) ou adiconar os impostos manual na tabela Impostos de Vendas e Taxas.

O total dos Impostos e taxas fica visivel em baixo da tabela. Fazendo o clique em Quebra de Imposto irá mostrar todos os componentes e valores.

<img class="screenshot" alt="Taxes in Quotation" src="{{docs_base_url}}/assets/img/selling/quotation-taxes.png">

Para adiconar impostos automaticamente via uma Categoria de Imposto, visite [esta pagina](/docs/user/manual/pt/contabilidade/categoria-imposto).

#### Regra de Envio
Uma Regra de Envio ajuda a definir o custo do envio do Item. O custo normalmente aumenta com a distancia do envio. Para saber mais, visite a pagina [Regras de Envio](/docs/user/manual/pt/vendas/regra-envio).

### 3.5 Desconto Adicional
Para alem de oferecer descontos por item, voce pode adiconar um desconto global a proforma nesta secção. O desconto pode ser com base no Total Geral i.e., pos impstos/taxas ou Total liquido i.e., antes dos impostos/taxas. O desconto adiconar pode ser aplicado como percentagem ou um valor.

Leia [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto) para mais detalhes.

### 3.6 Termos de Pagamento
Algumas vezes o pagamento não é feito por completo. Dependendo do acordo, metade do pagamento pode ser feito antes do envio e a outra parte depois de receber os bens/serviços. Voce pode adiconar o Modelo de Termos de Pagamento manualemente nesta secção.

<img class="screenshot" alt="Payment Terms in Quotation" src="{{docs_base_url}}/assets/img/selling/quotation-payment-terms.png">

Para saber mais sobre Termos de Pagamento, [clique aqui](/docs/user/manual/pt/contabilidade/termos-pagamento).

### 3.7 Termos e Condições
Em transações de Vendas/Compras pode ter alguns Termos e Condições com base no qual o Fornecedor entrega bens ou serviços a um Cliente. Voce pode aplicar os Termos e Condições as transações e elas vão aparecer quando imprimir o documento. Para saber sobre Termos e Condições, [clique aqui](/docs/user/manual//pt/configuração/imprimir/termos-e-condições)

### 3.8 Configuração de Impressão
#### Cabeçalho
Voce pode imprimir proformas/ordens de venda com o logotipo da empresa. Saiba mais [aqui](/docs/user/manual//pt/configuração/imprimir/cabeçalho-carta).

'Agrupar itens iguais' irá agrupar os itens iguais adiconados varias vezes na tabela de itens. Este pode ser visto ao imprimir.

#### Imprimir Cabeçalho
Proformas podem ter titulo como “Factura Proforma” ou “Proposta”.
Voce pode fazer isso selecionando **Imprimir Cabeçalho**. Para criar um novo Imprimir Cabeçalho va para: Home > Configurações > Imprimir > Imprimir Cabeçalho. Saiba mais [aqui](/docs/user/manual//pt/configuração/imprimir/imprimir-cabeçalhos).

### 3.9 Mais Informações
* **Campanha:** Uma campanha de Vendas pode ser associada a proforma. Um conjunto de proformas podem fazer parte de uma campanha de Vendas.
* **Fonte:** Um tipo de Fonte do Lead pode ser ligado se a proforma for para um lead, campanha, de um fornecedor, etc,. Selecione um Cliente existente se for para um cliente.
* **Proforma de Fornecedor:** Uma Proforma de Fornecedor pode ser ligado para comparar com a sua proforma corrente a um comprador. Voce pode ter uma ideia de lucro/perca ao compara os dois.

### 3.10 Submetendo a Proforma
Proforma é uma transação que pode ser “Submetida”. Quando voce faz o clique em Salvar, um rascunho é criado, ao submeter, será permanente. Vendo que voce envia esta Proforma para o seu Cliente our Lead, voce não deve fazer modificações depois de enviar a Proforma.

Ao submeter, voce criar uma Ordem de Vendas ou uma Subcrição apartir da Proforma usando o botão Criar. No Dashboard presente no topo, voce pode ir para as Ordens de Venda ligadas a esta Proforma. Em caso não funcionar, voce pode definir a Cotação como perdida fazendo o clique em 'Definir como Perdida'.

<img class="screenshot" alt="Submitted Quotation" src="{{docs_base_url}}/assets/img/selling/submitted-quotation.png">

### 4. Topicos Relacionados
1. [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto)

{next}
