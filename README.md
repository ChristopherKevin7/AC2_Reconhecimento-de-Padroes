# Projeto: Reconhecimento de Padrões

Este projeto foi desenvolvido como parte da disciplina Reconhecimento de Padrões do curso de graduação. Ele explora técnicas de classificação e regressão aplicadas a conjuntos de dados com o objetivo de identificar padrões e relações entre variáveis.

## Objetivos
- Pré-processar os dados para otimizar o desempenho dos modelos.
- Testar diferentes algoritmos de classificação, como K-Nearest Neighbors (KNN), Naive Bayes e Redes Neurais.
- Testar diferentes algoritmos de regressão, como Regressão Linear, Árvore de Decisão e Redes Neurais.
- Avaliar a influência de diferentes estratégias de validação, como o ajuste do tamanho do conjunto de teste (test_size).
- Identificar as colunas mais relevantes por meio da análise de correlação, eliminando atributos redundantes.

## Metodologia

### Classificação
    
#### Descrição do Dataset
    
  O dataset "Disease Symptom Prediction" conta com quase 5 mil linhas, com colunas que indicam a doenças e até 17 sintomas por doença. Contando com mais de 100 sintomas diferentes o dataset contém apenas dados nominais, o que dificulta o processamento dos dados.
    
#### Pré-processamento:
    
- Redução de classes no dataset para facilitar a análise. Contando inicialmente com 42 classes de doenças, foram reduzidos para apenas 6 classes de grupos de doenças.
- Utilizando a tecnica One Hot Encoder para transformar os dados nominais de sintomas em colunas binárias, que indicam a presença ou a falta de determinado sintoma
- Seleção de 15 colunas com maior correlação com a classe alvo, evitando redundância entre os atributos.
    
#### Modelos Utilizados:
    
- K-Nearest Neighbors (KNN): Apresentou a maior acurácia com 67%.
- Naive Bayes: Com a pior acurácia dentre os modelos apresentados, acabou gerando viés em uma das classes o que ocasionou perca na eficácia dos testes.
- Redes Neurais: Apesar da alta acurácia geral em relação aos outros modelos, ignorou a classe "Doenças Cardiovasculares e Circulatórias".
  
  
### Regressão
  
#### Descrição do Dataset
    
  Contando com cerca de 2,6 mil linhas, o dataset "Spotify by Genres" apresenta características de gêneros musicais, como valence, "loudness" e "danceability", que se correlacionam com a classe alvo, popularity.
    
#### Pré-Processamento:
    
- Análise de correlação dos atributos com a classe alvo mostrou que algumas características apresentam maior relevância como "loudness" e "acousticness", enquanto classes como "key" e "tempo" tiveram uma correlação extremamente baixa com a classe alvo.
- Normalização dos dados de colunas utilizando o metodo StandardScaler.
    
#### Modelos Utilizados:
    
- Regressão Linear: Com o pior desempenho dentre os modelos, atingindo um MAE 9,94 pontos, o que equivale a quase 10% do valor geral de popularidade variando entre 0 e 100.
- Árvore Binária: Apresentou uma melhora em relação à Regressão linear, porém ainda com baixa precisão.
- Redes Neurais: Conseguiu identificar melhor as nuances apresentadas pelas caracteristicas musicais, demonstrando que com um melhor tratamento dos dados e com mais testes poderia alcançar resultados positivos.

### Desafios

Baixa acurácia em alguns modelos devido a:
- Desequilíbrio nas classes do dataset.
- Necessidade de ajustes nos hiperparâmetros.
- Pré-processamento inicial que poderia ser mais refinado.

### Aprendizados

Este projeto proporcionou uma visão prática sobre os desafios do reconhecimento de padrões e a importância de um bom pré-processamento e validação dos dados.

## Como Executar

Clone o repositório:
  ```bash
    git clone https://github.com/seuusuario/nome-do-repositorio.git
  ```

Execute o notebook AC2_PADRÕES.ipynb para reproduzir os resultados.

### Links dos Datasets Utilizados

- [Spotify by Genres](https://www.kaggle.com/datasets/pesssinaluca/spotify-by-generes)
- [Disease Symptom Prediction](https://www.kaggle.com/datasets/itachi9604/disease-symptom-description-dataset?select=dataset.csv)

## Contribuições

Feedbacks e sugestões são bem-vindos! Sinta-se à vontade para abrir uma issue ou enviar um pull request.

