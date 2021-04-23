<!-- add-breadcrumbs -->
# Lote

**A funcionalidade do Lote no ERPNext permite agrupar varias unidade de um Item e atribuir ele um valor/numero/marca unico chamado Numero do Lote.**

Isto é feito com base no Item. Se o Item tiver lotes, então o Numero do Lote deve ser mencionado em cada transação de Stock. Numeros de Lote podem ser geridos manualmente ou automaticamente. Esta funcionalidade é util para definir a data de expiração de varios Itens ou move todos de uma so vez para armazens diferentes.

Para acessar a lista de Numeros de Lotes, va para:
> Home > Inventario > Numero de Serie e Lotes > Lotes


## 1. Pre-requisitos
Antes de criar e usar os Lotes, é aconselhavel primeiro criar os seguintes:

* [Item](/docs/user/manual/pt/inventario/item)
* Active 'Tem Nr. de Lote' na ficha do Item
    ![Lote não Activo](/docs/assets/img/stock/batch-no-enabled.png)


## 2. Como criar um novo Lote

Para definir o item como um item com lote, o campo "Tem Nr. Lote" deve estar activo na ficha do Item. Se voce não selecionou "Criar novo lote automaticamente" ao criar um Item, voce terá que criar os Lotes Manualmente. 

Para criar um novo Nr. de Lote para um item, va para:

1. Va para a lista de Lotes, clique em Novo.
1. Defina o ID do Lote.
1. Selecione o Item.
1. Se alguma transação for feito com um item, o lote não pode ser definido ou retirado.
1. Salve.

Quando os Lotes estão activos para um Item, a opção [reter amostra de stock](/docs/user/manual/pt/inventario/reter-amostra-stocks) tambem fica activa. 

### 2.1 Lote e Auto Criação
Se voce quiser a criação de lotes automaticos na altura da criação do Recibo de Compras, voce deve selecionar 'Criar novo lote automaticamente' na ficha do Item:

<img class="screenshot" alt="Item Setup for Batches" src="{{docs_base_url}}/assets/img/stock/item_setup_for_batch.png">

## 3. Funcionalidades
### 3.1 Dividindo e Movendo Lotes

Quando voce abre um lote, voce irá ver todas as quantidades do mesmo lote.

<img class="screenshot" alt="Batch View" src="{{docs_base_url}}/assets/img/stock/batch_view.png">

* Para mover o lote de um Armazem para outro, voce pode fazer o clique no botão **Mover**.

* Voce pode tambem dividir o lote em quantidades pequenas fazer o clique no botão **Dividir** button. This will create a new Batch based on this Batch and the quantities will be split between the batches.

    ![Split Batch](/docs/assets/img/stock/batch_split.png)

* Se voce definir data de expiração, o Lote ira mostrar 'Não Expirado' até a data de expiração, depois mostrará 'Expirado'. Se a data não for definida, o Lote irá mostrar 'Não Definido'.

### 3.2 Transação de Itens com Lotes

Um Lote mestre deve ser criado antes de criar o Recibo de Compra.
Daí, sempre que criar um Recibo de Compra ou Ordem de Trabalho for feita com um item de lote,
voce primeiro irá criar o Numero do Lote, e depois selecionar o mesmo na Ordem de Compra ou Registo de Stock.

Em cada transação de stock (Recibo de Compra, Guia de Remessa, Factura) com um item de lote,
deve providenciar o Numero do Lote do Item.

> Nota: Em transações de stock, IDs do Lote serao filtrados com base no Codigo do Item, Armazem,
Data de Expiração do Lote (comparado com a Data de Postagem de uma transação) e a Qtd Actual no Armazem.
Enquanto procura pelo ID do Lote sem valor no campo do Armazem, o filtro Qtd Actual não será aplicada.

### 4. Topicos Relacionados
1. [Numero de Serie](/docs/user/manual/pt/inventario/numero-serie)
1. [Registo de Abertura de Stock para Itens com Numero de Serie e Lote](/docs/user/manual/pt/inventario/artigos/abertura-balanco-stock-para-itens-serializados-e-lotes)
1. [Gerindo Inventario de Lotes de forma Inteligente](/docs/user/manual/pt/inventario/artigos/gerindo-inventario-de-lotes-inteligente)
