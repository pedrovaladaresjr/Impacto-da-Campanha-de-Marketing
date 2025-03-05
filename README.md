# Impacto da Campanha de Marketing

O objetivo deste projeto é verificar se a aplicação da Campanha de Marketing teve algum efeito significativo ou não.

A campanha será realizada por meio de cupons, distribuídos aos clientes que receberão o Tratamento (GT).

Para o nosso estudo, aplicamos o **Teste t de Welch** para determinar se a estratégia aplicada foi positiva ou não. Comparamos os resultados entre os Grupos através de um **Teste A/B**.

### Dados Históricos

Geramos dados randômicos com distribuição normal, com média de 500 e desvio padrão de 50. O objetivo é verificar os pontos necessários para a aplicação do teste e garantir que algumas exigências estejam de acordo.

* `id`: Identificador de cada cliente. Neste caso, há apenas um por linha;
* `Vendas`: Valores resultantes de vendas em R$.

### Amostra dos Dados

A amostra foi extraída dos dados históricos. Para isso, calculamos o tamanho da amostra necessário e, posteriormente, aplicamos uma função para extrair essa amostra de forma aleatória.

Usamos os seguintes parâmetros para a divisão dos Grupos:

* **Grupo Tratamento (GT)**: 70%;
* **Grupo Controle (GC)**: 30%.

### Dados Após a Campanha

Esses dados simulam a situação após a campanha de marketing, que é a distribuição de cupons.

* `id`: Identificador de cada cliente. Neste caso, há apenas um por linha;
* `Vendas`: Valores resultantes de vendas em reais;
* `vendas_campanha`: Resultado das vendas após a campanha, em reais;
* `Grupo`: Coluna com os rótulos de quem pertence ao Grupo Tratamento (GT) e ao Grupo Controle (GC).

### Aplicação do Teste

* Aplicamos um **Teste t de Welch** para determinar se houve um impacto significativo na campanha de marketing.

  Realizamos alguns testes de normalidade (Anderson-Darling), pois nossos dados possuem variações nas extremidades.

  Aplicamos também o **Teste de Levene** para verificar se os grupos seguem variações iguais ou não. Após o teste de Levene, constatamos que os grupos possuem variâncias heterogêneas.

  Em seguida, aplicamos o **Teste t de Welch**, que ajusta o cálculo dos graus de liberdade para diferenças de variância.

* **Tamanho do Efeito - Cohen's d**

  Calculamos o tamanho do efeito para avaliar a magnitude da diferença entre as médias.

### Resultado do Teste

O resultado do teste mostrou que houve um impacto significativo na campanha de marketing. Ou seja, a estratégia aplicada de enviar cupons de desconto para um determinado grupo de estudo foi positiva, e observamos resultados significativos nos valores de vendas.

O tamanho do efeito está entre moderado e grande, e, neste caso, o grupo que recebeu os cupons teve um desempenho melhor do que os clientes pertencentes ao grupo que não recebeu os cupons.

É importante lembrar que este é um teste controlado, onde definimos os dados antes e após a aplicação da campanha. No entanto, essa abordagem é perfeitamente aplicável em qualquer situação onde seja necessário realizar comparações, como em um Teste A/B.

---
