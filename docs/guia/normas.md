# Referencial Teórico e Marco Normativo

A acessibilidade não é opcional, mas sim um atributo inegociável de qualidade de software. No Brasil, a adoção de diretrizes inclusivas é o caminho para garantir autonomia e cidadania para mais de 18,6 milhões de brasileiros com deficiência, segundo a Pesquisa Nacional por Amostra de Domicílios Contínua (IBGE, 2022). Para assegurar essa inclusão e mitigar riscos jurídicos perante a Lei Brasileira de Inclusão (LBI), este Guia adota uma abordagem de complementaridade regulatória: unimos a didática e a cultura de desenho universal do Guia de Boas Práticas para Acessibilidade Digital (Brasil, 2023) com o rigor técnico e obrigatório da nova norma nacional (ABNT, 2025).

## 1. A Base Internacional: WCAG 2.2 e os Princípios P.O.U.R.

O alicerce técnico de qualquer avaliação de interface provém das Diretrizes de Acessibilidade para Conteúdo Web (WCAG 2.2). Segundo o W3C, interfaces inclusivas devem ser construídas sob quatro pilares:

* **Perceptíveis:** A informação e a interface devem ser claras e apresentadas de forma que os usuários possam percebê-las por diferentes sentidos.
* **Operáveis:** A navegação e os componentes devem ser utilizáveis por diversos dispositivos de entrada (como o uso exclusivo do teclado), oferecendo tempo suficiente para leitura e evitando armadilhas ou interações excludentes.
* **Compreensíveis:** A informação, os textos e a operação da interface devem ser lógicos, previsíveis e amparados por mecanismos de ajuda e prevenção de erros.
* **Robustos:** O código e a marcação semântica devem ser compatíveis com uma ampla gama de agentes de usuário, incluindo tecnologias assistivas atuais e futuras.

Os critérios da WCAG são classificados em três níveis:

1. **Nível A (Mínimo):** A página satisfaz todos os critérios de sucesso de Nível A. É o nível mais simples e oferece acessibilidade limitada, mas garante que um determinado número de pessoas não encontre barreiras básicas.

2. **Nível AA (Recomendado/Intermediário):** Satisfaz todos os critérios A e AA. É o nível recomendado para a maioria do conteúdo web, garantindo que muitas pessoas com deficiência não encontrem barreiras.

3. **Nível AAA (Aprimorado/Excelência):** Satisfaz todos os critérios A, AA e AAA. É o nível mais difícil de obter conformidade e não é indicado como requisito absoluto para todo o conteúdo, mas a sua adoção expande significativamente a acessibilidade.

## 2. O Foco Técnico da Auditoria: Perceptibilidade e Operabilidade

Para que um sistema interativo não imponha obstáculos aos cidadãos, é imprescindível focar primariamente na primeira metade dos princípios P.O.U.R.:

* **Aprofundando o Princípio Perceptível:** O conteúdo não pode ser invisível a todos os sentidos do usuário. Na prática da auditoria, elementos visuais informativos devem possuir alternativas em texto (atributos `alt` corretos), e o contraste visual deve ser alto o suficiente para evitar o aumento da carga cognitiva extrínseca.

* **Aprofundando o Princípio Operável:** A navegação deve ser utilizável primariamente pelo uso exclusivo do teclado. Isso exige foco visual explícito (`:focus`), ordem lógica de tabulação (`tabindex`) e controles acessíveis para pausar ou parar mídias dinâmicas, como carrosséis.

## 3. O Novo Marco Normativo: ABNT NBR 17225:2025

Publicada recentemente, a ABNT NBR 17225 é a primeira norma nacional exclusiva para aplicações web, definindo obrigações com foco total na independência física ou sensorial do usuario. A sua grande inovação para a engenharia de requisitos é a distinção clara entre o que é obrigação legal (textos com o verbo **"deve"**, configurando requisitos) e o que é boa prática (textos com o verbo **"convém"**, configurando recomendações).

A partir do alinhamento com a WCAG 2.2, a norma exige que as aplicações atinjam os seguintes graus de adequação jurídica:

* **Conformidade Regular:** É a barreira mínima legal para projetos. Exige o cumprimento de todos os itens estabelecidos como requisitos, garantindo, de forma simultânea, o atendimento aos níveis A e AA da WCAG 2.2.

* **Conformidade Plena:** Representa o estado da arte em acessibilidade. É atingida quando o sistema cumpre a Conformidade Regular e incorpora de forma ativa as recomendações associadas aos critérios AAA da WCAG. Caso a aplicação não cumpra determinada recomendação visando a conformidade plena, a norma exige a documentação de uma justificativa técnica razoável para a omissão.

