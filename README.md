# FIAP - Faculdade de Informática e Administração Paulista

<p align="center">
  <a href="https://www.fiap.com.br/">
    <img src="img/logo-fiap.png" alt="FIAP - Faculdade de Informática e Administração Paulista" border="0" width="80%" height="40%">
  </a>
</p>

## 👥 Grupo 21

## 👨‍🎓 Integrantes:

- Amanda Vieira Pires (RM565045)
- Ana Gabriela Soares Santos (RM565235)
- Bianca Nascimento de Santa Cruz Oliveira (RM561390)
- Milena Pereira dos Santos Silva (RM565464)
- Nayana Mehta Miazaki (RM565045)

## 👩‍🏫 Professores:

### Tutor(a)

- Lucas Gomes Moreira

### Coordenador(a)

- André Godoi

---

# 🌾 FarmTech Solutions - Projeto de IA para Agricultura

## 📋 Sobre o Projeto

O **FarmTech Solutions** é um projeto de Inteligência Artificial desenvolvido para a **Fase 5 do curso de Inteligência Artificial da FIAP**. O projeto visa analisar dados agrícolas de uma fazenda de médio porte (200 hectares) para prever rendimento de safras e identificar tendências de produtividade.

### 🎯 Objetivos

- **Análise Exploratória**: Compreender padrões nos dados agrícolas
- **Clustering**: Identificar grupos naturais de produtividade e detectar outliers
- **Modelagem Preditiva**: Desenvolver 5 modelos de regressão para prever Yield
- **Validação**: Avaliar performance dos modelos com métricas robustas

### 📊 Dataset

**Arquivo**: `crop_yield.csv`
**Registros**: 156 observações
**Culturas**: 4 tipos (Cocoa, Oil palm fruit, Rice paddy, Rubber)
**Variáveis**:
- **Crop**: Tipo de cultura
- **Precipitation**: Precipitação (mm/dia)
- **Specific Humidity**: Umidade específica (g/kg)
- **Relative Humidity**: Umidade relativa (%)
- **Temperature**: Temperatura (°C)
- **Yield**: Rendimento (toneladas/hectare)

## 🏗️ Estrutura do Projeto

```
chap1-phase05-farm-tech/
├── data/
│   ├── raw/
│   │   └── crop_yield.csv          # Dataset original
│   └── processed/
│       └── dataset_ready.csv       # Dataset processado
├── models/
│   └── scaler.pkl                  # Scaler salvo
├── notebooks/
│   ├── 01_eda.ipynb               # Análise Exploratória
│   ├── 02_data_preparation.ipynb  # Preparação dos Dados
│   ├── 03_clustering.ipynb        # Análise de Clustering
│   └── 04_modelos.ipynb           # Modelagem Preditiva
├── requirements.txt               # Dependências
└── README.md                      # Este arquivo
```

## 🔄 Pipeline de Machine Learning

### Fluxo do Projeto

```
📊 Dataset Original → 🔍 EDA → 🛠️ Preparação → 🔗 Clustering → 🤖 Modelagem → 📊 Validação → 🏆 Modelo Final
```

### Etapas Principais

**1. 📊 Dados** (156 registros, 4 culturas)

**2. 🔍 EDA** (Yield bimodal por cultura)

**3. 🛠️ Preparação** (12 features: 4 originais + 4 criadas + 4 dummies)

**4. 🔗 Clustering** (K-means, DBSCAN, Hierárquico)

**5. 🤖 Modelagem** (5 algoritmos: Linear, Random Forest, XGBoost, SVR, Neural)

**6. 📊 Validação** (5-fold CV, R², RMSE, MAE)

**7. 🏆 Seleção** (Random Forest: R² = 0.988)

### Critérios de Qualidade

**✅ Atendidos:**
- Reprodutibilidade (random_state=42)
- Validação robusta (5-fold CV)
- Métricas múltiplas (R², RMSE, MAE)
- Interpretabilidade (feature importance)

**⚠️ Limitações:**
- Heterocedasticidade nos resíduos
- Não-normalidade dos resíduos

## 📝 Metodologia

### 1. **Análise Exploratória (EDA)**
- Estatísticas descritivas
- Distribuições das variáveis
- Correlações entre features
- Análise por tipo de cultura

### 2. **Preparação dos Dados**
- One-hot encoding para variáveis categóricas
- Feature engineering (4 features derivadas)
- Normalização dos dados
- Validação da qualidade

### 3. **Clustering**
- K-means clustering
- DBSCAN clustering
- Clustering hierárquico
- Análise de tendências

### 4. **Modelagem Preditiva**
- 5 algoritmos de regressão
- Validação cruzada 5-fold
- Análise de resíduos
- Feature importance

## 🚀 Como Executar

### 1. **Pré-requisitos**

- Python 3.8+
- Jupyter Notebook
- Git

### 2. **Instalação**

```bash
# Clone o repositório
git clone https://github.com/fiap-ia-2025/chap1-phase4-agricultural-machine

# Entre no diretório
cd chap1-phase05-farm-tech

# Crie um ambiente virtual
python -m venv venv

# Ative o ambiente virtual
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

# Instale as dependências
pip install -r requirements.txt
```

### 3. **Execução**

```bash
# Inicie o Jupyter Notebook
jupyter notebook

# Execute os notebooks na ordem:
# 1. 01_eda.ipynb
# 2. 02_data_preparation.ipynb
# 3. 03_clustering.ipynb
# 4. 04_modelos.ipynb
```

## 🛠️ Tecnologias e Dependências

### Tecnologias Utilizadas

- **Python 3.8+**
- **Pandas**: Manipulação de dados
- **NumPy**: Operações numéricas
- **Scikit-learn**: Algoritmos de ML
- **XGBoost**: Gradient boosting
- **TensorFlow/Keras**: Neural networks
- **Matplotlib/Seaborn**: Visualizações
- **Jupyter Notebook**: Ambiente de desenvolvimento

### Dependências

```
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
xgboost>=1.5.0
tensorflow>=2.8.0
matplotlib>=3.5.0
seaborn>=0.11.0
jupyter>=1.0.0
```

## 🏆 Resultados Principais

### 🏆 Modelo Final Escolhido: Random Forest

**Performance:**
- **R² = 0.988**: Explica 98.8% da variância
- **RMSE = 3,291 ton/ha**: Erro médio aceitável
- **MAE = 1,866 ton/ha**: Erro absoluto baixo

**Robustez:**
- **Overfitting = 0.010**: Controlado
- **Estabilidade = 0.007**: Alta consistência

### 📊 Insights Principais

**Top 5 Features Mais Importantes:**
1. **Crop_Oil palm fruit**: Maior impacto no modelo
2. **Crop_Rice, paddy**: Segundo maior impacto
3. **Temperature at 2 Meters (C)**: Fator climático mais importante
4. **Precipitation (mm day-1)**: Segundo fator climático
5. **Crop_Cocoa, beans**: Terceiro tipo de cultura

**Categorização por Importância:**
- **Features Dummies (Culturas)**: ~60% da importância total
- **Features Originais (Climáticas)**: ~30% da importância total
- **Features Criadas (Derivadas)**: ~10% da importância total

### ⚠️ Limitações Identificadas

- **Heterocedasticidade**: Modelo menos preciso para Yield alto
- **Não-normalidade**: Resíduos não seguem distribuição normal
- **Padrão sistemático**: Erros não são completamente aleatórios

## 🎯 Conclusões

O projeto **FarmTech Solutions** demonstra que modelos preditivos podem apoiar significativamente a tomada de decisão agrícola, auxiliando no aumento da produtividade e na redução de riscos climáticos.

**Random Forest** foi escolhido como modelo final, oferecendo alta performance preditiva (98.8% de variância explicada) e interpretabilidade adequada, apesar das limitações identificadas nos resíduos.

## 📞 Contato

Para dúvidas ou sugestões sobre o projeto, entre em contato com o Grupo 21.

---

**Desenvolvido para a FIAP - Faculdade de Informática e Administração Paulista**