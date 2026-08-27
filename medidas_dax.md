# 🧮 Medidas DAX — Dashboard Administrativo e Financeiro

Este documento apresenta as principais medidas DAX utilizadas no desenvolvimento do Dashboard Administrativo e Financeiro.

As medidas foram criadas para calcular indicadores financeiros, operacionais e análises temporais no Power BI.

---

## 📊 Indicadores Financeiros

### Receita Total

Calcula o valor total das operações.

```DAX
Receita Total =
SUM(Base_Dados[Valor_Operacao])
