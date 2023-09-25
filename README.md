# Classificação dos Diários da AMUPE
Projeto da disciplina de Inteligência Artificial - Universidade de Pernambuco - POLI

Feito em grupo, com a participação de:
 - [Alexandre Rodolfo](https://github.com/AlexandreRodolfo)
 - [Andina Lerma](https://github.com/ANDINALERMAUPE)
 - [Brenda Barros](https://github.com/neobrendismo)
 - [João Gabriel Gila](https://github.com/joaogabrieltg)
 - [Matheus Souza de Oliveira](https://github.com/patitow)  
 - [Pedro Lyra](https://github.com/PedrolyraC)

Este projeto foi desenvolvido com o intuito de auxiliar o Tribunal de Contas do Estado de Pernambuco a classificar publicações do Diário Oficial da AMUPE com base na modalidade, tipo de publicação e presença de festividade através do uso de técnicas de Inteligência Artificial.

O [Dataset.ipynb](https://github.com/AlexandreRodolfo/classificacao_dos_diarios_da_amupe/blob/main/Dataset.ipynb) mostra o processo de extração das publicações a partir dos PDFs dos Diários. Aqui conseguimos construir a base de dados com todas as informações relevantes para o futuro agrupamento e classificação.

No [Word2Vec com TF-IDF.ipynb](https://github.com/AlexandreRodolfo/classificacao_dos_diarios_da_amupe/blob/main/Word2Vec%20com%20TF-IDF.ipynb) fizemos o agrupamento dos dados, separados por frases, com o intuito de gerar vetores para cada palavra e atibuí-las pesos de acordo com o seu valor TF-IDF médio ao longo das publicações.

Em [Tensorflow.ipynb](https://github.com/AlexandreRodolfo/classificacao_dos_diarios_da_amupe/blob/main/Tensorflow.ipynb) realizou-se o treinamento das redes neurais necessárias para a realização da classificação. Ela detalha da criação dos datasets, com divisões de treino e teste, até a arquitetura e treinamento das redes. Os resultados das melhores épocas foram salvos na pasta Modelos.

Por fim, [Resultado.ipynb](https://github.com/AlexandreRodolfo/classificacao_dos_diarios_da_amupe/blob/main/Resultado.ipynb) traz o produto final para o cliente. Nele, são unidas todas as tecnologias dos outros três arquivos para construir uma ferramenta poderosa que consegue a partir do texto de uma publicação extrair os tipos de publicação, modalidade e festividade em probabilidades conjuntas para cada uma das frases do texto, considerando os *topn* resultados mais relevantes.

Da perspectiva do cliente, ele precisará interagir apenas com uma função, *avaliar(publicacao, topn)*, que tem as entradas e saídas destrinchadas anteriormente. Note que como o projeto foi desenvolvido no Google Drive e Colab, caso se deseje rodar localmente algumas mudanças deverão ser realizadas para acomodar o caminho dos arquivos e baixar as bibliotecas necessárias à execução do projeto.
