# 🌾 FarmTech Solutions - Análise de Rendimento de Safra

## 📋 Descrição do Projeto

**FarmTech Solutions** é um projeto de Machine Learning desenvolvido para a **Fase 5 do curso de Inteligência Artificial da FIAP**. O projeto analisa dados agrícolas para prever rendimento de safras baseado em condições ambientais, aplicando técnicas de análise exploratória, clustering e modelagem preditiva.

### Contexto Acadêmico
- **Curso**: Inteligência Artificial - FIAP
- **Fase**: 5 (Projeto Final)
- **Objetivo**: Demonstrar aplicação prática de ML em agricultura de precisão
- **Dataset**: 156 registros de 4 culturas (Cocoa, Oil palm, Rice, Rubber)

## 🎯 Objetivos do Projeto

### Objetivo Principal
Desenvolver um sistema de **Machine Learning robusto** para previsão de rendimento de safras agrícolas, seguindo as melhores práticas de ciência de dados.

### Objetivos Específicos
1. **Análise Exploratória (EDA)**: Compreender padrões e distribuições dos dados
2. **Análise de Clustering**: Identificar grupos naturais e tendências de produtividade
3. **Modelagem Preditiva**: Desenvolver 5 modelos de regressão distintos
4. **Avaliação e Validação**: Comparar performance e selecionar melhor modelo

## 🚀 Status do Projeto

### ✅ Concluído
- [x] **Análise Exploratória de Dados (EDA)**
- [x] **Preparação de Dados para ML**
- [x] **Análise de Clustering**

### 🔄 Em Andamento
- [ ] **Modelagem Preditiva (5 algoritmos)**

### 📋 Pendente
- [ ] **Avaliação e Comparação dos Modelos**
- [ ] **Documentação Final**
- [ ] **Vídeo Demonstrativo**

## 🌱 Dataset

**Arquivo**: `crop_yield.csv` (156 registros)

**Variáveis**:
- **Crop**: Tipo de cultura (Cocoa, Oil palm, Rice, Rubber)
- **Precipitation**: Precipitação diária (mm/dia)
- **Specific Humidity**: Umidade específica a 2m (g/kg)
- **Relative Humidity**: Umidade relativa a 2m (%)
- **Temperature**: Temperatura a 2m (°C)
- **Yield**: Rendimento da safra (ton/ha) - **Variável Alvo**

## 📁 Estrutura do Projeto

```
chap1-phase05-farm-tech/
├── data/
│   ├── raw/
│   │   └── crop_yield.csv          # Dataset original
│   └── processed/
│       └── dataset_ready.csv      # Dataset processado (18 features)
├── models/
│   └── scaler.pkl                 # Scaler para normalização
├── notebooks/
│   ├── 01_eda.ipynb               # Análise Exploratória
│   ├── 02_data_preparation.ipynb  # Preparação de Dados
│   └── 03_clustering.ipynb        # Análise de Clustering
├── requirements.txt               # Dependências Python
└── README.md                      # Documentação
```

## 🔍 Análises Realizadas

### 1. Análise Exploratória (EDA) ✅
**Descobertas Principais**:
- **Yield bimodal por cultura**: Oil palm (~175k), Rice (~32k), Cocoa/Rubber (~8k)
- **Correlações ambientais**: Variáveis climáticas correlacionadas entre si
- **Qualidade dos dados**: 0 valores faltantes, sem duplicatas
- **Distribuições**: Dados bem distribuídos, sem outliers significativos

### 2. Preparação de Dados ✅
**Transformações Aplicadas**:
- **Feature Engineering**: 9 novas features criadas (interações, índices climáticos)
- **One-Hot Encoding**: Variável 'Crop' transformada em 4 dummies
- **Normalização**: 13 features padronizadas (StandardScaler)
- **Dataset final**: 18 features prontas para ML

### 3. Análise de Clustering ✅
**Algoritmos Testados**:
- **K-means**: 2 clusters baseados em condições ambientais (Silhouette=0.401)
- **DBSCAN**: Não conseguiu formar clusters com parâmetros padrão
- **Hierárquico**: 45 clusters com fragmentação excessiva (Silhouette=0.356)

**Conclusões**:
- **Tipo de cultura é determinante principal** do Yield
- **Clustering global não é adequado** para identificar tendências
- **Modelagem preditiva é mais eficaz** que clustering para este problema

## 🛠️ Tecnologias Utilizadas

- **Python 3.13**
- **Pandas, NumPy**: Manipulação de dados
- **Scikit-learn**: Algoritmos de ML e clustering
- **Matplotlib, Seaborn**: Visualizações
- **Jupyter Notebook**: Ambiente de desenvolvimento

## 🚀 Como Executar

1. **Clone o repositório**
```bash
git clone [URL_DO_REPOSITORIO]
cd chap1-phase05-farm-tech
```

2. **Configure o ambiente virtual**
```bash
python3 -m venv venv
source venv/bin/activate  # macOS/Linux
```

3. **Instale as dependências**
```bash
pip install -r requirements.txt
```

4. **Execute os notebooks**
```bash
cd notebooks
jupyter notebook
```

## 👥 Equipe

- [Seu Nome] - RM [Seu RM]
- [Nome do Colega] - RM [RM do Colega]
- [Nome do Colega] - RM [RM do Colega]

## 🔍 Análises Realizadas

### EDA Completa ✅
- ✅ **Análise Univariada**: Distribuições e características individuais
- ✅ **Análise Bivariada**: Correlações e relacionamentos entre variáveis
- ✅ **Análise Multivariada**: Padrões complexos e interações
- ✅ **Descobertas principais**: Yield bimodal por cultura, correlações ambientais

### Preparação de Dados ✅
- ✅ **Análise de outliers**: 0 outliers reais detectados
- ✅ **Feature Engineering**: 9 novas features criadas
- ✅ **One-Hot Encoding**: Variável 'Crop' transformada
- ✅ **Normalização**: 13 features padronizadas
- ✅ **Dataset final**: 18 features prontas para ML

## 📊 Próximos Passos

2. **Desenvolver 5 modelos** de regressão
3. **Avaliar performance** e comparar resultados
4. **Documentação final** e vídeo demonstrativo

## 📝 Licença

Este projeto é desenvolvido para fins educacionais no curso de IA da FIAP.

---

**Última atualização**: 04/09/2024  
**Versão**: 0.3.0  
**Status**: EDA, preparação de dados e clustering concluídos