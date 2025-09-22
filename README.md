**SentiClick: Análise de Segmentação Dinâmica de Clientes**

Este projeto, chamado SentiClick, é uma solução analítica desenvolvida para a TOTVS, focada em resolver o problema da segmentação estática de clientes. Ele permite que a empresa entenda o comportamento dos seus clientes de forma dinâmica, ajudando a ajustar estratégias de atendimento, retenção e expansão de receita.

**1. O Problema**

Empresas que oferecem serviços contínuos, como a TOTVS, têm dificuldade em monitorar e segmentar o comportamento de seus clientes ao longo do tempo. Isso leva a estratégias desatualizadas, que não acompanham as mudanças no comportamento do cliente, prejudicando a satisfação e o crescimento da receita.

**2. A Solução: SentiClick**

A SentiClick é uma plataforma de análise que combina dados internos e externos para criar **segmentações dinâmicas de clientes**. Ela opera no modelo SaaS (Software as a Service) e utiliza:

* **Dados Internos:** Informações comportamentais dos clientes, como engajamento, uso do produto, interações com o suporte e pontuações de satisfação (NPS).
* **Dados Externos:** Análise de menções à TOTVS no Reclame Aqui para extrair sentimentos, tópicos e dados geográficos.

Os resultados são apresentados em um dashboard visual, onde uma **IA Generativa** sintetiza explicações em linguagem natural. A solução é baseada em uma arquitetura de nuvem híbrida e os modelos de análise são retreinados automaticamente, garantindo que os insights estejam sempre atualizados.

---

**3. Metodologia do Projeto**

O desenvolvimento da SentiClick seguiu um processo rigoroso, desde a coleta dos dados até a modelagem e validação estatística.

**3.1. Fonte e Pré-processamento dos Dados**

* **Fonte de Dados:** O projeto não utilizou uma única fonte, mas consolidou dados de **17 fontes distintas**, agregando-as em um único conjunto de dados em nível de cliente.
* **Redução e Agregação:** Uma base massiva de bilhões de linhas de transações foi reduzida para um dataset mais gerenciável, contendo **910 clientes e 48 variáveis**. Essa agregação foi feita usando métricas como médias e contagens.
* **Janela Temporal:** Para garantir a consistência, todos os dados foram limitados a uma janela temporal única de **2024**.
* **Tratamento de Faltantes:** Valores ausentes foram tratados com estratégias específicas, garantindo que o dataset final tivesse **0% de missingness**.

**3.2. Features (Variáveis) Utilizadas**

As 48 variáveis do dataset foram categorizadas para melhor entendimento dos padrões de comportamento do cliente:

* **Financeiras:** Variáveis como `mrr12m_avg` e `contrato_media` para entender o valor financeiro de cada cliente.
* **De Engajamento e Uso:** Métricas como `h_qtd` (quantidade de solicitações de suporte) e `h_vl_total_sum` (valor total de uso do produto) para medir a interação do cliente.
* **De Satisfação:** Variáveis como `npsr_media` e `nts_media` para capturar o nível de satisfação do cliente.

**3.3. Machine Learning e Clusterização**

* **Algoritmo:** Foi utilizado o algoritmo de clusterização não supervisionada **K-means**.
* **Pré-processamento:** Antes da modelagem, os dados foram normalizados com o **StandardScaler** para dar a todas as variáveis a mesma importância.
* **Validação Estatística:** A definição de **3 clusters** foi justificada pelo método do cotovelo e validada com análises estatísticas rigorosas, como **ANOVA** e o **Teste de Tukey HSD**, para garantir que as diferenças entre os grupos fossem significativas.

---

**4. Perfis dos Clusters**

Com base na análise das variáveis, foram identificados 3 perfis distintos de clientes, cada um com suas características específicas.

* **Cluster 0 (Os Silenciosos):** Clientes com baixa interação e baixo volume de suporte, mas com **alta satisfação**. Suas médias de NTS e NPS são elevadas.
* **Cluster 1 (As Âncoras):** Este é o grupo de **alto valor e engajamento**. Eles têm as maiores médias em variáveis financeiras e de uso do produto, além de alta satisfação.
* **Cluster 2 (Os Crescentes):** Clientes que **demandam mais atenção**. Apresentam a menor satisfação entre os três grupos e o maior volume de solicitações de suporte.

A SentiClick permite que a TOTVS personalize suas estratégias para cada um desses perfis, otimizando o atendimento, a retenção e o crescimento da receita.

---

**5. Conclusão**

A jornada de desenvolvimento da SentiClick foi uma oportunidade valiosa de aplicar e aprofundar diversas competências. Este projeto não apenas transformou dados em inteligência de negócio, mas também solidificou habilidades cruciais, como a **capacidade de resolver problemas complexos**, a **análise crítica de dados de múltiplas fontes**, e o **domínio de técnicas de pré-processamento e modelagem estatística**. Ao lidar com os desafios do mundo real, como o tratamento de dados faltantes e a validação estatística de modelos, colocamos em prática o conhecimento teórico, consolidando um aprendizado essencial para a carreira. O resultado final, a SentiClick, é a prova de que a teoria, quando aplicada pode gerar soluções de alto impacto.

---
Time DataJorneyX
Janaina de Souza Silva
Jaqueline Andrade Bidoia 
Julia Silva de Oliveira 
Monica de Araujo 
Sofia Mesquita 


