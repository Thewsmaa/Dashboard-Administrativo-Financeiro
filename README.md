# 📊 Dashboard Administrativo e Financeiro — Excel & Power BI

Projeto de análise de dados desenvolvido utilizando **Microsoft Excel e Power BI**, com o objetivo de transformar dados operacionais e financeiros em informações úteis para acompanhamento de resultados e apoio à tomada de decisão.

O projeto simula um cenário empresarial no qual é necessário acompanhar faturamento, pagamentos, valores em aberto, inadimplência, clientes, departamentos, categorias e evolução mensal da receita.

---

## 🎯 Objetivo

Desenvolver uma solução de análise administrativa e financeira capaz de fornecer uma visão clara dos principais indicadores da organização.

O projeto busca responder perguntas como:

- Qual é o faturamento total?
- Quanto já foi pago?
- Quanto ainda está em aberto?
- Qual o valor em atraso?
- Qual é a taxa de inadimplência?
- Como o faturamento evolui ao longo dos meses?
- Quais departamentos apresentam maior faturamento?
- Quais clientes possuem maior participação na receita?
- Quais clientes concentram maior valor em atraso?
- Quais categorias possuem maior representatividade?
- Quais formas de pagamento são mais utilizadas?

---

## 🛠️ Tecnologias e Ferramentas

- Microsoft Excel
- Power Query
- Power BI Desktop
- DAX
- Tabelas Dinâmicas
- Git
- GitHub

---

## 📚 Conceitos Aplicados

Durante o desenvolvimento foram aplicados conceitos de:

- Tratamento e organização de dados
- Limpeza e padronização de informações
- Análise exploratória de dados
- Fórmulas do Excel
- Tabelas Dinâmicas
- Visualização de dados
- Power Query
- Modelagem de dados
- Relacionamentos entre tabelas
- Dimensão calendário
- Medidas DAX
- Indicadores de desempenho (KPIs)
- Análise temporal
- Segmentação de dados
- Dashboard interativo
- Storytelling com dados
- UX para dashboards

---

# 🔄 Processo de Desenvolvimento

## 1. Preparação dos Dados

Inicialmente foi criada e estruturada uma base contendo informações relacionadas às operações da empresa.

Entre os principais campos estão:

- Nota Fiscal
- Data da operação
- Cliente
- Departamento
- Categoria
- Valor da operação
- Forma de pagamento
- Responsável
- Prazo
- Data de vencimento
- Status
- Data de pagamento
- Valor pago
- Valor em aberto
- Dias de atraso

---

## 2. Análise no Excel

O Excel foi utilizado como primeira etapa de exploração e análise dos dados.

Foram desenvolvidos:

- Indicadores financeiros
- Fórmulas para consolidação dos dados
- Análises por departamento
- Análises por status
- Análises por cliente
- Análises mensais
- Tabelas Dinâmicas
- Gráficos
- Dashboard administrativo e financeiro

Essa etapa permitiu explorar e validar a estrutura dos dados antes da construção do modelo no Power BI.

---

## 3. Tratamento com Power Query

A base foi posteriormente importada para o Power BI e submetida a processos de tratamento utilizando o Power Query.

Entre os procedimentos realizados estão:

- Verificação dos tipos de dados
- Padronização de campos
- Limpeza de textos
- Remoção de espaços desnecessários
- Organização das colunas
- Preparação dos dados para modelagem

O objetivo dessa etapa foi garantir maior consistência e qualidade para as análises posteriores.

---

# 🧩 Modelagem de Dados

Foi criada uma tabela calendário para permitir análises temporais mais eficientes.

### Tabela Calendário

A dimensão calendário contém informações como:

- Data
- Ano
- Mês
- Número do mês
- Ano-Mês

Foi estabelecido um relacionamento entre:

`Calendario[Date]`

e

`Base_Dados[Data]`

Essa estrutura permite realizar análises temporais e utilizar funções de inteligência de tempo no DAX.

---

# 🧮 Medidas DAX

Foram desenvolvidas medidas DAX para criação dos principais indicadores financeiros, operacionais e temporais do projeto.

Entre os principais indicadores estão:

- Receita Total
- Valor Pago
- Valor em Aberto
- Valor em Atraso
- Quantidade de Operações
- Operações em Atraso
- Ticket Médio
- Taxa de Inadimplência
- Percentual da Receita Paga
- Percentual da Receita em Aberto
- Percentual da Receita em Atraso
- Clientes Ativos
- Receita Média por Cliente
- Receita do Mês Anterior
- Crescimento Mensal

As medidas DAX utilizadas no projeto estão documentadas separadamente:

👉 **[Ver documentação das medidas DAX](Medidas_DAX.md)**

---

# 📊 Dashboard Executivo

O Dashboard Executivo foi desenvolvido para fornecer uma visão geral dos principais indicadores da organização.

### Principais indicadores

- Receita Total
- Valor Pago
- Valor em Aberto
- Valor em Atraso
- Quantidade de Operações
- Ticket Médio
- Taxa de Inadimplência
- Crescimento Mensal
- Clientes Ativos

### Principais análises

- Evolução da receita mensal
- Receita por departamento
- Distribuição da receita por status
- Top 5 clientes por receita
- Receita por categoria
- Receita por forma de pagamento

### Interatividade

O dashboard possui segmentações de dados para permitir análises por:

- Período
- Departamento
- Status
- Categoria
- Responsável

---

# 💰 Análise Financeira

A página de análise financeira foi desenvolvida para permitir uma visão mais detalhada da situação financeira.

Entre os principais pontos analisados estão:

- Receita total
- Valores pagos
- Valores em aberto
- Valores em atraso
- Percentual pago
- Percentual em aberto
- Percentual em atraso
- Evolução da receita
- Receita por status
- Clientes com maior valor em atraso

O objetivo é facilitar a identificação de pontos de atenção e apoiar o acompanhamento financeiro.

---

# 👥 Análise de Clientes

A página de análise de clientes permite avaliar a concentração da receita e identificar clientes relevantes para o negócio.

São analisados:

- Clientes ativos
- Receita por cliente
- Receita média por cliente
- Top 5 clientes
- Valor em atraso por cliente
- Categorias associadas aos clientes

Essa análise pode auxiliar na identificação de clientes estratégicos e possíveis riscos relacionados à concentração ou inadimplência.

---

# 📸 Visualizações

## Dashboard Executivo

![Dashboard Executivo](Imagens/dashboard-executivo.png)

---

## Análise Financeira

![Análise Financeira](Imagens/analise-financeira.png)

---

## Análise de Clientes

![Análise de Clientes](Imagens/analise-clientes.png)

---

# 💡 Insights

A análise permite identificar diferentes aspectos relevantes da operação, como:

- Evolução do faturamento ao longo do período analisado;
- Departamentos com maior participação na receita;
- Clientes responsáveis pela maior concentração do faturamento;
- Distribuição da receita entre valores pagos, em aberto e em atraso;
- Categorias com maior representatividade financeira;
- Formas de pagamento mais utilizadas;
- Clientes que concentram maior valor em atraso;
- Evolução dos indicadores financeiros ao longo do tempo.

> **Observação:** os insights quantitativos podem ser explorados diretamente no dashboard por meio dos filtros e segmentações disponíveis.

---

# 📈 Storytelling com Dados

O dashboard foi estruturado seguindo uma sequência de análise orientada ao negócio:

### 1. Resultado

**Quanto a empresa movimentou?**

→ Receita Total

### 2. Recebimento

**Quanto já foi recebido?**

→ Valor Pago

### 3. Pendências

**Quanto ainda precisa ser recebido?**

→ Valor em Aberto

### 4. Risco

**Quanto está atrasado?**

→ Valor em Atraso e Inadimplência

### 5. Tendência

**Como o faturamento está evoluindo?**

→ Evolução Mensal e Crescimento

### 6. Concentração

**Quem gera maior receita?**

→ Top Clientes

### 7. Operação

**Onde está concentrada a receita?**

→ Departamentos e Categorias

---

# 🎨 Design e UX

O dashboard foi desenvolvido buscando priorizar:

- Clareza das informações
- Hierarquia visual
- Consistência entre indicadores
- Facilidade de navegação
- Interatividade
- Redução de elementos visuais desnecessários
- Destaque para indicadores relevantes
- Utilização de cores com significado

A organização visual foi pensada para permitir que o usuário encontre rapidamente as principais informações e posteriormente explore os dados de forma mais detalhada.

---

# 📚 Principais Aprendizados

O desenvolvimento do projeto permitiu colocar em prática conhecimentos relacionados a:

- Excel
- Power Query
- Power BI
- DAX
- Modelagem de dados
- Tratamento de dados
- Análise financeira
- Indicadores de desempenho
- Visualização de dados
- Storytelling
- UX de dashboards
- Organização de projetos
- Documentação de análises

Além do conhecimento técnico, o projeto reforçou a importância de compreender o **problema de negócio antes da criação das visualizações**.

---

# 📁 Estrutura do Projeto

```text
dashboard-administrativo-financeiro/
│
├── Excel/
│   └── Dashboard_Administrativo_Financeiro.xlsx
│
├── PowerBI/
│   └── Dashboard_Administrativo_Financeiro.pbix
│
├── Imagens/
│   ├── dashboard-executivo.png
│   ├── analise-financeira.png
│   └── analise-clientes.png
│
├── Documentacao/
│   ├── Dicionario_de_Dados.xlsx
│   └── Medidas_DAX.md
│
└── README.md
```

---

# 🔎 Considerações

Este projeto possui finalidade **educacional e de portfólio**.

Os dados utilizados representam um cenário empresarial fictício e foram utilizados exclusivamente para demonstrar processos de tratamento, análise e visualização de dados.

---

# 🚀 Próximos Aprimoramentos

Possíveis evoluções do projeto incluem:

- Criação de novos indicadores DAX;
- Análises de tendência mais avançadas;
- Comparação entre períodos;
- Indicadores de desempenho por departamento;
- Análise de concentração de receita;
- Melhorias na experiência de navegação;
- Integração com outras fontes de dados;
- Automatização da atualização dos dados.

---

# 👤 Autor

**Mathews Souza**

Profissional em transição para a área de Dados, com formação em Análise e Desenvolvimento de Sistemas e especialização em Análise de Dados.

### Áreas de interesse

- Análise de Dados
- Business Intelligence
- Power BI
- Excel
- SQL
- Análise Administrativa
- Análise Financeira

---

## ⭐ Tecnologias

`Excel` `Power Query` `Power BI` `DAX` `SQL` `Git` `GitHub`
