# AWS Data Lake Project – Parquet Partitioning with Athena

## 📌 Visão Geral

Este projeto demonstra a implementação de um fluxo completo de persistência e consulta de dados em ambiente cloud utilizando serviços da AWS e técnicas de otimização baseadas em armazenamento colunar.

O conjunto de dados foi processado com Pandas e persistido em formato Parquet, com compressão Snappy e particionamento por data, visando otimização de performance em consultas analíticas.

---

## 🛠 Tecnologias Utilizadas

- Python
- Pandas
- PyArrow
- Amazon S3
- Amazon Athena
- SQL

---

## ⚙️ Etapas do Projeto

1. Ingestão e leitura do dataset em DataFrame Pandas  
2. Padronização dos nomes das colunas  
3. Conversão de tipos de dados  
4. Criação da coluna `reference_date` para particionamento  
5. Persistência dos dados em:
   - CSV (formato orientado a linha)
   - Parquet (formato orientado a coluna, compressão Snappy)
6. Particionamento dos arquivos por `reference_date`
7. Upload do dataset particionado para Amazon S3
8. Criação de tabela externa no Amazon Athena
9. Atualização das partições com `MSCK REPAIR TABLE`
10. Execução de consultas SQL para validação

---

## 🧠 Conceitos Aplicados

- Armazenamento colunar (Parquet)
- Compressão de dados
- Estratégias de particionamento
- Arquitetura de Data Lake
- Integração entre Amazon S3 e Amazon Athena
- Consultas serverless
- Otimização de performance em workloads analíticos

---

## 🚀 Resultados

A integração entre Amazon S3 e Amazon Athena foi validada com sucesso, com reconhecimento correto das partições e execução eficiente das consultas SQL.

O particionamento por `reference_date` permitiu que as consultas fossem realizadas de maneira mais otimizada, reduzindo o volume de dados escaneados.

---

## 📊 Arquitetura Simplificada

Data → Pandas → Parquet (Particionado) → Amazon S3 → Amazon Athena → SQL
