<!-- add-breadcrumbs -->
# Armazem

**Um armazem é um edificio comercial para guardar bens. Armazens são usados
por fabricantes, importadores, exportadores, vendedores, transportadoras,
customs, etc.**

Eles são normalmente edificios largos numa area industrial de 
cidades, vilas. Por norma tem loading docks para carregar e descarregar
bens dos camiões.

A terminologia de 'Aramzem' no ERPNExt é um pouco ampla e pode vista como "locais de armazenamento". Você pode criar um sub-Armazem que poderá ser um armario na sua localização actual. 

Este pode vir a ser um Arvore detalhada como a seguinte:

*Aramzem > Quarto > Fila > Armario > Cesto*

Para aceder a lista de Armazem, va para:
> Home > Inventario > Configurações > Armazem

## 1. Como criar um Armazem
1. Va para a lista de Armazem, cliquem em Novo.
1. Digite um nome para o Armazem.
1. Mencione o Armazem Pai. Se você acionar em 'É Grupo', voce pode criar sub-Armazens dentro deste grupo de Armazem.
1. Salvar. 

Armzanes são salvos com a respectiva abreviação da Empresa. Isto facilita identificar que armazem pertence a que empresa de primeira.

### 1.1 Opcções Adicionais ao criar um Armazem
**Conta**: Defina uma conta padrão aqui para todas as transações com este Armazem. Definindo esta conta irá mostrar transações apartir deste Armazem no Razão de Contabilidade.
**Tipo de Armazem**: Vocẽ pode criar um Tipo de Armazem para classificar Armazens. Por exemplo, Armazens de Fornecedores, Armazens de Stock, Armazens WIP, Salas, etc. podem ser marcados. Esta classificação é util quando gerar relatorios ou em algumas transações de Stock.

#### Endereço e contacto
Você pode adicionar Cobranças, Shipping, e outros tipos de endereços para o Armazem. Você pode tambem adicionar um contacto, este pode ser o Gestor de Armazem por exemplo.

![Armazem](/docs/assets/img/stock/warehouse.png)

### 1.2 Depois de Salvar
Depois de salvar um Armaze, você irá ver as seguintes opções:

* **Balanço de Stock**: Este irá abrir o relatorio de Balanço de Stock para mostrar a quantidade, avaliação, balanço, etc.
* **Razão Geral**: Este irá abrir o Razão Geral para mostrar as transações de contabilidade.
* **Não-Grupo para Grupo**: Se o Armazem é um Armazem Não-Grupo, i.e. não pode conter outros Armazens dentro dele, este botão irá mudar para um Armazem de Grupo.

## 2. Funcionalidades

### 2.1 Visão em Arvore
Você pode tambem mudar para Visão 'Arvore' que irá mostrar todo os grupos e Armazens.

<img class="screenshot" alt="Warehouse" src="{{docs_base_url}}/assets/img/stock/warehouse-tree.png">

### 2.2 Conta de Armazem
No ERPNext, se voce activar [Inventario Perpetual](/docs/user/manual/pt/inventario/inventario-perpetual), todos Armazens dvem pertencer a uma empresa especifica para manter o balanço de stock.
Para fazer isso, cada Armazem deve estar ligado por uma 
Conta no Plano de Contas (o mesmo nome que o Armazem). Esta conta captura o equivalente monetario dos bens ou materiais guardados naquele armazem especifico.

Se voce tiver uma Arvore de Aramzens mais detalhada, será uma boa idea provavelmente ligar a sub-localizações (quarto, fila, armario, etc.) a conta do Armazem actual (O Armazem principal desta Arvore) como muitos cenarios não requerem ter um valor de contabilidade por Armario ou Cesto.
Por exemplo, se voce tem um Armazem A, e o quarto, filas B, C, etc., então liga B e C a conta do A.

> Dica: O ERPNext mantem o balanço de stock para qualquer combinação destinta de Item e Armazem. 
Então poderá obter o balanço de stock para qualquer Item num Armazem em particular em qualquer data.

### 3. Topicos Relacionado
1. [Motivo de Registo de Stock](/docs/user/manual/pt/inventario/artigos/motivo-registo-stock)
1. [Relatorio de Nivel de Stock](/docs/user/manual/pt/inventario/relatorio-nivel-stock)
