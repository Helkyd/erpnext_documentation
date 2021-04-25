<!-- add-breadcrumbs -->
# Reconciliação de Stock

**Reconciliação de Stock é o processo de contagem e avaliação do material/produtos, periodicamente no fim do ano.**

Isto é feito para:

* Manter a contagem fisica actual e alocar a contagem do stock sincronizado
* Valor do stock preparado para declarações de contabilidade

A funcionalidade Reconciliação de Stock no ERPNext é usado para:

* Postar a abertura do stock
* Reconciliar o alocado e o stock actual

Para acessar a lista de Reconciliação de Stock, va para:
> Home > Inventario > Ferramentas > Reconciliação de Stock

## 1. Como Criar uma Reconciliação de Stock para Abertura do Stock

Usnado Reconciliação de Stock voce pode actualizar o numero de itens especificos no armazem num tempo especifico.
Voce pode tambem adiconar Itens no stock para os que tenham Numeros de Serie ou Numeros de Lote.

1. Va para lista Reconciliação de Stock, clique em Novo.
1. Selecione o Motivo como 'Abertura de Stock'. Voce pode editar a Data e Hora de postagem.
1. Selecione o Codigo do Item, Armazem, Quantidade, e Taxa de Avaliação. Se existe um Numero de Serie / Numero de Lote envolvido, adicione.
1. Se voce quiser gerar-automaticamente Numero de Serie / Numero do Lote então mantenha esses campos em branco.
    * Para auto-gerar Numeros de Serie, voce precisa definir "Serie de Numeros de Serie" na tabela do Item.
    * Para auto-gerar Numeros de Lote, voce precisar activar a caixinha "Criar Numeros de Lote Automatico" na tabela item.
1. A Conta de Diferença sera definida como 'Abertura Temporaria'.
1. Salvar e Submeter.

    ![Abertura de Stock](/docs/assets/img/stock/opening_stock.png)

> Nota: A opção Actualizar Stock deve estar activa na tabela Item para que funcione.

## 2. Como Criar uma Reconciliação de Stock para Reconciliar o Alocado e a Contagem Fisica do Stock

Reconciliação de Stock é um process de contagem e avaliação do stock-para-comercializar, periodicamente no fim do ano de formas a dar valor ao stock total e preparar para as declarações de contabilidade. Neste process, o stock fisico actual são verificados e ordenados no sistema. O stock atual no sistema deve estar de acordo e certo. Caso não estejam, voce pode usar a ferramenta Reconciliação de Stock para reconciliar o balanço de stock e o valor com o fisico.

Para reconciliar o stock:

1. Va para a lista Reconciliação de Stock, clique em Novo
1. Selecione o Motivo como 'Reconciliação de Stock'. Voce pode editar a Data e Hora de Postagem.
1. Defina o Codigo do Item, Armazem.
1. A Quantidade corrente e a Taxa de Avaliação serao procurados, muda a quantidade caso necessario.
1. A conta de despesa na Conta de Diferença sera definida para 'Ajuste de Stock' por defeito.
1. O Centro de Custo padrão será 'Principal', troque caso necessario.
1. Salvar e Submeter.
  
    ![Reconciliação de Stock](/docs/assets/img/stock/stock_recon.png)


## 3. Funcionalidades

### 3.1 Carregar Dados Via Folha de Calculo

Se voce tem muitos itens, voce pode carregar os detalhes via uma folha de calculos.

1. Decarregue o Modelo

  Abra uma nova Reconciliação de Stock e clique no botão Descarregar para puxar o modelo no formato CSV.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-recon-1.png">

2. Digite os Dados no Modelo CSV.

  O formato CSV é Maiusculas e Minusculas (case-sensitive). Não edite o cabeçalho que estão pre-definidos no modelo. Na coluna Codigo do Item e Armazem, digite o Codigo do Item e Armazem exactamente como criado no seu ERPNext. Para quantidade, digite o nivel de stock que pretende definir para o item, no armazem especificado.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-reco-data.png">


3. Carregue o ficheiro CSV com os dados fazendo o clique no botão 'Carregar'.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-recon-2.png">


4. Faça a Revisão, Salve e Submeta.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-reco-upload.gif">

5. Verifique o Relatorio de Razão do Stock para o balanço actualizado do stock.

  <img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-reco-ledger.png">

### 3.2 Obtenha o Balanço de Stock e Avaliação apartir de uma Data e Hora Especifica

Voce pode importar o balanço de stock e avaliação apartir de uma data e hora especifica de um Armazem selecionado fazendo o clique no botão **Itens** . Voce pode actualizar a Quantidade e Taxa de Avaliação quando necessario.

<img class="screenshot" alt="Stock Reconciliation Items Button" src="{{docs_base_url}}/assets/img/stock/stock_reconciliation_items_button.gif">

## 4. Como Funciona a Reconciliação de Stocks

Uma vez a reconciliação de stock for inserida para actualizar as quantidades numa data e hora especifica para um item no armazem, não irá modificar transações subsequentes de stock mesmo que estas transações tenham uma data que seja inferior a data de reconciliação. Em outras palavras, registos antigos ou com datas anteriores não vão mudar o numero de stock depois de uma Reconciliação de Stock ter sido feita.

Exemplos de seguida.

### 4.1 Para Itens não serializados
Considere um item com o codigo no armazem 'Mumbai'.
Vamos assumir que o stock no dia 10 de Janeiro é de 100 unidades.
Reconciliação de Stock é feito no dia 12 de Janeiro para ajustar o balanço para 150 unidades.

Razão do Stock deve ser como em baixo:
<html>
<style>
    td {
    padding:5px 10px 5px 5px;
    };
    img {
    align:center;
    };
    table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
    }
</style>
 <table border="1" cellspacing="0px">
            <tbody>
                <tr align="center" bgcolor="#EEE">
                    <td><b>Data de Postagem</b>
                    </td>
                    <td><b>Qtd</b>
                    </td>
                    <td><b>Qtd Disponivel</b>
                    </td>
                    <td><b>Tipo de Voucher</b>
                    </td>
                </tr>
                <tr>
                    <td>10/01/2014</td>
                    <td align="center">100</td>
                    <td>100&nbsp;</td>
                    <td>Recibo de Compra</td>
                </tr>
                <tr>
                    <td>12/01/2014</td>
                    <td align="center">150</td>
                    <td>150</td>
                    <td>Reconciliação de Stock</td>
                </tr>
            </tbody>
        </table>
</html>

Se um novo Recibo de Compra for feito no dia 5 de Janeiro 2014, que é anterior a data do registo de Reconciliação de Stock, o Razão de Stock irá ficar como em baixo.
<html>
    <table border="1" cellspacing="0px">
        <tbody>
            <tr align="center" bgcolor="#EEE">
                <td><b>Data de Postagem</b></td>
                <td><b>Qtd</b></td>
                <td><b>Qtd Disponivel</b></td>
                <td><b>Tipo de Voucher</b></td>
            </tr>
            <tr>
                <td>05/01/2014</td>
                <td align="center">20</td>
                <td style="text-align: center;">20</td>
                <td>Recibo de Compra</td>
            </tr>
            <tr>
                <td>10/01/2014</td>
                <td align="center">100</td>
                <td style="text-align: center;">120</td>
                <td>Recibo de Compra</td>
            </tr>
            <tr>
                <td>12/01/2014</td>
                <td align="center"><br></td>
                <td style="text-align: center;"><b>150</b></td>
                <td>Reconciliação de Stock<br></td>
            </tr>
        </tbody>
    </table>
</html>

Como pode ver, a Qtd Disponivel no dia 10 de Janeiro foi actualizada de 100 para 120. Mas a Qtd Disponivel no dia 12 de Janeiro não foi actualizado de 150 para 170.


### 4.2 Para Itens Serializados

Para um Item, ITEM-00225 que tem 6 numeros de serie HJF00020, HJF00021, HJF00022, HJF00023, HJF00024, HJF00025 com a taxa de avaliação 530 por numero de serie. No fim do ano, o usuario vem a saber que tem somente 3 Numeros de Serie para este item com a Taxa de Avaliação de 620. Então para remover os Numeros de Serie antigos HJF00020, HJF00021, HJF00022, HJF00023, HJF00024, HJF00025 e adiconar os novos Numeros de Series com a nova Taxa de Avaliação, Reconciliação de Stock pode ser feito da seguinte forma:

Selecione o item ITEM-00225 na reconciliação de stock, na seleção do Item o sistema ira puxar automaticamente os numeros de serie existentes e depois defina 3 como Qtd, Taxa de Avaliação como 530 e numeros de serie como HJF00026, HJF00027, HJF00028.


<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock-recon-for-serialized.png">

Antes da reconciliação, a taxa de avaliação era 530 e a qtd disponivel era 6, então o valor total do stock erá de 3,180. Depois da reconciliação, a taxa de avaliação mudou para 620 e a qtd disponivel mudou para 3, então o novo valor do stock passa para 1,860. Para ajustar o valor do stock na contabilidade, o sistema creditou um valor extra de 3,180 - 1,860 = 1,320 na conta do Armazem e debitou na conta de ajuste de stock. Os registos do GL (Razão Geral) para as entradas acima citadas são as seguintes:

Para ver os Registo do Razão Geral, clique no botão Visão > Livro Contabilistico

<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/gl_entry_for_serialized_items.png">

O balanço do stock depois de submetida a reconciliação de stock:
<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/stock_balance_after_stock_reco_submission.png">

O razão geral para a conta do armazem Nagpur depois de submitida a reconciliação de stock:
<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/general_ledger_after_stock_reco_submission.png">

### 4.3 Para Itens com Lote

Reconciliação de Stock para itens com lote sera usado para adicionar um novo lote ou para actualizar a quantidade existente de lotes. Por exemplo, o lote JHGJH00003 tem a quantidade actual como 60 mas se o usuario quiser tornar 100 utilizando a reconciliação de stock, o usuario podera actualizar a quantidade de lotes.

<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/for_batch_item_after_stock_reco_submission.png">

Relatorio de Balanço do Lotes-Inteligentes depois da submissão da reconciliação de stock:
<img class="screenshot" alt="Stock Reconciliation" src="{{docs_base_url}}/assets/img/stock/batchwise_balance_history_after_stock_reco_submission.png">

## 5. Video

<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/nlHX0ZZ84Lw" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>

### 6. Topicos Relacionados
1. [Entrada de Stock](/docs/user/manual/pt/inventario/entrada-stock)
1. [Contabilidade do Inventario de Stock](/docs/user/manual/pt/inventario/accounting-of-inventory-stock)


{next}
