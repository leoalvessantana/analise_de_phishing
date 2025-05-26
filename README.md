# Análise de Ameaças Phishing Utilizando Machine Learning



Este projeto tem como objetivo principal a análise e detecção de ameaças de phishing utilizando técnicas de Machine Learning. Inicialmente, começamos importando as bibliotecas necessárias para manipulação de dados, visualização e modelagem, como pandas, scikit-learn, seaborn, matplotlib, TensorFlow e outras.

Os dados foram carregados e passaram por um processo cuidadoso de limpeza e tratamento para garantir qualidade, incluindo normalização, identificação e tratamento de variáveis binárias e não binárias, além da análise exploratória para entender as características dos dados e suas correlações com a variável alvo.

Após a preparação dos dados, aplicamos escalonamento para as variáveis numéricas e mantivemos as variáveis binárias em sua forma original. Também realizamos uma divisão dos dados em conjuntos de treino, validação e teste para garantir uma avaliação justa dos modelos.

Em seguida, testamos diversos modelos de Machine Learning clássicos, como Regressão Logística, K-Nearest Neighbors, Random Forest, XGBoost, LightGBM e redes neurais multi-layer perceptron, avaliando-os por métricas como acurácia, precisão, recall, F1-score e AUC, usando validação cruzada para garantir robustez.

A partir desses resultados, realizamos a otimização dos hiperparâmetros do melhor modelo, que no caso foi o LightGBM, usando Grid Search e validação cruzada. Após a escolha dos melhores parâmetros, treinamos o modelo final combinando os dados de treino e validação, e avaliamos o desempenho no conjunto de teste, confirmando alta performance na detecção de phishing.

Por fim, implementamos uma rede neural com TensorFlow/Keras, com múltiplas camadas densas e ativação ReLU, monitorando a perda e acurácia em treino e validação com Early Stopping para evitar overfitting. O modelo apresentou resultados consistentes e competitivos, confirmando a eficácia das redes neurais para este tipo de problema.

O código e análises contemplam toda a pipeline, desde a preparação dos dados, análise exploratória, modelagem clássica e deep learning, além de visualizações para interpretar e validar os resultados.

Este projeto serve como uma base sólida para desenvolvimento de sistemas de detecção de phishing, podendo ser expandido com mais dados, engenharia de características avançada e técnicas de deep learning mais complexas.



## Como Executar
1. Instale as dependências:

- pip install -r requirements.txt

2. Execute o script na ordem:

- Bibliotecas Utilizadas
- Pré-processamento e divisão dos dados
- Treinamento dos modelos clássicos e avaliação final
- Treinamento da rede neural e avaliação final
