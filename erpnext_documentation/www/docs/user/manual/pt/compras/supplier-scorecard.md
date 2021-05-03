<!-- add-breadcrumbs -->
# Scorecard do Fornecedor

**Um Scorecard do Fornecedor é uma ferramenta de evolução usado para avaliar o desempenho dos fornecedores.**

Scorecards do Fornecedores podem ser usado para rastrear a qualidade do item, entra, e tempo de resposta dos fornecedores ao longo de um periodo de tempo. Este dado é usado normalmente para ajudar nas decisões de compra.
Um Scorecard do Fornecedor é manualmente criado para cada fornecedor.

Para acesso Scorecard do Fornecedor, va para:
> Home > Comprar > Scorecard Fornecedor > Scorecard Fornecedor


## 1. Pre-requisitos
Antes de criar e usar o Scorecard do Fornecedor, é aconselhavel criar estes:

* [Fornecedor](/docs/user/manual/pt/compras/fornecedor)

## 1. Como criar um Scorecard de Fornecedor

1. Va para a lista de Scorecard do Fornecedor, clique em Novo.
2. Selecione o Fornecedor para marcar.
3. Selecione o periodo de avaliação caso seja semanal, mensal ou anual.
4. Defina as funções de marcação (detalhes na proxima secção).
5. Um scorecard de Fornecedor é criado para cada fornecedor individual. Somente um scorecard de fornecedor pode ser criado para cada fornecedor. 
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard.png">

## 2. Funcionalidades
### 2.1 Configuração do Scoring
O scorecard do fornecedor consiste num conjunto de periodos de avaliação, durante o qual o desempenho de um fornecedor é avaliado. Este periodo pode ser semanal, mensal ou anual. O score (pontuação) actual é calculado apartir do score do periodo de cada avaliação com base nas funções de peso. A formula pardrão é linearmente ponderada sobre os 12 periodos de marcação anteriores. 
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard-weighing.png">
Esta formula é customizada.

#### Classificação do Fornecedor

A classificação do fornecedor é usado para rapidamente organizar os fornecedores com base nos seu desempenhos. Estes são customizaveis para cada fornecedor. 

O scorecard que fica de um fornecedor pode ser usado para restringir fornecedores de serem incluidos nas Solicitações de Cotação ou de serem criadas Ordens de Compra. Os seguintes ecrã podem ser vistos ao expandir a linha na tabela 'Classificação de Pontuações', clique na seta virada para baixo.
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard-standing.png">

### 2.2 Configuração de Criterios
Um fornecdor pode ser avaliado em varios criterios individuais de avaliação, incluindo (mas não limitado a) tempo de resposta de cotação, qualidade de entrega do tiem, e tempo das entregas. Estes criterios são pesados para determinar a pontuação do periodo final. 

Para criar um novo Criterio, va para Comprar > Scorecard Fornecedor > Criterios do Scorecard do Fornecedor:
<img class="screenshot" alt="Purchase Order" src="{{docs_base_url}}/assets/img/buying/supplier-scorecard-criteria.png">

Nota: Peso dos Criterios para um scorecard deve somar até 100. 

### 2.3 Variaveis do Scorecard do Fornecedor
O metodo para calcular cada criterio é determinado pelo campo Formula do Criterio, que pode usar um numero de variaveis pre criadas. Este podem ser vistos no ecrã mais em baixo.

O valor de cada uma das variaveis é calculada sobre o periodo de pontuação para cada fornecedor. Exemplos de tais variaveis:

 - O total de itens recebidos de um fornecedor
 - O total de itens aceites apartir de um fornecedor
 - O total de itens rejeitados apartir de um fornecedor
 - O total de entregas apartir de um fornecedor
 - O valor total (em dolares) recebidos de um fornecedor

![Variavel do Scorecard do Fornecedor](/docs/assets/img/buying/supplier-scorecard-variables.png)

Variaveis pre definidas, variaveis adicionais  pode ser incluidas via customização. Selecione a caixa Personalizado se a variavel que estiver a criar for para um campo customizado.

A formula do criterio deve ser customizado para avaliar os fornecedores de cada criterio de uma forma que possa servir os requisitos da empresa.

### 2.4 Formula de Avaliação
A formula de avaliação usa as pre-estabelicidas ou variaveis customizadas para avaliar um aspecto do desempenho do fornecedor durante um periodo de pontuação. Formulas podem usar as seguintes funções matematicas:

* soma: + 
* subtração: -
* multiplicação: *
* divisão: /
* min: min(x,y)
* max: max(x,y)
* if/else: (x) if (formula) else (y)
* menor que: <
* maior que: >
* variaveis: {variable_name}

É crucial que a formula seja resolvida para todos os valores das variaveis. É normalmente um problema se o valor resolve para 0. Por exemplo:
```
{total_accepted_items} / {total_received_items}
```

Este exemplo deve resolver para 0 / 0 em periodos aonde não tem itens recebidos, e para tal deve ter uma condição para proteger este caso:
```
({total_accepted_items} / {total_received_items}) 
if {total_received_items} > 0
else 1.
```

### 2.5 Avaliando o Fornecedor
Uma avaliação pode ser gerada para cada Periodo de Pontuação do Fornecedor fazendo o clique no botão "Periodo do Scorecard do Fornecedor". A pontuação actual do fornecedor pode ser visto, bem com um grafico visual mostrando o desempenho do fornecedor ao longo do tempo. Qualquer acção contra o fornecedor tambem são vistos aqui, incluindo avisos ao criar SDCs e PCs ou quando não são permitidos.

### 3. Topicos Relacionados
1. [Fornecedor](/docs/user/manual/pt/compras/fornecedor)
1. [Cotação de Fornecedor](/docs/user/manual/pt/compras/cotação-do-fornecedor)

{next}