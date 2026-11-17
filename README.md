# T2-aprendizagem-de-maquina
Trabalho da matéria aprendizagem de máquina IESB

Etapa 1

1. Artigo-Inteligencia Artificial e Aprendizado de Máquina na Sociedade

A aprendizagem não supervisionada é um aprendizado que permite o sistema descobrir agrupamentos e formas dentro dos dados de entrada sem orientações claras. Já a supervisionada a IA é treinada com exemplos já rotulados.

2. O que é clustering e qual problema essa abordagem procura resolver?

   Como o aprendizado não supervisionado recebe dados não rotulados, a IA divide conjuntos de dados em grupos (clusters) analisando padrões semelhantes entre eles.
   Imagine ter que analisar uma enorme quantidade de dados não rotulados e desorganizados um a um, a técnica de clustering permite que a IA divida os dados e organize em padrões mais rapidamente e ainda separar registros atípicos. Tudo isso para facilitar uma análise posterior com mais contexto e organização.

3. O significado de similaridade, distância, grupo (cluster), centróide e ruído/outlier no contexto de agrupamento.

Similaridade: Critério que o clustering utiliza para agrupar itens similares considerando suas características. A similaridade é o quanto os itens se parecem.

Distância: forma matemática de medir a similaridade apresentando um gráfico em que cada característica é um eixo e que cada item é um ponto no espaço, a distância mede o quão longe os pontos estão. A distância age proporcionalmente com a similaridade, quanto menor a distância, maior a similaridade entre os itens representados pelos pontos.

Grupo (cluster): Agrupamento de pontos que estão próximos ou são similares e mais distantes de pontos de outros conjuntos.

Centróide: Média de cada características de todos os pontos de um grupo. Resume o comportamento típico do cluster e serve de referência para atribuições

Ruído/outlier: Pontos que não se encaixam em nenhum grupo (atípicos). valores muito diferentes dos padrões representam os outliers, e o rótulo que é dado para pontos que não pertencem a nenhum cluster chama-se ruído.

4. Por que um algoritmo de clustering não atribui, por si só, rótulos semânticos como     “normal” ou “suspeito” aos
    grupos encontrados?

   Rotular características como "normal" ou "suspeito" depende de uma análise de contexto. O aprendizado não supervisionado é utilizado para facilitar rotulagem, tomada de decisões. Quem rotula são os analistas após uma análise do resultado gerado.

Etapa 2

K-Means é o algoritmo que executa a tarefa de clustering dentro do aprendizado não supervisionado. Com o K definido, escolhem-se K posições para os centróides essas posições podem ser aleatórias ou utilizando o K-Means++, que escolhe o primeiro K e os outros são definidos com base na probabilidade de ficarem longe do K já escolhido. 
Depois os pontos são agrupados com base na distância até à centróide mais próxima.
Como as posições das centróides são inicializadas ao acaso, é necessário atualizar suas posições com base na média dos pontos de cada grupo.
Como o K-Means depende de um K inicial, a escolha dele é fundamental para que haja bons resultados. Informações contextuais ajudam muito a definir, já que um bom valor é a quantidade de grupos que o modelo terá. O método baseia-se em distâncias até o centro, e isso dificulta seu desempenho em grupos que fogem do padrão esférico. Não reconhece ruído, sempre atribui um ponto a um grupo. É um método intuitivo, rápido e eficiente, funciona bem com grandes volumes de dados, seu resultado é de fácil compreensão e está disponível em diversas bibliotecas.

Etapa 3







   
