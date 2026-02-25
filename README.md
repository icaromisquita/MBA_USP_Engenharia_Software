Predição de Break-Even de Tarifas ANEEL com Deep Learning
Este repositório contém um pipeline completo de Machine Learning para prever o ponto de equilíbrio (VbreakEvenPoint) de tarifas de energia elétrica, utilizando dados das distribuidoras (base AneelVerdeTE e AneelAzulTE).

🚀 Visão Geral do Projeto
O objetivo deste projeto é modelar a relação complexa entre diversas variáveis tarifárias e o ponto de equilíbrio financeiro. Devido à alta colinearidade presente nos dados originais, o projeto implementa técnicas avançadas de pré-processamento para garantir a estabilidade e a precisão de uma Rede Neural Artificial (RNA).

🛠️ Tecnologias Utilizadas
Linguagem: Python 3.10+

Deep Learning: TensorFlow & Keras

Wrapper Scikit-Learn: SciKeras

Processamento de Dados: Pandas & NumPy

Redução de Dimensionalidade: Scikit-Learn (PCA)

Visualização: Matplotlib & Seaborn

🧠 Arquitetura e Pipeline
O notebook segue um fluxo rigoroso de Ciência de Dados:

Limpeza de Dados: Tratamento de valores ausentes e remoção de identificadores (Sigla, Unidade).

Engenharia de Features: Codificação One-Hot para variáveis categóricas.

Normalização: Aplicação de StandardScaler (essencial para redes neurais).

Redução de Dimensionalidade (PCA): Aplicação de Análise de Componentes Principais para manter 95% da variância, eliminando problemas de multicolinearidade.

Modelagem (Rede Neural):

Arquitetura de múltiplas camadas densas (Perceptron Multicamadas).

Função de ativação ReLU.

Otimizador Adam com taxa de aprendizado dinâmica.

Otimização: GridSearchCV para encontrar a melhor combinação de neurônios, taxa de aprendizado e tamanho de lote (batch size).

Regularização: Implementação de EarlyStopping para prevenir overfitting.


Getty Images
📊 Resultados e Avaliação
O modelo é avaliado através das métricas:

MSE (Mean Squared Error): Para penalizar grandes erros.

MAE (Mean Absolute Error): Para interpretação linear do erro médio.

R² (R-squared): Para medir a proporção da variância explicada.

O notebook também gera gráficos de:

Curvas de Aprendizado: Comparação de perda entre treino e validação.

Real vs. Previsto: Visualização da precisão do modelo.

Análise de Resíduos: Verificação da distribuição normal dos erros.

📂 Como Executar
Clone o repositório:

Bash
git clone https://github.com/seu-usuario/seu-repositorio.git
Instale as dependências:

Bash
pip install pandas numpy tensorflow scikeras scikit-learn matplotlib seaborn
Certifique-se de que os datasets (AneelAzulTECorrigido.csv ou AneelVerdeTECorrigido.csv) estejam na pasta ./dataset/.

Execute o Jupyter Notebook ou o script Python.
