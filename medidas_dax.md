# 🧮 Medidas DAX — Dashboard Administrativo e Financeiro

Este documento apresenta as principais medidas DAX utilizadas no desenvolvimento do Dashboard Administrativo e Financeiro.

As medidas foram criadas para calcular indicadores financeiros, operacionais e análises temporais no Power BI.

---

# 📊 Indicadores Financeiros

## Receita Total

Calcula o valor total das operações.

```DAX
Receita Total =
SUM(Base_Dados[Valor_Operacao])
```

---

## Valor Pago

Calcula o valor total efetivamente pago.

```DAX
Valor Pago =
SUM(Base_Dados[Valor_Pago])
```

---

## Valor em Aberto

Calcula o valor total que ainda está pendente de pagamento.

```DAX
Valor em Aberto =
SUM(Base_Dados[Valor_Em_Aberto])
```

---

## Valor em Atraso

Calcula o valor associado às operações que estão em atraso.

```DAX
Valor em Atraso =
CALCULATE(
    [Receita Total],
    Base_Dados[Status] = "Em atraso"
)
```

---

# 📦 Indicadores Operacionais

## Quantidade de Operações

Calcula a quantidade total de registros/operações da base.

```DAX
Quantidade de Operações =
COUNTROWS(Base_Dados)
```

---

## Operações em Atraso

Calcula a quantidade de operações cujo status está como "Em atraso".

```DAX
Operações em Atraso =
CALCULATE(
    [Quantidade de Operações],
    Base_Dados[Status] = "Em atraso"
)
```

---

## Clientes Ativos

Calcula a quantidade distinta de clientes presentes na base.

```DAX
Clientes Ativos =
DISTINCTCOUNT(
    Base_Dados[Cliente]
)
```

---

# 💰 Indicadores de Desempenho

## Ticket Médio

Calcula a receita média por operação.

```DAX
Ticket Médio =
DIVIDE(
    [Receita Total],
    [Quantidade de Operações],
    0
)
```

---

## Receita Média por Cliente

Calcula a receita média gerada por cliente.

```DAX
Receita Média por Cliente =
DIVIDE(
    [Receita Total],
    [Clientes Ativos],
    0
)
```

---

# ⚠️ Indicadores de Inadimplência

## Taxa de Inadimplência

Calcula a proporção de operações que estão em atraso.

```DAX
Taxa de Inadimplência =
DIVIDE(
    [Operações em Atraso],
    [Quantidade de Operações],
    0
)
```

---

## Percentual da Receita em Atraso

Calcula quanto da receita total está associado a operações em atraso.

```DAX
% Receita em Atraso =
DIVIDE(
    [Valor em Atraso],
    [Receita Total],
    0
)
```

---

## Percentual da Receita Paga

Calcula a proporção da receita total que já foi paga.

```DAX
% Receita Paga =
DIVIDE(
    [Valor Pago],
    [Receita Total],
    0
)
```

---

## Percentual da Receita em Aberto

Calcula a proporção da receita que permanece em aberto.

```DAX
% Receita em Aberto =
DIVIDE(
    [Valor em Aberto],
    [Receita Total],
    0
)
```

---

# 📅 Análise Temporal

## Receita do Mês Anterior

Calcula a receita correspondente ao mês anterior ao período atualmente selecionado.

```DAX
Receita Mês Anterior =
CALCULATE(
    [Receita Total],
    DATEADD(
        Calendario[Date],
        -1,
        MONTH
    )
)
```

---

## Crescimento Mensal

Calcula a variação percentual da receita em relação ao mês anterior.

```DAX
Crescimento Mensal % =
DIVIDE(
    [Receita Total] - [Receita Mês Anterior],
    [Receita Mês Anterior],
    0
)
```

---

# 📌 Resumo das Medidas

| Medida | Finalidade |
|---|---|
| Receita Total | Total faturado |
| Valor Pago | Total efetivamente pago |
| Valor em Aberto | Total pendente |
| Valor em Atraso | Total em atraso |
| Quantidade de Operações | Número de operações |
| Operações em Atraso | Quantidade de operações atrasadas |
| Ticket Médio | Receita média por operação |
| Taxa de Inadimplência | Percentual de operações atrasadas |
| % Receita Paga | Percentual da receita já paga |
| % Receita em Aberto | Percentual da receita pendente |
| % Receita em Atraso | Percentual da receita atrasada |
| Clientes Ativos | Quantidade de clientes distintos |
| Receita Média por Cliente | Receita média por cliente |
| Receita Mês Anterior | Receita do período anterior |
| Crescimento Mensal % | Variação percentual da receita |

---

# 🧠 Principais Funções DAX Utilizadas

As principais funções utilizadas no projeto são:

- `SUM`
- `COUNTROWS`
- `DISTINCTCOUNT`
- `CALCULATE`
- `DIVIDE`
- `DATEADD`

Essas funções permitem trabalhar com agregações, contexto de filtro, cálculos percentuais e análises temporais.

---

# 📚 Conceitos Demonstrados

O conjunto de medidas demonstra conhecimentos de:

- DAX básico e intermediário;
- Contexto de filtro;
- Agregações;
- Cálculos percentuais;
- Funções de inteligência de tempo;
- Indicadores financeiros;
- Indicadores operacionais;
- Análise de desempenho;
- Análise temporal.

---
