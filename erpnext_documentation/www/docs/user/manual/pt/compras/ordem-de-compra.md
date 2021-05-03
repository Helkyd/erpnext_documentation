<!-- add-breadcrumbs -->
# Ordem de Compra

**Uma Ordem de Compra é um contracto que liga com o seu Fornecedor no qual voce prometeu comprar um conjunto de itens dentro das condições definidas.**

É igual a Ordem de Venda mas em veze de enviar a um parceiro externo, voce guarda para registo internos.

> Home > Comprar > Aquisição > Ordem de Compra

![Fluxo de Compras](/docs/assets/img/buying/buying_flow_po.png)

## 1. Pre-requisitos
Antes de criar e usar uma Ordem de Compra, é aconselhavel criar o seguinte:

* [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
* [Item](/docs/user/manual/pt/inventario/item)


## 2. Como criar uma Ordem de Compra

Uma Ordem de Compra pode ser criado automaticamente apartir de uma Solicitação de Material ou de um Cotação de Fornecedor.

1. Va para a lista de Ordem de Compra, clique em Novo.
1. Selecione o Fornecedor, requerido por data.
1. Na tabela Itens, selecione o item pelo codigo, voce pode mudar o requerido por data para cada item.
1. Defina a quantidade e o preço sera automaticamente inserido se definido no Item.
1. Defina os Impostos.
1. Salvar e Submeter.
    <img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/purchase-order.png">

### 2.1 Configuração de Armazens

* **Defina o Armazem Alvo**: Opcional, voce pode definir o Armazem alvo padrão aonde os itens comprados sera entregues. Este sera inserido nas linhas da tabela.

### 2.2 Procurando Itens apartir de uma Solicitação de Material Aberta
Itens pode ser procurados na Ordem de Compra automaticamente apartir de uma [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material) aberta. Para que isto funcione, siga os seguintes passos:

1. Selecione o Fornecedor na Ordem de Compra.
1. Defina o Fornecedor padão no formulario do Item [Padrão do Item](/docs/user/manual/pt/inventario/item#39-padrões-do-item).
1. Uma [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material) precisar ser do tipo 'Compra'.
1. Clique no botão **Obter Itens apartir da Solicitação de Material Aberta** em baixo do nome do Fornecedor. Agora uma caixa de dialogo irá aparecer com as Solicitações de Material contendo itens no qual o Fornecedor padrão é igual para todos os selecionados na Ordem de Compra. Ao selecionar a Solicitação de Material e fazendo o clique em **Obter Itens**, os Itens vao ser procurados apartir da Solicitação de Material.
<img class="screenshot" alt="Get Items from Open Material Requests" src="{{docs_base_url}}/assets/img/buying/get-items-from-open-mr.png">

> **Nota:** O botão **Obter Itens apartir da Solicitação de Material Aberta** é visivel até que a tabela de Itens fique vazia.

## 3. Funcionalidades

### 3.1 Endereço e Contacto

* **Selecionar o Endereço do Fornecedor**: O Endereço de cobrança do Fornecedor.
* **Selecionar o Endereço de Envio**: O Endereço de envio do Fornecedor no qual eles vão enviar os itens.
* Endereço, Endereço de Envio, Contacto, email de Contacto sao procurados se foram salvos na ficha do Fornecedor.

Para India:

* **Supplier and Company GSTIN**: The GST Identification Number of your Supplier and your company.
* **Place of Supply**: For GST, Place of Supply is necessary. It consists of the state's name and number.

### 3.2 Moeda e Lista de Preços
Voce pode definir a moeda no qual a ordem de compra é guardada. Se voce definir a Lista de Preço, então os preços dos itens vao ser procurados apartir desta lista. Selecionando em Ignorar Regras de Preço ira ignorar as Regras de Preço definidos em Contabilidade > Regras de Preço.

Para saber sobre Listas de Preços, [clique aqui](/docs/user/manual/pt/inventario/lista-preços).

Para saber sobre gerirndo transações em varias moedas, [clique aqui](/docs/user/manual/pt/contabilidade/artigos/gerir-transações-multiplas-moedas).

### 3.3 Subcontratando ou 'Fornecer Materia Prima'

Definindo a opção 'Fornecer Material Prima' é util para subcontractar aonde voce providencia a materia prima para o fabrico de um item. Para saber mais, visite a [pagina Subcontractando](/docs/user/manual/pt/fabrico/subcontratação).

### 3.4 A tabela de Itens

* **Codigo de Barras**: Voce pode adiconar Itens na tabela Item fazendo o scan dos codigos de barra se tiver um leitor. Saiba como rastrear [aqui](/docs/user/manual/pt/inventario/artigos/rastrear-itens-usando-codigo-de-barras)

* **Quantidade e Preço**: Quando voce seleciona o Codigo do Item, o seu nome, descrição, e UDM vao ser procurados. O 'Factor de Conversão UDM' é definido por defeito 1, voce pode mudar dependendo da UDM que recebeu do seu vendedor, mais aqui neste secção.

    'Taxa da Lista de Preço' sera procurada se uma taxa de Compra Padrão foi definida. 'Ultima Taxa de Compra' mostra o preço do item da sua ultima Ordem de Compra. Preço sera procurado se foi definido na tabela Item. Voce pode anexar um Modelo de Imposto de Item para aplicar uma taxa de imposto ao item.

* **Peso do Item** sera procura se definido na tabela Item caso contrario digite manual.

* **Armazem**: O armazem aonde os itens vão ser entregues, sera auto preenchido se 'Defina Armazem Alvo' foi defino na Ordem de Compra. Pela Ordem de Cobertura, uma Ordem de Cobertura pode ser ligada, saiba mais [clique aqui](/docs/user/manual/pt/vendas/pedido-cobertura). Um 'Projecto' pode ser ligado para rastrear o progresso. Uma 'LDM' ou Lista de Materiais pode tambem ser ligado para rastrear o progresso.

* 'Qtd de acordo o UDM de Stock' irá mostrar o stock corrente de acordo a UDM definido na Item. 'Qtd Recebida' ira ser actualizado quando os itens são cobrados.

* **Detalhes de Contabilidade**: Neste secção é auto preenchido para a Ordem de Compra. 'Conta de Despesas' é uma conta contra o qual a OC é cobrada e o Centro de Custo é Centro de Custo contra o qual a OC é cobrada.

Um “Necessario pela” data em cada Item: Se voce estiver a espera entrega de peça, o seu Fornecedor irá saber a quantidade a entregar e em que data. Isto irá ajudar voce em não ter um volume alto de stock. Ajuda tambem voce a rastria como o seu Fornecedor esta.

**Permitir Taxa de Avaliação Zero**: Selecionando 'Permitir Taxa de Avaliação Zero' irá permitir submeter o Recibo de Compra mesmo que a Taxa de Avaliação do Item seja 0. Este pode ser para um item de amostra ou devido a um entendimento mutuo com o seu fornecedor.

### 3.6 Fornecido Materia Prima
Esta secção aparece quando 'Fornecer Materia Prima' é definido como 'Sim'. Esta secção mostra a tabela com os Itens a serem entregues ao Fornecedor para o processo de Subcontratação.

* **Defina o Armazem Rerserva**: Quando [Subcontractando](/docs/user/manual/pt/fabrico/subcontratação), a materia prima pode ser reservada em Armazens separados. Ao selecionar o Armazem Reservado aqui, ira inserido nas linhas dos itens da tabela de Materias Primas.

#### Tabela de Itens Entregues

* **Quantidade Necessaria**: A contagem dos Itens necessarios para completar a subcontracação como especificado na [LDM](/docs/user/manual/pt/fabrico/lista-de-materiais).
* **Quantidade Fornecida**: Este sera actualizado quando voce criar o Registo de Entrada para transferir materiais para o Armazem do Fornecedor apartir do Armazem Reserva usando o botão **Transferir**.
    ![Transferencia de Material do Subcontracto](/docs/assets/img/buying/subcontract-transfer-materials.gif)

### 3.7 Conversão de UDM de Compra e UDM de Stock

Voce pode mudar a sua UDM de acordo o seu requesito de stock na Ordem de Compra.

Por exemplo, se voce comprou a sua materia prima em grandes quantidades com UDM - caixas, e deseja guardar em UDM - Nos; voce pode fazer quando estiver a criar a Ordem de Compra.

1. Guarde a UDM como Nos no Item. Nota que a UDM no Item é a UDM do Stock.

2. Na Ordem de Compra mencione a UDM como Caixa. (Vendo que o material chega em Caixas)

3. No Armazem e secção de Referencia, a UDM sera puxadas em Nos (apartir do formulario do Item):

 <img class="screenshot" alt="Purchase Order - UOM" src="{{docs_base_url}}/assets/img/buying/purchase-order-uom.png">

4. Mencione o Factor de Conversão. Por exemplo, (1); Se uma caixa tem 1 kilo.

5. Note que a quantidade de stock sera actualizado automaticamente.

 <img class="screenshot" alt="Purchase Order - UOM" src="{{docs_base_url}}/assets/img/buying/po-stock-uom.png">

### 3.8 Impostos e Taxas

Se o seu Fornecedor cobrar impostos adicionais ou cobrar como taxa de
envio ou segurança, voce pode adiconar aqui. Irá ajudar voce a 
ter um controle de custo certo. Tambem, se algum dos impostos adicionam valor 
ao produto voce tera de mencionar na tabela de Impostos.

Visite a pagina [Modelo de Impostos de Compra e Taxas](/docs/user/manual/pt/compras/modelo-impostos-taxas-compra) para saber mais sobre impostos.

O total dos impostos e taxa vao ser mostrados em baixo da tabela.

Para adicionar impostos automaticamente via Categoria de Imposto, visite [esta pagina](/docs/user/manual/pt/contabilidade/categoria-imposto).

Tenha a certeza em marcar todos os impostos na tabela de Impostos e Taxa correctamente para uma avaliação correcta.

#### Regras de Envio
Uma Regra de Envio ajuda a definir o custo do envio do Item. O custo irá aumentar com a distancia do envio. Para saber mais, visite a pagina [Regras de Envio](/docs/user/manual/pt/vendas/regras-envio).

<img class="screenshot" alt="Purchase Order Taxes" src="{{docs_base_url}}/assets/img/buying/po-taxes.png">

Por exemplo, voce compra Itens no valor de X e vendo por 1.3X. Então o seu Cliente
paga 1.3 veze o imposto que voce paga ao seu Fornecedor. Vendo que voce já pagou o imposto
ao seu Fornecedor por X, o que voce deve ao governo é somente o valor do imposto em 0.3X.

Isto é muito facil ver no ERPNext veno que cada imposto é uma Conta.
O ideal é voce criar duas Contas para cada tipo de VAT que paga e recebe,
“Compras VAT-X” (activos) e “Vendas VAT-X” (responsabilidade), ou algo para esse efeito.

### 3.9 Desconto Adiconal
Para alem de gravar descontos por item, voce pode adionar um desconto a ordem de compra completa nesta secção. Este desconto pode ser com base no Total Geral i.e., depois do imposto/taxa ou no Total Liquido i.e., antes do imposto/taxas. O Desconto adicional pode ser aplicado em percentagem ou em valor.

Leia [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto) para mais detalhes.

### 3.10 Termos de Pagamento
Algumas vezes o pagamento não é feito na totalidade. Dependendo do acordo, metade do pagamento pode ser feito antes do envio e a outra parte depois de receber os bens/serviços. Voce pode adiconar o Modelo de Termos de Pagamento ou adiconar os termos manualmente nesta secção.

Para sber mais sobre Termos de Pagamento, [clique aqui](/docs/user/manual/pt/contabilidade/termos-pagamento).

### 3.11 Termos e Condições
Em transações de Vendas/Compras pode haver alguns Termos e Condições com base em que o Fornecedor forneça bens ou serviços ao Cliente. Voce pode aplicar os Termos e Condições a transações que vão aparecer quando imprimir o docume nto. Para saber sobre Termos e Condições , [clique aqui](/docs/user/manual/pt/configuração/imprimir/termos-e-condições)

### 3.12 Configurações de Impressão
#### Cabeçalho
Voce pode imprimir o seu pedido de cotação / compra com o cabeçalho da sua empresa. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

'Agrupar Itens iguais' irá agrupar os itens iguais adiconados varias vezes na tabela de itens. Este pode ser visto ao imprimir.

#### Imprimir Cabeçalho
Titulos dos seu documentos pode ser trocado. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/imprimir-cabeçahos).

O Desconto Adiconal do vendedor, Termos de Pagamento, Termos e Condições podem ser registados na Ordem de Compra.

### 3.13 Mais Informação
Esta secção mostra o status da Ordem de Compra, percentagem de itens recebidos, e pertencegem de itens cobrado. Se for um pedido Inter Empresas, a Ordem de Venda por de ser ligada aqui.

### 3.14 Depois de Submetido
Uma vez que “Submetida” a Ordem de Compra, voce pode acionar acções:

* Voce pode Adiconar, Actualizar, Apagar itens na Ordem de Compra fazendo o clique no botão **Actualizar Itens**. Contudo voce não pode apagar itens que ja foram recebidos.

* Status: Uma vez submetidos, voce pode por em espera a Ordem de Compra ou Fechar.

* Criar: Apartir de uma Ordem de Compra Submetida, voce pode criar os seguintes:

    * [Recibo de Compra](/docs/user/manual/pt/inventario/recibo-compra) - Um recibo indicando que voce recebeu os itens.
    * [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra) - Uma factura/cobrança para a ordem de compra.
    * [Registo de Pagamento](/docs/user/manual/pt/contabilidade/registo-pagamento) - Um registo de pagamento indica que o pagamento foi feito contra uma ordem de compra.
    * [Lançamento Contabilistico](/docs/user/manual/pt/contabilidade/lançamento-contabilistico) - Um Lançamento Contabilistico é guardado no Razão Geral.

    ![Depois de Submeter uma Ordem de Compra](/docs/assets/img/buying/po-after-submit.png)

### 4. Topicos Relacionados
1. [Solicitação de Cotação](/docs/user/manual/pt/compras/solicitação-cotação)
1. [Modelo de Imposto de Compras e Taxas](/docs/user/manual/pt/compras/modelo-impostos-taxas-compra)
1. [Comprando em Unidades Diferentes](/docs/user/manual/pt/compras/artigos/comprando-em-unidades-diferentes)
1. [Emendando Ordem de Compra depois de Submetida](/docs/user/manual/pt/compras/artigos/corrigindo-ordens-compra-depois-de-submetido)

{next}
