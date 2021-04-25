<!-- add-breadcrumbs -->
#Devolução de Compra

**Um Item comprado sendo devolvido é conhecido como Retorno de Compra.**

Com a funcionalidade de Retorno de Compra, voce pode devolver produtos para o 
seu Fornecedor. Este pode ter varios motivos como defeito nos bens, 
ma qualidade, o comprador não precisa do item, etc.

## 1. Pre-requisitos
Antes de criar e usar um Devolução de Compra, é aconselhavel criar os seguintes:

* [Item](/docs/user/manual/pt/inventario/item)
* [Factura de Compras](/docs/user/manual/pt/contabilidade/factura-compra)
    
    Ou

    [Recibo de Compras](/docs/user/manual/pt/inventario/recibo-compra)


## 2. Como criar um Devolução de Compra
1. Primeiro abra o Recibo de Compra original, no qual o fornecedor entregou os Bens.

    <img class="screenshot" alt="Original Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-return-original-purchase-receipt.png">

1. Clique em 'Criar > Devolução de Compra', irá abrir um novo Recibo de Compras com 'É um Retorno' activo. Itens, Preços, e impostos ficam a negativo.

    <img class="screenshot" alt="Return Against Purchase Receipt" src="{{docs_base_url}}/assets/img/stock/purchase-return-against-purchase-receipt.png">

1. Ao submeter o Retorno das Compras, o sistema irá reduzir a quantidade do Armazem mencionado. Para manter avaliação correcta do stock, o balanço de stock irá tambem irá subir de acordo o preço da compra original dos bens devolvidos.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/purchase-return-stock-ledger.png">

1. No Razão da Contabilidade, a conta do Stock em Mão será creditado e a conta dos Stocks Recebidos mas não Cobrados será debitada.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/purchase-return-general-ledger.png">

Se o Inventario Perpetuo estiver activo, o sistema irá tambem postar um registo contabilistico contra a conta do Armazem para sincronizar o balanço da conta do armazem com o balanço de stock de acordo o Razão do Stock.

### 3. Topicos Relacionados
1. [Devolução de Vendas](/docs/user/manual/pt/inventario/retorno-vendas)
1. [Inventario Perpetuo](/docs/user/manual/pt/inventario/inventario-perpetual)
