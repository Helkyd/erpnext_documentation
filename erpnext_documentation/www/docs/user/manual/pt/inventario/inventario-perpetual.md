<!-- add-breadcrumbs -->
# Inventario Perpetuo

De acordo o sistema de inventario perpetual, registo de contabilidade é feito para cada transação de stock. Caso contrario, é feito em intervalos maiores por exemplo mensal ou cada quatro meses. Cada armazem está ligado com uma Conta de contabilidade.

Ao receber os itens num armazem em particular, o balanço na Conta do Armazem irá aumentar. De igual modo, quando os Itens são entregues apartir de um Armazem, um despesa será alocada, e o balanço na Conta do Armazem será reduzida.

### 1. Como criar um inventario perpetuo

1. Activar Inventario Perpetuo:

    **Home > Contabilidade > Empresa > Activar Inventario Perpetuo**

    <img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-1.png">
    De notar que se desactivar o inventario Perpetuo, os usuarios vão ter que gerir as entradas de contabilidade manualmente.
1. Defina as seguintes contas padrão para cada Empresa se não estiver definidas. Estas contas são criadas automaticamente no ERPNext.

    * Conta de Inventario Padrão (Activos)
    * Stock Recebido mas não Cobrado (Responsabilidade)
    * Conta de Ajuste de Stock (Despesas)
    * Despesas Incluidas na Avaliação (Despesas)
    * Centro de Custo

1. Se o usuario quiser definir uma conta individual para cada armazem, crie uma conta para cada. Va para:

    **Contabilidade > Plano de Contas > Empresa > Aplicação de Fundos (Activos) > Activo Corrente > Activo de Stock > *Criar uma nova conta com o mesmo nome que o Armazem***

    Agora, va para o armazem e ligue esta conta ao armazem. Isto ajudará no filtro e visualizaçao de demonstração de armazens.

1. Para transações de Stock, entradas de Razão Geral feitos contra uma Conta definida no Armazem, se o usuario não definiu a conta para o armazem então o sistema irá usar a conta do armazem Pai. Se a Conta não foi definida no armazem Pai então o sistema busca a conta (Conta Padrão de Inventario) na tabela da Empresa.

* * *

### 2. Exemplo

Considere o seguinte Plano de Contas e Armazens configurados para a sua Empresa:

Planos de Contas:

* Activos (Dr)
    * Activos Corrente
        * Contas a Receber
            * Devedores
        * Activos de Stock
            * Armazens
            * Bens Produzidos
            * Trabalhos em Progresso
        * Impostos de Activos
            * VAT
* Responsabilidades (Cr)
    * Responsabilidades Correntes
        * Conta a Pagar
            * Credores
        * Resposabilidades de Stock
            * Stock Recebido mas Não Cobrado
        * Responsabilidades de Imposto
            * Imposto de Serviço
* Entradas (Cr)
    * Entradas Directas
        * Conta de Vendas
* Despesas (Dr)
    * Despesas Directas
        * Despesa de Stock
            * Custo dos Bens Vendidos
            * Depesas Incluidas na Avaliação
            * Ajuste de Stock
    * Despesas Indirectas
        * Custos de Shipping
        * Despesas de Alfandega

#### 2.1 Armazem - Configuração de Contas

  * Armazens
  * Trabalhos em Progresso
  * Bens Produzidos

#### 2.2 Recibo de Compra

Vamos assumir que comprou _10 nos_ do item "RM0001" por _$200_ e _5 nos_ do item "Base Plate" por **$100** do fornecedor "Arcu Vel Quam Fabricators". Em baixo os detalhes do Recibo de Compra:

**Fornecedor:** Arcu Vel Quam Fabricators

**Itens:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Armazem</th>
            <th>Qtd</th>
            <th>Preço</th>
            <th>Valor</th>
            <th>Taxa de Avalição</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>10</td>
            <td>200</td>
            <td>2000</td>
            <td>2250</td>
        </tr>
    </tbody>
</table>
<p><strong>Impostos:</strong>
</p>
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Conta</th>
            <th>Valor</th>
            <th>Categoria</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Imposto de Shipping</td>
            <td>100</td>
            <td>Total e Avaliação</td>
        </tr>
        <tr>
            <td>VAT (10%)</td>
            <td>200</td>
            <td>Total</td>
        </tr>
        <tr>
            <td>Taxa de Alfandega</td>
            <td>150</td>
            <td>Avaliação</td>
        </tr>
    </tbody>
</table>

**Razão do Stock**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-receipt-sl-1.png">

**Razão Geral**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-receipt-gl-2.png">

Vendo que o balanço de Stock aumenta pelo Recibo de Compra, as contas do "Armazem" são debitadas e uma conta temporaria "Stock Recebido mas não Cobrado" é creditado, para manter o duplo registo do sistema de contabilidade. Ao mesmo tempo, a despesa negativa é alocada na conta com a categoria "Avaliação" ou "Total e Avaliação" na tabela impostos e taxas pelo valor adicionado para motivos de avaliação, pra evitar alocação dupla de despesas.

#### 2.3 Factura de Compra

Ao receber a Factura do fornecedor, para o Recibo de Compra em cima, você irá fazer uma Factura de Compra para o mesmo. As entradas do razão geral são:

**Razão Geral**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-pinv-gl-3.png">

Aqui a conta "Stock Recebido Mas Não Cobrado" é debitada que anula o efeito do Recibo de Compra.

#### 2.4 Guia de Remessa

Podemos dizer, que voce fez o pedido a "Utah Automation Services" para entregar 5 nos do item "RM0001"
por $300. De seguida os detalhes da Guia de Remessa:

**Cliente:** Utah Automation Services

**Itens:**
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Armazem</th>
            <th>Qtd</th>
            <th>Preço</th>
            <th>Valor</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>5</td>
            <td>300</td>
            <td>1500</td>
        </tr>
    </tbody>
</table>
<p><strong>Impostos:</strong>
</p>
<table class="table table-bordered">
    <thead>
        <tr>
            <th>Conta</th>
            <th>Valor</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Imposto de Serviço</td>
            <td>150</td>
        </tr>
        <tr>
            <td>VAT</td>
            <td>100</td>
        </tr>
    </tbody>
</table>

**Razão do Stock**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-dn-sl-4.png">

**Razão Geral**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-dn-gl-5.png">

Como um item é entregue apartir do armazem "Stores", a conta "Stores" é creditada e um valor igual é
debitado a conta de despesas "Custo dos Bens Vendidos". O valor
debito/credito é igual ao valor total de avaliação (custo de compra) dos
itens vendidos. E o valor da avaliação é calculado com base no metodo de avaliação preferido
(FIFO / Media Movel) ou custo actual dos itens serializados.



    Neste exemplo, nós consideramos o metodo de avaliação FIFO.
    Taxa de Avaliação  Preço de Compra + Taxas Incluidas na Avaliação
                    = 200 + (250 / 10)
                    = 225
    Valor Total da Avaliação = 220 * 5
                            = 1125



* * *

### 2.5 Facturas de Venda com Actualizar Stock

Digamos, que voce não fez a Guia de Remessa contra a ordem em cima e em vez disso,
voce fez a Factura de Venda directa, com a opção "Actualizar Stock". Os detalhes da Factura de Venda 
são iguais aos da Guia de Remessa.

**Razão do Stock**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-inv-sl-6.png">

**Razão Gerarl**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-inv-gl-7.png">

Aqui, para alem dos registos contabilisticos normais para um facturas, contas dos "Armazens" e "Custo dos Bens Vendidos"
 tambem são afectado com base no valor da avaliação.

#### 2.6 Registo de Stock (Recepção de Material)

**Itens:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Armazem Alvo</th>
            <th>Qtd</th>
            <th>Preço</th>
            <th>Valor</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>50</td>
            <td>220</td>
            <td>11000</td>
        </tr>
    </tbody>
</table>

**Razão de Stock**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-receipt-sl.png">

**Razão Geral**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-receipt-gl.png">

#### 2.7 Registo de Stock (Solicitação de Material)

**Itens:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Armazem Fonte</th>
            <th>Qtd</th>
            <th>Preço</th>
            <th>Valor</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>10</td>
            <td>220</td>
            <td>2200</td>
        </tr>
    </tbody>
</table>

**Razão do Stock**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-issue-sl.png">

**Razão Geral**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-issue-gl.png">

#### 2.8 Registo de Stock (Transferencia de Material)

**Itens:**

<table class="table table-bordered">
    <thead>
        <tr>
            <th>Item</th>
            <th>Armazem Fonte</th>
            <th>Armazem Alvo</th>
            <th>Qtd</th>
            <th>Preço</th>
            <th>Valor</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>RM0001</td>
            <td>Stores</td>
            <td>Work In Progress</td>
            <td>10</td>
            <td>220</td>
            <td>2200</td>
        </tr>
    </tbody>
</table>

**Razão do Stock**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-transfer-sl.png">

**Razão Geral**

<img class="screenshot" alt="Perpetual Inventory" src="{{docs_base_url}}/assets/img/accounts/perpetual-st-transfer-gl.png">

#### 3. Topicos Relacionados
1. [Contabilidade do Inventario de Stock](/docs/user/manual/pt/inventario/contabilidade-inventario-stock)
1. [Emigrar para o Inventario Perpetuo](/docs/user/manual/pt/inventario/artigos/emigrar-para-inventario-perpetual)