<!-- add-breadcrumbs -->
# Quantidade Projectada

**Quantidade Projectada é o nivel de stock que é previsto para um Item em particular com base no nivel do stock corrente e outros requisitos.**

É a quantidade dos inventario completo que inclui entrega e demanda no passado que faz parte
do processo de planeamento.

O inventario projectado é usado pelo planeamente do sistema para minitorizar a ponto de encomenda 
e determinar a quantidade de reencomenda. A Quantidade projectada é usada pela maquina
de planeamento para monitorizar os niveis de segurança do stock. Este niveis são
mantidos para servir as demandas não esperadas.

Tendo um control rigido do inventario projectado é crucial para determinar
escasez e para calcular a quantidade de solicitação correcta.

<img class="screenshot" alt="Projected Quantity" src="{{docs_base_url}}/assets/img/stock/projected_quantity.png">

A formula para calcular a quantidade projectada é a seguinte:

*Qtd Projectada = Qtd Actual + Qtd Planeada + Qtd Solicitada + Qtd Requisitada - Qtd Reservada - Qtd Reservada para Produção - Qtd Reservada para Subcontração*

* **Qtd Actual**: Quantidade disponivel no Armazem. Este é o stock fisico actual que tem.
* **Qtd Planeado**: Quantidade, pelo o qual, Ordem de Trabalho foi criada, mas está pendente para ser fabricado.
* **Qtd Solicitada**: Quantidade solicitada via [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material). É adicionado ao submeter a Solicitação de Material e reduzida quando a Ordem de Compra/Ordem de Trabalho/Registo de Stock é criada com base no tipo de Solicitação de Material.
* **Qtd Pedida**: Quantidade pedida para compra ([Ordem de Compra](/docs/user/manual/pt/compras/ordem-compra)), mas não recebido (via um [Recibo de Compra](/docs/user/manual/pt/inventario/recibo-compra) ou uma [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra). 
* **Qtd Reservada**: Quantidade solicitada para venda pelo seu Cliente ([Ordem de Vendas](/docs/user/manual/pt/vendas/ordem-vendas)), mas não entregues (via uma [Guia de Remessa](/docs/user/manual/pt/inventario/guia-de-remessa)). Esta quantidade aumenta quando uma Ordem de Venda é submetida e diminui quando uma Guia de Remessa ou Factura de Vendas é criada contra essa Ordem de venda quando submetida.
* **Qtd Reservada para Fabrico**: Materia primas são reservadas ao submissão de [Ordem de Trabalho](/docs/user/manual/pt/fabrico/ordem-trabalho) e é reduzido quando materia prima é transferida para o Armazem Trabalhos em Progresso via Registo de Stock.
* **Qtd Reservada para Subcontratação**: Materias primas reservadas quando uma subcontratação de Ordem de Compra é submetida. Quando materia prima é transferida para um Armazem do Fornecedor via Registo de Stock, esta quantidade é reduzida. Para saber sobre subcontratação [clique aqui](/docs/user/manual/pt/fabrico/subcontratação).

#### Topicos Relacionados
1. [Armazem](/docs/user/manual/pt/inventario/armazem)
1. [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material)