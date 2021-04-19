<!-- add-breadcrumbs -->
# Configurações de Stock

Você pode definir configurações padrão para as transações de stock apartir da pagina de Configurações de Stock.


## 1. Nome do Item por

![Configuraçoes de Stock](/docs/assets/img/stock/stock-settings-1.png)

Por defeito, o Nome do Item é posto como o Codigo do Item digitado. Se você quer que os Itens sejam por um nome escolha [Serie de Atributo de Nomes](/docs/user/manual/pt/configuração/configurações/nome-das-series) a opção 'Serie de Atributo de Nomes' .


## 2. Padrões

### 2.1 Item do Grupo Padrão
Esta será o grupo de item padrão alocado ao novo item criado. Grupos de Item são uteis para classificação e configuração de propriedades para o grupo todo. Para saber mais visite a pagina [Grupo de Item](/docs/user/manual/pt/inventario/grupo-item) .

### 2.2 UDM de Stock Padrão
A unidade de medida padrão para o stock é posta como numeros (Nos), pode ser trocado aqui.

### 2.3 Armazem Padrão
Defina o Aramzem Padrão pelo o qual as transações são feitas. Esta será procurada no Armazem Padrão e na ficha de Item:
    ![Definições de Stock](/docs/assets/img/stock/stock-settings-def.png)

### 2.4 Armazem de Retenção de Amostra
Este é o Armazem aonde as retenções das amostras são guardadas. Para saber mais, visite [esta pagina](/docs/user/manual/pt/inventario/reter-amostra-stock).

### 2.5 Metodo de Avaliação Padrão
FIFO - Primeiro entrou primeiro saiu ou Media movel (moving average valuation) para os seus itens. O metodo padrão é o FIFO. Se você selecionar Media Movel, novos Items seram avaliados com base na movimentação movel. Você pode mudar ao criar novos Itens no formulário do Item. Uma vez o Item salvo, o Metodo de Avalição não pode ser trocado. Leia mais [aqui](https://frappe.io/blog/erpnext-features/inventory-valuation-method-fifo-vs-moving-average).

## 3. Limite de Percentagem
Esta é a percentagem que você permite para receber ou enviar mais contra a quantidade encomendada. Por exemplo se você encomendou 100 unidades, o Fornecedor envia 120 unidade e a parcentagem está como 10% então será permitido receber 110 unidades. Por defeito, está definido como 0.

## 4. Mostrar o campo de Codigo de Barras
Um campo para digiar os detalhes do Codigo de Barras para um item. Se não selecionado, o campo não ficará visivel no formulario do item.

## 5. Converter a Descrição do Item para HTML
Normalmente, descrições são copia-colar de uma Pagina ou ficheiro Word/PDF e contem muitos estilos escondidos. Isto cria confusão ao fazer Pre-Impressão das suas facturas ou proformas.

Para arranjar, você pode selecionar "Converter Descrição de Item para HTML" em Definições de Stock. Isto irá fazer com que quando ao salvar os Itens, as suas descrições estaram limpas.

Se voce quiser controlar a descrição, visualizações, e permitir qualquer codigo HTML, você pode não selecionar esta opção.

## 6. Auto inserir

![Definições de Stock](/docs/assets/img/stock/stock-settings-2.png)

### 6.1 Auto inserir Taxa de Preço de Lista caso não tenha
Activando esta opção irá inserir um Preço de Item a Lista de Preços de um Item automaticamente ao utilizar esta Iten na sua primeira transação. Este preço é procurado apartir da 'Taxa' definida na primeira transação com o Item. O Preço de Lista depende se estiver a usar a transação de Compra ou Vendas.

De notar que, o Preço de Item será inserido automaticamente somente no caso da primeira transação se não estiver já feito.

Se está opção não for selecionada, o 'Preço de Venda Standard' definido no Item ao criar o item será adicionado a Lista de Preço.

### 6.2 Automaticamente definir o Numero de Serie com base no FIFO
Numeros de Serie para o Stock serao automaticos com base nos Itens digitados com base no primeiro entrou primeiro saiu. O Numero de Serie será definido automaticamente nas transações como Facturas de Compra/Vendas, Guias de Remessa, etc.

## 7. Permitir Stock Negativo
Este irá permitir que o stock dos Itens fiquem com valores negativos. Usnado esta opção depende do seu caso. Por exemplo, os registo de transações são digitados no fim de semana ou fim do mês. Neste caso, stock negativo precisa estar activo para que você possa continuar com as transações de Compras/Vendas.

## 8. Definir Qtd em Transações com base no Numero de Serie Inputado
A quando de Itens será definida de acordo os Numeros de Serie. Por exemplo, se o usuario adicionar numeros de serie como A001, A002 e A003 então o sistema irá definir a quantidade como 3 nas transações.

## 9. Requisição de Material Automatica

![Definições de Stock](/docs/assets/img/stock/stock-settings-3.png)

### 9.1 Criar Solicitação de Material quando o Stock atingir o nivel de encomenda

Esta opção é util se você quer ter a garantia de fornecimento constante de um raw materials/produtos e evitar escacêz.
Uma [Solicitação de Material](/docs/user/manual/pt/inventario/solicitação-material) será criado automaticamente quando o nivel do stock atingir o nivel de encomenda definido no [Formulario do Item](/docs/user/manual/pt/inventario/item#34-encomenda-automatica).

### 9.2 Notificar via Email na criação de uma Solicitação de Material
Um email será enviado para notificar o Usuario com o papel de 'Gestor de Compras' quando uma Solicitação de Material automatica for criada.

## 10. Configurações de Transferencia entre Armazens Internos

<img class="screenshot" alt="Delivery Note Material Transfer" src="{{docs_base_url}}/assets/img/stock/inter-warehouse.png">

### 10.1 Activar armazem de clientes para transferencia de material apartir de uma Guia de Remessa e Factura de Venda

Esta opção é util quando a transferencia de material precisa ser apresentada como uma Guia de Material. Por exemplo, se existe requesitos obrigatorios aonde os impostos são aplicadas para cada transferencia ou Material. É facil gerir a transferencia numa Guia de Remessa, do que numa Entrada de Stock

### 10.2 Activar armazem de fornecedores para transferencia de material apartir de um Recibo de Compra e Factura de Compra

É igual a opção em cima, é util quando a transferencia de material precisa ser apresentada como Recibo de Compra.

Para saber mais sobre transferencia de material interna via Guia de Remessa e Factura de Compra por favor ver esta artigo [Transferencia de Material apartir de um Guia de Remessa](/docs/user/manual/pt/inventario/artigos/transferencia-material-pela-guia-de-remessa)

## 11. Congelar Entradas de Stock

O Usuario não será permitido a fazer registo de Stock depois desta data.

![Definições de Stock](/docs/assets/img/stock/stock-settings-4.png)

* **Congelar Stock até**: Uma data limite no qual o stock ficará congelado.
* **Congela Stocks anteriores a [Dias]**: Stocks anteriores a x dias serao congelados. É calculado com base na data de criação do item.
* **Papel Permitido para editar stock congelado**: O papel que você ecolhe aqui será permitido editar o stock congelado.

## 12. Indentificação de Lote
Configuração Global para lotes de stocks a serem identificado por um [Nome de Series](/docs/user/manual//pt/configuração/configurações/nome-das-series). Você pode passar por cima no DocType do Item.
