# 📊 Python Insights – Análise de Cancelamento de Clientes (Churn)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)

> Projeto de análise de dados que investiga os principais motivos de cancelamento em uma base com mais de 800 mil clientes, propondo ações para reduzir o churn.

---

## 🎯 Sobre o Projeto

Uma empresa com mais de **800 mil clientes** percebeu que a maioria da sua base estava inativa — ou seja, já havia cancelado o serviço. Precisando melhorar seus resultados, ela contratou uma análise para entender **os principais motivos dos cancelamentos** e **quais ações seriam mais eficientes** para reduzir esse número.

Este projeto resolve esse problema aplicando **análise exploratória de dados** com Python, identificando padrões e propondo soluções baseadas em evidências.

---

## 🛠️ Tecnologias Utilizadas

- **Python 3** – Linguagem principal
- **Pandas** – Leitura, tratamento e manipulação dos dados
- **Plotly Express** – Visualizações interativas
- **Jupyter Notebook / VS Code** – Ambiente de desenvolvimento

---

## 📁 Estrutura do Projeto
hashtag_aula_2-analise_de_dados/ <br/>
├── inicial.ipynb # Notebook com a análise completa <br/>
├── cancelamentos.csv # Base de dados <br/>
└── README.md # Documentação do projeto <br/>

---

## 🔍 Etapas da Análise

### 1️⃣ Tratamento de Dados
- Remoção da coluna `CustomerID` (irrelevante para a análise).
- Eliminação de valores nulos com `dropna()`.

### 2️⃣ Análise Exploratória
- Contagem e proporção de cancelamentos.
- Criação de **histogramas interativos** com Plotly para cada variável, coloridos pela coluna `cancelou`.

### 3️⃣ Identificação dos Principais Fatores

| Fator | Insight |
|-------|---------|
| 📅 **Contrato Mensal** | 100% dos clientes com contrato `Monthly` cancelaram |
| 📞 **Ligações ao Call Center** | Clientes que ligaram mais de 4 vezes cancelaram |
| 💸 **Atraso no Pagamento** | Clientes com mais de 20 dias de atraso cancelaram |

**Taxa geral de cancelamento:** `56%`

### 4️⃣ Aplicação de Filtros
Com base nos insights, foram aplicados filtros para simular uma base "saudável":
- ❌ Removidos clientes com contrato `Monthly`
- ✅ Mantidos clientes com até **4 ligações** no call center
- ✅ Mantidos clientes com até **20 dias** de atraso

---

## 📈 Resultado

Após a aplicação dos filtros, a **taxa de cancelamento caiu para 18%**, comprovando que os três fatores identificados são os principais responsáveis pelo churn.

---

## 💡 Ações Sugeridas

| Ação | Objetivo |
|------|----------|
| 🎁 **Desconto para migração** | Incentivar clientes mensais a migrarem para planos anuais |
| 🚨 **Alerta vermelho no call center** | Acionar equipe especializada quando o cliente ligar mais de 3 vezes |
| ⏰ **Alerta de atraso** | Acionar time de retenção para clientes com atraso acima de 15 dias |

---

## 🚀 Como Executar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/Sotnaslegit/hashtag_aula_2-analise_de_dados.git

2. **Instale as dependências:**
   ```bash
   pip install pandas plotly

3. **Abra o notebook:**
   * No VS Code, abra o arquivo inicial.ipynb.
   * Ou rode no Jupyter Notebook:
     ```bash
     jupyter notebook inicial.ipynb

4. **Execute as células** em ordem para reproduzir a análise completa.
