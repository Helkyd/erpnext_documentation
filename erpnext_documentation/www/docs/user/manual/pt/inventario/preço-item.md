<!-- add-breadcrumbs -->
# Preço do Item

**Preço do Item é um registo no qual voce pode gravar os preços de venda e compra de um item.**

## 1. Como criar um Preço de Item
1. Existem tudas formas de alcançar o formulario de um novo Preço de Item:

    **Vendas/Comprar/Inventario > Itens e Preços > Preço do Item > Novo**.
 
    Ou

    **Inventario > Item > Clique em "+" proximo do Preço do Item**.
1. Selecione o Item. O nome, UdME e descrição serao procurados.
1. Selecione a Lista de Preço quer Vendas/Compras ou qualquer lista de preço que ja tenha criado.
1. Digite o preço actual no campo Valor.
1. Salvar.
    <img class="screenshot" alt="Item Price list" src="{{docs_base_url}}/assets/img/stock/item-price-1.png">


### 1.1 Selecionando a Lista de Preço

Voce pode criar varias Listas de Preço para um Item no ERPNext para rastrear Preço das Vendas e Compras de um Item. Tambem se os preços de venda de um Item muda com base no Territorio ou devido a outros criterios, voce pode criar varias listas de Preço de Venda para tal.

Ao selecionar a Lista de Preço, a moeda e aplicabilidade para venda/compra or ambos sera procurado tambem. Para procurar o Preço do Item nas transações de vendas ou compras, voce deve selecionar 'Lista de Preço' na transação em Moedas e Lista de Preço.

Para selecionar todos os Preços do Item, va para:

**Inventario > Relatorios de Stock > Preço do Item Preço**

Visite a pagina [Lista de Preços](/docs/user/manual/pt/inventario/lista-preços) para saber mais.

## 2. Funcionalidades

###2.1 Unidade de Pacote
Este é a quantidade que deve ser comprado ou vendido por unidade de medida. Por exemplo, se a Unidade do Pacote for dois, e UDM é um, dois itens na quantidade serao transacionados. O padrão é 0, voce pode usar UdM não-inteiro como 1.5Kg Oats para 1 Unidade de Pacote. Se voce deixar como 0, não irá afectar qualquer transação.

###2.2 Quantidade Minima
Este é a quantidade minima de itens a ser transacionado para este preço ser aplicado e actualizado na lista do Preço do Item. 

### 2.3 Aplicadndo Lista de Preço a um Cliente/Fornecedor especifico
Se voce selecionar a lista de Preços de Venda, um campo de cliente irá aparecer aonde poderá atribuir este Preço de Item a um cliente especifico. Da mesma forma, se voce selecionar uma lista de Preços de Compra, um campo de Fornecedor ira aparece aonde podera o Fornecedor

###2.4 Validade 
Tem dois campos aqui —'Valido Apartir' e 'Valido Até'. Valido apartir é definido a data que criou o Preço do Item, voce pode definir a data de Valida Até no qual o Preço do Item expira.

###2.5 Tempo de Entrega em dias
O numero aproximado de dias que leva o produto até o armazem. Voce pode definir Preços de Item com base na quantidade de tempo o mesmo produto irá levar até si apartir de diferentes vendedores.

###2.6 Nota
Voce pode adiconar qualquer nota sobre o Preço do Item neste campo.

## 3. Video 

<div>
    <style>.embed-container { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; } .embed-container iframe, .embed-container object, .embed-container embed { position: absolute; top: 0; left: 0; width: 100%; height: 100%; }</style>
    <div class='embed-container'>
        <iframe src='https://www.youtube.com/embed/FcOsV-e8ymE?start=193' frameborder='0' allowfullscreen>
        </iframe>
    </div>
</div>

### 4. Topicos Relacionados
1. [Item](/docs/user/manual/pt/inventario/item)
1. [Aplicando Desconto](/docs/user/manual/pt/vendas/artigos/aplicando-desconto)