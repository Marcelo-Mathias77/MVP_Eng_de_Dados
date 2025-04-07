# MVP Engenharia de Dados

### Objetivo
O objetivo desta análise é explorar e obter insights sobre um conjunto de dados de avaliações de filmes, com base nas informações de filmes, usuários, avaliações e gêneros. 
A partir do conjunto de dados, deseja-se responder à seguintes perguntas:
1. Quais os filmes com maior número de avaliações?
2. Quais os filmes (títulos) com a melhor avaliação?
3. Qual o gênero com a melhor avaliação?
4. Qual o total de Filmes avaliados?
5. Qual o total de usuários que avaliaram filmes?
6. Qual o total de avaliações por ano?
7.  Quais os filmes com as piores avaliações?

### Coleta dos Dados
Os dados originais foram obtidos diretamente entre as bases de dados gratuitas do Databricks no seguinte caminho: dbfs:/databricks-datasets/cs100/lab4/data-001/, onde dentificou-se que o dataset escolhido tinha 2 tabelas: movies e ratings.

### Modelagem / Carga
Foi necessário identificar o delimitador do arquivo antes da leitura dos mesmos no formato csv. Inicialmente os dados brutos foram salvos na camada bronze. Na camada silver foi realizada a etapa de data quality e verificou-se que, apesar de permitir valor nulos, todos os campos continham dados, conforme evidenciado nas contagens de valores nulos nas tabelas movies e ratings. Não foram encontrados outros problemas com os dados que pudessem comprometer a qualidade da análise. 

Modelo de dados (camadas bronze e silver)

![Modelo de dados](https://github.com/user-attachments/assets/33939785-ad83-42aa-8c9b-7ef357ee2523)


Na camada gold foi realizada a conversão do campo timestamp, que era do tipo número inteiro, para o tipo datetime e a junção entre as tabelas movies (dimensão) e ratings (fato), utilizando a coluna movieId como chave.

### Análise
Posteriormente às etapas de modelagem e carga dos dados, os dados foram manipulados via SQL, diretamente no Databricks, para obtenção das respostas formuladas no objetivo do trabalho.

### Dicionário de Dados
O dicionário a seguir descreve os dados disponíveis na base, fornecendo informações sobre cada campo, incluindo seu significado, tipo de dado, domínio esperado e possíveis categorias.

![Catálogo de dados](https://github.com/user-attachments/assets/ca12f31f-b591-45e8-92d1-c631a17cf227)

### Autoavaliação
Antes do início da pós graduação, já trabalhava com análise de dados, usando linguagem M (power query), DAX e Python, mas sem utilizar as ferramentas propostas para o MVP. 
O conhecimento em SQL adquirido ao longo do curso, me permitiu realizar consultas, manipulação e análise de dados. 
Essas habilidades foram úteis para extrair informações relevantes do conjunto de dados, realizar filtragens, agregações e cálculos.
No entanto, não possuia conhecimento prévio em Databricks, uma das ferramentas utilizadas nesse trabalho. Tal fato representou um desafio inicial, bem com a utilização do Spark.

Diante desse cenário, identifiquei como meus pontos fortes:
- Capacidade de estruturar consultas em SQL para explorar os dados.
- Facilidade em aprender novas ferramentas e conceitos, dada a experiência prévia com análise de dados / programação.

Já os desafios incluíram:
- Familiarização com o ambiente do Databricks e sua interface.
- Compreensão do funcionamento de Spark SQL e PySpark.

Para superar as dificuldades expostas acima, explorei tutoriais, documentações, cursos introdutórios sobre Databricks e PySpark, tirei dúvidas com colegas, além de praticar a execução de queries e scripts dentro da plataforma para consolidar o aprendizado.

