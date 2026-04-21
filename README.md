# 📊 Caderno Temático: Engenharia de Dados com NotebookLM

> Projeto desenvolvido como parte do Desafio de Projeto da [DIO](https://www.dio.me/) — explorando a IA como ferramenta de aprendizagem ativa com o NotebookLM do Google.

---

## 📌 Contexto e Objetivos

### Por que Engenharia de Dados?

A Engenharia de Dados é a espinha dorsal de qualquer iniciativa de dados bem-sucedida. Sem pipelines confiáveis, dados limpos e arquiteturas bem projetadas, nenhuma análise ou modelo de Machine Learning consegue entregar valor real. Com o crescimento exponencial do volume de dados nas organizações, a demanda por profissionais especializados nessa área cresce junto.

Já possuo conhecimentos básicos em SQL, Python e conceitos de banco de dados. Com este caderno temático, quero avançar para um entendimento mais sólido e aplicável de Engenharia de Dados moderna.

### 🎯 Objetivos de Estudo

| # | Objetivo | Status |
|---|----------|--------|
| 1 | Compreender as arquiteturas modernas de dados (Data Lake, Data Lakehouse, Data Mesh) | 🔄 Em progresso |
| 2 | Entender o ciclo de vida completo de um pipeline de dados (ETL/ELT) | 🔄 Em progresso |
| 3 | Conhecer as principais ferramentas do ecossistema (Apache Spark, Airflow, dbt, Kafka) | 🔄 Em progresso |
| 4 | Aprender boas práticas de qualidade, governança e observabilidade de dados | 🔄 Em progresso |
| 5 | Consolidar um glossário técnico de referência para futuras consultas | 🔄 Em progresso |

---

## 📚 Curadoria de Fontes

As fontes abaixo foram selecionadas por serem abertas, técnicas e atualizadas. Todas foram carregadas no NotebookLM para análise.

### Fonte 1 — Fundamentos de Engenharia de Dados
**"Fundamentals of Data Engineering" — Excerpts & Summary**
- 🔗 [https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/](https://www.oreilly.com/library/view/fundamentals-of-data/9781098108298/)
- **Por que escolhi:** Referência mais completa sobre o ciclo de vida de dados (Data Engineering Lifecycle), cobrindo geração, armazenamento, ingestão, transformação e consumo.
- **Formato no NotebookLM:** PDF do capítulo introdutório + notas pessoais

---

### Fonte 2 — Arquiteturas Modernas de Dados
**"The Data Engineering Cookbook" — Andreas Kretz (PDF gratuito)**
- 🔗 [https://github.com/andkret/Cookbook](https://github.com/andkret/Cookbook)
- **Por que escolhi:** Abordagem prática com casos reais, cobrindo desde infraestrutura até ferramentas como Kafka, Spark e Hadoop. Totalmente gratuito e atualizado pela comunidade.
- **Formato no NotebookLM:** PDF completo

---

### Fonte 3 — dbt e Transformação de Dados
**"dbt — Official Documentation & Best Practices Guide"**
- 🔗 [https://docs.getdbt.com/docs/introduction](https://docs.getdbt.com/docs/introduction)
- **Por que escolhi:** O dbt se tornou o padrão de mercado para transformação de dados na camada analítica. A documentação oficial é clara, bem estruturada e ideal para estudo.
- **Formato no NotebookLM:** Páginas salvas em PDF (Introdução + Tutorial)

---

### Fonte 4 — Apache Airflow para Orquestração
**"Apache Airflow Documentation — Concepts & Architecture"**
- 🔗 [https://airflow.apache.org/docs/apache-airflow/stable/index.html](https://airflow.apache.org/docs/apache-airflow/stable/index.html)
- **Por que escolhi:** Airflow é a ferramenta de orquestração de pipelines mais usada no mercado. Entender seus conceitos (DAGs, Operators, Hooks) é essencial para qualquer engenheiro de dados.
- **Formato no NotebookLM:** PDF dos capítulos de conceitos principais

---

### Fonte 5 — Qualidade e Governança de Dados
**"The Practical Guide to Data Quality Management" — DAMA International (resumo aberto)**
- 🔗 [https://www.dama.org/cpages/body-of-knowledge](https://www.dama.org/cpages/body-of-knowledge)
- **Por que escolhi:** Governança é um tema frequentemente negligenciado por iniciantes. Esta fonte cobre Data Quality, Data Lineage e Metadata Management de forma estruturada.
- **Formato no NotebookLM:** PDF + artigo complementar do blog da Databricks

---

## 🧪 Engenharia de Prompts e Cicatrizes

Esta seção documenta o processo real de interação com o NotebookLM — incluindo os prompts que funcionaram, os que não funcionaram e o que aprendi com cada tentativa.

---

### 🔬 Experimento 1 — Entendendo o Pipeline de Dados

#### Prompt Inicial (v1)
```
O que é um pipeline de dados?
```
**Resultado:** Resposta muito genérica, sem profundidade técnica. O NotebookLM trouxe definições básicas sem conectar com as fontes carregadas de forma significativa.

**⚠️ Dificuldade encontrada:** Prompts abertos demais geram respostas de enciclopédia, não de aprendizado.

---

#### Prompt Refinado (v2)
```
Com base nas fontes carregadas, explique as etapas do Data Engineering Lifecycle 
(geração → ingestão → transformação → consumo), dando um exemplo prático de 
ferramenta usada em cada etapa.
```
**Resultado:** ✅ Muito melhor! O NotebookLM citou trechos específicos do Cookbook e do Fundamentals, montando uma resposta estruturada com referências a Kafka (ingestão), dbt (transformação) e Metabase/Superset (consumo).

**💡 Aprendizado:** Especificar o formato da resposta esperada ("com exemplos práticos de ferramentas") muda completamente a qualidade da entrega.

---

### 🔬 Experimento 2 — Comparando Arquiteturas

#### Prompt (v1)
```
Diferença entre Data Warehouse e Data Lake.
```
**Resultado:** Resposta correta, mas superficial. Nada que eu já não soubesse.

#### Prompt Refinado (v2)
```
Quais são as principais diferenças entre Data Warehouse, Data Lake e Data Lakehouse 
do ponto de vista de um Engenheiro de Dados que precisa decidir qual arquitetura 
adotar? Quais os trade-offs de cada uma em termos de custo, latência e governança?
```
**Resultado:** ✅ Excelente! A resposta trouxe uma análise comparativa com perspectiva de decisão arquitetural — exatamente o que eu precisava para entender quando usar cada abordagem.

**💡 Aprendizado:** Adicionar o **contexto do tomador de decisão** ("do ponto de vista de um Engenheiro de Dados que precisa decidir") faz o modelo gerar respostas mais aplicadas e menos teóricas.

---

### 🔬 Experimento 3 — Aprendendo sobre dbt

#### Prompt (v1)
```
Como funciona o dbt?
```
**⚠️ Problema:** Resposta genérica, colando quase literalmente a introdução da documentação.

#### Prompt Refinado (v2)
```
Explique o fluxo de trabalho do dbt para um engenheiro que já conhece SQL mas 
nunca usou a ferramenta. Quais são os conceitos de Models, Tests e Sources? 
Como o dbt se integra com um Data Warehouse como BigQuery ou Snowflake?
```
**Resultado:** ✅ A resposta construiu uma progressão pedagógica — partindo do que eu já sei (SQL) e conectando ao novo (dbt). As citações vieram da documentação oficial que carregui.

---

### 🔬 Experimento 4 — Troubleshooting real

#### Prompt que falhou
```
Me dê um resumo de todas as fontes que carreguei.
```
**❌ Problema:** O NotebookLM tentou resumir TUDO de uma vez e gerou um texto genérico, misturando conceitos sem profundidade em nenhum deles.

**✅ Solução encontrada:** Quebrar em prompts menores e temáticos, um por fonte ou por conceito. Exemplo:
```
Com base apenas no "Data Engineering Cookbook", quais são as 5 tecnologias 
mais recomendadas para construir um pipeline de dados em produção em 2024?
```
**💡 Aprendizado de ouro:** O NotebookLM performa melhor com prompts focados em UMA fonte ou UM conceito por vez. Pedir para resumir tudo ao mesmo tempo é a receita para respostas rasas.

---

### 📋 Tabela de Prompts — Bom vs. Ruim

| ❌ Prompt Fraco | ✅ Prompt Forte | Por que funciona melhor |
|----------------|----------------|------------------------|
| "O que é ETL?" | "Explique a diferença entre ETL e ELT com exemplos de quando cada abordagem é preferível em pipelines modernos baseados em cloud." | Contexto + comparação + critério de decisão |
| "Fale sobre Airflow" | "Quais são os componentes principais do Apache Airflow (Scheduler, Executor, Worker, DAG) e como eles se comunicam durante a execução de uma task?" | Específico, estruturado, técnico |
| "O que é governança de dados?" | "Segundo as fontes carregadas, quais são os pilares de governança de dados mais importantes para uma empresa que está estruturando seu primeiro Data Lake?" | Âncora nas fontes + contexto de aplicação |
| "Resuma tudo" | "Quais são os 3 conceitos mais complexos abordados no capítulo X e como eles se relacionam?" | Foco + relação entre conceitos |

---

## 📖 Miniguia de Estudo — Engenharia de Dados

### 1. Resumos Estruturados

#### 🏗️ Bloco 1: O Ciclo de Vida da Engenharia de Dados

O **Data Engineering Lifecycle** é o framework central da área. Ele descreve o caminho que os dados percorrem desde sua origem até o consumo final por analistas, cientistas de dados ou sistemas de BI.

**As etapas principais são:**

1. **Geração** — Dados são criados em sistemas transacionais (bancos de dados OLTP, APIs, IoT, logs de aplicações).
2. **Ingestão** — Coleta e movimentação dos dados para um repositório centralizado. Pode ser em **batch** (lotes periódicos) ou **streaming** (tempo real). Ferramentas: Apache Kafka, AWS Kinesis, Fivetran, Airbyte.
3. **Armazenamento** — Onde os dados ficam: Data Warehouse (estruturado, otimizado para consultas analíticas), Data Lake (bruto, em qualquer formato) ou Data Lakehouse (híbrido moderno). Exemplos: Snowflake, BigQuery, Delta Lake, Apache Iceberg.
4. **Transformação** — Limpeza, enriquecimento e modelagem dos dados para uso analítico. Ferramentas: dbt, Apache Spark, SQL puro.
5. **Consumo** — Uso final pelos stakeholders: dashboards (Power BI, Tableau, Metabase), consultas ad hoc, features para ML, APIs de dados.

---

#### 🏗️ Bloco 2: Arquiteturas Modernas Comparadas

| Característica | Data Warehouse | Data Lake | Data Lakehouse |
|----------------|---------------|-----------|----------------|
| **Tipo de dados** | Estruturados | Todos os tipos | Todos os tipos |
| **Custo de armazenamento** | Alto | Baixo | Médio |
| **Desempenho de queries** | Excelente | Fraco (sem otimização) | Bom (com Delta/Iceberg) |
| **Governança** | Alta | Baixa | Alta |
| **Flexibilidade** | Baixa | Alta | Alta |
| **Exemplos** | Snowflake, Redshift, BigQuery | S3, ADLS, GCS | Databricks, Delta Lake, Apache Hudi |
| **Quando usar** | BI tradicional, relatórios | Exploração, ML, dados brutos | Ambos os casos |

---

#### 🏗️ Bloco 3: Ferramentas Essenciais do Ecossistema

**Ingestão & Streaming**
- **Apache Kafka** — Plataforma de streaming distribuída. Ideal para eventos em tempo real (logs, cliques, transações).
- **Airbyte / Fivetran** — Conectores prontos para extrair dados de centenas de fontes (SaaS, bancos, APIs) sem escrever código.

**Processamento & Transformação**
- **Apache Spark** — Engine de processamento distribuído. Referência para Big Data. Suporta Python (PySpark), SQL e Scala.
- **dbt (data build tool)** — Padrão de mercado para transformação analítica. Escreve SQL modular com testes, documentação e versionamento.

**Orquestração**
- **Apache Airflow** — Agenda e monitora pipelines como DAGs (Directed Acyclic Graphs). Altamente extensível com Operators para qualquer serviço.
- **Prefect / Dagster** — Alternativas mais modernas ao Airflow, com melhor observabilidade e developer experience.

**Armazenamento & Formatos**
- **Parquet** — Formato colunar altamente eficiente para dados analíticos. Padrão de fato em Data Lakes.
- **Delta Lake / Apache Iceberg** — Camada de tabelas ACID sobre Data Lakes. Habilitam o conceito de Lakehouse.

---

### 2. Glossário Técnico

| Termo | Definição |
|-------|-----------|
| **Pipeline de Dados** | Conjunto de etapas automatizadas que movem e transformam dados de uma origem para um destino. |
| **ETL** | Extract, Transform, Load — dado é transformado antes de ser carregado no destino. Padrão clássico. |
| **ELT** | Extract, Load, Transform — dado é carregado bruto e transformado no destino. Padrão moderno com cloud warehouses. |
| **DAG** | Directed Acyclic Graph — representação de um pipeline no Airflow onde tasks são nós e dependências são arestas. |
| **Data Lineage** | Rastreabilidade da origem e transformações de um dado ao longo de todo seu ciclo de vida. |
| **Schema-on-Read** | Estrutura do dado definida apenas na leitura (Data Lake). Flexível, mas menos governado. |
| **Schema-on-Write** | Estrutura definida na escrita (Data Warehouse). Mais rígido, mais confiável. |
| **Particionamento** | Divisão física dos dados por uma coluna (ex: data, região) para otimizar queries. Crítico em grandes volumes. |
| **Idempotência** | Propriedade de um pipeline que garante que re-executar a mesma operação produz o mesmo resultado, sem duplicatas. |
| **Data Catalog** | Inventário de metadados que documenta quais dados existem, onde estão, quem os criou e o que significam. |
| **SLA de Dados** | Acordo de nível de serviço para pipelines — define o prazo máximo aceitável para dados ficarem disponíveis. |
| **Slowly Changing Dimension (SCD)** | Técnica para rastrear mudanças históricas em dados dimensionais (ex: endereço de um cliente). |
| **Batch Processing** | Processamento de dados em lotes em intervalos de tempo (horário, diário). Mais simples e barato. |
| **Stream Processing** | Processamento contínuo de dados à medida que chegam. Maior complexidade, menor latência. |
| **Data Mesh** | Arquitetura descentralizada onde cada domínio de negócio é responsável por seus próprios dados como produtos. |
| **dbt Model** | Arquivo SQL no dbt que representa uma transformação — vira uma tabela ou view no Data Warehouse. |
| **Orchestration** | Coordenação e agendamento da execução de tasks em um pipeline, gerenciando dependências e falhas. |
| **Observabilidade de Dados** | Capacidade de monitorar a saúde, qualidade e comportamento dos dados em produção. |
| **ACID** | Atomicidade, Consistência, Isolamento, Durabilidade — propriedades de transações confiáveis em bancos de dados. |
| **Data Contract** | Acordo formal entre produtor e consumidor de dados sobre estrutura, qualidade e SLAs. |

---

### 3. Prompts Reutilizáveis para Revisão Futura

Use estes prompts diretamente no NotebookLM (ou em qualquer IA) para revisar e aprofundar os conceitos deste caderno:

#### 🔁 Prompts de Revisão Conceitual
```
Explique [CONCEITO] como se eu fosse um engenheiro de dados com 1 ano de experiência. 
Use uma analogia do mundo real e depois descreva como isso se aplica em produção.
```

```
Quais são as 3 principais armadilhas que engenheiros de dados cometem ao trabalhar 
com [TECNOLOGIA/CONCEITO] pela primeira vez? Como evitá-las?
```

```
Compare [FERRAMENTA A] e [FERRAMENTA B] sob 4 critérios: maturidade, curva de 
aprendizado, custo e casos de uso ideais. Conclua com uma recomendação.
```

#### 🔁 Prompts de Aplicação Prática
```
Descreva passo a passo como você construiria um pipeline de dados para o seguinte 
cenário: [DESCREVER O CENÁRIO]. Quais ferramentas escolheria e por quê?
```

```
Quais perguntas um entrevistador de engenharia de dados provavelmente faria sobre 
[TÓPICO]? Responda cada uma delas de forma técnica mas clara.
```

```
Com base nas fontes carregadas, quais são os padrões de projeto (design patterns) 
mais importantes para [PIPELINES BATCH / STREAMING / TRANSFORMAÇÃO]?
```

#### 🔁 Prompts de Glossário e Síntese
```
Crie um quiz de 5 perguntas sobre [TÓPICO] baseado nas fontes carregadas. 
Inclua gabarito comentado ao final.
```

```
Liste os 10 termos técnicos mais importantes relacionados a [TÓPICO] e explique 
cada um em no máximo 2 frases, do mais básico para o mais avançado.
```

```
Faça um mapa mental em texto (com hierarquia de tópicos e subtópicos) sobre 
[TÓPICO CENTRAL] conectando todos os conceitos que aparecem nas fontes carregadas.
```

---

## 🛠️ Estrutura do Repositório

```
📁 miniguia-estudos-notebooklm/
│
├── 📄 README.md                    ← Este arquivo (entrega principal)
│
├── 📁 fontes/
│   ├── data-engineering-lifecycle-notes.pdf
│   ├── data-engineering-cookbook-excerpt.pdf
│   └── links.md                   ← Links para as fontes online
│
├── 📁 prompts/
│   └── prompts-testados.md        ← Log completo de testes de prompts
│
└── 📁 glossario/
    └── glossario-dados.md         ← Versão expandida do glossário
```

---

## 🚀 Tecnologias & Ferramentas Mencionadas

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Apache Spark](https://img.shields.io/badge/Apache_Spark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![dbt](https://img.shields.io/badge/dbt-FF694B?style=for-the-badge&logo=dbt&logoColor=white)
![Airflow](https://img.shields.io/badge/Apache_Airflow-017CEE?style=for-the-badge&logo=apacheairflow&logoColor=white)
![Snowflake](https://img.shields.io/badge/Snowflake-29B5E8?style=for-the-badge&logo=snowflake&logoColor=white)
![BigQuery](https://img.shields.io/badge/BigQuery-4285F4?style=for-the-badge&logo=googlebigquery&logoColor=white)
![NotebookLM](https://img.shields.io/badge/NotebookLM-4285F4?style=for-the-badge&logo=google&logoColor=white)

---

## 📈 Próximos Passos

- [ ] Implementar um pipeline simples com Airflow + dbt localmente (Docker)
- [ ] Completar o módulo de Apache Spark na trilha da DIO
- [ ] Estudar Apache Iceberg e o conceito de Open Table Formats
- [ ] Aprofundar em Data Quality com Great Expectations
- [ ] Criar um projeto end-to-end e adicionar ao portfólio

---

## 👤 Autor

Feito por **Geovana Queiroz** como parte do Bootcamp da [DIO](https://www.dio.me/).

---

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar, adaptar e compartilhar!
