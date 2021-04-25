<!-- add-breadcrumbs -->
#Relatorio do Nivel de Stock

Relatorio do Nivel do Stock lista as quantidades de stock dos itens existentes num armazem em particular.

Existem varios relatorios disponiveis aonde pode verificar o nivel de stock dos itens.

####Relatorio de Quantidade de Stock Projectado

Voce pode acessar este relatorio `Inventario > Relatorios de Stock > Qtd Projectada de Stock`

Este relatorio lista nivel de stock de itens inteligentes - armazens de um item considerando todas as transações de stock. Com a Quantidade Actual de um Item, tambem mostra outros detalhes como:

1. Qtd Actual: Quantidade disponivel no Armazem.
2. Qtd Planeada: Qunatidade, pelo qual, Ordem de Trabalho foi criada, mas está pendente para ser fabricado.
3. Qtd Solicitada: Quantidade solicitada para comprar, mas ainda não foi criada.
4. Qtd Pedida: Quantidade pedida para comprar, mas ainda não foi recebida.
5. Qtd Reservada: Quantidade pedida para vender, mas ainda não foi entregue.
6. Qtd Projectada: Quantidade Projectada é calculada como 

<div class="well">Qtd Planeada = Qtd Actual + Qtd Planeada + Qtd Solicidada + Qtd Pedida - Qtd Reservada</div>

O inventario projectado é usado pelo sistema de planeamento para monitorizar o ponto de encomenda e determinar a quantidade de encomenda. A Quantidade projectada é usado pelo sistem de planeamento para monitorizar os niveis de segurança do stock. Estes niveis são mantidos para servir pedidos inesperados.

Tendo um control rigido do inventario projectado é crucial para determinar escassez e calcular a quantidade certa para encomenda.
