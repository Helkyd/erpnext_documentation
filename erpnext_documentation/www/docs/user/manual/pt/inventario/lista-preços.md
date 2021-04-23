<!-- add-breadcrumbs -->
# Listas de Preço

**Uma Lista de Preço é um coleção de Preços de Item para Venda, Compra ou ambos.**

O ERPNext permite que mantenha varios preços de Venda ou Compra [Preços de Item](/docs/user/manual/pt/inventario/preço-item) usando a Lista de Preços.

Lista de Preços podem ser usado num cenario aonde voce tem preços diferente para zonas diferentes (com base nos custos de envio), para moedas diferentes, etc. Um Item pode ter varios preços com base no cliente, moeda, região, custos de envio, etc, que pode ser guardado os varios preços.

No ERPNext, todos os Preços dos Itens são guardados separados. Preço de Compra para um item é diferente do Preço de Venda e para tal são guardados em separado.

Para acessar a Lista de Preços va para:

> Home > Vendas/Comprar/Inventario > Itens e Preços > Lista de Preços

<img class="screenshot" alt="Price List" src="{{docs_base_url}}/assets/img/stock/price-list.png">

## 1. Como usar a Lista de Preços

* Lista de Preços será usado ao criar [Preços de Item](/docs/user/manual/pt/inventario/preços-item) para gerir os preços das vendas ou compras de um item.

* Paises especificos podem ser atribuidos na Lista de Preços.

* Para desactivar a Lista de Preços, desactive a caixa 'Activado'. Lista de Preços desactivas não vão estar disponiveis para a selecção de transações de Facturas e Compras.

* **Preço não Dependente do UDM**: Considere um item, Tomate no qual voce compra em Caixas e vende a Kilo. 1 Caixa = 10 Kilos e 1 Kilo compra por 10rs. Se esta Caixa não estiver selecionada e voce selecionar 1 Caixa na sua transação, o preço irá mostrar somente para o Kilo venod que é o unico Preço do Item salva.

    Agora, se voce selecionar esta caixa e fizer uma transação com a Caixa de Tomate, então o preço irá automaticamente ser 100 vendo que o prelo de 1 Caixa (10 Kilo) é 100.

* Listas de Preço Compra e Venda Padrão são criados por defeito.

**Nota**: Se voce tiver varias Listas de Preço, voce pode selecionar a Lista de Preço ou marcar a um Cliente (que foi auto-selecionado). Os seus Preços de Item vão ser automaticamente actualizados apartir da Lista de Preços. 

### Topicos Relacionados
1. [Preço de Item](/docs/user/manual/pt/inventario/preço-item)
