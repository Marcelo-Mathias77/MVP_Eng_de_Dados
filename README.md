# MVP Engenharia de Dados

### Objetivo
O objetivo desta análise é explorar e obter insights sobre um conjunto de dados de avaliações de filmes, com base nas informações de filmes, usuários, avaliações e gêneros. A partir do conjunto de dados, deseja-se responder à seguintes perguntas:
1. Qual o filme com mais avaliações (contagem;
2. Identificar o título do filme que recebeu o maior número de avaliações, com base na contagem de registros de avaliação (rating);
3. Qual o filme com a melhor avaliação (média);
4. Determinar o filme com a maior média de avaliações, fornecendo o título que obteve a melhor nota média entre todos os filmes.
5. Gênero com a melhor avaliação (média);
6. Analisar os gêneros de filmes e identificar aquele que obteve a maior média de avaliações, permitindo entender quais gêneros são mais bem avaliados pelos usuários;
7. Total de filmes avaliado;
Contabilizar o número de filmes distintos que receberam pelo menos uma avaliação, fornecendo uma visão geral da quantidade de filmes avaliados no dataset.
8. Total de avaliações por ano;
9. Calcular o número total de avaliações feitas a cada ano, a partir da coluna timestamp, permitindo observar a distribuição de avaliações ao longo do tempo.
Esses objetivos fornecem uma visão abrangente da popularidade e qualidade dos filmes e gêneros, assim como a dinâmica temporal das avaliações.

### Coleta dos Dados
### Modelagem
### Carga
### Análise
Os dados originais foram obtidos diretamente nas bases de dados do Databricks no seguinte caminho: dbfs:/databricks-datasets/cs100/lab4/data-001/, onde dentificou-se que o dataset tinha 2 tabelas: movies e ratings. Foi necessário identificar o delimitador do arquivo antes da leitura dos mesmos no formato csv. Inicialmente os dados brutos foram salvos na camada bronze. Na camada silver foi realizada a etapa de data quality e verificou-se que, apesar de permitir valor nulos, todos os campos continham dados. Na camada gold foi realizada a junção entre as tabelas movies e ratings, além da conversão do campo timestamp, que era do tipo número inteiro, para o tipo datetime e a junção das tabelas movies e ratings. Posteriormente os dados foram manipulados via SQL, diretamente no Databricks, para obtenção das respostas formuladas no objetivo do trabalho.

### Dicionário de Dados

### Autoavaliação
Antes do início da pós graduação, já trabalhava com análise de dados, usando linguagem M (power query) e DAX e Python, mas sem utilizar as ferramentas propostas para o MVP. 
O conhecimento em SQL adquirido ao longo do curso, me permitiu realizar consultas, manipulação e análise de dados. 
Essas habilidades foram úteis para extrair informações relevantes do conjunto de dados, realizar filtragens, agregações e cálculos.
No entanto, não possuia conhecimento prévio em Databricks, uma das ferramentas utilizadas nesse trabalho. Tal fato representou um desafio inicial, bem com a utilização do spark.

Diante desse cenário, identifiquei como pontos fortes:
- Capacidade de estruturar consultas em SQL para explorar os dados.
- Facilidade em aprender novas ferramentas e conceitos, dada a experiência prévia com análise de dados / programação.

Já os desafios incluíram:
- Familiarização com o ambiente do Databricks e sua interface.
- Compreensão do funcionamento de Spark SQL e PySpark.

Para superar as dificuldades expostas acima, explorei tutoriais, documentações, cursos introdutórios sobre Databricks e PySpark, tirei dúvidas com colegas, além de praticar a execução de queries e scripts dentro da plataforma para consolidar o aprendizado.

