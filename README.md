# MVP Engenharia de Dados

### Objetivo
O objetivo desta análise é explorar e obter insights sobre um conjunto de dados sobre avaliações de filmes, com base nas informações de filmes, usuários, avaliações e gêneros, realizadas entre os anos de 2000 a 2003. 
A partir do conjunto de dados, deseja-se responder à seguintes perguntas:
1. Quais os filmes com maior número de avaliações?
2. Quais os filmes (títulos) com a melhor avaliação?
3. Qual o gênero com a melhor avaliação?
4. Qual o total de Filmes avaliados?
5. Qual o total de usuários que avaliaram filmes?
6. Qual o total de avaliações por ano?
7.  Quais os filmes com as piores avaliações?

### Coleta dos Dados
Os dados originais foram obtidos diretamente entre as bases de dados do Databricks no seguinte caminho: dbfs:/databricks-datasets/cs100/lab4/data-001/, onde identificou-se que o dataset escolhido tinha 2 tabelas: movies (dimensão) e ratings (fato).

### Carga / Modelagem
Foi necessário identificar o delimitador do arquivo antes da leitura dos mesmos no formato csv. Inicialmente os dados brutos foram salvos na camada bronze. Na camada silver foi realizada a etapa de data quality e verificou-se que, apesar de permitir valor nulos, todos os campos continham dados, conforme evidenciado nas contagens de valores nulos das tabelas movies e ratings. Não foram encontrados outros problemas com os dados que pudessem comprometer a qualidade da análise. 

Modelo de dados (camadas bronze e silver)
![Modelo de dados](https://github.com/user-attachments/assets/33939785-ad83-42aa-8c9b-7ef357ee2523)


Na camada gold foi realizada a junção entre as tabelas movies e ratings, utilizando a coluna movieId como chave, além da conversão do campo timestamp, que era do tipo número inteiro, para o tipo datetime. Após isso foi criada uma tabela gold consolidando as duas tabelas (gold.movies_ratings).

### Análise
Posteriormente às etapas de carga e modelagem, os dados foram manipulados via SQL, diretamente no Databricks, para obtenção das respostas às perguntas que foram formuladas no objetivo desse trabalho.
Uma cópia da análise realizada foi inserida nesse repositório.
O trabalho original encontra-se no link a seguir: 
(https://databricks-prod-cloudfront.cloud.databricks.com/public/4027ec902e239c93eaaa8714f173bcfc/908816867272057/816507647137833/1974515297805925/latest.html).

### Dicionário de Dados
O dicionário a seguir descreve os dados disponíveis na tabela gold.movies_ratings, fornecendo informações sobre cada campo, incluindo seu significado, tipo de dado, domínio esperado e possíveis categorias.

![Catálogo de dados](https://github.com/user-attachments/assets/11f830f0-90d1-4a79-a6cc-8a8cc02fc690)

### Respostas para as perguntas formuladas no Objetivo

1. Quais os filmes com maior número de avaliações?
Na tabela abaixo estão os 5 filmes com o maior número de avaliações.
![Resp  perg  1](https://github.com/user-attachments/assets/a165d6df-df8e-4124-92e5-2e33583410de)
 
2. Quais os filmes (títulos) com a melhor avaliação?
Na tabela abaixo estão os 3 filmes com as melhores avaliações (média das notas).
![image](https://github.com/user-attachments/assets/565c5374-e0b5-49c5-85fd-90f53a5bb716)

3. Qual o gênero com a melhor avaliação?
O gênero com a melhor avaliação foi Sci-Fi|War, com média de 4,45.
![image](https://github.com/user-attachments/assets/70446652-cd87-48f9-87f8-593351824a92)

4. Qual o total de Filmes avaliados?
O total de filmes avaliados foi 3.615.
![image](https://github.com/user-attachments/assets/5a95366a-269d-43e4-8c1c-542be05029b0)
 
5. Qual o total de usuários que avaliaram filmes?
O total de usuários que avaliaram filmes foi de 2.999.
![image](https://github.com/user-attachments/assets/7ad44b12-c44d-400a-a16b-b3731fdc644b)

7. Qual o total de avaliações por ano?
O total de avaliações por ano está no gráfico abaixo. O ano com mais avaliações foi 2000 com 424.406 avaliações.
![image](https://github.com/user-attachments/assets/a27edefd-53fd-425b-8b7c-f74b210b2267)

9.  Quais os filmes com as piores avaliações?
Os 10 filmes com as piores avaliações (nota média = 1) estão na tabela abaixo.
![image](https://github.com/user-attachments/assets/3d70b2c4-8491-462c-b01c-1beef178f887)

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

Para superar as dificuldades expostas acima, explorei tutoriais, documentações, cursos introdutórios sobre Databricks e PySpark, tirei dúvidas com colegas, além de praticar a execução de queries e scripts dentro da plataforma.
Para consolidar o aprendizado, pretendo continuar buscando formas para melhorar a qualidade das minhas entregas futuras.

