# Plano de Testes — Dashboard de Análise de Demografia de Animes

## 1. Objetivo dos Testes

O objetivo deste plano de testes é validar o funcionamento dos dashboards desenvolvidos para análise da influência da demografia na visibilidade e popularidade de animes, garantindo a integridade dos dados, funcionamento das funcionalidades e qualidade das visualizações apresentadas.

Os testes visam verificar:
- Funcionamento correto dos dashboards;
- Consistência dos dados apresentados;
- Funcionamento dos filtros e interações;
- Carregamento adequado dos gráficos;
- Responsividade e usabilidade da interface;
- Tratamento de erros e ausência de dados.

---

# 2. Escopo dos Testes

Serão realizados testes funcionais e não funcionais nos dois dashboards desenvolvidos em HTML.

## Funcionalidades testadas
- Carregamento dos datasets;
- Integração com a API do [MyAnimeList](https://myanimelist.net?utm_source=chatgpt.com);
- Exibição de gráficos;
- Filtros por demografia;
- Rankings de popularidade;
- Exibição de notas médias;
- Tratamento de dados ausentes;
- Responsividade da interface.

---

# 3. Tipos de Testes

## 3.1 Testes Funcionais
Verificam se as funcionalidades do sistema operam corretamente de acordo com os requisitos definidos.

## 3.2 Testes de Interface
Avaliam organização visual, legibilidade e interação com os elementos gráficos.

## 3.3 Testes de Responsividade
Validam o comportamento do dashboard em diferentes tamanhos de tela.

## 3.4 Testes de Desempenho
Verificam tempo de carregamento e comportamento com grande volume de dados.

---

# 4. Casos de Teste

| ID | Caso de Teste | Objetivo | Resultado Esperado | Status |
|---|---|---|---|---|
| TC01 | Abrir dashboard principal | Verificar carregamento inicial | Dashboard deve abrir sem erros | OK |
| TC02 | Carregar dados dos datasets | Validar leitura dos dados | Dados devem ser exibidos corretamente | OK |
| TC03 | Integrar dados da API | Validar comunicação com API | Dados complementares devem aparecer corretamente | OK |
| TC04 | Filtrar por demografia shoujo | Validar funcionamento do filtro | Apenas animes shoujo devem ser exibidos | OK |
| TC05 | Filtrar por demografia shounen | Validar funcionamento do filtro | Apenas animes shounen devem ser exibidos | OK |
| TC06 | Exibir gráfico de distribuição | Validar renderização dos gráficos | Gráfico deve apresentar os dados corretamente | OK |
| TC07 | Exibir notas médias | Validar cálculo das médias | Médias devem corresponder aos dados processados | OK |
| TC08 | Exibir ranking de popularidade | Validar ordenação dos rankings | Ranking deve ser exibido em ordem correta | OK |
| TC09 | Identificar ausência de demografia | Validar tratamento de dados faltantes | Sistema deve indicar dados ausentes corretamente | OK |
| TC10 | Testar interação com gráficos | Validar interatividade | Tooltips e interações devem funcionar | OK |
| TC11 | Testar tempo de carregamento | Avaliar desempenho | Dashboard deve carregar rapidamente | OK |
| TC12 | Testar responsividade em celular | Validar adaptação do layout | Interface deve permanecer organizada | OK |
| TC13 | Testar responsividade em notebook | Validar layout em tela média | Elementos devem permanecer alinhados | OK |
| TC14 | Simular falha de conexão | Validar tratamento de erros | Sistema deve exibir mensagem amigável | OK |
| TC15 | Navegar entre dashboards | Validar navegação | Troca entre páginas deve funcionar corretamente | OK |

---

# 5. Critérios de Sucesso

Os testes serão considerados aprovados quando:
- Todas as funcionalidades executarem sem erros;
- Os dados apresentados forem consistentes;
- Os gráficos forem exibidos corretamente;
- A interface permanecer organizada em diferentes dispositivos;
- Não houver falhas críticas durante a navegação.

---

# 6. Ferramentas Utilizadas

- HTML
- JavaScript
- API oficial do [MyAnimeList](https://myanimelist.net/apiconfig/references/api/v2?utm_source=chatgpt.com)
- Bases de dados do [Kaggle](https://www.kaggle.com?utm_source=chatgpt.com)
- Navegador Google Chrome

---

# 7. Considerações Finais

A execução dos testes permite validar a qualidade e confiabilidade dos dashboards desenvolvidos, garantindo que as análises apresentadas sejam consistentes e compreensíveis para os usuários.

Além da validação técnica, os testes contribuem para assegurar que o projeto cumpra sua proposta de analisar possíveis desigualdades de visibilidade entre diferentes demografias de animes, especialmente obras classificadas como shoujo.