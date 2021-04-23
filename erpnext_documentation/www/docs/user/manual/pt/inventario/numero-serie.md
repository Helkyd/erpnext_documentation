<!-- add-breadcrumbs -->
# Numero de Serie

Como visto na pagina [Item](/docs/user/manual/pt/inventario/item), se um **Item** for _serializado_, um
registo **Numero de Serie** (Serial No) é mantido para cada quantidade desse
**Item**. Esta informação ajuda a rastrear a localização do Nº de Serie,
sua garantia e informação do fim-da-vida (data de expiração).

**Numeros de Serie** são tambem uteis para para activos fixos. [Calendario de Manutenção](/docs/user/manual/pt/suporte/calendario-manutencao) pode ser criado contra Numeros de Serie para planeamento e actividade do calendario de manutenção para estes activos (se precisam de manutenção).

Voce pode tambem rastrear de que **Fornecedor** voce comprou o **Nº de Serie** e
para quem **Cliente** voce vendeu. O status do **Nº de Serie** irá dizer
o status do inventario corrente.

Se o seu Item for _serializado_ voce tera de digitar o Nº de Serie na
coluna correcta para cada Nº de Serie numa linha nova.
Voce pode manger unidades singulares de itens serializados usando o Numero de Serie.

Para acessar a lista de Numeros de Serie, va para:
> Home > Inventario > Nº de Serie e Lotes > Nº de Serie

## 1. Pre-requisitos
Antes de criar e usar o Numero de Serie, é aconselhado criar o seguinte:

* [Item](/docs/user/manual/pt/inventario/item)
* Activar na tabela do Item 'Tem Nº de Serie'
    ![Serie não Activado](/docs/assets/img/stock/serial-no-enabled.png)


## 2. Como criar um Numero de Serie
Normalmente, Numeros de Serie são auto-criados quando as transações são feito contra um Item serializado. Este funciona somente quando 'Tem Nº de Serie' esta activo e uma serie é definida no formulario do Item.

Por exemplo, uma serie foi definido para o seguinte Item como 'PB2L.#####'. Então um Registo de Stock foi submetido para receber o Item. Os Numeros de Serie são criado de acordo.

![Nº de Serie Criados](/docs/assets/img/stock/serial-no-created.png)

Contudo, se voce quer criar um Nº de Serie _manualmente_ siga estes passos:

1. Va para a lista de Numeros de Serie, clique em Novo.
1. Digite o Numero de Serie.
1. Digite o Codigo do Item e os detalhes seram procurados.
1. Se qualquer transação for feita com um item, Nº de Serie não pode ser definido ou removido.
1. Salvar.

Inventario de um Item somente pode ser afectado se o Nº de Serie for transacionado via
Transação de Stock (Registo de Stock, Recibo de Compra, Guia de Remessa, Facturas de Venda). 
Quando um Nº de Serie é criado directamente, o Armazem não pode ser definido.

<img class="screenshot" alt="Serial Number" src="{{docs_base_url}}/assets/img/stock/serial-no.png">

### 2.1 Notas sobre o Numero de Serie

* O Status é definido com base no Registo de Stock.
* Somente Numeros de Serie com status 'Disponivel' podem ser entregues.
* Numeros de Serie podem ser automaticamente criados apartir de um Registo de Stock ou Recibo de Compra. Se voce mencionar o Numero de Serie na coluna de Numero de Serie, irá automaticamente criar estes Numeros de Serie.
* Se na tabela Item, o Numero de Serie for mencionado, voce pode deixar a coluna Numero de Serie em branco num Registo de Stock / Recibo de Compra. Numeros de Serie serao automaticamente criados apartir da serie.

## 3. Funcionalidades
### 3.1 Detalhes de Compra/Fabrico
O documento no qual o Numero de Serie foi criado sera mostrado. Se voce comprou de um Fornecedor, ficará ligado aqui.

### 3.2 Detalhes de Entrega
Se o Numero de Serie foi gerado apartir de uma Ordem de Venda, o Cliente será ligado aqui.

### 3.3 Detalhes de Garantias/AMC
Se o Item estiver em garantia ou AMC (Contracto de Manutenção Anual), as datas de expiração para este podem ser definidas.

### 3.4 Mais Informações
Qualquer informação adicional sobre este Item especifico pode ser definido em 'Detalhes do Numero de Serie'.

## 4. Video
<div class="embed-container">
    <iframe src="https://www.youtube.com/embed/Q4tYKYTbVek" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
    </iframe>
</div>

### 5. Topicos Relacionados
1. [Codificação do Item](/docs/user/manual/pt/inventario/artigos/codificacao-item)
1. [Variantes do Item](/docs/user/manual/pt/inventario/variantes-item)
1. [Nome do Numero de Serie](/docs/user/manual/pt/inventario/artigos/serial-no-naming)

