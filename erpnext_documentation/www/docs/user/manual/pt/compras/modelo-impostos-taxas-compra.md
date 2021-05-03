<!-- add-breadcrumbs -->
# Modelo de Impostos de Compra e Taxas

**Modelo de Impostos de Compra e Taxas poidem ser aplicadas a qualquer item que voce compra.**

O Modelo de Impostos de Compra e Taxas é igual ao Modelo de Impostos de Vendas e Taxas. Os modelos criados neste formulario pode ser usados em Ordens de Compra e Facturas de Compra para registos internos.

Para Contas de Imposto que voce quiser usar nos modelos de impostos, voce deve primeiro definir o campo Tipo de Conta como 'Imposto' para esta conta em particular.

Para acessar o Modelo de Imposto de Compras e Taxas, va para:
> Home > Comprar > Configurações > Modelo de Impostos e Taxas de Compra

## 1. Como adicionar Impostos/Taxas de Compra via um Modelo
Antes de criar um novo modelo, note que os modelos existentes podem ser usados para varios impostos.

1. Clique em Novo.
2. Digite um nome para o tituel do Imposto.
3. Em baixo do tipo, defina como o imposto será calculado e o valor do imposto. Existem cinco opções em baixo to tipo no o imposto será calculado.
  1. Actual: No valor actual de cada item.
  1. No Total Liquido: No total geral de todos os itens.
  1. Na Linha Anterior do Valor: Isto é para aumentar as taxas. Por exemplo, cess cobra sobre o valor no qual imposto já foi aplicado na linha anterior.
  1. Na Linha Anterior do Total: O mesmo que acima mas aplicado no total cobrado e não somente o total do item.
4. Selecione a conta no qual tem uma pre taxa ou crie uma.
1. Selecionando padrão irá aplicar este modelo pode defito a todas novas transações de Compra.
5. Salve.
<img class="screenshot" alt="Purchase taxes" src="{{docs_base_url}}/assets/img/buying/purchase-taxes.png">

É Inter Estado: Para India. On selection of a customer in Sales Invoice or Delivery Note, if the GST codes of place of supply and customer shipping address don't match, the template with 'Is Inter State' ticked will be set as the taxes template. If the place of supply and shipping address are the same, the default taxes template will be applied. This also applies to Purchase Invoice, on selection of Supplier, the templates are set depending on the addresses. For example, IGST.

## 2. Funcionalidades
### 2.1 Tabela de Impostos de Compra e Taxas

* **Considere Imposto ou Taxa para**: Total - para o total de todos os itens. Avaliação - para cada item. Avaliação e total - aplicar imposto/taxa em ambos. [Verifique este artigo](/docs/user/manual/pt/contabilidade/artigos/qual-diferença-total-valuação-impostos-taxas) para saber a diferença.
* **Adicone ou Deduzir:** Caso queira adiconar ou deduzir o imposto do item.

* **Linha de Referencia #**: Se o imposto é com base em "Total da Linha Anterior" voce pode selecionar o numero da linha no qual sera usado como base para este calculo (padrão é a linha anterior).
   <img class="screenshot" alt="Purchase taxes table" src="{{docs_base_url}}/assets/img/buying/purchase-taxes-table.png">

* **Esta este Imposto incluido no Preço Base?**: Se selecionado, o valor do imposto sera considerado como ja incluido no Preço ao Imprimir / Valor Impresso.
* **Conta:** A conta do razão no qual o imposto será alocado. Se voce selcionar VAT ou qualquer outro, o valor sera automaticamente preenchido.
* **Centro de Custo:** se o imposto/taxa for lucro (como envio) ou despesa sera necessario alocar contra um Centro de Custo.
* **Descrição:** Descrição do Imposto (que irá ser impresso nas facturas/proformas).
* **Taxa:** o valor da Taxa, eg: 14 = 14% imposto.
* **Valor:** o Valor do Imposto a ser aplicado, eg: 100.00 = ₹100 imposto.


### 3. Topicos Relacionados
1. [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
1. [Configurações de Compra](/docs/user/manual/pt/compras/configuração-compras)

{next}