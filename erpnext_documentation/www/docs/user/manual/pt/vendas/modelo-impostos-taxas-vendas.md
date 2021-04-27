<!-- add-breadcrumbs -->
# Impostos de Vendas e Modelo de Encargos

**Impostos de Vendas e Taxas podem ser aplicadas a qualquer item que voce venda.**

Os modelos criados apartir deste formulario podem ser usados em Ordens de Venda e Facturas de Venda.

Para Contas de Impostos que voce quiser usar nos modelos de impostos, voce deve definir no campo Tipo de Conta como 'Imposto' para essa conta em particular. A forma como o ERPNext define os impostos é por via de modelos. Outros tipos de taxas que podem ser aplicadas as suas facturas 
(como envio, seguro, etc.) tambem podem ser configurados como impostos.

Para saber mais sobre configuração de impostos visite [esta pagina](/docs/user/manual/pt/configuração/configurar-impostos).

Para acessar Impostos de Vendas e Modelo de Encargos, va para:
> Home > Vendas > Configurações > Impostos de Vendas e Modelo de Encargos

Para saber mais sobre impostos visite [esta pagina](/docs/user/manual/pt/configuração/configurar-impostos)

## 1. Como adicionar Imposto de Vendas/Taxas via um modelo
Antes de criar um novo modelo, note que os modelos ja foram criados para outros impostos.

1. Va para a lista Impostos de Vendas e Modelo de Encargos, clique em Novo.
2. Digite o nome do titulo do Imposto.
3. No Tipo, defina que imposto irá calcular e a valor. Tem cinco opções no tipo no qual o imposto será calculado.
  1. Actual: Voce pode directamente digitar o valor das despesas.
  1. No Total Liquido: No total liquido de todos os itens.
  1. Na Linha do Valor Anterior: Este é para compor imopstos. Por exemplo, cess cobra o valor no qual o imposto ja foi aplicando na linha anterior.
  1. Na Linha do Total Anterior: O mesmo que em cima mas aplicado no total cobrado e não somente no valor de um item.
  1. Na Quantidade do Item: Imposto será calculado como Preço de Imposto * Quantidad do Item. Por exemplo, se o Preço do Imposto for 2% e o numero de Itens for 1, então o Preço do Imposto será 4, se o numero de Itens for 5, Preço do Imposto será 10, e assim por diante.
4. Selecione uma Conta que tenha pre taxas de imposto ou crie as suas.
1. Selecionando padrão irá aplicar o modelo por defeito para todas as novas transações de Vendas.
5. Salve.
  ![Impostos de Vendas](/docs/assets/img/selling/sales-taxes.png)

**Esta entre os estados**: Para India. Ao selcionar um cliente na Factura de Vendas ou Guia de Remessa, se o codigo GST do lugar de entrega e endereço de envio do cliente não forem iguais, o modelo com 'Esta entre os Estados' selecionado será definido como o modelo de impostos. Se o lugar de entrega e envio de endereço forem iguais, o modelo padão sera usado. Este é tambem aplicado a Facturas de Compra, a selecionar o Fornecedor, os modelos são definidos de acordo os endereços. Por exemplo, IGST.

## 2. Funcionalidades
### 2.1 Impostos de Vendas e Tabela de Taxas

* **Considere Imposto ou Cobre por**: Total - para o total de todos os itens. Avaliação - para cada item. Avaliação e total - aplica imposto/taxa para ambos. [verifique este artigo](/docs/user/manual/pt/contabilidade/artigos/qual-diferença-total-valuação-impostos-taxas) para saber a diferença.

* **Linha de Referencia #**: Se o imposto for com base em "Linha do Total Anterior" voce pode selcionar o numero da linha no qual sera tido como base para este calculo (padrão é a linha anterior).
    ![Tabela de Imposto de Vendas](/docs/assets/img/selling/sales-taxes-table.png)

* **Esta o Imosto incluido no Preço Base?**: Se selecionado, o valor do imposto será considerado as ja incluido na Preço de Impressão / Valor de Impressão na tabela do Item de uma transação. Este é util quando voce quer dar preços incluindo imposto aos clientes. Para levar em conta os impostos incluidos nos preços, o sistema calcula o Valor Liquido por deduzindo o valor do imposto a ser aplicado e depois calcula o imposto sobre o mesmo.
* **Cabeçalho de Conta:** A Conta do Razão no qual este imposto será alocado. Se voce selecionar VAT ou qualquer cabeçalho, o preço sera preenchido automaticamente..
* **Centro de Custo:** Se o Imposto/Taxa for receita (como envio) ou despesa vai precisar ser alocado contra um Centro de Custo.
* **Descrição:** Descrição do imposto (que sera impresso nas facturas/proformas).
* **Taxa:** O preço da Taxa, eg: 14 = 14% imposto.
* **Valor:** O valor da Taxa a ser aplicado, eg: 100.00 = ₹100 imposto.

As taxas do imposto voce define no modelo para ser a taxa padrão para todos os Itens. Se houver Itens que devem ter uma taxa diferente, voce pode passar por cima da taxa padrão do imposto definindo o Modelo de Imposto do Imte para o Item ou Grupo de Item.

### 3. Topicos Relacionados
1. [Ordens de Venda](/docs/user/manual/pt/vendas/ordem-vendas)
1. [Configurações de Venda](/docs/user/manual/pt/vendas/configurações-venda)

{next}