## Introdução / Problema
Olá. Me chamo Paulo Felipe e estou buscando me tornar um analista de dados. Este é o projeto que escolhi para demonstrar o uso de uma das ferramentas (Planilhas Google) aprendidas durante o curso Google Data Analytics Professional Certificate.

Há algum tempo tenho interesse em me mudar de cidade. E morando no Brasil, um fator importante de se pesquisar sobre uma possível próxima cidade é sua segurança. Existem diversos índices para medi-la, mas a taxa de homicídios em 1 ano (a cada 100 mil habitantes) costuma dar uma boa visão sobre o tema. 

Não é um indicador perfeito: A cidade do Rio de Janeiro, embora muito violenta se encontra com taxa média de 18,76 homicídios por ano a cada 100 mil habitantes nos 5 anos analisados. Para comparação, em 2022 a taxa de homicídios do Brasil (como um todo) foi de 24,5.

Como precisava fazer uma correlação para esta análise, a princípio quis buscar dados sobre médias de custo de vida ou aluguel nas cidades. Mas esses dados são muito difíceis de se encontrar de modo confiável e acessível. Procurei então no site do IBGE dados que são disponibilizados para todas as cidades. Destes, a Escolarização (6 a 14 anos) me chamou a atenção para uma possível correlação.

Como tive que manualmente inserir os dados de Escolarização do site do IBGE, limitei minha análise às 100 cidades mais populosas do Brasil.

## Link para a planilha:
<https://docs.google.com/spreadsheets/d/1iPvCGluCRVSooIrLmBuBE5s1o0rofLiCTUSh4n6AH18/edit?usp=sharing>

## Objetivos da análise
1) Ter uma tabela limpa (sem inconsistências gritantes) de cidades brasileiras e suas taxas de homicídios usando Dados Brutos da seguinte fonte: <https://www.ipea.gov.br/atlasviolencia/dados-series/20>. 
- *Vou chamá-la de Dados_Limpos_Hom*.

2) Ter uma tabela com as cidades brasileiras listadas por população. Isso foi fácil: <https://pt.wikipedia.org/wiki/Lista_de_munic%C3%ADpios_do_Brasil_por_popula%C3%A7%C3%A3o_(2022)>
- E depois manualmente inserir ao lado dados sobre a educação das 100 cidades mais populosas do país. No caso, escolhi a taxa de Escolarização (de 6 a 14 anos) fornecida pelo IBGE.
- *Vou chamá-la de Pop_e_Escol*.

3) Formar uma tabela com parte dos dados das duas tabelas acima necessários pra eu traçar uma possível correlação entre taxa de homicídios em uma cidade e sua taxa de não-escolarização.
- Comecei copiando da *Pop_e_Escol* dados das 100 cidades mais populosas (entre as linhas 2 e 101, incluindo estas). Escolhi as colunas B (nomes dos *Municípios*) e F (*Taxa de não-escolarização (%)*). 
- Depois, usando a função =VLOOKUP() foi relativamente fácil puxar as taxas médias de homicídios dos 5 anos que escolhi para esta análise. Tive somente 2 desafios: 1) Os valores estavam sendo inconsistentes: Aí pesquisei sobre a função e lembrei da importância do argumento FALSE no final 2) Em caso de cidades que possuem homônimas, tive que padronizar o nome do município tanto nesta tabela quanto nos Dados_Limpos_Hom pro padrão Cidade X (abreviação do estado) (exemplo: Campo Grande (MS)).

4) Fazer um gráfico de dispersão, com Taxa de não-escolarização (%) no eixo X, e Taxa média de homicídios no eixo Y.
- Ignoro os nomes dos municípios neste gráfico. Servem nessa página da planilha só para checar os dados mais facilmente.
- Colocar uma linha de tendência facilita notar a correlação.

## Conclusão / Soluções
Este é um tema bastante estudado pelas áreas de Sociologia, Educação e Segurança Pública. Como projeto para o meu portfólio, não me compete olhar estudos já existentes com suas soluções, e sim fazer a análise, demonstrando meu conhecimentos técnico, e sugerir diante de informações limitadas extraídas dos dados. 
- Correlação não é causalidade. Indo a fundo neste problema, pesquisaria por estudos que pudessem comprovar essa causalidade. Se não houvessem, aconselharia estudos para testar essa hipótese (que a princípio parece óbvia, mas queremos evitar o viés).
- Provada a causalidade, se formos olhar só pelo aspecto da segurança pública (porque todos merecem acesso a educação de qualidade independente disto), proporia ao Estado e à ONGs específicas formas de aumentar essa taxa de escolaridade. Mas antes, teríamos que estudar, possivelmente através de pesquisas, os motivos que fazem com que crianças fiquem longe das escolas e como poderíamos reduzi-los.
- Em resumo: Este estudo é mais um incentivo a melhoria da educação das crianças e adolescentes, já que além de beneficiá-los, pode contribuir a maior segurança da sociedade no futuro.

## O que faria se tivesse mais tempo
1) Incluiria mais pontos no meu gráfico de correlação. O que significa que teria que colocar manualmente mais taxas de escolaridade ou tentar achar uma tabela com cidades e suas taxas (de modo que não tivesse que acessar 1 página da internet do IBGE pra copiar cada taxa de escolarização).
2) Tentaria corrigir a falta (a princípio) de municípios homônimos em mais casos. Se 2 ou mais cidades se chamam "Campo Grande", por exemplo, o Atlas da Violência só me retorna os dados de 1. E geralmente nem é a maior cidade. Sei de que estado é a que aparece pesquisando pelo estado das cidades adjacentes. O Atlas agrupou as cidades por estados.
3) Pesquisaria por diversos estudos sobre o tema.
