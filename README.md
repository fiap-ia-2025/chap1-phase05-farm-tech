# 🌾 FarmTech Solutions - Análise de Rendimento de Safra

## 📋 Descrição do Projeto

**FarmTech Solutions** é um projeto de Machine Learning focado na análise preditiva de rendimento de safras agrícolas. Utilizando técnicas avançadas de análise de dados e modelagem estatística, o projeto visa compreender a relação entre condições ambientais e produtividade agrícola, fornecendo insights valiosos para tomada de decisões no setor agrícola.

### Contexto
O projeto foi desenvolvido para a **Fase 5 do curso de Inteligência Artificial da FIAP**, demonstrando a aplicação prática de conceitos de Machine Learning em um cenário real de agricultura de precisão. A solução analisa dados de uma fazenda de médio porte (200 hectares) que produz múltiplas culturas.

### Problema
Agricultores enfrentam desafios para prever o rendimento de safras baseado em variáveis ambientais como temperatura, umidade e precipitação. A capacidade de prever produtividade permite:
- **Otimização de recursos** (água, fertilizantes, mão de obra)
- **Planejamento financeiro** mais preciso
- **Redução de riscos** climáticos
- **Aumento da eficiência** produtiva

## 🎯 Objetivos

### Objetivo Principal
Desenvolver um sistema de **Machine Learning robusto e confiável** para previsão de rendimento de safras agrícolas, aplicando as melhores práticas de ciência de dados e engenharia de ML.

### Objetivos Específicos

#### 1. **Análise Exploratória de Dados (EDA)**
- Compreensão profunda dos padrões e distribuições dos dados
- Identificação de correlações entre variáveis ambientais
- Detecção de outliers e anomalias climáticas
- Análise da qualidade e integridade dos dados

#### 2. **Análise de Clustering e Tendências**
- Identificação de grupos naturais de condições ambientais
- Análise de tendências sazonais e padrões temporais
- Detecção de cenários climáticos discrepantes
- Segmentação de dados por tipo de cultura

#### 3. **Modelagem Preditiva Avançada**
- Desenvolvimento de **5 modelos de regressão** com algoritmos distintos
- Implementação de técnicas de feature engineering
- Validação cruzada e tuning de hiperparâmetros
- Comparação de performance entre diferentes abordagens

#### 4. **Avaliação e Validação**
- Métricas de avaliação apropriadas para problemas de regressão
- Análise de resíduos e validação de suposições
- Interpretabilidade dos modelos para stakeholders
- Documentação de limitações e pontos de melhoria

### Impacto Esperado
- **Precisão preditiva** superior a 80% para rendimento de safras
- **Redução de 15-20%** na incerteza de planejamento agrícola
- **Framework replicável** para outras regiões e culturas
- **Base científica** para decisões de agricultura de precisão

## 🚀 Status do Projeto

### ✅ Concluído
- [x] Estrutura do projeto organizada
- [x] Ambiente virtual configurado
- [x] Dependências instaladas
- [x] Dataset carregado e verificado
- [x] Análise exploratória iniciada (EDA - Parte 1)

### 🔄 Em Andamento
- [ ] Análise exploratória completa
- [ ] Análise de clustering
- [ ] Desenvolvimento dos modelos

### 📋 Pendente
- [ ] Avaliação e comparação dos modelos
- [ ] Documentação final
- [ ] Vídeo demonstrativo

## 🌱 Dataset

**Arquivo**: `crop_yield.csv`
**Variáveis**:
- **Crop**: Tipo de cultura
- **Precipitation (mm day-1)**: Precipitação diária
- **Specific Humidity at 2 Meters (g/kg)**: Umidade específica a 2m
- **Relative Humidity at 2 Meters (%)**: Umidade relativa a 2m
- **Temperature at 2 Meters (C)**: Temperatura a 2m
- **Yield**: Rendimento da safra (variável alvo)

## 🛠️ Tecnologias Utilizadas

- **Python 3.13**
- **Pandas, NumPy, Scikit-learn**
- **Matplotlib, Seaborn**
- **Jupyter Notebook**
- **Git para versionamento**

## 📁 Estrutura do Projeto

```
farm-tech-ml/
├── data/
│   ├── raw/
│   │   └── crop_yield.csv          # Dataset original
│   └── processed/                  # Dados processados
├── notebooks/
│   └── crop_yield_analysis.ipynb  # Notebook principal
├── src/                           # Código Python
├── models/                        # Modelos treinados
├── results/                       # Resultados e métricas
├── plots/                         # Gráficos e visualizações
├── venv/                          # Ambiente virtual
├── requirements.txt               # Dependências
└── README.md                      # Documentação
```

## 🚀 Como Executar

1. **Clone o repositório**
```bash
git clone [URL_DO_REPOSITORIO]
cd farm-tech-ml
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

4. **Execute o Jupyter**
```bash
cd notebooks
jupyter notebook
```

## 👥 Equipe

- [Seu Nome] - RM [Seu RM]
- [Nome do Colega] - RM [RM do Colega]
- [Nome do Colega] - RM [RM do Colega]

## 📚 Notebooks

- **`crop_yield_analysis.ipynb`**: Análise principal (em desenvolvimento)

## 🔍 Análises Realizadas

### EDA - Parte 1: Análise Univariada ✅
- ✅ Distribuição das culturas
- ✅ Análise de equilíbrio dos dados
- ✅ Visualizações (gráficos de barras e pizza)
- ✅ Verificação de qualidade dos dados

## 📊 Próximos Passos

1. **Completar EDA** com análise de variáveis numéricas
2. **Implementar clustering** para identificar tendências
3. **Desenvolver 5 modelos** de regressão
4. **Avaliar performance** e comparar resultados

## 📝 Licença

Este projeto é desenvolvido para fins educacionais no curso de IA da FIAP.

---

**Última atualização**: 27/08/2024
**Versão**: 0.1.0
**Status**: EDA em andamento
