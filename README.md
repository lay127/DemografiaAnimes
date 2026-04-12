# 📊 Como a demografia impacta a visibilidade de animes: um estudo sobre a subvalorização de obras shoujo

## 🎯 1. Objetivo do Projeto

Este projeto tem como objetivo analisar como a demografia dos animes (shounen, shoujo, seinen e josei) influencia sua popularidade, distribuição e visibilidade no mercado. O foco principal está na investigação da sub-representação de obras classificadas como *shoujo*, tradicionalmente voltadas ao público feminino.

A proposta busca identificar padrões e possíveis vieses estruturais que impactam a valorização dessas obras, contribuindo para uma análise crítica baseada em dados.


## 🌍 2. Alinhamento com os Objetivos de Desenvolvimento Sustentável (ODS)

O projeto está alinhado ao **ODS 5 – Igualdade de Gênero**, ao analisar possíveis desigualdades na visibilidade e valorização de conteúdos voltados ao público feminino na indústria do entretenimento.

A partir da análise de dados, busca-se evidenciar padrões de sub-representação e contribuir para discussões sobre equidade de gênero, especialmente no contexto da cultura pop e mídia digital.


## ❗ 3. Definição do Problema

Apesar da ampla produção de animes ao longo dos anos, observa-se que obras classificadas como *shoujo* tendem a apresentar menor visibilidade, popularidade e reconhecimento quando comparadas a outras demografias, como *shounen*.

Esse cenário levanta a hipótese de que fatores culturais, sociais e mercadológicos influenciam diretamente na distribuição e valorização desses conteúdos. Além disso, a possível ausência ou inconsistência de informações sobre demografia em bases de dados públicas pode dificultar análises mais profundas, reforçando a invisibilidade dessas categorias.

Dessa forma, o problema central deste projeto é:

> **Como a demografia dos animes impacta sua visibilidade e popularidade, e em que medida obras shoujo são sub-representadas em relação a outras categorias?**


## 💻 4. Tipo de Solução Proposta

A solução proposta consiste no desenvolvimento de um dashboard interativo de análise de dados, que permitirá a visualização e exploração de métricas relevantes relacionadas aos animes.


## 📊 5. Fontes de Dados

Serão utilizadas bases de dados públicas e uma API para coleta e enriquecimento das informações:

### 📁 Datasets:

* https://www.kaggle.com/datasets/azathoth42/myanimelist
* https://www.kaggle.com/datasets/CooperUnion/anime-recommendations-database
* https://www.kaggle.com/datasets/mikeytracegod/anime-viewers-data-1960s2025-10k

### 🌐 API:

* https://api.jikan.moe (API baseada no MyAnimeList)

Essas fontes fornecem dados sobre animes e sobre avaliações de úsuarios no MyAnimeList.

Os dados vão passar por etapas de limpeza, integração e enriquecimento para viabilizar a análise proposta.


## ⚙️ 6. Requisitos do Sistema

✅ 6.1 Requisitos Funcionais
- **RNF01**: Carregar e integrar dados de diferentes fontes (datasets e API)
- **RNF02**: Permitir filtragem de animes por demografia
- **RNF03**: Exibir gráficos de distribuição de animes por demografia
- **RNF04**: Apresentar métricas de popularidade (ex: número de membros)
- **RNF05**: Exibir notas médias por demografia
- **RNF06**: Permitir comparação entre categorias (shounen, shoujo, etc.)
- **RNF07**: Apresentar rankings de animes por popularidade e avaliação
- **RNF08**: Indicar ausência de dados (ex: demografia não informada)

### ⚙️ 6.2 Requisitos Não Funcionais

- **RNF01**: O dashboard deve apresentar uma interface clara e intuitiva, permitindo que usuários compreendam os dados sem necessidade de conhecimento técnico.
- **RNF02**: As visualizações devem ser carregadas de forma eficiente, garantindo tempo de resposta adequado durante a interação com os dados.
- **RNF03**: A aplicação deve ser executável em ambiente local, sem necessidade de conexão contínua com a internet após a obtenção dos dados.
- **RNF04**: O sistema deve garantir a consistência e integridade dos dados apresentados, evitando erros ou duplicidades nas informações exibidas.
- **RNF05**: As visualizações devem utilizar representações adequadas (gráficos e tabelas) que facilitem a comparação entre diferentes demografias de animes.
- **RNF06**: O sistema deve ser capaz de processar e visualizar conjuntos de dados de grande volume (até aproximadamente 400 mil registros) sem comprometer significativamente o desempenho.
- **RNF07**: O dashboard deve manter organização visual e padronização de layout, facilitando a navegação e interpretação das informações.

## 🚀 7. Considerações Iniciais

Este projeto busca unir análise de dados e reflexão social, explorando como fatores estruturais podem influenciar a visibilidade de diferentes tipos de conteúdo.

A partir da construção do dashboard, espera-se não apenas apresentar dados, mas também gerar insights relevantes sobre desigualdade de representação no universo dos animes.
