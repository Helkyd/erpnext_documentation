<!-- add-breadcrumbs -->
# Variantes de Item

**Uma Variante de Item é uma versão de um Item com diferentes atributos como tamanhos e cores.**

Eg: Vamos supor uma Casmia é um Item e vem em tamanhos diferentes e cores como pequeno, medio, grande, vermelho, azul, verde. No ERPNext a camisa será considerada como um Modelo de Item e cada uma das variações será uma Variante do Item. 

Uma camisa _azul_ em tamanho _pequeno_ em vez de somente um camisa. As Variantes dos Itens permitem tratar as versões _pequeno_, _medioa_, e _grande_ de uma camisa como variações de um Item 't-shirt'.

Sem as Variantes do Item, voce teria que tratar as versões _pequeno_, _medio_ and _grande_ de uma camisa como três Itens separados.

## 1. Usando Variantes de Item

Variantes podem ser com em duas coisas:

1. Atributo dos Itens
1. Fabricantes

> Dica: Uma vez um modelo d item for criado, quando actualizar este modelo, todas as variantes tambem são actualizadas.

### 1.1 Criando um Modelo de Variante de Item

1. Para usar Variantes de Item no ERPNext, crie um Item e selecione 'Tem Variantes' em baixo de Variantes. 

1. O Item depois sera referenciado com o 'Modelo'. Tal Modelo não é identico ao 'Item' normal. Por exemplo, o (Modelo) não pode ser usado directamente em qualquer transação (Ordem de Vendas, Guia de Remessa, Factura de Compra).
 
1. Somente as Variantes de Item (camisa _azul_ em tamanho _pequeno)_ podem ser usados. Assim sendo seria bom decidir se vai usar um item 'Tem Variantes' ou não ao cirar.
    <img class="screenshot" alt="Has Variants" src="{{docs_base_url}}/assets/img/stock/item-has-variants.png">

1. Ao selecionar a tabela 'Tem Variantes' irá aparecer. Especifique os atributos da variante para o Item na tabela. Em caso o atributo ter Valores Numericos, especifique o intervalo e crie intervalos com base nos valores incrementados.
    <img class="screenshot" alt="Valid Attributes" src="{{docs_base_url}}/assets/img/stock/item-attributes.png">
> Nota: Voce não pode fazer Transações contra um 'Modelo'.

### 1.2 Criando Variantes de Item com base em Atributos de Item
Para criar 'Variantes de Item' contra um 'Modelo' clique me 'Criar'. Apartir daí, escolha criar uma unica variante ou varias. Singular é aonde voce cria somente um ou mais atributos para um unico Item. Ao escolher varioas variantes, selecione os atributos e varios itens seram criados. Por exemplo, se escolher a Cor: Vermelha, Verda e Tamanho: Pequeno, Medio, Grande, 6 variantes serao criadas.

Criando varias variantes no ERPNext:

<img class="screenshot" alt="Make Variants" src="{{docs_base_url}}/assets/img/stock/make-multiple-variants.png">

Para aprender mais sobre configurando atributos verifique [Atributos do Item](/docs/user/manual/pt/inventario/atributo-item)

### 1.3 Variantes de Item com Base em Fabricante

Para configurar variantes com base nos Fabricantes, no seu modelo de Item, defina "Variantes com Base em" como "Fabricantes"
Neste caso, para criar variantes, cliquem em Criar > Criar Variante. O sistem irá perguntar para selecionar o Fabricante. Voce pode opcionalmente por um Numero de Peça do Fabricante.

<img class='screenshot' alt='Setup Item Variant by Manufacturer' src='{{docs_base_url}}/assets/img/stock/select-mfg-for-variant.png'>

O nome de uma variante sera com base no nome (ID) do modelo de Item com um sufixo de numero. e.g. "Chave de Fenda" terá uma variante "Chave de Fenda-1".

## 2. Actualizar Variantes de Item com Base no Modelo
Va para: **Home > Inventario > Itens e Preços > Configurações de Variante de Item**. Os campos mostrados aqui vão ser copiados para as variantes tambem. Por defeito, todos os campos são mostrados, apague qualquer linha que não queira actualizar apartir do modelo do item para as variantes.

## 3. Video

### 3.1 Criando Variantes de Item um por um
<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/kogIricF40I?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>

### 3.2 Criando Variantes de Item em Volumes
<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/SngZtDIMdiQ" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>

### 4. Topicos Relacionados
1. [Grupo de Item](/docs/user/manual/pt/inventario/grupo-item)
1. [Atributo de Item](/docs/user/manual/pt/inventario/atributo-item)
1. [Preço de Item](/docs/user/manual/pt/inventario/preço-item)
1. [Codificação de Item](/docs/user/manual/pt/inventario/artigos/codificacao-item)
