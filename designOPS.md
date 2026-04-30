## 1. Introdução, Objetivo e Filosofia DesignOps

### Contexto e objetivo
No contexto da construção do nosso módulo de CI/CD para o parceira do projeto (Jacto Drones), a entrega contínua de valor exige que a interface e a experiência do usuário (UX) fluam sem atritos pela nossa esteira de automação. O objetivo desta seção é fundamentar a arquitetura da nossa infraestrutura operacional, adotando a premissa fundamental de que a prática de DesignOps deve ser encarada e operada como o "DevOps do Design".

### 1.1. A Filosofia: DesignOps como o DevOps do Design
Historicamente, o DevOps emergiu (com destaque a partir da palestra de Patrick Debois na Agile 2008) para solucionar gargalos de eficiência e conflitos operacionais entre as áreas de desenvolvimento e operações de TI. Trata-se de uma abordagem cultural e técnica que melhora a colaboração, automação e produtividade rumo à integração e entrega contínuas. 

De maneira análoga, o DesignOps é a prática de otimizar processos, infraestrutura e ferramentas que dão suporte ao trabalho de design. Sua filosofia baseia-se na orquestração e otimização de pessoas e fluxos de trabalho para amplificar o impacto e o valor do design em escala. No fluxo de entrega contínua, o DesignOps atua para que as definições de componentes e protótipos sejam validadas e transpostas para código de maneira tão automatizada quanto as próprias builds de software.

### 1.2. Os Três Pilares Operacionais
Para estruturar as operações em nosso time, baseamos nossa governança nos três pilares estabelecidos pelo Nielsen Norman Group (NN/g):
* **Como trabalhamos juntos (*How we work together*):** Foco em Organizar (estrutura e papéis), Colaborar (rituais e ambientes) e Humanizar (desenvolvimento e embarque).
* **Como realizamos o trabalho (*How we get work done*):** Esforço para Padronizar processos, Harmonizar o sistema (Design System) e Priorizar o fluxo de trabalho de forma equilibrada.
* **Como nosso trabalho cria impacto (*How our work creates impact*):** Estratégias para Medir o desempenho, Socializar o sucesso (recompensas) e Possibilitar o avanço técnico (guias e treinamentos).

### 1.3. Paralelo: DevOps ↔ DesignOps
Para que a esteira CI/CD seja bem-sucedida, estabelecemos o seguinte pareamento funcional entre engenharia e design no projeto:

| Dimensão | DevOps | DesignOps |
| :--- | :--- | :--- |
| **Automação e Ferramentas** | Utiliza ferramentas de CI/CD para automatizar a construção, teste e implantação do software de forma sistêmica. | Implementa sistemas para automatizar fluxos de trabalho de design, gestão de ativos e prototipagem (ex: Design Tokens pipeline). |
| **Integração e Colaboração** | Promove integração contínua facilitando a resolução de problemas de infraestrutura rapidamente. | Enfatiza a integração entre designers e desenvolvedores para que as decisões de design sejam implementadas com fidelidade. |
| **Ciclos de Feedback Rápido** | Feedback veloz devido à integração e testes automatizados (Test, Build, Deploy). | Avaliação rápida por meio de revisões sistemáticas, testes de usuários e iterações constantes de usabilidade. |
| **Qualidade e Consistência** | Foco em entregar software escalável através de monitoramento. | Foco em assegurar consistência usando guias de estilo, bibliotecas de componentes e auditorias de UI. |

Ambas as abordagens visam a quebra de silos, a colaboração multidisciplinar, a eficiência operacional e a entrega contínua de valor de ponta a ponta.

### Decisões de trade-off
* **Cultura Estrutural vs. Adoção Puramente Ferramental:** No planejamento do nosso modelo de DesignOps, consideramos inicialmente a adoção exclusiva de ferramentas de versionamento visual. Descartamos essa via técnica isolada pois a história inicial do DevOps demonstrou que focar unicamente em agilidade de infraestrutura oferece uma "visão parcial" que não resolve conflitos reais entre equipes. Optamos por um *rollout* híbrido, onde a mudança de processos e rituais antecede a configuração dos *pipelines* técnicos.
* **Padronização Total vs. Autonomia:** Consideramos aplicar políticas rígidas para todos os componentes criados. Como *trade-off*, relaxamos essa regra na fase de ideação (Discovery) para não reduzir a velocidade criativa. O rigor da padronização (linting, revisão) só ocorre ao tentar inserir componentes na biblioteca global (Delivery).

### Referências da Seção 1
[1] Kaplan, K. (Nielsen Norman Group). *DesignOps 101*.
[2] Atlassian. *O que é DevOps?*. URL: https://www.atlassian.com/br/devops
[3] Gaea. *Conheça a incrível história do DevOps*. URL: https://gaea.com.br/conheca-a-incrivel-historia-do-devops/

**Responsável:** Davi Versan