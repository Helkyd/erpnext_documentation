<!-- add-breadcrumbs -->
# Configuração de Compras

Configuração de Compras é aonde voce pode definir propriedades no qual serao aplicadas nas transações do Modulo de Compras.
Voce pode encontrar as Configurações de Compra em:
> Home > Comprar > Configurações > Definições de Compra

![Definições de Compra]({{docs_base_url}}/assets/img/buying/buying-settings.png)

Vamos olhar as varias opções que podem ser configuradas:

## 1. Fornecedor
### 1.1 Nome do Fornecedor por

Quando um Fornecedor é salvo, o sistema gera uma identidade unica ou nome para esse Fornecedor que pode ser usado como referencia do Fornecedor em varias transações de Compra.

Se não for configurado, o ERPNext usa o Nome do Fornecedor como um nome unico. Se voce quiser identificar Fornecedores usando nomes como SUPP-00001, SUPP-00002, ou talvez outro tipo de series, selecione o valor do Nome do Fornecedor por como "Series de Nome".

Voce pode definir ou selecionar as Series de Nome apartir: **Configurações > Dados > Serie de Atrib. de Nomes**

[clique aqui](/docs/user/manual/pt/configuração/configurações/nome-das-series) para saber mais sobre definindo Series de Nome.

### 1.2 Grupo de Fornecedor Padrão

Defina qual o Grupo de Fornecedor Padrão ao criar um novo Fornecedor. Por exemplo, se muito dos fornecedores somente vende hardware, voce pode definir o padrão como 'Hardware'.

## 2. Compras
### 2.1 Lista de Preço de Compras Padrão

Definia o qual deva ser a Lista de Preço Padrão quando criar uma nova transação de Compra, o padrão é definido como 'Standard Buying'. Preço de Itens sera procurado apartir desta Lista de Preço. Voce pode modificar a 'Lista de Preço' usando a seta no lado direito do campo para modificar a moeda e País.

### 2.2 Ordem de Compra Obrigatorio

Se esta opção for configurado para "Sim", o ERPNext não irá permitir criar uma Factura de Compra ou um Recibo de Compra directamente sem criar uma Ordem de Compra primeiro. Se as transações de compra forem feitas offline, então as Ordens de Compra podem ser puladas. Se voce aceita amostra de Itens, voce pode criar directamente um Recibo de Compra para recebre os Itens no seu Armazem.

Esta configuração pode ser passada por cima para um fornecedor em particular activando a caixinha "Permitir Criar Factura de Compra Sem Ordem de Compra" na ficha de fornecedor

<img alt="Purchase Order Required" class="screenshot" src="{{docs_base_url}}/assets/img/buying/po-required.png">

### 2.3 Recibo de Compras Obrigatorio

Se esta opção for configurada como "Sim", o ERPNext não ira permitir criar uma Factura de Compra sem criar primeiro um Recibo de Compra. No caso do Item a ser usado na transação for um serviço, não será necessario um recibo, voce pode criar a Factura directamente.

Esta configuração pode ser passada por cima para um fornecedor em particular bastando activar a caixinha "Permitir Criar Factura de Compra Sem Recibo de Compra" na ficha do fornecedor

<img alt="Purchase Receipt Required" class="screenshot" src="{{docs_base_url}}/assets/img/buying/pr-required.png">

### 2.4 Manter Mesmo Preço no Ciclo de Compras

Se estiver activo, o ERPNext não irá permitir que voce mude o preço do Item numa Factura de Compra ou Recibo de Comra criado pela Ordem de Copmra, i.e. irá manter o mesmo preço durante o ciclo de compras. Se tiver uma necessidade aonde o preço do Item poderá mudar, voce deve desactivar esta opção.

## 3. Permitir o Item ser adiconado varias vezes numa transação

Quanto não estiver activa esta opção, um item não poderá ser adicionado varias vezes numa Ordem de Compra. Contudo, voce pode mudar a quantidade. Isto é uma caixinha de validação para previnir comopras acidentais de um item. Este pode ser selecionado para casos especificos aonde existem varias fontes para o mesmo material, por exemplo facbrico.

### 4. Topicos Relacionados
1. [Grupo de Fornecedor](/docs/user/manual/pt/compras/grupo-fornecedor)

{next}