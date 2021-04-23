<!-- add-breadcrumbs -->
# Voucher de Custo de Entrega

**Voucher de Custo de Entrega é o custo total associado com o produto até chegar a porta do comprador.**

Voucher de Custo de Entrega inclui o custo original do item, custo completo do envio, alfandegas, impostos, segurança, taxas de cambio de moedas, etc. Todos os componentes podem não ser aplicados em todos os envios, mas os componentes relevantes podem ser considerados como parte do Custo Final.

> **O que é Voucher de Custo de Entrega?**

> Para entender melhor o Custo Final, vamos tomar como exemplo baseado no nosso dia a dia. Voce precisa comprar um nova maquina de lavar para casa. Ante de fazer uma compra, voce provavelmente faz uma procura para saber o melhor preço. Neste processo, voce pode encontrar o preço ideal de um loja que fica distante da sua casa. Mas voce deve considerar o preço de envio ao comprar dessa loja. O Custo total incluindo o envio pode ser maior que o preço numa loja proximo da sua casa. Neste casao, voce irá escolher comprar numa loja proxima de casa, vendo que o Custo Final do Item é maior na loja proxima de casa.

De igual modo no seu negocio, indentificando o custo final para um Item/Produto é crucial, como ajuda a decidir o preço de venda deste item e tem um impacto de lucro para Empresa. Assim sendo todos as taxas de Custo Final aplicadas deve ser incluidos no preço de avaliação do Item.

DE acord o [Estudo de Logistica de Terceiros](http://www.3plstudy.com/), somente 45% dos representantes disseram que usam o Custo Final extensivo. A principal razão de não usar os Custos Finais devido a falta de dados (49%), falta de ferramentas (48%), tempo insuficiente (31%), e não tem a certeza de como aplicar o Custo Final (27%).

Para acessar a lista do Voucher de Custo de Entrega, va para:
> Home > Inventario > Ferramentas > Voucher de Custo de Entrega

## 1. Pre-requisitos
Antes de cirar um Voucher de Custo de Entrega, é aconselhavel criar os seguintes primeiro:

* [Recibo de Compra](/docs/user/manual/pt/inventario/recibo-compra)

    Ou

* [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra)


## 2. Como criar um Voucher de Custo de Entrega

1. Va para a lista Voucher de Custo de Entrega, clique em Novo.
1. Selecione o Tipo de Documento do Recibo se é Factura de Compra ou Recibo. Voce pode selecionar varios documentos.
1. Selecione a respectiva Factura ou Recibo. O nome do fornecedor e o Total Geral será procurado automaticamente.
1. Clique em Obter Itens apartir do Botão Recibo de Compras para obter os detalhes do item apartir do Recibo de Compras ou Factura.
1. Selecione Distribuir Taxas com Base em se é quantidade ou valor.
1. Digite a Conta de Despesas e o Valor para Custos Adicionais na tabela de Impostos e Taxas. O valor será distribuido em igual com base na quantidade ou valor de acordo a sua selecção.
1. Salvar e Submeter.

    <img class="screenshot" alt="Landed Cost Voucher" src="{{docs_base_url}}/assets/img/stock/landed-cost-voucher.png">


Neste documento, voce pode selecionar varios Recibos de Compra ou Facturas e ir buscar todos os itens para estes Recibos de Compra. Então voce deve adicionar as "Taxas e Impostos" aplicaveis. Voce pode facilmente apagar um item se as taxas aplicadas não se aplicam para este item.

As taxas adicionadas são proporcionamente distribuidos entre todos os itens com base no valor e quantidade. Se o você selecioniou com base no valor, o Item com o maior valor será alocado para a maior proporção das taxas. No caso da quantidade, o Item com a maior quantidade será alocado a maior parte das taxas e outros Itens serao alocados com menor valores. Isto é mostrado no seguinte:

<img class="screenshot" alt="Landed Cost Voucher" src="{{docs_base_url}}/assets/img/stock/landed-cost-distribution.png">

## 3. Acções Relacionadas
### 3.1 Adicionando Voucher de Custo de Entrega no Recibo de Compra

No ERPNext, voce pode adiconar o custo de entregra relacionado com as taxas na tabela “Impostos e Taxas” ao criar o Recibo de Compra (RC). Voce pode adicionar estas taxas para "Total e Avaliação" ou "Avaliação" no campo 'Considerar Imposto ou Taxa para'. Impostos são pagos ao mesmo Fornecedor no qual voce está a comprar itens deve ser marcado com "Total e Avaliação". Caso contrario, se taxas são pagas a um terceiro, deve estar marcado como "Avaliação". Ao submeter o Recibo de Compra, o sistema irá calcular o custo de entrega de todos os itens, considerando estes impostos. Este custo de entrega irá ser considerado para calcular a Taxa de Avaliação do item (com base no metodo FIFO / Media Movel).

Mas na realidade, ao fazer o Recibo de Compra nós podemos não saber de todas as Taxas que são aplicadas para o custo de entrega. O seu transportador pode enviar a factura depois de 1 mês, mas não tem sentido em esperar para alocar o Recibo de Compra até lá. Empresas que importam os seu produtos/peças, pagam um valor enorme em Alfandegas. E geralmente, eles recebem facturas do Departamento das Alfandegas depois. Em muitos casos, "Voucher de Custo de Entrega" é util, pois permite adicionar taxas adicionais mais tarde, e actualizar o custo de entrega dos itens comprados.

### 3.2 O que acontece ao submeter?

1. Taxa de Avaliação de itens é recalculado com base nos custos de entrega novos.

3. Se você estiver a usar "Inventario Perpetuo", o sistema irá postar um registo do razão geral para corrigir o balanço do Stock-Em-Mão. Irá debitar (aumentar) na "conta de armazem" correspondente e creditar (diminuir) **Conta de Despesa** mencionado na tabela Impostos e Taxas. Se os itens já forma entregues, o valor do Custo-dos-Bens-Vendidos (CoGS) foi alocado de acordo a taxa de avaliação. Assim sendo, os registos do razão geral são respostos a todas as entradas futuras dos itens associados, para corrigir os valores do CoGS.

### 4. Topicos Relacionados
1. [Viagem de Entrega](/docs/user/manual/pt/inventario/viagem-de-entrega)
1. [Recibo de Compra](/docs/user/manual/pt/inventario/recibo-compra)
