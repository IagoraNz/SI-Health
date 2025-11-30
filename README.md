# 🏥 SI-Health: Predição de Insuficiência Cardíaca

![Status do Projeto](https://img.shields.io/badge/Status-Concluído-green)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

Este repositório contém o trabalho final da disciplina de **Sistemas Inteligentes**, focado na análise e classificação de dados clínicos para predição de mortalidade por insuficiência cardíaca.

## 📄 Sobre o projeto

O objetivo deste projeto é desenvolver modelos de aprendizado de máquina capazes de prever a mortalidade de pacientes com insuficiência cardíaca com base em seus registros clínicos.

O projeto utiliza o dataset **Heart Failure Clinical Records**, obtido do repositório da UCI Machine Learning.

### 🎯 Objetivos específicos
- Realizar análise exploratória dos dados.
- Pré-processar os dados (codificação de variáveis categóricas, normalização).
- Implementar e comparar algoritmos de classificação:
    - **K-Nearest Neighbors (KNN)**
    - **Naive Bayes (Gaussian)**
- Avaliar os modelos utilizando Validação Cruzada (Stratified K-Fold).

## 📊 Dataset

O conjunto de dados contém 299 registros e 12 atributos clínicos, além da variável alvo (`DEATH_EVENT`).

- **Fonte:** [UCI Machine Learning Repository - ID 519](https://archive.ics.uci.edu/dataset/519/heart+failure+clinical+records)
- **Atributos:** Idade, Anemia, Creatinina Fosfoquinase, Diabetes, Fração de Ejeção, Pressão Alta, Plaquetas, Creatinina Sérica, Sódio Sérico, Sexo, Tabagismo, Tempo de Acompanhamento.

## 🛠️ Tecnologias utilizadas

O projeto foi desenvolvido em **Python** utilizando Jupyter Notebook. As principais bibliotecas são:

- **Pandas** & **Numpy**: Manipulação e análise de dados.
- **Matplotlib** & **Seaborn**: Visualização de dados.
- **Scikit-Learn**: Construção de modelos de ML e métricas de avaliação.
- **UCIMLRepo**: Importação direta do dataset.

## 🚀 Como executar

### Pré-requisitos
Certifique-se de ter o Python instalado. É recomendado usar um ambiente virtual.

### Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/SI-Health.git
   cd SI-Health
   ```

2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

3. Execute o Jupyter Notebook:
   ```bash
   jupyter notebook src/main.ipynb
   ```

## 📈 Resultados

Os modelos foram avaliados utilizando validação cruzada (5-fold). Abaixo um resumo comparativo das métricas médias obtidas:

| Modelo | Acurácia | F1-Score | Precision | Recall | ROC AUC |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Naive Bayes** | **77.59%** | **0.5745** | 0.7443 | **0.4689** | **0.8515** |
| **KNN (K=11)** | 74.92% | 0.4057 | **0.8333** | 0.2711 | 0.8092 |

> **Conclusão:** O modelo **Naive Bayes** apresentou um desempenho geral superior, especialmente na métrica ROC AUC e Recall, indicando uma melhor capacidade de generalização e identificação dos casos positivos em comparação ao KNN.

## 📂 Estrutura do repositório

```
📂SI-Health/
├── 📂 src/
│   └── 🐍 main.ipynb      # Notebook principal com todo o código do projeto
├── 📄requirements.txt     # Lista de dependências do projeto
├── 📝 LICENSE             # Licença de uso
└── 📄 README.md           # Documentação do projeto
```

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
