<!-- add-breadcrumbs -->
# Solicitação de Cotação

**Uma Solicitação de Cotação é um documento que uma organização envia a um ou mais fornecedores pedindo uma proforma para itens.**

![Fluxo de Compra](/docs/assets/img/buying/buying_flow_rfq.png)

Para acessar a Solicitação de Cotação, va para:
> Home > Comprar > Aquisição > Solicitação de Cotação

## 1. Pre-requisitos
Antes de criar e usar uma Solicitação de Cotação, é aconselhavel criar os seguinte:

* [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
* [Item](/docs/user/manual/pt/inventario/item)

## 2. Como criar uma Solicitação de Cotação
1. Va para a lista de Solicitação de Cotação, clique em Novo.
2. Digite a data.
3. Escolha o fornecedor a quem a Solicitação de Cotação sera enviada.
4. Na tabela seguinte, digite os itens, quatindades e o armazem alvo aonde voce irá enviar estes itens.
1. O Armazem pode deixar em branco se 'Actualizar Stock' não estiver activado para o item.
5. Salvar e Submeter.

Uma Solicitação de Cotação (SDC) pode tambem ser criado apartir de uma Solicitação de Material submetida. Uma vez uma SDC é criada, voce pode imprimir e enviar o PDF que terá todas as informações que digitou relevantes a SDC e receber a resposta por emai. Voce pode tambem receber a resposta deles pelo ERPNext (Cotação deo Fornecedor), veja a secção _4.1 Cotação de Fornecedor por Usuario_. Contudo, para um numero grande de itens, o seu fornecedor pode estar mais confortavel com uma folha de Excel etc.,

## 3. Funcionalidades

### 3.1 Obter itens apartir
Os itens na tabela de itens podem ser procurados por outros documentos. As opções são: Solicitação de Material, Oportunidade, e Possivel Fornecedor.

* **Solicitação de Material**: Itens vao ser procurados apartir de uma Solicitação de Material submetido que voce seleciona. Uma Solicitação de Material poide ser procurado com algumas palavras e um intervalo de datas tambem pode ser usado para filtrar as Solicitações de Material.

* **Oportunidade**: Itens vao ser procurados apartir de uma Oportunidade salva. O itervalo de datas podem ser selecionadas aqui tambem.

* **Possivel Fornecedor**: Selecione um possivel fornecedor. E se tiver alguma Solicitação de Material submetida contra este fornecedor, itens pode ser procurados por aqui.

### 3.2 O botão Obter Fornecedores
Em vez de digitar os fornecedores manual na tabela, voce pode tambem procurar usando esta botão. Quando voce fizer o clique no botão Obter Fornecedore, ira ver um campo 'Obter Fornecedores Por'. Existem duas opções para procurar fornecedores: por marca ou por grupos. 

* **Por marca**: Va para 'Categoria de Marca' via ferramenta de procura no topo. Voce deve criar as marcas primeiro e atribuir elas no DocType do Fornecedor no Modulo de Compras. Depois pode selecionar por Marca. Ao fazer o clique em Adicionar 'Todos Fornecedores', os fornecedores que tiverem a marca serao procurados.

* **Por Grupo**: Selecione 'Grupo de Fornecedor' e escolha o grupo do fornecedor no qual os fornecedores precisam ser adiconado. Por exemplo, se voce selecionar Hardware, todos os fornecedores de Hardware vao ser adiconado para que voce pode obter as cotações de todos eles.

Na tabela do Fornecedor, ao expandir a linha com o triangulo invertido, voce irá ver uma opção 'Descarregue PDF' que irá abrir o PDF da SDC.

### 3.3 Mensagem para o Fornecedor
Digite qualquer mensagem adicional para o Fornecedor neste campo. Os campos podem ser auto preenchido usando um 'Modelo de Email'. O campo para selecionar um Modelo de Email fica mesmo em baixo do Mensagem para Fornecedor.

### 3.4 Termos e Condições

Em transações de Vendas/Compras, podem ter alguns Termos e Condições com base no qual o Fornecedor providencia bens ou serviços ao Cliente. Voce pode aplicar os Termos e Condições as transações que vao aparecer quando imprimir o documento. Para saber sobre Termos e Condições, [clique aqui](/docs/user/manual/pt/configuração/imprimir/termos-e-condições)

### 3.5 Configuração de Impressão
#### Cabeçalho
Voce pode imprimir o seu pedido para cotação/ordem de compra no logotipo da empresa. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/cabeçalho-carta).

'Agrupar itens iguais' irá agrupar os itens iguais adicionados varias vezes na tabela de itens. Isto pode ser visto ao imprimir.

#### Imprimir Cabeçalho
Titulo dos documentos podem ser trocados. Saiba mais [aqui](/docs/user/manual/pt/configuração/imprimir/iprimir-cabeçalhos).

### 3.6 Mais

**Botão Ligar as Solicitações de Material**: Este botão liga a Solicitação de Cotação a qualquer Solicitação de Material. Os itens devem estar na mesma Solicitação de Cotação e Solicitação de Material.

![Ligar a Solicitação de Material]({{docs_base_url}}/assets/img/buying/link-to-material-request.png)

Agora, quando a Solicitação de Cotação é salva, voce pode ver no Dashboard que esta ligado a Solicitação de Material.
Se existe varias Solicitações de Material com o mesmo iten, então o link sera criado com a mais nova Solicitação de Material.

## 4. Criando uma Cotação de Fornecedor depois de um SDQ
Depois de criar uma Solicitação de Cotação, existem duas formas para gerar uma Cotação de Fornecedor apartir de uma Solicitação de Cotação.

### 4.1 Cotação de Fornecedor por Usuario

1. Abre Solicitação de Cotação e faça o clique em **Cotação de Fornecedor > Criar**.

    ![Cotação de Fornecedor apartir de SDC]({{docs_base_url}}/assets/img/buying/make-supplier-quotation-from-rfq.png)

2. Selecione o Fornecedor, clique no fornecedor novamente. Nesta pagina, clique no + proxuo do 'Cotação de Fornecedor'. Uma nova pagina Cotação de Fornecedor ira abrir, o usuario tem que digitar a quantidade, preço e submeter.

    ![Contação de Fornecedor apartir do Fornecedor]({{docs_base_url}}/assets/img/buying/supplier-quotation-from-sup.png)
    
### 4.2 Cotação de Fornecedor apartir do Fornecedor

1. Se um [Contacto](/docs/user/manual/pt/CRM/contacto) é criado para o Fornecedor e um endereço de email for associado com o Contacto, os Detalhes de contacto e o endereço de email vao ser procurados ao selecionar o Fornecedor. Cria um Contact e um endereço de email se não tiver ja criado.

2. Clique no botão 'Enviar Emails aos Fornecedores'.

    **Se a conta do Fornecedor não estiver presente**: O sistema ira criar uma Conta do Fornecedor e enviar os detalhes ao Fornecedor. O Fornecedor ira precisar fazer um clique no link presente no email (Password Update). Depois de actualizado a senha, o Fornecedor pode acessar o portal com o formulario do Solicitação de Cotação. O Fornecedor será criado como um Usuario de Pagina.

    ![Email do Fornecedor se conta não tiver conta]({{docs_base_url}}/assets/img/buying/supplier-password-update-link.png)

    
    **Se a conta do Fornecedor estiver presente**: O sistema envia o link da Solicitação de Cotação ao Fornecedor, o Fornecedor tera de fazer o login usando as suas credenciais para ver o formulario de Solicitação de Cotação no portal. 

    ![Email do Fornecedor se a tiver conta]({{docs_base_url}}/assets/img/buying/send-rfq-link.png)

3. De qualquer maneira, quando o Fornecedor entra para o sistema, os seguintes ecrãns são mostrados. Apartir daqui eles pode enviar-lhe uma Cotação:

    ![Ecrã da Solicitação de Fornecedor]({{docs_base_url}}/assets/img/buying/rfq-supplier-quotation.png)

    O fornecedor tem que digiar o valor e notas (termos de pagamento) no formulario e fazer um clique em submeter. Na secção de Cotações, cotações anteriores ficam visiveis.

4. Ao submeter, o sistema irá criar uma Cotação de Fornecedor (modo de rascunho) contra o fornecedor. O usuario tem que revisar a Cotação de Fornecedor e submeter. Quando todos os itens partir da Solicitação de Cotação forem cotadas pelo Fornecedor, o status é actualizado para 'Recebido' na tabela do Fornecedor da tabela de 'Solicitação de Cotação'.

    ![Status da SDC depois da cotação do Fornecedor]({{docs_base_url}}/assets/img/buying/rfq-supplier-quoted.png)

## 5. Sem Cotação do Fornecedor

Se o Fornecedor indicar que não ira enviar uma cotação para os itens, pode ser indicado no documento de SDC fazendo o clique na caixa 'Sem Cotaçaõ' depois da Solicitação de Cotação ter sido submetida. A caixa de Sem Cotação pode ser vista quando expandir a linha do Dados do Fornecedor fazendo um  clique no triangulo invertido.

![Sem Cotação apartir do Forneedor]({{docs_base_url}}/assets/img/buying/no-quote-supplier.png)

Para saber mais sobre criando uma Cotação de Fornecedor, [clique aqui](/docs/user/manual/pt/compras/cotação-do-fornecedor).

## 6. Video
<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/q85GFvWfZGI?rel=0" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>


### 7. Topicos Relacionados
1. [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
1. [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
1. [Cotação do Fornecedor](/docs/user/manual/pt/compras/cotação-do-fornecedor)
1. [Cotação](/docs/user/manual/pt/vendas/proforma)
1. [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material)

{next}