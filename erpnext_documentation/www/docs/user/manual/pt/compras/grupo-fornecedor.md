<!-- add-breadcrumbs -->
# Grupo de Fornecedor
**Grupo de Fornecedor é uma agregação de fornecedores que são similares de alguma forma.**

Um fornecedor pode ser destinguido pelo seu contratante ou subcontratado, que normalmente adiciona inputs para entregas especializados. Um fornecedor é tambem conhecido como um vendedor. Existem tipos de fornecedores com base em bens e produtos que eles providenciam.

O ERPNext permite que voce crie a sua propria categoria de fornecedores. Estas categorias são tambem conhecidas como Grupo de Fornecedores. Por exemplo, se o seu fornecedor for uma empresa farmaceutica e distribuidores FMCG, voce pode criar um novo Grupo de categorias.

Para acessar o Grupo de Fornecedores, va para:
> Home Comprar > Fornecedor > Grupo de Fornecedores

## 1. Pre-requisitos
Antes de criar e usar o grupo de Fornecedores, é aconselhavel criar o seguinte:

* [Fornecedor](/docs/user/manual/pt/compras/fornecedor)

## 2. Como criar um Grupo de Fornecedores
1. Va para a lista de Grupo de Fornecedores, clique em Novo.
1. Digite o nome para a sua nova Categoria de Fornecedor.
1. Voce pode definr o Grupo de Fornecedor Principal para este Grupo de Fornecedores.
1. Selecionando a caixinha de É Grupo irá fazer um Grupo de Fornecedores Principal.
1. Voce pode tambem atribuir um Modelo de Termos de Pagamentos padrão para o grupo de Fornecedores. Util em casos aonde o seu fornecedor de hardware faz metade do pagamento na Ordem de Vendas e metade deois do Envio.
1. Salvar.

<img class="screenshot" alt="Supplier Group" src="{{docs_base_url}}/assets/img/buying/supplier-group.png">

Voce pode classificar os seu Fornecedores apartir de uma variedade de escolhas disponiveis no ERPNext.
Escolha apartir de um conjunto de opções dadas como Fornecedor, Eletrico, Hardware, Local, Famaceutico, Materia Prima, Serviços etc. Classifique o seu Fornecedor em varios tipos de contas de facilidades e pagamentos.

## 3. Arvore de Grupo de Fornecedor

Voce pode tambem construir o Grupo de Fornecedores em forma de Arvore Hierarquica, similar ao Plano de Contas.

Para ver a estrutuda da Arvoce, clique em  **Arvore** no lado. Para voltar para a lista, simplesmente 
selecione: **Menu > Ver Lista**.

<img class="screenshot" alt="Supplier Group" src="{{docs_base_url}}/assets/img/buying/supplier-group-tree.png">

Com a nova [Permissão de Usuario](/docs/user/manual/pt/configuração/usuarios-e-permissões)
a funcionar, voce pode aplicar permissões com base em Hierarquia.
Isto é, se o Usuario for permitido ver o No principal de um Grupo de Fornecedores,
ele/ela automaticamente está qualificada para ver os nos dos filhos de um No Principal.

Por exemplo, se a imagem em cima, digamos que a permissão é aplicada ao usuario for para um Usuario no documento 
'Distribuidor'. Então o usuario pode tambem ter permissão para visualizar os 
nos dos filhos 'Distribuidor de Livros', 'Distribuidor de Electronicos', etc.

### 4. Topicos Relacionados
1. [Fornecedor](/docs/user/manual/pt/compras/fornecedor)

{next}
