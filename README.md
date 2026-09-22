# Pipeline de Engenharia de Dados — UCI Online Retail

Projeto de Engenharia de Dados desenvolvido utilizando Databricks, PySpark, Delta Lake e Unity Catalog, com o objetivo de construir um pipeline completo de ingestão, tratamento, transformação e análise de dados.

O projeto utiliza o dataset **Online Retail**, disponibilizado pelo **UCI Machine Learning Repository**, contendo transações de uma empresa britânica de varejo online.

---

## 🎯 Objetivo

Construir um pipeline de dados seguindo a arquitetura **Medallion (Bronze, Silver e Gold)**, transformando dados brutos em informações estruturadas para análise de vendas.

O projeto também utiliza **Lakeflow Jobs** para orquestração do pipeline e **Databricks Genie** para realizar consultas aos dados utilizando linguagem natural.

---

## 🏗️ Arquitetura

```text
UCI Online Retail
       │
       ▼
   🥉 BRONZE
   Dados brutos
       │
       ▼
   🥈 SILVER
Limpeza e transformação
       │
       ▼
    🥇 GOLD
Dados analíticos
       │
       ├───────────────┐
       ▼               ▼
 Lakeflow Job      Genie Agent
                       │
                       ▼
              Consultas em
             linguagem natural
