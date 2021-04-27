# Definições de Vendas

Definições de Vendas é aonde voce pode definir propriedades e validações que vao ser aplicadas nas tabelas e transações envolvidas no ciclo de vendas.

Vamos ver cada opção disponivel em Definições de Vendass no ERPNext.

<img class="screenshot" alt="Selling Settings" src="{{docs_base_url}}/assets/img/selling/selling-settings.png">

Para acessar as Definições de Vendass, va para:
> Home > Vendas > Configurações > Definições de Vendas

## 1. Serie dos Nomes
###1.1 Nome do Cliente por

Quando um cliente é salvo, um ID unico é gerado para este Cliente.

Por defeito, o ID do Cliente é gerado com base no Nome do Cliente. Se voce quiser salvar o Cliente usando um Nome de Serie, no campo Nome de Series do Cliente, defina o valor "Nome de Series". Exemplo de um ID de Cliente salvo no Nome de Series - "CUST00001, CUST00002, CUST00003..." e assim por diante.

Voce pode definr o Nome de Series para Clientes apartir:

**Configurações > Dados > Serie de Atrib. de Nomes**

### 1.2 Campanha de Nome por

Tal como o Cliente, voce pode tambem configura o metodo do nome para a Campanha. Por defeito, uma campanha será salva com o Nome da Campanha.

## 2. Padrões
### 2.1 Grupo de Cliente e Territorios Padrão

Selecione o GRupo de Cliente Padrão no qual sera auto-actualizado quando criar um novo Cliente.

Cotações podem ser criadas para os Clientes como para as Leads. Ao converter uma Cotação em Ordem de Vendas, que foi criado para uma Lead, o sistema tenta converter essa Lead em Cliente. Ao criar um Cliente, valores para o Grupo de Cliente e Territorio são procurados nas Configurações de Vendas. Se não tiver valores padrões para o Grupo de Cliente e Territorio, então irá receber uma mensagem de validação pedindo o Grupo do Cliente e Territorio. Voce pode tambem converter manualmente uma Lead para Cliente.

### 2.2 Lista de Preços Padrão

Lista de Preços definidos neste campo será auto-actualizado no campos de Lista de Preços das transações de vendas como Cotações, Ordem de Vendas, Guia de Remessa e Factura de Vendas.

### 2.3 Fechar Oportunidade Depois de Dias

Se existem Oportunidade com o status diferente de Aberto, então eles vao ser auto-fechados depois do Numero de Dias mencionado neste campo.

### 2.4 Dias de Validação Padrão da Proforma

Cotações para o cliente são validas somente por alguns dias. Na Cotação, voce pode actualizar a Data Valida Até manualmente. Por defeito, a Data de Validade até é auto posta por 30 dias apartir da Data de Postagem da Cotação. Voce pode mudar o numero de dias deste campo de acordo o seu tipo de negocio.

## 3. Verificação de Requisitos
### 3.1 Ordem de Vendas Obrigatorio

Se voce quiser tornar uma Orde de Venda obrigatoria antes de criar uma Factura de Venda, então deve definir o campo 'Ordem de Vendas Obrigatorio' como  'Sim'. Por defeito, estará como 'Não'.

Esta configuração pode ser ultrapassada para um cliente em particular activando a caixinha "Permitir Criar Factura de Vendas sem uma Ordem de Venda" na tabela do cliente

<img alt="Sales Order Required" class="screenshot" src="{{docs_base_url}}/assets/img/selling/so-required.png">

### 3.2 Guia de Remessa Necessaria

Para tornar uma Guia de Remessa obrigatoria antes da criação de uma Factura de Vendas, voce deve definir este campo como 'Sim'. Por defeito, estará como 'Não'.

Esta configuração pode ser ultrapassada para um cliente em particular activando a caixinha "Permitir Criar Factura de Vendas sem uma Guia de Remessa" na tabela do cliente

<img alt="Delivery Note Required" class="screenshot" src="{{docs_base_url}}/assets/img/selling/dn-required.png">

### 3.3 Actualização Frequente das Vendas
A frequencia no qual um projecto e os detalhes de transação de uma empresa são actualizados. Por defeito é para cada Transação, voce pode tambem definir para ser Diario ou Mensal se voce tiver muitas transações todos os dias.

## 4. Outras Verificações
### 4.1 Manter a mesma Taxa dentro do Ciclo de Vendas

O sistema por defeito valida o preço do item e que será o mesmo durante o ciclo de vendas (Ordem de Venda -> Guia de Remessa -> Facturas de Venda). Se o preço do item será mudado dentro do ciclo e voce precisa passar a validação com o mesmo preço posto no ciclo, deixe esta caixinha não activada.

### 4.2 Permitir Usuario Editar Taxa de Lista de Preço em Transação

A tabela do item nas transações de venda tem u mcampo chamado Taxa de Lista de Preço. Este campo não é editado por defeito em todas as transações de vendas. Isto é para ter a certeza que o preço de um item é procurado apartir do registo Preço do Item e o usuario não tenha a possibilidade de editar.

Se voce precisa procurar o Preço do Item apartir da Lista de Preço de um item para ser editado, voce deve não selecionar esta campo.

### 4.3 Permitir adiconar o Item varias vezes numa transação
Este é um ponto de validação que previne um item em ser adiconado varias vezes na mesma transação quando não selecionado. Em alguns caso, poderá haver a necessidade de selecionar esta caixa.

### 4.4 Permitir Ordens de Venda Multiplas contra Ordem de Compra de Clientes
Ao criar Ordens de Venda, voce pode actualizar o ID da Ordem de Venda e a Data de recepção pelo Cliente. Voce pode criar somente Ordens de Venda contra um Numero de PO e Data de um Cliente. Contudo, se voce quiser permiir a criação de uma Ordem de Venda contra um Numero de PO do Cliente, selecione esta caixinha "Permitir Ordens de Venda Multiplas contra Ordem de Compra de Clientes".

### 4.5 Validar o Preço de Venda para um Item contra um Preço de Compra ou Taxa de Avaliação
Ao fazer vendas, é importante saber que voce não está perdido. Activando esta validação ira permitir o Preço de Venda do item com o seu preço de Avaliação/compra. Se o preço de venda do item encontrado for menor que o preço de compra, então irá receber uma janela se esta caixinha estiver activa.

### 4.6 Esconder o NIF do Cliente nas Transações de Vendas
Como obrigação, muitos do Clientes lhes é atribuido um unico ID NIF. Eles tambem precisam ter este NIF nas transações de vendas. Contudo, se não quiser usar esta funcionalidade, voce pode desactivar esta propriedade.

{next}
