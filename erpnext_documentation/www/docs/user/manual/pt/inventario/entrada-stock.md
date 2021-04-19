<!-- add-breadcrumbs -->
# Registo de Stock

**Um Registo de Stock pemite registar o movimento do Item entre Armazens.**

Para aceder va para lista de Registo de Stock, va para:
> Home > Inventario > Transações de Stock > Registo de Stock

Registo de Stocks pode ser feito com os seguintes propositos:

* **Requisição de Material**: Se o material esta a ser soliçitado para alguem dentro ou fora da empresa. Estes Itens serao deduzidos do Armazem definidos no Armazem Fonte.
* **Receção de Material**: Se o material esta a ser recebido. Os Itens serao adicionados ao Armazem definido no Armazem Alvo.
* **Transferencia de Material**: Se o material está a ser movido de um Armazem interno para outro.
* **Transferencia de Material para Fabrico**: Se a materia prima está a ser transferida para produção. A transferencia pode ser contra uma [Ordem de Trabalho](/docs/user/manual/pt/fabrico/ordem-trabalho) ou um [Cartão de Trabalho](/docs/user/manual/pt/fabrico/cartao-trabalho). Para saber mais, visite a pagina  [Lista de Materiais](/docs/user/manual/pt/fabrico/lista-de-materiais) .
* **Material de Consumo para Fabrico**: Pode have varios registo de consumo de stock contra uma Ordem de Trabalho para fabrico. [Siga esta link para mais detalhes](/docs/user/manual/pt/fabrico/artigos/consumo-de-material)
* **Fabrico**: Se o Material a ser recibo de um Fabrico/Operação de Produção.
* **Reembalar**: Se o item/Itens Originais estão a ser reembalados para um novo item/itens.
* **Subcontracto**: Se o Material esta ser solicitado para uma operação de um Sub-contracto. Esta entrada é feita para a Ordem de Compra. Para saber mais, visite a pagina [subcontratação](/docs/user/manual/pt/fabrico/subcontratação) .
* **Enviar para o Armazem**: Se o Material a ser enviado a um Armazem e precisa de confirmação pela parte a receber, este documento será selecionado no Registo de Stock com o tipo 'Receba no Armazem' para confirmar quantos itens foram recebidos. O status será 'Bens em Transito' até que todos os bens sejam recebidos, no depois o status irá mudar para 'Bens Transferidos'.
* **Receba no Armazem**: Se o Material está a ser recebido no Armazem o tipo de Registo de Stock 'Enviar para o Armazem' será selecionario aqui e o numero de bens recebidos será atualizado.

Para saber mai em detalhe sobre os tipos de registo de stock, [visite esta pagina](/docs/user/manual/pt/inventario/artigos/motivo-registo-stock).


## 1. Pre-requisitos
Antes de criar e utilizar o Registo de Stock, é aconselhavel que crie os seguintes primeiro:

* [Armazem](/docs/user/manual/pt/inventario/armazem)
* [Item](/docs/user/manual/pt/inventario/item)


## 2. Como criar um Registo de Stock
Registos de Stock para motivos de Fabrico são criados apartir de uma [Ordem de Trabalho](/docs/user/manual/pt/fabrico/ordem-trabalho). Para criar um Registo de Stock manual para outros motivos, siga estes passos:

1. Va para a lista de Entrada de Stock, clique em Novo.
1. Selecion o Motivo do Registo de Stock apartir dos listados em cima.
1. Se voce definir a Fonte Padrão ou os Armazens Alvo, eles serao automaticamente preenchidos nas linhas da table de Itens.
1. Armazens Fonte/Alvo ficaram disponiveis de acordo o Motivo de Registo de Stock que selecionou.
1. Selecione Itens e digite a quantidade.
1. O preço basico sera procurado e o valor será calculado automaticamente.
1. Salvar e Submeter.

    <img class="screenshot" alt="Stock Entry" src="{{docs_base_url}}/assets/img/stock/stock-entry.png">

Normalmente, "Armazem Fonte" e "Armazem Alvo" ambos são definidos para gravar um movimento.

### 2.1 Opções Adicionais ao criar um Registo de Stock

* **Ordem de Trabalho**: Se este for um registo de Fabrico, a Ordem de trabalho será mostrada neste campo.
* **Editar a Data e Hora de Postagem**: Irá permitir que você edite a data e hora do Registo de Stock.
* **Inspeção Necessaria**: Se uma [Inspeção de Qualidade](/docs/user/manual/pt/inventario/inspecao-de-qualidade) for necessaria aos Itens antes de submeter o Registo de Stock.
* **Apartir do LDM**: Se este registo for um Fabrico, a LDM associada para o Item sendo fabricado será mostrado.

### 2.2 Tipo de Registo de Stock
Vocẽ pode tambem criar um Tipo de Registo de Stock aonde somente o nome será diferente, por exemplo 'Entrada de Desgaste'. O motivo será Transferencia de Materia mas o nome será diferente. É util se você quer que certo usuarios tenha acesso somente a acções especificas relacionadas ao Stock.

![Tipo de Registo de Stock](/docs/assets/img/stock/stock-entry-type.png)

## 3. Funcionalidades

### 3.1 A tabela de Itens
Detalhes sobre o Item, Preço, Quantidade, etc. serao mostrados aqui.

Selecionando 'Permitir Taxa de Avalição Zero' irá permitir submeter o Recibo de Compra mesmo que a Taxa de Avaliação do Item seja 0. Isto pode ser um Item de amostra ou devido a um acordo mutuo com o seu Fornecedor.

Armazens Fonte e Alvo diferentes podem ser definidos para Itens diferentes.

### 3.2 Custos Adicionais

Se o regito de stock é para um registo de entrada i.e  qualquer item é recebido no armazem alvo, você pode inserir custos adicionais relacionados (como Taxa de Shipping, Direitos de Alfandega, Custos de Operação, etc) associados com o processo. Os custos adicionais seram considerados para calcular o Valor da Avaliação dos itens.

Para adicionar Custos Adicionais:

1. Selecione a Conta de Despesa no qual a despesa deste Registo de Stock será guardado.
1. Digite a descrição e valor do custo na tabela de Custos Adicionais.

<img class="screenshot" alt="Stock Entry Additional Costs" src="{{docs_base_url}}/assets/img/stock/additional-costs-table.png">

Os Custos Adicionais serao distribuidos entre os itens recebidos (aonde o Armazem Alvo mencionado) proporcionalmente com base no Valor Basico dos itens. E o custo adicional distribuido será adicionado ao custo basico do item, para calcular o Valor de Avaliação.

Quantidade e Preço é mostrado como em baixo quando você expande a tabela de Itens.
<img class="screenshot" alt="Stock Entry Item Valuation Rate" src="{{docs_base_url}}/assets/img/stock/stock-entry-item-valuation-rate.png">

### 3.3 Contabilidade de Dimensões
você pode marcar transações diferentes com base em dimensões diferentes. Por defeito, [Projectos](/docs/user/manual/pt/projectos/projecto) pode ser considerado como um dimensão como é de practica analizar custos de projectos diferentes. Para saber mais sobre Contabilidade de Dimensões, [visite esta pagina](/docs/user/manual/pt/contabilidade/dimensao-contabil).

### 3.4 Configurações de Impressão

#### Cabeçalho
Você pode imprimir o seu Recibo de Compra com o logotipo da sua empresa. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

#### Imprimir Cabeçalho
Cabeçalho de Recibo de Compra pode tambem ser trocado ao imprimir o documento. Vocẽ pode fazer isso selecionando um **Imprimir Cabeçalho**. Para criar um novo Imprimir Cabeçalho va para: Home > Configurações > Impressão > Imprimir Cabeçalho. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/imprimir-cabeçalhos).

### 3.5 Mais Informações

* **É Abertura**: Se este registo é de abertura de stock para os Itens.
* **Remarks**: Qualquer remarks adicional sobre o Item.
* **Percentagem Transferida**: A percentagem dos Itens transferidos dependendo do motivo do Registo de Stock.
* **Valor Total**: O valor total de Itens transferidos.

### 3.6 Inventario Perpetual

Se o sistema do Inventario perpetual estiver activo, custos adicionais seram alocado em Conta de Despesas mencionadas na tabela de Custos Adicionais.

<img class="screenshot" alt="Additional Costs General Ledger" src="{{docs_base_url}}/assets/img/stock/stock-entry-additional-cost.png">

<img class="screenshot" alt="Additional Costs General Ledger" src="{{docs_base_url}}/assets/img/stock/additional-costs-general-ledger.png">

### 3.7 Depois de Submeter
Depois de submeter um Registo de Stocks, você poide ir para o Razão do Stock ou Razão Geral pelo dashboard.

<img class="screenshot" alt="Additional Costs General Ledger" src="{{docs_base_url}}/assets/img/stock/stock-entry-submit.png">

## 4. Video

<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/Njt107hlY3I?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>

### 5. Topicos Relacionados
1. [Motivo de Registo de Stock](/docs/user/manual/pt/inventario/artigos/motivo-registo-stock)
1. [Reconciliação de Stock](/docs/user/manual/pt/inventario/reconciliacao-de-stock)
1. [Abertura de Balanço de Stock para Itens Serializados e Lotes](/docs/user/manual/pt/inventario/artigos/abertura-balanco-stock-para-itens-serializados-e-lotes)
1. [Ordem de Trabalho](/docs/user/manual/pt/fabrico/ordem-trabalho)
1. [Plano de Produção](/docs/user/manual/pt/fabrico/plano-de-producao)
1. [Cartão de Trabalho](/docs/user/manual/pt/fabrico/cartao-trabalho)
