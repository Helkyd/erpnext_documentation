<!-- add-breadcrumbs -->
# Proforma do Fornecedor

**Uma Proforma do Fornecedor é o documento de um potencial fornecedor especificando os bens ou serviços que eles tem dentro de um periodo de tempo.**

Uma Proforma de Fornecedor poide tambem ter termos de venda, termos de pagamento e garantias. Aceitação da proforma pelo comprador pode ser considerado como um acordo por ambas as partes.

![Fluxo de Compras](/docs/assets/img/buying/buying_flow_sq.png)

Para acessar a Proforma do Fornecedor, va para:
> Home > Comprar > Aquisição > Cotação do Fornecedor

## 1. Pre-requisitos
Antes de criar e usar a Cotação de Fornecedor, é aconselhavel criar os seguintes:

* [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
* [Item](/docs/user/manual/pt/inventario/item)

## 2. Como criar uma Cotação de Fornecedor

### 2.1 Cotação de Fornecedor apartir de uma Solicitação de Material

Voce pode criar uma cotação de fornecedor apartir de uma Solicitação de Material:
![Cotação de Fornecedor apartir de um Recibo de Material]({{docs_base_url}}/assets/img/buying/supplier-quotation-from-mr.png)

Ou:

Uma Cotação de Fornecedor pode ser criado apartir do [Ficha do Fornecedor](/docs/user/manual/pt/compras/fornecedor).

Ou:

O fornecedor pode submeter uma proforma ele mesmo via ERPNext. Para saber mais sobre isto, visite a secção [pagina de Solicitção de Cotação](/docs/user/manual/pt/compras/solicitação-cotação#4-criando-uma-cotação-de-fornecedor-depois-de-um-sdq).

### 2.2 Criando uma Cotação de Fornecedor manual
1. Voce pode tambem criar uma Cotação de Fornecedor directamente apartir de:

    **Comprar > Aquisição > Cotação do Fornecedor > Novo**.
1. Selecione o Fornecedor que enviou a proforma.
1. O Endereço e Contacto sao procurados e voçe salvou na ficha do fornecedor.
1. Digite o Codigo do Item, selecione a quantidade. Preço sera procurado se voce definiu o preço de Compra Padrão para o item em [Preço do Item](/docs/user/manual/pt/inventario/preço-item).
    <img class="screenshot" alt="Supplier Quotation" src="{{docs_base_url}}/assets/img/buying/supplier-quotation.png">

Se voce tem varios Fornecedores que fornecem o mesmo Item, voce normalmente
envia uma [Solicitação de Cotação](/docs/user/manual/pt/compras/solicitação-cotação) para varios Fornecedores. Em muitos dos casos,
especialmente se voce tem compras centralizadas, voce pode quere guardar registo de todas as cotações para que:

  * Voce pode facilmente comparar os preços no futuro
  * Auditar para verificar se todos os Fornecedores foram dados a oportunidade.

Cotação de Fornecedores não necessario para os pequenos negocios. Avalie sempre o custo
de recolher informação pelo valor que realmente vale!
Como uma recomendação, voce pode fazer isto somente para itens de grande valor.

## 3. Funcionalidades
### 3.1 Impostos e Taxas
Se o seu Fornecedor lhe cobrar impostos adiconais ou taxas como envio e seguro, voce pode adicionar aqui. Isto vai ajudar a rastrear os custos de forma correcta. Tambem, se alguns destes impostos adicionam ao valor do produto voce irá ter que mencionar na tabela de Impostos. Voce pode tambem usar os modelos para os impostos. Para mais informações em configurar os seus impostos veja [Modelo de Impostoso de Compra e Taxas](/docs/user/manual/pt/compras/modelo-impostos-taxas-compra).

### 3.2 Mais
Existem campos para Categoria de Impostos, Regras de Envio, Modelo de Impostos de Compra e Taxas, Descontos, Termos e Condições, Configurações de Impressão. Voce pode preencher estes campos para o seu registo. Visite a pagina [Proforma](/docs/user/manual/pt/vendas/proforma) para saber mais sobre estas secções. De notar que os detalhes que voce preenche aqui como Regras de Envio, Impostos, Descontos, Termos e Condições etc., são do seu fornecedor e poidem ser guardados para um controle correcto.

Nota:

- Categoria de Imposto sera procurado apartir do fornecedor caso definido
- Configurações de Impressão é para fazer alterações a impressão da Proforma do Fornecedor
- Os Termos e Condições aqui são dos fornecedores
- A Cotação do Fornecedor pode estar ligada a solicitação de material usando o botão 'Ligar as solicitações de material'

### 3.3 Depois de Submeter
Os seguintes itens podem ser criados depois de submeter uma Cotação de Fornecedor:

* Ordem de Compra - Uma Ordem de Compra se voce concordar com as cotações de fornecedor.
* Proforma - Uma cotação para o seu cliente.
* Auto Repetição - Auto Repetir a cotação do fornecedor aos intervalos especificados.

### 4. Topicos Relacionados
1. [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
1. [Grupo de Fornecedor](/docs/user/manual/pt/compras/grupo-fornecedor)
1. [Ordem de Compra](/docs/user/manual/pt/compras/ordem-de-compra)
1. [Solicitação de Cotação](/docs/user/manual/pt/compras/solicitação-cotação)

{next}