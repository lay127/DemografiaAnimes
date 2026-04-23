# 📊 C4 Model - Análise de Demografia em Animes

## 📌 Visão Geral

Este documento descreve a arquitetura do sistema desenvolvido para análise da influência da demografia (shounen, shoujo, seinen e josei) na visibilidade e popularidade de animes.

O modelo arquitetural foi elaborado utilizando o **C4 Model**, que permite representar o sistema em diferentes níveis de abstração, facilitando a compreensão da estrutura e funcionamento da solução.

# 🌍 1. Diagrama de Contexto

## 📌 Descrição

O diagrama de contexto apresenta uma visão geral do sistema, destacando:

* O usuário que interage com a aplicação
* O sistema principal
* As fontes externas de dados

## 📊 Diagrama
![Diagrama de Contexto](https://kroki.io/plantuml/svg/eNpdUbtSwzAQ7P0Vh6swQ-ImFVWCoQCSGQ-Z1JmzdeOIyJLRSZDwN6n4Ar7AP4bkvJhUWu2tdu9OE3ZonW8U5ONVbrSjrUtupK6UF-StgrVzLd9nmcWvUS3d2peeyVZRqd2oMk3WKtTRYchOKFlm-XhYRGo5n2UNsiObXbxHbVAmSUGWjR549miluYN0yb7bB5gGXBCzQfjwBN5JJb8RDAjkdWnQCmjRIqDu9koypbdJstiFkGbAMh4YDBYHBIJgetQdsGyIY8JUYyCDAIXhWMK-BAS0lSXBpwyNxeDup_sNT84hq6etG2ywrhUFm0d0yOQYXnsmOj8Eone8sg4W_xze5QZ17KN4hpeI0-NFGJjv-j5nYYaY-0bqsqbLiMvDYoIiCs78ubUcraX6OOG16hQf_oS9cqc9oJCVNBplP_CEtAh_9QfR0L8j)

## 🧠 Interpretação

O usuário interage diretamente com o sistema por meio do dashboard.

O sistema depende de duas fontes externas:

* **Datasets do Kaggle**, que fornecem dados históricos
* **API Jikan**, utilizada para enriquecimento das informações


# 🧱 2. Diagrama de Containers

## 📌 Descrição

Este diagrama detalha os principais blocos que compõem o sistema.

Cada container representa uma responsabilidade dentro da arquitetura.

## 📊 Diagrama

![Diagrama de Containers](https://kroki.io/plantuml/svg/eNp9Ustu20AMvOsrGJ8ctLEuOfWURM4hrQsINdJrQEusvPU-BC7XqVP0Y4IeCvQ3_GNdKrGjBkV14nKHw5lZXURBluQsVOd3VfCCxhMXJz1j5xAs7kISiI4EPRYnxjc2tZTYwlqkj-_KkvF-1hlZp1WKxE2mIC-zJriyt-iV-ixKa82qrM7Pam3dflyUDqMQl-Olsz5jiyJujO-R0cEKm03HIfm2CjYw3K-NUFHUxDH4aYoJ2YS3MLmNaf-Yy8lpUSx3mdfdXekU8m4ajZ4xo5ZPFbQEl37_aE2kySl8LwrI31HEtMW4XgXkNo_MD_VE54UJnTVSals7N9kqf8GGYGuyGAtGGyhmiyrlb96eQ0MxosvpqOh6fFZRc2xDVNp6J-vg4Q3UmD0MrYVxPT1kF7qhY9z_2v8MQIDPRiCPQjsQvF48X02Hi8xyhYocbaqWn8tFaNDq4ZIdPpDHJx6QbOSZ8Mcx1utvMt1g11ka0pFMKBE-DJ0MHKG-mg16Za1v4L3WKuwT2ZdnGwc9JImdcihmdPU6tmWwpjGCR7eKfwU6-F3sf5fXsWHa0r-BRysVMlP3X9KDoRxsTDYLyM7U0wX5Nv-3fwDOHSN9)

## 🧠 Interpretação

A arquitetura está dividida em três partes principais:

### 🖥️ Dashboard (Power BI)

Responsável pela interface com o usuário, permitindo:

* Filtros por demografia
* Visualização de gráficos
* Comparações entre categorias

### ⚙️ Processamento de Dados

Responsável por:

* Limpeza dos dados
* Integração entre diferentes fontes
* Cálculo de métricas

### 💾 Base de Dados (Arquivos CSV)

Armazena os dados já tratados em arquivos CSV, permitindo:

* Melhor desempenho
* Evitar reprocessamento constante

# ⚙️ 3. Diagrama de Componentes

## 📌 Descrição

Este diagrama detalha a estrutura interna do módulo de processamento de dados.

## 📊 Diagrama

![Diagrama de Componentes](https://kroki.io/plantuml/svg/eNptks9OAkEMxu_zFIUTJMJeOHmCrB5IMCFGzqbsVphk_mxmuho0PozxYDz4FPtidoCwC7qndvr1N-23M42MgWtrIJ885t5W3pFj1asCbiyCwZ2vGaIlRoeqp11h6pLqYGDLXMXrLAv4Mt5o3tbrOlIovGMBjAtvs8qgS-hR5NLodZZPRst0tLpbZBYjU8i6l44r0SqVCwG1ozCogi8oRrRS9FfQX3ZzKAlusPSxP4Q3pUC-E2lQeCMDS0u-D1ptoux4612KcgyBNlJFxkgcgWC2nPeHlzSjbUWvCbc4ROc8dCXuo4eA6a5UgCc04hhTgopp3kUdkzEU__K1HG8CFpiWnB-S5qv59OfjrhxBqZ8o7DGwlpn_gclvMjqS6Geu-Ujh5dKmqA2Cbb456ALTgCSPgJufyClPyHel7smcbGwNuHXP-rii6JLmVDvboqMDTra0DV1dO2y34ag4tKgpuVIexi8htur3)

## 🧠 Interpretação

O processamento de dados foi dividido em etapas sequenciais:

### 📥 Coleta de Dados

* Carrega datasets do Kaggle
* Realiza requisições na API Jikan

### 🧹 Limpeza

* Remove inconsistências
* Trata valores nulos
* Padroniza dados

### 🔗 Integração

* Une diferentes bases
* Resolve conflitos entre dados

### 📊 Análise

* Calcula métricas como:

  * Popularidade
  * Média de notas
  * Distribuição por demografia
 
# 🛠️ 4. Tecnologias Utilizadas

O sistema foi desenvolvido utilizando ferramentas voltadas para análise e visualização de dados, priorizando simplicidade, eficiência e facilidade de uso.

### 📊 Visualização de Dados
- Power BI

O Power BI foi escolhido por permitir a criação de dashboards interativos e facilitar a análise visual dos dados de forma intuitiva, sem necessidade de desenvolvimento front-end.

### ⚙️ Processamento de Dados
- Python
- Pandas
- NumPy

Essas tecnologias foram utilizadas por sua eficiência no processamento de grandes volumes de dados e ampla adoção em projetos de ciência de dados.

### 🔗 Coleta de Dados
- Datasets do Kaggle (arquivos CSV)
- API Jikan (MyAnimeList)

A utilização de datasets do Kaggle e da API Jikan permite obter dados amplos e atualizados sobre animes, garantindo maior diversidade, completude e confiabilidade das informações utilizadas na análise.

### 💾 Armazenamento
- Arquivos CSV armazenados no GitHub

A utilização de arquivos CSV no GitHub permite versionamento dos dados e fácil integração com ferramentas de visualização como o Power BI.

# 🧠 5. Justificativa da Arquitetura

A arquitetura do sistema foi definida com base na separação clara entre as etapas de coleta, processamento, armazenamento e visualização dos dados, seguindo princípios de organização e eficiência.

A escolha do uso do Power BI como camada de visualização permite desacoplar o processamento de dados da interface com o usuário. Isso possibilita que os dados sejam previamente tratados em Python e posteriormente consumidos pelo dashboard, reduzindo o custo computacional durante a interação e melhorando o desempenho geral da aplicação.

O armazenamento dos dados processados em arquivos CSV no GitHub foi adotado por sua simplicidade e eficiência. Essa abordagem dispensa o uso de um banco de dados dedicado, ao mesmo tempo em que garante versionamento, rastreabilidade e fácil compartilhamento dos dados.

Além disso, essa arquitetura é adequada para cenários de análise de dados exploratória, nos quais:

* o processamento ocorre de forma offline ou periódica;
* os dados são relativamente estáticos após o tratamento;
* a visualização exige alta interatividade e clareza na apresentação.

O modelo C4 foi escolhido por permitir uma visualização clara da arquitetura em diferentes níveis de abstração, facilitando o entendimento do sistema tanto para desenvolvedores quanto para stakeholders não técnicos.

A divisão em containers (dashboard, processamento e armazenamento) segue o princípio de separação de responsabilidades, permitindo maior organização, manutenção e escalabilidade do sistema.

Além disso, essa arquitetura é adequada para aplicações de análise de dados, onde há uma clara distinção entre:
- ingestão de dados
- processamento
- visualização

# 🧪 Considerações Arquiteturais

A arquitetura foi projetada com foco em:

### ✅ Separação de responsabilidades

Cada parte do sistema possui uma função bem definida

### ⚡ Eficiência

Os dados são armazenados localmente após o processamento

### 📈 Escalabilidade

A estrutura permite expansão futura, como:

* Novas fontes de dados
* Novas métricas
* Deploy em ambiente web
