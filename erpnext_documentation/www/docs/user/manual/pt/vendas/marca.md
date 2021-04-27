<!-- add-breadcrumbs -->
# Marca

**Um Marca identifica itens com um um nome especifico.**

Normalmente, uma Marca é do fabricante ou empacotador de um produto especifico. Por exemplo, a Apple é um marca de fabricantes de laptops. Uma Marca não é necessariamente o [Fabricante](/docs/user/manual/pt/inventario/fabricante) de um Item, é somente o nome no qual o produto é vendido. Por exemplo, se voce fabrica copos de plastico, voce pode licenciar para uma marca grande para que eles vendam em nome da Marca deles.

No ERPNext, Marcas podem ser atribuidas a Itens para identificar e atribuir certos padrões.

Para acessar alista de Marcas, va para:

> Home > Inventario > Configurações > Marca

## 1. Como Criar uma Marca
1. Va para a lista de Marca e clique em Novo.
1. Digite o Nome da Marca e digite a descrição se necessario.
1. Salve.

    ![Marca](/docs/assets/img/selling/brand.png)

Agora esta Marca pode ser associada por defirentes Itens.

![Marca no Item](/docs/assets/img/selling/brand-in-item.png)

## 2. Funcionalidades
### 2.1 Configurando Padrões para Itens desta Marca

![Padrão da Marca](/docs/assets/img/selling/brand-defaults.png)

Os seguintes padrões podem ser definidos para uma Marca. Ao atribuir esta marca a um Item, as definições padrão vao ser procuradas quando ao criar transações de Vendas/Compras com o Item desta Marca.

* **Armazem Padrão**: O Armazem no qual o Item será procurado/guardado dependendo da transação.
* **Lista de Preço Padrão**: A Lista de Preço definida aqui sera procurada nas transações de Compras/Vendas.

#### Padrões de Compra
Ao fazer transações de Compras como Ordens de Compra, Recibo de Compra, ou Factura de Compra, os padrões definidos aqui vão ser procurados ao selecionar o Item desta Marca.

* Centro de Custo para Compra Padrão
* Fornecedor Padrão
* Conta de Despesa Padrão

#### Padrão de Vendas
Ao criar transações de Vendas como Ordens de Venda, Guias de Remessa, ou Facturas de Venda, os padrões definidos aqui vao ser procurados ao selecionar o Item desta Marca.

* Centro de Custo para Venda Padrão
* Conta de Receitas Padrão

## 3. Topicos Relacionados
1. [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
1. [Ordens de Venda](/docs/user/manual/pt/vendas/ordem-vendas)
1. [Recibo de Compra](/docs/user/manual/pt/inventario/recibo-compra)
1. [Guia de Remessa](/docs/user/manual/pt/inventario/guia-de-remessa)
1. [Facturas de Venda](/docs/user/manual/pt/contabilidade/factura-vendas)
1. [Facturas de Compra](/docs/user/manual/pt/contabilidade/factura-compra)
