<!-- add-breadcrumbs -->
# Devolução de Vendas

**Um Item vendido sendo devolvido é conhecido como Devolução de Venda.**

Bens vendidos sendo devolvidos é normal. Eles podem ser devolvidos pelo cliente por questões de qualidade, não entrega na data acordada, ou qualquer outra razão. 

## 1. Pre-requisitos
Antes de criar e usar a Devolução de Venda, é aconselhavel criar os seguintes:

* [Item](/docs/user/manual/pt/inventario/item)
* [Devolução de Vendas](/docs/user/manual/pt/contabilidade/retorno-vendas)
    
    Ou

    [Guia de Remessa](/docs/user/manual/pt/inventario/guia-de-remessa)

## 2. Como criar uma Devolução de Venda

1. Primeiro abra a Guia de Remessa / Factura de Venda original, no qual o Cliente devolveu os bens.

    <img class="screenshot" alt="Original Delivery Note" src="{{docs_base_url}}/assets/img/stock/sales-return-original-delivery-note.png">

1. Depois faça o clique em 'Criar > Retorno de Vendas', que irá abrir uma nova Guia de Remessa com 'É um Retorno' selecionado, Itens, Preços e impostos ficam a negativo.

    <img class="screenshot" alt="Return Against Delivery Note" src="{{docs_base_url}}/assets/img/stock/sales-return-against-delivery-note.png">

1. Voce pode tambem criar um registo de retorno contra uma Factura de Venda, para devolver o stock com uma Nota de Credito, selecione a opção "Actualizar Stock" na Devolução da Factura de Vendas.

    <img class="screenshot" alt="Return Against Sales Invoice" src="{{docs_base_url}}/assets/img/stock/sales-return-against-sales-invoice.png">

1. Ao submeter a devolução de uma Guia de Remessa / Factura de Vendas, o sistema irá aumentar o balanço de stock no Armazem mencionado. Para manter a avaliação do correcta, balanço de stock irá aumentar de acordo a taxa de compra original dos itens devolvidos.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/sales-return-stock-ledger.png">

1. No de devolução de Factura de Vendas, a conta do Cliente será creditada e o valor de entrada associado e conta de imposto seram debitados como mostra no Razão de Contabilidade.

    <img class="screenshot" alt="Return Stock Ledger" src="{{docs_base_url}}/assets/img/stock/sales-return-general-ledger.png">

Se o Inventario Perpetuo estiver activo, o sistema irá tambem postar registos contabilisticos contra a conta do armazem para sincronizar a conta de balanço do stock como o Razão do Stock.

## 3. Topicos Relacionados
1. [Devolução de Compras](/docs/user/manual/pt/inventario/retorno-compras)
1. [Inventario Perpetuo](/docs/user/manual/pt/inventario/inventario-perpetual)
