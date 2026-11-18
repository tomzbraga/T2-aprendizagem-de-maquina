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

O DBSCAN diferente da ideia de procurar centros, o algoritmo identifica quantos vizinhos cada ponto tem. Caso o resultado seja suficiente, define-se uma região densa. Os pontos que se tocam entre regiões densas formam uma ligação e essa cadeia forma um cluster. Esse método não exige a informação da quantidade de clusters.
O parâmetro Epsilon é o raio que define se dois pontos podem ser considerados vizinhos caso sua distância for menor ou igual ao valor e Epsilon.
MinPts/MinSamples é o parâmetro que define se uma região é densa ou não com base na quantidade de pontos dentro do raio Epsilon.
Com base nos dois parâmetros citados acima, os pontos são considerados centrais, com ao menos MinPts vizinhos em Epsilon, de borda, dentro do raio, porém sem vizinhos suficientes, e de ruído, que não tem nenhuma ligação com nenhuma região densa. Os clusters se formam a partir da cadeia de pontos, mantendo os ruídos de fora dos grupos. 

Etapa 4

Diferente do DBSCAN o qual há a necessidade de escolher um único Epsilon, o HDBSCAN considera todos os valores possíveis de Epsilon ao mesmo tempo e os melhores grupos são escolhidos com base em uma hierarquia. O critério que estabelece essa hierarquia é a estabilidade, que mede o quanto cada grupo persiste ao longo dessa faixa de estabilidade. O Min Cluster Size define o menor tamanho aceito para um grupo e o Min Samples controla a estimativa da densidade local e a rigidez do algoritmo. O método facilita trabalhar com grupos de densidades diferentes e mantem sua estabilidade mesmo que parâmetros variem muito. Porém exige muito custo computacional, é mais complexo de interpretar e há a necessidade de normalizar as variáveis.

Etapa 5

Etapa 6

Como os dados da organização não são rotulatos, que o perfil do comportamento é desconhecido e que a densidade das máquinas são distindas, o HDBSCAN seria a abordagem mais adequada para a análise, já que ele não exige a definição prévia do número de grupos nem do raio Epsilon, mantém os ruídos e tem a capacidade de formar simultaneamente grupos densos e esparsos.
O K-Means precisaria da informação de grupos "suspeitos" "normais" antes para definir as posições de K, porém ele desconsideraria ruídos.










   
