<!-- add-breadcrumbs -->
# Contabilidade do Inventario de Stock

O valor do inventario disponivel é tratado como um Activo Corrente no [Plano de Contas](/docs/user/manual/pt/contabilidade/plano-de-contas). Para prepara uma Folha de Balanço, você deve criar os registos contabilisticos destes activos. Existem dois metodos diferentes para contabilidade do inventario.

## 1. Auto/Perpetual Inventory

Neste processo, para cada transação de stock, o sistema posta os registos relavantes para sincronizar o balanço do stock e balanço de contabilidade. Este é a configuração padrão no ERPNext para novas contas. Por defeito, Perpetual Inventory é activo em [Empresa](/docs/user/manual/pt/configuração/configuração-empresa#23-configurações-de-stock).

Quando você compra e recebe os itens, estes itens são alocados como activos da empresa
(stock-em-mão). Quando você vende e entrega estes itens, uma despesa
(Custo dos Bens Vendidos) equal to the landed cost of the items is booked.
Entradas do Razão Geral são criadas apos cada transação de stock. Como resultado, o valor por cada Razão do Stock sempre será igual as contas do balanço. Isto melhora a precisão da Folha de Balanço e os Calculos de Lucros e Perdas.

Para verificar os registos de contabilidade para uma transação de stock em particular,
[clique aqui](/docs/user/manual/pt/inventario/perpetual-inventory)

### 1.2 Vantagens do Perpetual Inventory

O sistema Perpetual Inventory irá tornar facil para manter a precisão dos activos da empresa e os custos de despesas. Balanço de Stock será sempre sincronizado com as contas de balanço, então não será necessário mais entradas manuais mensais para balanciar.

No caso de uma nova transação de stock com data-antiga or cancelamento/correção de um uma transação existente, todos os registo do Razão de stock e Registos do GL serão recalculadas em todos os itens dessa transação. O mesmo é aplicavel se qualquer custo for adicionado aos Recibos de Compra submetidos depois pelo Voucher de Custo de Entrega.

> Nota: Perpetual Inventory depende completamente da taxa de avaliação.
Daí, você precisar ter muito cuidade ao digiar a taxa de avaliação quando estiver a criar qualquer Entrada de stock como Recibo de Compra, Recepção de Material, ou Fabrico/Reembalar.

* * *

## 2. Inventario Periodico

Neste metodo, registos contabilisticos precisam ser criados manualmente de forma a sincronizar o balanço do stock e as contas relevantes do balanço. O sistema não cria registos automaticos para activos na hora da compra de matarial ou venda.

Num periodo de contabilidade, quando compra e recebe materiais, uma despesa é alocada no seu sistema de contabilidade. Você vende e entrega alguns destes materiais.

No fim do periodo de contabilidade, o total valor dos itens a serem vendidos, precisam ser alocados como activos da empresa, tambem conhecidos como 
stock-em-mão.

A diferença entre o valor dos itens por vender e dos valores dos periodos anteriores do 
stock-em-mão podem ser positivos ou negativos. Se positivo,
este valor é removido das despesas (Custo dos Bens Vendidos) e é
adicionado aos activos (stock-em-mão). Se negativo, um entrada contraria é feita.

Este processo completo é chamado de **Inventario Periodico**.

Se você for um usuario existente a usar o Inventario Periodico e quiser usar o Perpetual
Inventory, você precisa seguir [alguns passos](/docs/user/manual/pt/inventario/artigos/migrate-to-perpetual-inventory) para migrar. 

### 3. Topicos Relacionados
1. [Perpetual Inventory](/docs/user/manual/pt/inventario/perpetual-inventory)
1. [Migrar para Perpetual Inventory](/docs/user/manual/pt/inventario/artigos/migrate-to-perpetual-inventory)