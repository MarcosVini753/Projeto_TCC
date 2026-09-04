# Protocolo de busca bibliográfica — TCC

**Versão:** v0.1  
**Data de início:** 03/09/2026  
**Status:** protocolo inicial, sujeito a refinamento após as primeiras buscas.

## Objetivo

Identificar trabalhos diretamente relacionados à classificação automática de issues/issue reports em repositórios de software, com atenção especial a:

- construção de benchmarks e datasets;
- taxonomias de tipos de issues;
- métodos clássicos de aprendizado de máquina;
- Transformers e modelos contextuais;
- protocolos de avaliação;
- generalização entre projetos;
- estudos envolvendo português ou português brasileiro.

## Tipo de levantamento

Este TCC não adota uma revisão sistemática da literatura como método principal. Será realizado um **levantamento bibliográfico estruturado e rastreável** para fundamentar o problema, as decisões metodológicas e a comparação com trabalhos relacionados.

Os trabalhos já identificados antes deste protocolo serão tratados como **trabalhos-semente de uma busca exploratória inicial**. A partir deles, serão realizadas novas buscas registradas em `log-buscas.csv` e rastreamento de referências/citações em `snowballing.csv`.

## Fontes de busca planejadas

- Google Scholar
- IEEE Xplore
- ACM Digital Library
- Scopus
- Springer Nature Link
- SBC OpenLib

Outras fontes poderão ser usadas de forma complementar para localizar versões publicadas, DOI, metadados ou trabalhos citados/citantes.

## Estratégias de busca

1. Busca por strings combinando termos do objeto, da tarefa e dos métodos.
2. **Backward snowballing:** inspeção das referências dos trabalhos selecionados.
3. **Forward snowballing:** inspeção de trabalhos posteriores que citam os estudos selecionados.
4. Registro de cada consulta em `log-buscas.csv` com data, base, string exata, filtros, quantidade de resultados, itens inspecionados e selecionados.

## Blocos conceituais iniciais

- **Objeto:** issue report, GitHub issue, bug report, issue tracker.
- **Tarefa:** classification, categorization, triage, labeling, issue type prediction.
- **Métodos:** machine learning, NLP, TF-IDF, SVM, Random Forest, Logistic Regression, Transformer, BERT.
- **Contexto linguístico:** Portuguese, Brazilian Portuguese, português, pt-BR.

## Trabalhos-semente iniciais — Top 5 do Notion

- **P01** — Kallis et al. — *The NLBSE'23 Tool Competition*. DOI: https://doi.org/10.1109/NLBSE59153.2023.00007
- **P02** — Kallis et al. — *Predicting Issue Types on GitHub / Ticket Tagger*. DOI: https://doi.org/10.1016/j.scico.2020.102598
- **P03** — Izadi — *CatIss: An Intelligent Tool for Categorizing Issues Reports using Transformers*. DOI: https://doi.org/10.1145/3528588.3528662
- **P04** — Andrade et al. — *An Empirical Study on the Classification of Bug Reports with Machine Learning*. DOI: https://doi.org/10.1109/OJCS.2026.3692087
- **P05** — Nadeem et al. — *Automatic Issue Classifier: A Transfer Learning Framework for Classifying Issue Reports*. DOI: https://doi.org/10.1109/ISSREW53611.2021.00113

## Triagem e extração

Para cada estudo selecionado, `matriz-estudos.csv` registrará, quando disponível:

- dataset;
- idioma;
- número de issues;
- classes;
- representação textual;
- modelos;
- estratégia de split;
- métricas;
- principal resultado;
- limitações;
- contribuição para o TCC.

## Critérios preliminares de inclusão

- Trabalhos que estudem classificação, categorização, triagem ou rotulação automática de issues/bug reports.
- Trabalhos que proponham ou utilizem datasets/benchmarks relevantes para a tarefa.
- Trabalhos que avaliem métodos de NLP ou aprendizado de máquina aplicáveis ao problema.
- Trabalhos que contribuam para decisões metodológicas do TCC, como taxonomia, split, métricas ou generalização.

## Critérios preliminares de exclusão

- Trabalhos sem relação direta com artefatos textuais de Engenharia de Software ou issue trackers.
- Trabalhos cujo foco seja outra tarefa e que não ofereçam contribuição metodológica clara para este TCC.
- Duplicatas ou versões preliminares quando houver versão final publicada mais adequada para citação e análise.

## Rastreabilidade

- `log-buscas.csv`: registra **como** cada busca foi realizada.
- `matriz-estudos.csv`: registra **o que** cada estudo fez e o que será aproveitado.
- `snowballing.csv`: registra trabalhos encontrados a partir das referências e citações dos estudos-semente/selecionados.

## Observação metodológica

A afirmação sobre inexistência ou escassez de benchmark comparável em português brasileiro será tratada como **resultado do levantamento bibliográfico**, e não como pressuposto inicial da pesquisa.
