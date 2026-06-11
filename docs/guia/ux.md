# Introdução à Engenharia de UX e Empatia

O desenvolvimento de sistemas computacionais contemporâneos exige a superação definitiva do paradigma da "Ilha Tecnológica", uma visão limitante que compreende o software puramente como um bloco isolado de código, um conjunto de funções algorítmicas ou uma pilha estática de arquitetura de dados. No ecossistema da Engenharia de Software voltada para o cidadão, as plataformas digitais não operam em vácuo social; elas constituem o motor central de ecossistemas de serviços complexos e interconectados, nos quais a qualidade de uso e a comunicabilidade da interface determinam o sucesso ou a falha catastrófica de políticas institucionais e direitos fundamentais.

Projetar interfaces acessíveis, inclusivas e universais não se resume a um recurso cosmético opcional, um refinamento estético de design ou uma mera lista de checagem técnica a ser cumprida de forma reativa. Sob a ótica da Interação Humano-Computador (IHC), a acessibilidade digital consolida-se como um requisito de qualidade não funcional de altíssima prioridade, mandatório para garantir a eficácia, a eficiência e a satisfação de sistemas interativos. A engenharia de interfaces deve atuar de forma preditiva, alinhando duas variáveis críticas mapeadas pela literatura clássica de fatores humanos: os Modelos Mentais dos utilizadores e a Carga Cognitiva imposta pelas barreiras de interação.

O desalinhamento destas variáveis em portais governamentais e jurídicos – como o portal do Tribunal Regional Federal da 1ª Região (TRF1) – gera severas fraturas de usabilidade que marginalizam grupos vulneráveis. Para mitigar estes riscos operacionais e jurídicos, este Guia adota como pilares técnicos as diretrizes internacionais do Web Content Accessibility Guidelines (WCAG 2.2) e a sua respetiva internalização normativa brasileira pela ABNT NBR 17225:2025, promovendo a inclusão digital por meio do rigor analítico.

## 1. Modelos Mentais na Experiência do Usuário

Conforme postulam Barbosa e Silva (2010), os modelos mentais são estruturas psicológicas, dinâmicas e frequentemente instáveis, que os indivíduos constroem internamente para compreender, explicar e prever o funcionamento de um determinado sistema, objeto ou fenómeno. Ao interagir com uma interface digital, o utilizador comum não possui visibilidade, e nem necessita possuir, sobre a lógica do código-fonte ou sobre as consultas estruturadas executadas nos bancos de dados do backstage. Em vez disso, o indivíduo projeta na tela as suas experiências prévias com outros sistemas, os seus vieses conceituais, as suas analogias cotidianas e as suas expectativas comportamentais.

A Engenharia de IHC identifica três conceitos interdependentes neste processo:

* **O Modelo de Design:** A estrutura conceitual do sistema idealizada pelos engenheiros e designers.
* **A Imagem do Sistema:** A manifestação física e interativa da interface (menus, rótulos, comportamentos de foco, links e fluxos).
* **O Modelo Mental do Utilizador:** A teoria interna desenvolvida pelo cidadão ao interagir com a imagem do sistema.

A harmonia da interação ocorre quando a imagem do sistema comunica com clareza a lógica do modelo de design, permitindo que o utilizador crie um modelo mental preciso e preditivo. Contudo, quando a interface falha em fornecer pistas semânticas adequadas — omitindo o indicador de foco visual do teclado, quebrando a hierarquia lógica de títulos, utilizando rótulos ambíguos em botões ou negligenciando descrições alternativas em imagens informativas —, manifesta-se uma ruptura severa entre o utilizador e o sistema. Esta desconexão desorienta o utilizador, induz ao erro involuntário, gera extrema frustração e destrói o princípio da autonomia digital, transformando a interface numa barreira burocrática intransponível.

## 2. Carga Cognitiva e Ruído de Interface

A carga cognitiva refere-se ao volume total de esforço mental e processamento na memória de curto prazo (ou memória de trabalho) exigido de um ser humano para executar uma determinada tarefa computacional. A memória de trabalho humana possui limitações biológicas estritas de capacidade e retenção temporal. Na disciplina de IHC, a carga cognitiva é classificada em três dimensões distintas:

* **Carga Cognitiva Intrínseca:** Associada à complexidade inerente da própria tarefa que o utilizador deseja realizar (ex.: compreender os trâmites legais de um processo jurídico).
* **Carga Cognitiva Pertinente (Germane):** O esforço mental benéfico, dedicado ao processamento, construção de esquemas e aprendizagem do conteúdo.
* **Carga Cognitiva Extrínseca (Extraneous):** O esforço mental puramente desperdiçado devido ao mau design da interface, ruídos visuais e falhas lógicas de navegação.

Interfaces governamentais saturadas de informações, carrosséis de imagens em movimento perpétuo sem controlos explícitos de interrupção, textos longos com baixo rácio de contraste visual e formulários extensos sem mecanismos de validação preditiva em tempo real sobrecarregam massivamente a carga cognitiva extrínseca do utilizador.

Para indivíduos com limitações cognitivas situacionais (como stresse, fadiga extrema ou distrações ambientais) ou permanentes (como Transtorno do Défice de Atenção com Hiperatividade – TDAH, dislexia e o declínio cognitivo associado ao envelhecimento natural), este ruído interativo exaure os recursos de atenção que deveriam ser aplicados exclusivamente na resolução do seu problema prático.

O software acessível deve atuar como um mediador invisível e previsível, eliminando fricções periféricas para poupar a capacidade de processamento mental do cidadão.

## 3. Acessibilidade por Design (Shift-Left)

A mitigação definitiva das falhas de acessibilidade e das quebras nos modelos mentais exige a adoção rigorosa do paradigma da Acessibilidade por Design, conceitualmente correlacionado à abordagem *Shift-Left* (deslocamento para a esquerda) na Engenharia de Software contemporânea.

Tradicionalmente, os testes de acessibilidade e usabilidade eram relegados à periferia do ciclo de vida do desenvolvimento, executados como auditorias corretivas aplicadas às pressas nas vésperas do lançamento do produto. Tal prática resulta em "remendos" de interface superficiais que não resolvem as falhas estruturais subjacentes e aumentam exponencialmente os custos de manutenção de software.

A filosofia *Shift-Left* determina que a acessibilidade e a empatia com o utilizador devem ser injetadas de forma proativa na fase de conceção, elicitação de requisitos e modelagem da arquitetura de informação. Ao tratar a acessibilidade como um requisito de arquitetura primário, a equipa assegura árvores de elementos semanticamente coerentes, fluxos previsíveis e layouts robustos.

Esta postura preventiva blinda o projeto contra retrabalhos analíticos dispendiosos em fases avançadas de maturação do sistema, transformando métricas brutas de conformidade legal em valor real, dignidade e inclusão para a sociedade.
