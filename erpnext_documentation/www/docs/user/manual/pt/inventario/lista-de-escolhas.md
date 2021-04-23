---
titulo: Lista de Escolha
add_breadcrumbs: 1
show_sidebar: 0

metatags:
 descrição: Uma lista de Escolha é um documento que indica quais os itens que devem sair do seu inventario para comprir as solicitações. Este é util para os expeditores com um volume grande de inventario, volume de solicitações, ou clientes solicitando muitas Unidade de Armazenamento (SKU).
 keywords: Lista de Escolha, Escolhendo Lista, frappe, Bilhete de Escolha, novas funcionalidade do erpnext, erp, open source erp, free erp, stock
---

# Lista de Escolha

**Uma Lista de Escolha é um documento que indica quais os itens que deve ser retirados do seu inventario para comprir com as solicitações.**

Este é particularmente util para expeditores com grandes volumes de inventario, volume de solicitações, our clientes solicitando muitas Unidades de Armazenamento (SKU).
A Lista de Escolha seleciona o Armazem aonde o Item está disponivel com base no FIFO (Primeir-in-Primerio-sair).
Seleção do Armazem para itens do Lote é diferente. Em casos de itens de lote, Armazem aonde o lote está proximo a sua data de expiração que será selecionado.

Para acessar a Lista de Escolha, va para:

> Home > Inventario > Transações de Stock > Lista de Escolha

## 1. Pre-requesitos

Antes de criar e usar a Lista de Escolha, é aconselhavel que crie os seguintes:

- [Item de Stock](/docs/user/manual/pt/inventario/item)
- [Armazem](/docs/user/manual/pt/inventario/armazem)

## 2. Como criar a Lista de Escolha

1. Va para a lista de Lista de Escolha, clique em Novo.
 <img class='screenshot' alt='Unsaved Pick List' src='{{docs_base_url}}/assets/img/stock/pick-list-unsaved-doc.png'>

1. Defina a Empresa.
1. Selecione o Motivo da Lista de Escolha. Estas são as opções no Motivo:

   - **Entrega:** Esta opção irá permitir que você adicione Itens apartir da Ordem de Venda, para a entrega. Depois de submeter a Lista de Entrega uma nova Guia de Remessa pode ser criado com base no Armazem no qual os itens foram levantados.

   - **Transferencia de Material para Fabrico:** Este irá permitir selecionar a Ordem de Trabalho no qual as materias primas vao ser usados pela lista de escolha. Ira ser apresentado uma opção para selecionar o numero de bens produzidos no qual voce quer escolher materias primas. Depois de selecionar o stock voce pode criar o Registo de Stock para os itens selecionados i.e., materias primas.

   - **Transferencia de Material:** Este permite selcionar a Solicitação de Material no qual voce que escolher os itens. Depois de escolher o stock voce pode criar um Registo de Stock para os itens ecolhidos.

1. Adicione o Item e a quantidade que voce quer escolher na tabela de Localizações do Item. Clique em **Obter Localização de Item** para obter o Armazem e outros detalhes para cada Item.

1. **Parente do Armazem:** Se um parente de Armazem é selecionado, somente os Armazens somente dentro do Parente do Armazem será sugerido.
1. **Obter Localização do Item:** Uma vez os itens a serem escolhidos foram produzidos voce pode fazer o clique no botão **Obter Localização o Item** para ter o Armazem selcionado para cada item. Vendo que o Armazem irá automaticamente procurado se obter o Item de qualquer documento referente, este botão pode ser util para manualmente adicionar Itens ou mudar a quantidade de Itens existentes na tabela de Localização de Itens.

1. **Localização de Item:** Este irá ter a informação da localização do item (Armazem), Numero de Serie para itens serializados e para numeros de lote para itens com lote.
 <img class='screenshot' alt='Item Locations' src='{{docs_base_url}}/assets/img/stock/pick-list-item-locations.png'>

 Se os numeros de serie estiverem, a linha do Item será visto assim:
 <img class='screenshot' alt='Item Location Detail' src='{{docs_base_url}}/assets/img/stock/pick-list-item-location-detail.png'>

1. Salvar e Submeter.
 <img class='screenshot' alt='Submitted Pick List' src='{{docs_base_url}}/assets/img/stock/pick-list-submitted-doc.png'>

### 2.1 Criar a Lista de Escolha pela Ordem de Vendas

1. Va para a [Ordem de Vendas](/docs/user/manual/pt/vendas/ordem-vendas).
1. Clique no botão **Criar** no lado direito em cima do formulario e depois fazer um clique na opção **Lista de Escolha**.
1. Quando fizer o clique na Lista de Escolhas, todos os dados necessarios para a Lista de Entrega serao procurados apartir da Ordem de Vendas.
1. Voce podreá ver a Tabela de Localizações de Item com os Armazens selcionados para cada um dos itens.
1. Salve esta documento e poderá ser usado para recolher o stock pela pessoa permitida nesta actividade.
1. Submeter o documento uma vez a lista de stock feita e as quantidades do item actualizados no documento.

**Dica:** Voce pode criar uma Lista de Escolha para varias Ordens de Venda apartir do Cliente. Clique em Obter Itens e selecione as Ordens de Venda.

> **Nota:**
>
> - Lista de Escolha somente pode ser criada para as Ordens de Venda no qual tem Itens pendentes para ser entregues.
> - Uma **Guia de Remessa** pode ser criada somente se a Lista de Escolha for submetida.

### 2.2 Crie um Lista de Escolha apartir da Ordem de Trabalho

1. Va para a [Ordem de Trabalho](/docs/user/manual/pt/fabrico/ordem-trabalho).
1. Clique no botão **Crie a Lista de Escolha** .
1. Voce irá ver uma caixa de dialogo pedindo a quantidade dos Bens Produzidos. Este é necessario para calcular o numero de materia prima os itens precisam para fabricar a quantidade digitada dos Bens Produzidos.
<img class='screenshot' alt='Dialog For qty' src='{{docs_base_url}}/assets/img/stock/pick-list-dialog-for-qty.png'>

1. Voce deve poder ver a tabela de Localização do Item com o Armazem selecionado para cada linha de material.
1. Salve o documento e depois esta documento poderá ser enviado para a pessoa que irá pegar o stock.
1. Submeta o documento uma vez que a recolha do stock for feita e os itens recolhidos forem atualizados no documento.

> **Nota:**
>
> - Lista de Escolha somente pode ser criado para Ordens de trabalho que ainda estão no estado de 'Não Inciado' ou 'Em Progresso'.
> - Um **Registo de Stock** pode ser criado somente depois da Lista de Escolha ter sido submetida.

### 2.3 Crie a Lista de Escolha apartir da Solicitação de Material

1. Va para a [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material).
1. Clique no botão **Criar** e depois clique na opção **Lista de Escolha**.
1. Voce podera ver a tabela de Localização do Item com o Armazem selecionado para cada item na Solicitação de Material.
1. Salve este documento e depois poderá transferir para a pessoa que irá levantar o material.
1. Submeta o documento uma vez a recolha de stock for feita e os itens recolhidos actualizados no documento.

> **Nota:**
>
> - Somente Solicitação de Material com o tipo 'Transferencia de Material' pode ser usado para criar uma Lista de Escolha.
> - Um **Registo de Stock** do tipo 'Transferencia de Material' pode ser criado depois da Lista de Escolha ter sido submetida.

## 3. Funcionalidades

### 3.1. Actualizar o Stock Corrente

Se a Lista de Escolha estiver desactualizada, poderá have uma troca na disponibilidade do stock na altura da criação da Guia de Remessa ou Registo de stock. Fazendo o clique em **Actualizar Stock Corrente** irá actualizar as quantidades e os armazens na tabela de localização do Item.

> **Nota:** Este botão é visivel desde que não tenha Guias de Remessa ou Registos de Stock contra a Lista de Escolha.

## 4. Topicos Relacionados

1. [Ordem de Vendas](/docs/user/manual/pt/vendas/ordem-vendas)
1. [Ordem Trabalho](/docs/user/manual/pt/fabrico/ordem-trabalho)
1. [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material)
