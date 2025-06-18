# Robustez de Modelos de Detecção de Phishing com URLs Manipuladas

Este projeto avalia o desempenho e a robustez de modelos de detecção de phishing diante de manipulações leves em URLs, como *typosquatting*, *leetspeak*, inserção de subdomínios, troca de TLDs e inversão de palavras-chave.

## Objetivo

Testar modelos de aprendizado supervisionado e redes neurais convolucionais (CNNs) na detecção de phishing, comparando o desempenho:

- Em URLs legítimas e phishing tradicionais
- Em URLs de phishing modificadas de forma adversarial


## Bases de Dados Utilizadas

1. **Web Page Phishing Detection Dataset**  
   Fonte: [Kaggle](https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset/data)  
   Arquivo: `datasets/web_page_phishing.csv`

2. **Phishing and Benign Websites Dataset**  
   Fonte: [Zenodo](https://zenodo.org/records/5807622)  
   Arquivo: `datasets/phishing_and_benign_websites.csv`

3. **PhiUSIIL Phishing URL Dataset**  
   Fonte: [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/967/phiusiil+phishing+url+dataset)  
   Arquivo: `datasets/PhiUSIIL_Phishing_URL_Dataset.csv`


## Etapas do Projeto

### 1. Modelos Clássicos com Features de Engenharia
- Dataset: [Kaggle](https://www.kaggle.com/datasets/shashwatwork/web-page-phishing-detection-dataset/data)
- Modelos: Logistic Regression, Random Forest, XGBoost, SVM, KNN, Redes Neurais
- Avaliação: Accuracy, Precision, Recall, F1-score, Matriz de Confusão, ROC AUC

### 2. CNNs com URLs Brutas
- Dataset: URLs originais transformadas em sequências de caracteres
- Processamento: Tokenização por caractere + padding
- Arquitetura: Embedding → Conv1D → Pooling → Dropout → Dense

### 3. Avaliação Adversarial
- Geração de URLs de phishing modificadas
- Avaliação da mesma CNN sem re-treinamento
- Comparação das métricas pré e pós-manipulação


## Resultados 

Os resultados mostram que tanto os modelos clássicos quanto as CNNs podem apresentar alto desempenho em cenários tradicionais de detecção de phishing. 
No entanto, quando expostos a manipulações leves nas URLs, os modelos nem sempre mantêm sua eficácia, revelando vulnerabilidades importantes.

Essa fragilidade evidencia uma limitação crítica nos datasets públicos, que frequentemente não representam cenários adversariais reais, e podem levar 
a uma falsa sensação de segurança nos sistemas de detecção.

### Recomendamos que futuras abordagens:

- Incorporarem estratégias mais inteligentes de pré-processamento e normalização;
- Sejam testadas com URLs adversariais geradas sistematicamente;
- Combinen análise de URLs com outras fontes de informação (conteúdo da página, IPs, DNS, etc.);
- Explore a criação de modelos mais robustos via adversarial training ou técnicas de data augmentation realistas.



## Como Executar

1. Criar ambiente virtual
- python -m venv venv
- source venv/bin/activate  # ou venv\Scripts\activate no Windows

2. Instale as dependências:
- pip install -r requirements.txt

3. Rodar o notebook
- jupyter notebook
