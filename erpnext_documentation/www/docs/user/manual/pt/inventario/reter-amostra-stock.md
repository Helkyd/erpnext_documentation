<!-- add-breadcrumbs -->
# Reter Amostra de Stock

**Amostra de stock é um lote de mujitos Itens guardados para analizar caso necessario mais tarde.**

O Item pelo o qual a amostra é guardada pode ser materia prima, material para empacotar, ou produto fabricado.

## 1. Pre-requisitos
Antes de usar a retenção de amostra, é aconselhavel criar os seguintes:

* [Item](/docs/user/manual/pt/inventario/item)
* [Lotes](/docs/user/manual/pt/inventario/lote)
* [Armazem](/docs/user/manual/pt/inventario/armazem)

## 1. Como Definir o Armazem de Retenção da Amostra em Configurações de Stock

É aconselhavel criar um novo Armazem separado para manter as amostras e não usar em produção.

<img class="screenshot" alt="Sample Retention Warehouse" src="{{docs_base_url}}/assets/img/stock/sample-warehouse.png">

### 1.2 Activar Retenção de Amostra na tabela Item
Reter Amostra é com base no Lote daí o Numero de Lote ser activado primeiro. Verifique Reter Amostra e defina o Maximo de Amostras permitidas para o Lote. 

<img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/retain-sample.png">

### 1.3 Fazer Entrada de Stock

* Sempre que uma [Entrada de Stock](/docs/user/manual/pt/inventario/entrada-stock) é criada com o motivo de Recepção de Material, para itens que tenham Reter Amostra activa, a Quantidade da Amostra pode ser definida durante o Registo de Entrada do Stock. Voce precisa selecionar o Numero do Lote para o Item/Itens. Quantidade de Amostra não pode ser mais que o Maximo de Amostra definido na tabela de Item.

    <img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/material-receipt-sample.png">

* Ao submeter este Registo de Stock, o botão 'Fazer Registo de Retenção de Stock' ficará visivel para fazer outra Entrada de Stock para fazer a transferencia das amostras dos itens do lote mencionado para o armazem de retenção definido nas Configurações de Stock.

    ![Botão de Retenção de Amostra](/docs/assets/img/stock/sample-retention-button.png)

* Fazendo o clique neste botão irá direcionar-lhe para uma nova Entrada de Stock do tipo 'Transferencia de Material'. Esta entrada irá transferir as amostras de retenção so seu Armazem Alvo (Stores) para o Armazem de Retenção de Amostras. Irá conter todas as informações, verifique e faça o clique em Submeter.

    <img class="screenshot" alt="Retain Sample" src="{{docs_base_url}}/assets/img/stock/material-transfer-sample.png">

### 2. Topicos Relacionados
1. [Armazem](/docs/user/manual/pt/inventario/armazem)
