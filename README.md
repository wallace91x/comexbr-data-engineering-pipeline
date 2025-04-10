# 📦 COMEXBR – Pipeline de Dados e Análise de Comércio Exterior Brasileiro

Este projeto é o MVP de Engenharia de Dados desenvolvido por Wallace Lima como parte do curso da PUC-Rio. O objetivo foi construir um pipeline completo de ingestão, modelagem, transformação e análise de dados de comércio exterior do Brasil, utilizando a plataforma **Databricks Community Edition** e tecnologias modernas de Big Data e visualização.

## 🧠 Objetivo

Investigar padrões, principais origens e destinos, produtos mais exportados/importados e comportamentos temporais nas operações de comércio exterior do Brasil. O projeto responde a 5 perguntas principais com base em dados oficiais.

## 🚀 Stack Utilizada

- **Databricks Community Edition**
- **Apache Spark / PySpark**
- **Delta Lake**
- **SQL (SparkSQL)**
- **Pandas & Matplotlib / Plotly**
- **Google Drive (armazenamento temporário de dados)**
- **GeoPandas e Folium (para visualização geográfica)**

---

## 📂 Estrutura do Projeto

| Pasta / Arquivo            | Descrição                                                             |
|----------------------------|----------------------------------------------------------------------|
| `COMEXBR_Wallace_Lima_MVP_Engenharia_de_dados.ipynb` | Notebook principal com todo o pipeline e análises                |
| `documentacao_projeto_comercio_exterior.pdf`        | Documento de apoio e descrição do projeto (modelo acadêmico)    |
| `README.md`                  | Este arquivo com visão geral e orientações                         |

---

## 🔄 Etapas do Projeto

### 1. 📥 Coleta e Armazenamento
- Fontes: Planilhas CSV extraídas de fontes oficiais e armazenadas no Google Drive.
- Ingestão automática via `gdown` no DBFS do Databricks.

### 2. 🏗️ Modelagem
- Modelo Estrela implementado.
- Tabelas fato (`fato_exportacao`, `fato_importacao`) e tabelas dimensão (`dim_pais`, `dim_uf`, `dim_ncm` etc.).
- Dicionário de dados e definição explícita de schemas com tipos de dados.

### 3. 🧼 Tratamento e ETL
- Padronização de nomes, schemas, codificações (`latin1`).
- Conversão de campos monetários e numéricos do padrão brasileiro para float.
- Junções, enriquecimento e persistência em Delta Lake.
- Views permanentes: `vw_exportacao` e `vw_importacao`.

### 4. 📊 Análise de Dados
- Top 10 países por volume FOB (exportação/importação)
- Produtos mais exportados e importados
- Unidades federativas com maior movimentação
- Evolução histórica anual (exportação/importação)
- Comparativos e gráficos interativos (Plotly, GeoMapas)

---

## 📈 Resultados Visuais

- Gráficos de barras e pizza
- Gráficos temporais
- Mapas coropléticos interativos (Plotly)
- Análises comparativas entre países, produtos e anos

---

## 💬 Conclusões

- O pipeline é escalável, robusto e cobre todas as etapas exigidas em um ambiente real de engenharia de dados.
- Identificou-se claramente os principais players do comércio exterior brasileiro ao longo do tempo.
- As visualizações fornecem insights relevantes para tomada de decisão e entendimento do cenário comercial internacional do Brasil.

---

## 📄 Licença

Este projeto é de uso acadêmico. O uso dos dados e do código é permitido apenas com atribuição ao autor.

---

## 👨‍💻 Autor

**Wallace Lima**  
Engenharia de Dados | Ciência de Dados | Finanças | Compliance  
[LinkedIn](https://www.linkedin.com/in/wallacelima17/)

---

