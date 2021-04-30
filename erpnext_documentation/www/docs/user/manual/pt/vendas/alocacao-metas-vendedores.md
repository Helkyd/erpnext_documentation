<!-- add-breadcrumbs -->
# Alocação de Metas para Vendedores

**É a tarefa de um Vendedor para com um item ou territorio.**

Em conjunto da gestão de Vendedores, o ERPNext tambem permite que voce atribua metas aos Vendedores com base no Grupo de Item e Territorio. Com base na meta alocada e as vendas actuais alocadas pelos Vendedore, voce pode obter um Relatorio das Variações das Metas dos Vendedores.

##1. Vendedor - Alocação de Metas por Item

###1.1 Abrir o Mestre de Vendedores

Para alocar a meta, voce precisa abrir o mestre de Vendedores.

**Vendas > Vendas > Vendedor > Editar**

###1.2 Alocar metas por Grupo de Item

Na tabel de Vendedores, voce irá encontrar uma tabela Meta de Vendedores.

<img class="screenshot" alt="Sales person target" src="{{docs_base_url}}/assets/img/selling/sales-person-target-item-group.png">

Nesta tabela, voce deve selecionar o Grupo de Item, Anos Fiscal, Qtd Alvo, Valor Alvo, e Objectivo de Distribuição. 

Voce pode atribuir metas em valor e quantidades, ou ambos. Grupo de Item poide ser deixado em branco. Neste caso, o sistema irá calcular com base nos Todos os Grupos dos Itens.

**Objectivo de Distribuição**

Voce pode separar as metas pelos meses. Para isto crie uma nova Distribuição mensal, voce pode ver a opção quando fizer o clique no campo Objectivo de Distribuição na tabel. Por exemplo, uma meta de vendas de 1,000 unidade para o primeiro quarto do Anos Fiscal 2019-2020 como mostra a imagem em baixo.

<img class="screenshot" alt="Target Distribution" src="{{docs_base_url}}/assets/img/selling/sales-person-target-distribution.png">

###1.3 Relatioro - Variação das Metas do Vendedor por Grupo de Item

Para ver este relatorio, va para:

**Selling > Other Reports > Sales Person Target Variance Item Group-wise**

Este relatorio irá mostrar a variação entre a meta e o desempenho actual dos Vendedores. Este relatorio é com base no Relatorio das Ordens de Venda.

Aqui, pelo relatorio, metas alocadas aos Vendedores foi de 83 em quantidades para um mês, mas ele atingiu a meta de 80 ao ver o relatorio, assim sendo o relatorio de variação está correcto.

<img class="screenshot" alt="Target Item Group" src="{{docs_base_url}}/assets/img/selling/sales-person-item-group-report.png">

**Nota:** Para o relatorio reflectir os detalhes correctos, voce precisa ligar os Vendedores a uma Ordem de Vendas, esta presente na secção Equipa de Vendas da Ordem de Vendas. A Ordem de vendas tambem deve estar na fase de Submissão.

---

##2. Vendedor - Alocação da Meta pode Territorio

Para alocar metas por Territorio ao Vendedor, selecione o Vendedor na lista de Territorios. Este Vendedor é adicionado somente como referencia. Detalhes do Vendedor não são actualizados no relatorio de variação para Alocação de Metas do Territorio.

###2.1 Va para o Territorio

**Vendas > Configurações > Territorio > (Edite o Territorio)**

No Territorio selecionado, voce ira encontra um campo para selcionar o Gestor do Territorio. Este campo esta ligado ao Vendedor.

<img class="screenshot" alt="Sales Person Territory Manager" src="{{docs_base_url}}/assets/img/selling/sales-person-territory-manager.png">

###2.2 Alocando Metas

Alocação de Metas na tabela Territorio é igual ao Vendedor. Voce pode seguir os seguintes passos dados na secção _1.2 Alocar metas por Grupo de Item_ para espeficar a meta na tabela Territorio tambem.

###2.3 Relatorio - Variação de Meta do Territorio por Grupo de Item

Este relatorio irá mostra a variação entre a meta o desempenho actual das Vendas num territorio em particular. Este relatorio é com base no relatorio de Ordens de Venda. Apesar do Vendedor estar definido na tabela Territorios, os seu detalhes não são mostrados no relatorio.

**Nota** que o Terrotiro de um Cliente/Clientes devem ser definidos para que este relatorio funcione. Por exemplo, na imagem em baixo, a meta foi de aproximadamente oito unidade e cinco foram atingidas, dai a variação ser três.

<img class="screenshot" alt="Sales Person Territory Report" src="{{docs_base_url}}/assets/img/selling/sales-person-territory-report.png">

---

##3. Objectivo de Distribuição

Para criar um novo Objectivo de Distribuição, va para:
**Contabilidade > Distribuição Mensal**

O documento de Objectivo de Distribuição permite que divida as metas alocadas em varios meses. Se os seus produtos forem sazonais, voce pode distribuir as metas das vendas de acordo. Por exemplo, se voce estiver no negocio de Sombrinhas, então a meta alocada no tempo de chuva será maior que nos outros meses.

<img class="screenshot" alt="Target Distribution" src="{{docs_base_url}}/assets/img/selling/target-distribution.png">

Voce pode ligar a Distribuição Mensal ao mesmo passo que estiver a alocar as metas nos Vendedores e na tabela de Territorios.

### 4. Topicos Relacionados
1. [Vendedores em Transações de Vendas](/docs/user/manual/pt/vendas/artigos/vendedores-nas-transacoes-de-vendas)
1. [Usando Vendedores em Transações](/docs/user/manual/pt/vendas/artigos/vendedores-nas-transacoes-de-vendas)

{next}
