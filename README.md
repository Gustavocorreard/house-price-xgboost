# 🏡 Previsão de Preços de Casas com XGBoost

Este projeto tem como objetivo prever o **preço de venda de imóveis residenciais** com base em suas características estruturais e localização. A modelagem foi feita com o algoritmo **XGBoost**, uma das técnicas de regressão mais eficazes para problemas com dados tabulares.

---

## 📊 Dataset

- **Fonte**: [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data)
- **Amostras**: 1.460 registros de imóveis
- **Atributos**: Mais de 70 colunas com informações como:
  - Área útil da casa (`GrLivArea`)
  - Número de banheiros (`FullBath`)
  - Qualidade geral (`OverallQual`)
  - Ano de construção (`YearBuilt`)
  - Localização (bairro) e muito mais

---

## 🚀 Técnicas Utilizadas

- Análise Exploratória de Dados (EDA)
- Tratamento de valores ausentes
- Engenharia de atributos temporais
- Codificação de variáveis categóricas com One-Hot Encoding
- Algoritmo de regressão **XGBoost**
- Avaliação com métricas: MAE, RMSE e R²
- Interpretação com gráfico de importância das variáveis
- **Simulação prática** de precificação de um imóvel

---

## 🧪 Resultados do Modelo

- **R²**: 0.92 → O modelo explica 92% da variância do preço
- **MAE**: US$ 16.016 → Erro médio absoluto
- **RMSE**: US$ 25.248 → Erro médio com penalização para outliers

> O modelo apresenta ótimo desempenho e pode ser utilizado em contextos reais para **precificação inteligente de imóveis**.

---

## 🧠 Principais Variáveis

As variáveis mais influentes foram:

- `OverallQual`: Qualidade geral da construção
- `GrLivArea`: Área útil acima do solo
- `TotalBsmtSF`: Tamanho total do porão
- `GarageCars`: Número de vagas de garagem
- `YearBuilt`: Ano de construção

---

## 📸 Visualizações

### 📈 Comparação Real vs Previsto

![Comparação](images/real_vs_pred.png)

### 🔍 Importância das Variáveis

![Importância](images/top_20_features.png)

---

## 🧪 Simulação Prática

Criamos uma simulação para prever o valor de uma nova casa com as seguintes características:

- Qualidade geral: 7  
- Área útil: 2200 pés²  
- Garagem: 2 carros  
- Porão: 1000 pés²  
- Ano de construção: 2005  
- Banheiros: 2  
- Bairro: NridgHt

📌 **Preço estimado pelo modelo: US$ 289.000**

Essa simulação mostra como o modelo pode ser usado para **estimar o valor de novos imóveis** com base em atributos conhecidos.

---

## 🧰 Como Executar

```bash
git clone https://github.com/seu-usuario/house-price-xgboost.git
cd house-price-xgboost
pip install -r requirements.txt
jupyter notebook
