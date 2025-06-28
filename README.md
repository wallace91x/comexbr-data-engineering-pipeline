# 📦 COMEXBR – Pipeline de Dados e Análise de Comércio Exterior Brasileiro

Este projeto é o MVP de Engenharia de Dados desenvolvido por Wallace Lima como parte do curso da PUC-Rio. O objetivo foi construir um pipeline completo de ingestão, modelagem, transformação e análise de dados de comércio exterior do Brasil, utilizando a plataforma **Databricks Community Edition** e tecnologias modernas de Big Data e visualização de dados.

---

## 🧠 Objetivo do Projeto

Investigar padrões de comércio, principais países de origem e destino, produtos mais exportados e importados, além de comportamentos temporais nas operações de comércio exterior do Brasil. O projeto responde a cinco perguntas principais com base em dados oficiais.

---

## 🚀 Stack Utilizada

- **Databricks Community Edition**
- **Apache Spark / PySpark**
- **Delta Lake**
- **SQL (SparkSQL)**
- **Pandas & Matplotlib / Plotly**
- **Google Drive** (para armazenamento temporário dos dados)
- **GeoPandas e Folium** (para visualizações geográficas)
- **`gdown`** (para automação da ingestão de arquivos via Google Drive)

---

## 📂 Estrutura do Projeto

| Pasta / Arquivo                                       | Descrição                                                            |
|--------------------------------------------------------|----------------------------------------------------------------------|
| `COMEXBR_Wallace_Lima_MVP_Engenharia_de_dados.ipynb`   | Notebook principal com todo o pipeline e análises                   |
| `documentacao_projeto_comercio_exterior.pdf`           | Documento acadêmico de apoio e descrição do projeto                 |
| `README.md`                                            | Este arquivo com visão geral do projeto                             |

---

## 🔄 Etapas do Projeto

### 1. 📥 Coleta e Armazenamento
- Fontes: Planilhas CSV extraídas de fontes oficiais e armazenadas no Google Drive.
- Ingestão automatizada utilizando a biblioteca `gdown` diretamente no DBFS do Databricks.

### 2. 🏗️ Modelagem dos Dados
- Implementação de modelo em estrela (Star Schema).
- Tabelas fato (`fato_exportacao`, `fato_importacao`) e tabelas dimensão (`dim_pais`, `dim_uf`, `dim_ncm`, etc.).
- Definição de dicionário de dados e schemas com tipos explícitos.

### 3. 🧼 Tratamento e ETL
- Padronização de nomes, schemas e codificações (`latin1`).
- Conversão de campos monetários e numéricos do padrão brasileiro para o tipo `float`.
- Junções, enriquecimento e persistência em Delta Lake.
- Criação de views permanentes: `vw_exportacao` e `vw_importacao`.

### 4. 📊 Análise de Dados
- Top 10 países por volume FOB (exportação/importação)
- Produtos mais exportados e importados
- Unidades federativas com maior movimentação
- Evolução histórica anual das operações
- Gráficos comparativos e interativos com Plotly e GeoMapas

---

## 📈 Resultados Visuais

- Gráficos de barras e pizza
- Séries temporais
- Mapas coropléticos interativos (Plotly)
- Análises comparativas por país, produto e ano

---

## 💬 Conclusões

- O pipeline desenvolvido é escalável, robusto e cobre todas as etapas exigidas em um cenário real de engenharia de dados.
- Foram identificados claramente os principais players do comércio exterior brasileiro ao longo dos anos.
- As visualizações geradas oferecem insights relevantes para a tomada de decisão e para a compreensão do cenário comercial internacional do Brasil.

---

## 📄 Licença

Este projeto possui fins acadêmicos. O uso dos dados e do código é permitido apenas mediante atribuição ao autor.

---

## 👨‍💻 Autor

**Wallace Lima**  
Engenharia de Dados | Ciência de Dados | Finanças | Compliance  
[LinkedIn](https://www.linkedin.com/in/wallacelima17/)
