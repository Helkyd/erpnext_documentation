<!-- add-breadcrumbs -->
# Fornecedor

**Fornecedores são empresas ou individuos que lhe providenciam produtos ou serviços.**

Para acessar a lista de Fornecedores, va para:
> Home > Comprar > Fornecedor > Fornecedor

## 1. Como criar um Fornecedor
1. Va para a lista de Fornecedores e clique em Novo.
2. Digite o nome para o Fornecedor.
4. Selecione o grupo de fornecedor.
5. Salvar.
    <img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-master.png">

As opções para Avisar PDOs,POs, Prevenir PDOs, POs ficam disponiveis quando voce cria um [Scorecard do Fornecedor](/docs/user/manual/pt/compras/supplier-scorecard) e transações são feitas.

## 2. Funcionalidades

Campos em transações futuras são auto preenchidas se os campos 'Padrão' como Conta do Banco Padrão, Modelo de Termos de Pagamento Padrão, etc., são definidos no Fornecedor.

### 2.1 Detalhes de Imposto

* **Pais**: Se o fornecedor for de um outro País, voce pode mudar aqui.
* **NIF**: Numero de Indentificação de Imposto do fornecedor.
* **Categoria de Imposto**: Esta ligado a [Regra de Imposto](/docs/user/manual/pt/contabilidade/regra-imposto). Se uma Categoria de Imposto for definida aqui, ao selecionar o fornecedor, o Modelo de Imposto de Compra e Taxas respectiva será aplicada. Este modelo esta ligado as Regras de Imposto e as Regras de Imposto ligadas a uma Categoria de Imposto. Uma Categoria de Imposto pode ser usado para um grupo de Fornecedores no qual a mesma taxa é aplicada. Por exemplo: Governo, comercial, etc,.
* **Idioma de Impressão**: A lingua no qual o documento será impresso.
* **Categoria de Retenção Fiscal**: Para India, categoria TDS para o Fornecedor. Ao definir uma categoria aqui, sera procurado em [Factura de Compra](/docs/user/manual/pt/contabilidade/factura-compra). Para mais informações, visite a pagina [Categoria de Retenção Fiscal](/docs/user/manual/pt/contabilidade/categoria-retenção-imposto).
* **Desactivado**: Desactiva o Fornecedor e não sera mostrado na lista de Fornecedores.
* **É um Transportador**: Se o fornecedor estiver a vender os seus seviços de transporte, selecione esta caixinha.
* **Fornecedor Interno**: Se o fornecedor for de uma empresa de grupo, selecione este campo e selecione a empresa que eles representam.

For India:
* **GST Category**: Select a GST Category of the supplier.
* **PAN**: For India, PAN (Permanent Account Number) card details of the Supplier.

### 2.2 Permitir criar uma Factura de Compra sem Ordem de Compra e Recibo de Compra

Se a opção "Ordem de Compra Obrigatorio" ou "Recibo de Compra Necessario" configurados como "Sim" em [Configurações de Compra](/docs/user/manual/pt/compras/configuração-compras), pode ser passado por cima para um fornecedor em particular selecionando "Permitir criar Factura de Compra sem Ordem de Compra" ou "Permitir criar Factura de Compra sem Recibo de Compra" na ficha do Fornecedor.

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-po-pr-required.png">

### 2.3 Moeda e Lista de Preço
**Moeda de Cobrança**: A Moeda do seu fornecedor pode ser diferente que o da sua empresa. Se voce escolher USD para o fornecedor, então a moeda usada ser USD e a taxa de cambio mostrada para transações futuras.

![Moeda do Fornecedor](/docs/assets/img/buying/supplier-currency.gif)

Cada Fornecedor poide ter uma **Lista de Preço** padrão para que sempre que voce compre um novo item apartir deste fornecedor por preços diferentes, a lista de preço associada com o fornecedor possa ser actualizada tambem. Dentro da lista de preços vira o preço do item, voce pode ver os preços em Comprar > Itens e Preços > Preço de Item.

Se voce selcionar este fornecedor, então a Lista de Preço associada ira usada nas transações de Compra.

### 2.4 Limite Credito

* **Modelo de Termos de Pagamento Padrão**: Se um Modelo de Termos de Pagamento for definido aqui, sera automaticamente selecionado nas transações futuras.
* **Bloquear Fornecedor**: Voce pode bloquear facturas, pagamento ou ambos de um fornecedor até uma data especifica. Escolha 'Hold Type', se voce não selecionar um tipo de espera, o ERPNext ira definir para "Tudo". Quando o fornecedor é bloqueado, o seu status sera visto como 'Em Espera'.

    Os tipos de espera são:
    - Facturas: O ERPNext não irá permitir Facturas de Compra ou Ordens de Compra a serem criadas para o fornecedor
    - Pagamentos: o ERPNext não ira permitir Entradas de Pagamento a serem criadas para o Fornecedor
    - Tudo: O ERPNext irá aplicar para ambos os tipos de espera em cima

    Se voce não definir uma data de Liberação (release date), o ERPNext irá manter o Fornecedor em espera para **sempre**.

### 2.5 Contas de Pagamento Padrão
Adicone a conta padão no qual as facturas deste fornecedor serao pagas. Adiconne linhas adicionais para mais empresas, voce pode selecionar somente uma conta pode cada Empresa.

Voce pode **integrar** um fornecedor com uma conta. Para os Fornecedores, conta "Credor" é definido como Conta a Pagar padrão. Quando uma Factura de Compra é criada, pagamentos para este fornecedor é bloquado contra a conta Crededores".

Se voce quiser customizar a conta a pagar para o Fornecedor, voce deve primeiro criar a Conta a pagar no Plano de Contas, e depois selecionar a Conta a Pagar na ficha do Fornecedor.

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-payable-account.png">

Se voce não quiser customizar a conta a pagar, e proseguir com a conta padrão "Credor", então não precisa actualizar qualquer valor na tabela Contas a Pagar Padrão do Fornecedor.

> Dica: Conta a Pagar Padrão é definida na tabela mestre da Empresa. Se voce quiser definir outra conta como a Conta Padrão, va para a ficha da Empresa, e defina a conta em "Conta a Pagar Padrão".

Dependendo do seu [plano](https://erpnext.com/pricing), voce poide adiconar varias empresas no seu ERPNext. Um Fornecedor pode ser usado em varias empresas. Em muito dos casos, voce deve definir uma Conta a Pagar por Empresa para o Fornecedor na tabela "Contas a Pagar Padrão", i.e, adicione varias linhas.

### 2.6 Mais Informações
Voce pode adiconar a pagina do Fornecedor e qualquer detalhe adicional sobre o seu fornecedor nesta secção. Se voce congelar um fornecedor com a opção 'Esta Congelado', os registos de contabilidade para este fornecedor ficam congelados. Neste caso somente os registos dos usuarios que tenham a regra atribuida em 'Função Permitida para Definir Contas Congeladas e Editar Registo Congelados' em Contabilidade > Mestres Contabeis > Definições de Contas poderam criar. Isto é util quando o nome do fornecedor ou os detalhes do banco estao a ser corrigidos.

### 2.7 Endereços e Contactos
Contactos e Endereços no ERPNext são guardados separados para que voce possa criar varios Contactos e Endereços para um Fornecedor. Uma vez o Fornecedor salvo, voce ira encontrar as opções para criar Contactos e Endereços para o Fornecedor.

<img class="screenshot" alt="Supplier Master" src="{{docs_base_url}}/assets/img/buying/supplier-new-address-contact.png">

> Dica: Quando voce criar uma Fornecedor em qualquer transação, Contacto para o qual o campo "É Primario" esta activo, sera auto procurado nos detalhes do Fornecedor.

### 2.8 Depois de Salvar
Uma vez todos os detalhes preenchidos, salva o documento. Ao salvar, opções para criar os seguintes ficam visiveis no Dashboard:

* **Solicitação de Cotação**: Um SDQ para este fornecedor.
* **Cotação de Fornecedor**: Qualquer cotação que o fornecedor enviou para sim e voce submeteu no sistema.
* **Ordem de Compra**: Ordens de Compra que voce criou contra este fornecedor.
* **Recibo de Compra**: Recibos de Compra dados pelo seu fornecedor que voce salvou no sistema.
* **Facturas de Compra**: Facturas de Compra que voce criar contra este fornecedor.
* **Registo de Pagamento**: Registo de Pagamentos para as Facturas de Compra contra este Fornecedor.
* **Regras de Preço**: Qualquer Regra de Preço ligada a este fornecedor. Veja a secção  _2.3 Moeda e Lista de Preço_ para saber como funciona.

![Salvar Fornecedor](/docs/assets/img/buying/supplier-save.png)

Ao fazer o clique no botão Visão, voce pode ver o Livro Contabilistico ou Contas a Pagar directamente para este fornecedor.


## 3. Video
<div>
    <div class='embed-container'>
        <iframe src='https://www.youtube.com/embed//zsrrVDk6VBs?start=213' frameborder='0' allowfullscreen>
        </iframe>
    </div>
</div>

### 4. Topicos Relacionados
1. [Solicitação de Fornecedor](/docs/user/manual/pt/compras/solicitação-cotação)
1. [Scorecard do Fornecedor](/docs/user/manual/pt/compras/supplier-scorecard)
1. [Mantendo o Codigo do Item do Fornecedor na Tabela do Item](/docs/user/manual/pt/compras/artigos/mantendo-codigo-item-fornecedor-na-tabela-item)
{next}