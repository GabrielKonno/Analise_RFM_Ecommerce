# 📊 Análise de Dados e Segmentação de Clientes com RFM

## 💡 Sobre o Projeto
Este projeto implementa uma análise completa de dados e segmentação de clientes utilizando a metodologia RFM (Recency, Frequency, Monetary). O objetivo é identificar padrões de comportamento dos clientes e criar segmentos para ações de marketing personalizadas, permitindo uma abordagem mais estratégica no relacionamento com clientes.

## 🎯 Objetivos do Projeto
1. Limpeza e pré-processamento de dados:

- Remoção de dados inconsistentes, duplicados e irrelevantes.
- Tratamento de valores ausentes e outliers.
- Conversão de tipos de dados para otimizar análises.

2. Criação de análises descritivas:

- Identificação de padrões de vendas por país, produto e período.
- Visualização de tendências de vendas.

3. Implementação do modelo RFM:

- Cálculo de métricas de Recência (R), Frequência (F) e Valor Monetário (M).
- Segmentação de clientes com base nas métricas RFM.
- Geração de insights estratégicos para ações de marketing.

## 🛠 Tecnologias Utilizadas
- Python 3.x
- Pandas e NumPy para manipulação de dados
- Matplotlib e Seaborn para visualizações
- Pandas Profiling para relatórios descritivos

## 📋 Passos Realizados

### 1. Limpeza e Pré-Processamento dos Dados
- **Tratamento de valores ausentes e inválidos**:
  - Remoção de linhas sem `CustomerID` (25% dos dados)
  - Manutenção de cancelamentos (InvoiceNo com "C")
  - Remoção de valores inválidos em UnitPrice
- **Remoção de duplicatas**:
  - Identificação e exclusão de 4.879 linhas duplicadas
- **Conversão de tipos de dados**:
  - `InvoiceDate` → datetime
  - Ajuste de colunas categóricas e numéricas
- **Criação de métricas derivadas**:
  - `TotalPrice` = `Quantity * UnitPrice`
  - Marcação de transações de cancelamento

### 2. Análises Descritivas
- **Exploração de Outliers**
  - Identificação e tratamento de valores extremos
  - Análise de cancelamentos e devoluções
- **Visualizações Principais**:
  - Top 10 países por valor de vendas
  - Produtos mais vendidos
  - Tendências mensais de vendas
  - Análise comparativa por região

### 3. Segmentação RFM
- **Cálculo das Métricas**:
  - **Recency**: Dias desde última compra
  - **Frequency**: Número de compras
  - **Monetary**: Valor médio gasto
- **Sistema de Pontuação**:
  - Escores de 1-5 baseados em quartis
  - Combinação de scores para segmentação

## 📈 Interpretação dos Scores RFM

| Score | Percentil | Significado |
|-------|-----------|-------------|
| 5 | 80-100% | Excelente |
| 4 | 60-80% | Acima da média |
| 3 | 40-60% | Média |
| 2 | 20-40% | Abaixo da média |
| 1 | 0-20% | Necessita atenção |

### Segmentos Principais
- **555**: Clientes Premium
- **111**: Clientes que Precisam de Atenção
- Outras combinações indicam níveis intermediários

## 🚀 Como Executar

1. Clone o repositório
```bash
git clone https://github.com/seu-usuario/nome-do-repo.git
```

2. Instale as dependências
```bash
pip install -r requirements.txt
```

3. Execute o script principal
```bash
python rfm_analysis.py
```

## 📁 Estrutura do Projeto
```
.
├── data/
│   └── data.csv
├── notebooks/
│   └── analise_rfm.ipynb
├── output/
│   └── rfm_output.csv
├── requirements.txt
└── README.md
```

## 📊 Resultados e Insights
- Métricas RFM calculadas e exportadas para `rfm_output.csv`
- Identificação de padrões de compra por segmento
- Base para estratégias de marketing personalizado
- Visualizações detalhadas de tendências de vendas

## 🤝 Contribuições
Contribuições são bem-vindas! Para contribuir:

1. Faça um Fork
2. Crie uma Branch (`git checkout -b feature/NovaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona NovaFeature'`)
4. Push para a Branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

## 👤 Autor
* **Seu Nome** - [SeuGitHub](https://github.com/GabrielKonno)
