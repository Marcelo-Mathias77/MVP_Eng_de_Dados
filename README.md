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
Os dados originais foram obtidos diretamente nas bases de dados do Databricks no seguinte caminho: dbfs:/databricks-datasets/cs100/lab4/data-001/, onde dentificou-se que o dataset tinha 2 tabelas: movies e ratings. Foi necessário identificar o delimitador do arquivo antes da leitura dos mesmos no formato csv. Inicialmente os dados brutos foram salvos na camada bronze. Na camada silver foi realizada a etapa de data quality e verificou-se que, apesar de permitir valor nulos, todos os campos continham dados. Na camada gold foi realizada a junção entre as tabelas movies e ratings, além da conversão do campo timestamp, que era do tipo número inteiro, para o tipo datetime. Posteriormente os dados foram manipulados via SQL, diretamente no Databricks, para obtenção das respostas formuladas no objetivo do trabalho.

### Dicionário de Dados

### Modelagem
### Carga
### Análise
### Autoavaliação
Atualmente, possuo um conhecimento básico em SQL, o que me permite realizar consultas, manipulação e análise de dados de forma fundamental. Essas habilidades serão úteis para extrair informações relevantes do conjunto de dados, realizar filtragens, agregações e cálculos estatísticos simples.
No entanto, não possuo conhecimento prévio em Databricks, que será uma das ferramentas utilizadas na análise. Isso pode representar um desafio inicial, especialmente no que diz respeito à configuração do ambiente, ao uso de notebooks colaborativos e à execução de operações distribuídas em grandes volumes de dados.

Diante desse cenário, meus principais pontos fortes são:
- Capacidade de estruturar consultas em SQL para explorar os dados.
- Facilidade em aprender novas ferramentas e conceitos.

Já os desafios incluem:
- Familiarização com o ambiente do Databricks e sua interface.
- Compreensão do funcionamento de Spark SQL e PySpark para lidar com grandes volumes de dados.
- Aprendizado de boas práticas para otimizar consultas e melhorar a performance no processamento de dados distribuído.

Para superar essas dificuldades, pretendo explorar tutoriais, documentações e cursos introdutórios sobre Databricks e PySpark, além de praticar a execução de queries e scripts dentro da plataforma para consolidar o aprendizado.

