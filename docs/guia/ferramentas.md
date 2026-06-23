# Caderno de Ferramentas de Validação Digital

A auditoria de acessibilidade digital exige um arsenal técnico capaz de varrer o código-fonte e a interface renderizada em busca de barreiras de interação. As ferramentas automatizadas são a primeira linha de defesa no paradigma *Shift-Left*, permitindo que programadores e avaliadores identifiquem violações às diretrizes da WCAG 2.2 e à ABNT NBR 17225:2025 de forma ágil e padronizada.

Abaixo, apresenta-se a matriz comparativa e o microtutorial operacional das três principais ferramentas de varredura adotadas neste Guia.

## 1. Lighthouse (Google Chrome DevTools)

**Foco Técnico:** Auditoria rápida de desempenho e conformidade de acessibilidade em tempo de execução (*runtime*).

### Microtutorial de Execução

1. Abra o navegador Google Chrome e acesse a página alvo que será auditada.
2. Pressione a tecla `F12` (ou `Ctrl + Shift + I`) para abrir o painel do DevTools.
3. Navegue até a aba superior identificada como **Lighthouse**.
4. No painel de configuração, selecione a categoria **Accessibility** e escolha o dispositivo de simulação (Mobile ou Desktop).
5. Clique no botão **Analyze page load**. A ferramenta compilará um relatório detalhado com a nota de acessibilidade e a lista de elementos do DOM (*Document Object Model*) que precisam de correção.

## 2. WAVE (Web Accessibility Evaluation Tool)

**Foco Técnico:** Análise visual injetada diretamente na interface gráfica, destacando erros de contraste de cor, hierarquia semântica de cabeçalhos e estrutura de leitura para tecnologias assistivas.

### Microtutorial de Execução

1. Instale a extensão oficial do WAVE no seu navegador web (disponível para Chrome, Firefox ou Edge).
2. Acesse a página web que será submetida à avaliação.
3. Clique no ícone da extensão WAVE (geralmente localizado no canto superior direito do navegador).
4. Navegue pelo painel lateral esquerdo para analisar o resumo quantitativo: **Errors**, **Contrast Errors** e **Structure**.
5. Clique nos ícones injetados sobre os elementos da página para ler a justificativa da WCAG para cada falha apontada.

## 3. ASES (Avaliador e Simulador de Acessibilidade em Sítios)

**Foco Técnico:** Validação estrita baseada no Modelo de Acessibilidade em Governo Eletrônico (eMAG), sendo uma ferramenta nacional indispensável para a auditoria de portais do setor público brasileiro.

### Microtutorial de Execução

1. Acesse a plataforma web do ASES ou instale a sua respetiva extensão.
2. Insira a URL do portal governamental que será auditado ou cole diretamente o código HTML no campo de avaliação.
3. Execute a varredura para obter a matriz de resultados.
4. O ASES retornará o percentual de adequação do site, categorizando os achados em erros críticos, avisos e a nota final de aderência aos padrões nacionais de acessibilidade.

---

## 4. Os Limites da Automação: O Fator Humano em IHC

Embora as varreduras automatizadas sejam essenciais para o ganho de produtividade no ciclo de desenvolvimento, elas possuem limitações lógicas inerentes à sua natureza algorítmica. Do ponto de vista da Interação Humano-Computador (IHC), ferramentas automáticas conseguem detectar apenas uma parcela das barreiras reais de acessibilidade.

Um algoritmo é capaz, por exemplo, de verificar a presença estrutural do atributo textual alternativo (`alt`) numa tag de imagem (`<img>`), validando o código com sucesso. Contudo, a máquina é incapaz de julgar adequadamente o valor semântico, o contexto ou a clareza desse texto.

Se o programador preencher o atributo como `alt="imagem123"`, uma ferramenta automatizada poderá aprovar o critério técnico, mas o usuário que utiliza um leitor de tela continuará sem compreender a informação visual apresentada e enfrentará uma quebra significativa no seu modelo mental da interface.

Por essa razão estrutural, a automação nunca substitui o julgamento analítico humano. Para garantir a eficácia, a eficiência e a real satisfação no uso do sistema, é indispensável que a equipe de engenharia complemente as varreduras automáticas com testes manuais e empíricos.

Isso inclui a navegação exclusiva por teclado, para auditar armadilhas de foco e ordem de tabulação, e o uso real de leitores de tela, como NVDA, VoiceOver ou TalkBack, validando de forma holística a verdadeira comunicabilidade da interface digital.
