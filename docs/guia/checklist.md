### 📊 Critérios de Avaliação e Algoritmo de Conformidade

A matriz deste checklist interativo foi estruturada com base na criticidade das barreiras de acesso, inspirada nos níveis de validação do WCAG 2.2 e da ABNT NBR 17225:2025. O nosso sistema não atribui "pesos" numéricos distintos por item; em vez disso, trata os 23 critérios como requisitos booleanos (Atende / Não Atende) de igual valor fracional. A justificativa para isso é que, em acessibilidade digital, a violação de um único critério crítico (como a impossibilidade de navegação por teclado) pode gerar exclusão sistêmica severa, independentemente do sucesso nos demais itens.

A lógica dos intervalos da barra de progresso foi definida analiticamente da seguinte forma:

* **🔴 Risco Crítico de Exclusão (0 a 20 itens / Abaixo de 50%):** O sistema reprova na maioria simples dos testes. Apresenta falhas de Nível A (ex: falta de semântica ou foco oculto), bloqueando completamente a jornada de usuários com deficiências severas ou que dependem de tecnologias assistivas.
* **🟡 Conformidade Parcial (21 a 40 itens / 51% a 99%):** O limite de 21 itens representa a superação da maioria simples. Nesta faixa, o site garante a operabilidade das funções vitais e permite a navegação básica, mas ainda peca em critérios de Nível AA (ex: contraste insuficiente em telas secundárias ou falta de expansão visual), exigindo um elevado esforço cognitivo do usuário.
* **🟢 Conformidade Regular Alcançada (41 itens / 100%):** O sistema atende plenamente aos requisitos de engenharia de *front-end* estipulados para a avaliação, garantindo uma interface universal e sem fricção.

---
<style>
  .checklist-container {
    background: #ffffff;
    padding: 25px;
    border-radius: 10px;
    border: 1px solid #d1d5db;
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    box-shadow: 0 4px 6px rgba(0,0,0,0.05);
  }
  .ihc-block {
    margin-bottom: 25px;
    padding-bottom: 15px;
    border-bottom: 1px solid #f3f4f6;
  }
  .ihc-block h4 {
    color: #1f2937;
    margin-bottom: 15px;
    font-size: 1.1rem;
    border-left: 4px solid #3b82f6;
    padding-left: 10px;
  }
  .checklist-item {
    margin-bottom: 12px;
    display: flex;
    align-items: flex-start;
    padding: 8px;
    border-radius: 5px;
    transition: background-color 0.2s;
  }
  .checklist-item:hover {
    background-color: #f9fafb;
  }
  .checklist-item input[type="checkbox"] {
    margin-top: 4px;
    margin-right: 15px;
    transform: scale(1.3);
    cursor: pointer;
    accent-color: #3b82f6;
  }
  .checklist-item label {
    font-size: 14px;
    color: #4b5563;
    line-height: 1.5;
    cursor: pointer;
    width: 100%;
  }
  .checklist-item strong {
    color: #111827;
  }
  .progress-section {
    position: sticky;
    bottom: 0;
    background: white;
    padding: 20px 0;
    margin-top: 20px;
    border-top: 2px dashed #d1d5db;
  }
  .progress-bar-container {
    width: 100%;
    background-color: #e5e7eb;
    border-radius: 20px;
    height: 28px;
    overflow: hidden;
  }
  .progress-bar {
    height: 100%;
    background-color: #ef4444;
    width: 0%;
    transition: width 0.5s ease-out, background-color 0.5s ease;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
    font-size: 12px;
  }
  #score-text {
    font-weight: bold;
    font-size: 18px;
    margin-top: 12px;
    display: block;
    text-align: center;
    color: #ef4444;
  }
  .auditoria-nota {
    background-color: #fef3c7;
    border-left: 4px solid #f59e0b;
    padding: 15px;
    font-size: 13px;
    color: #92400e;
    margin-bottom: 20px;
    border-radius: 4px;
    line-height: 1.5;
  }
</style>

<div class="checklist-container">
  <h2 style="text-align: center; margin-bottom: 10px;">Checklist Completo de Verificação IHC (41 Itens)</h2>
  
  <div class="auditoria-nota">
    <strong>Nota de Auditoria:</strong> Ferramentas automáticas como Lighthouse e ASES capturam apenas de 30% a 40% dos problemas. A inspeção manual da árvore de elementos por um analista WCAG é indispensável para garantir a conformidade com a NBR 17225:2025.
  </div>
  
  <div class="ihc-block">
    <h4>Estrutura Global e Idioma da Aplicação</h4>
    <div class="checklist-item"><input type="checkbox" id="chk1" class="ihc-check"><label for="chk1"><strong>Idioma Principal (lang):</strong> A tag mestre &lt;html&gt; possui o atributo lang="pt-BR" configurado corretamente? (Se omitido ou incorreto, os leitores de tela adotarão sotaques estrangeiros, inviabilizando a compreensão lógica).</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk2" class="ihc-check"><label for="chk2"><strong>Links de Salto (Skip Links):</strong> Existem links internos ocultos logo no início do código (ex: "Ir para o conteúdo principal") que se tornam visíveis ao primeiro comando Tab?</label></div>
  </div>

  <div class="ihc-block">
    <h4>Arquitetura Semântica e Navegação Estrutural</h4>
    <div class="checklist-item"><input type="checkbox" id="chk3" class="ihc-check"><label for="chk3"><strong>Marcos Semânticos (Landmarks):</strong> O código utiliza as tags estruturais do HTML5 puro para delimitar as zonas de tela (&lt;header&gt;, &lt;nav&gt;, &lt;main&gt;, &lt;footer&gt;) em vez de aninhar múltiplos blocos genéricos de &lt;div&gt;?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk4" class="ihc-check"><label for="chk4"><strong>Hierarquia Rígida de Títulos:</strong> A interface possui uma árvore de títulos coerente? Existe apenas um único &lt;h1&gt; por página? Os subtítulos seguem uma ordem estrita sem pular níveis lógicos (como pular de um h2 direto para um h5)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk5" class="ihc-check"><label for="chk5"><strong>Validação de Sintaxe e IDs:</strong> A árvore DOM está livre de IDs duplicados (id="...") que quebram o mapeamento de leitores de tela?</label></div>
  </div>

  <div class="auditoria-nota" style="background-color: #e0f2fe; border-left-color: #3b82f6; color: #1e3a8a;">
    <strong>Bloco A: Elementos de Interação e Formulários no Backstage</strong><br>
  </div>

  <div class="ihc-block">
    <h4>Conteúdo e Linguagem Compreensível</h4>
    <div class="checklist-item"><input type="checkbox" id="chk6" class="ihc-check"><label for="chk6"><strong>Linguagem Simples:</strong> Os textos utilizam frases diretas, palavras conhecidas e estruturas objetivas, evitando termos jurídicos ou técnicos desnecessários?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk7" class="ihc-check"><label for="chk7"><strong>Explicação de Siglas:</strong> Siglas, abreviações e expressões especializadas são explicadas na primeira vez em que aparecem?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk8" class="ihc-check"><label for="chk8"><strong>Títulos Descritivos:</strong> Os títulos identificam claramente o assunto ou a finalidade de cada página, seção ou etapa da tarefa?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk9" class="ihc-check"><label for="chk9"><strong>Links Descritivos:</strong> O texto de cada link informa claramente seu destino, evitando expressões genéricas como “clique aqui” ou “saiba mais”?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk10" class="ihc-check"><label for="chk10"><strong>Consistência de Nomenclatura:</strong> Elementos que possuem a mesma função são identificados com os mesmos termos ao longo da interface?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk11" class="ihc-check"><label for="chk11"><strong>Previsibilidade da Interação:</strong> A seleção, o preenchimento ou o foco em um componente evita mudanças inesperadas de contexto (como abertura automática ou envio imediato)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk12" class="ihc-check"><label for="chk12"><strong>Disponibilidade de Ajuda:</strong> Tarefas complexas possuem instruções, exemplos ou mecanismos de ajuda facilmente localizáveis?</label></div>
  </div>

  <div class="ihc-block">
    <h4>Identificação e Instruções dos Campos</h4>
    <div class="checklist-item"><input type="checkbox" id="chk13" class="ihc-check"><label for="chk13"><strong>Rótulos de Formulário (&lt;label&gt;):</strong> Todos os campos de entrada possuem um rótulo associado explicitamente ao campo (for e id)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk14" class="ihc-check"><label for="chk14"><strong>Campos Obrigatórios:</strong> Os campos obrigatórios são identificados por texto ou símbolo, sem depender exclusivamente da cor?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk15" class="ihc-check"><label for="chk15"><strong>Formato Esperado:</strong> A interface informa previamente o formato esperado para dados (CPF, data, senha)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk16" class="ihc-check"><label for="chk16"><strong>Instruções Associadas:</strong> Instruções complementares estão associadas programaticamente ao campo (ex: aria-describedby)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk17" class="ihc-check"><label for="chk17"><strong>Agrupamento de Campos:</strong> Conjuntos de opções relacionados utilizam elementos como &lt;fieldset&gt; e &lt;legend&gt; para comunicar seu contexto?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk18" class="ihc-check"><label for="chk18"><strong>Preenchimento Automático:</strong> Campos de dados pessoais utilizam atributos como 'autocomplete' quando aplicável?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk19" class="ihc-check"><label for="chk19"><strong>Semântica de Botões e Links:</strong> Elementos que executam ações usam a tag &lt;button&gt;, enquanto elementos que navegam usam a tag &lt;a&gt;?</label></div>
  </div>

  <div class="ihc-block">
    <h4>Prevenção, Identificação e Correção de Erros</h4>
    <div class="checklist-item"><input type="checkbox" id="chk20" class="ihc-check"><label for="chk20"><strong>Identificação Clara do Erro:</strong> Quando ocorre uma falha, a interface identifica explicitamente qual campo apresenta o problema?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk21" class="ihc-check"><label for="chk21"><strong>Descrição do Problema:</strong> A mensagem de erro explica objetivamente o que está incorreto, evitando avisos genéricos?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk22" class="ihc-check"><label for="chk22"><strong>Sugestão de Correção:</strong> A interface informa como o usuário pode corrigir o erro, apresentando o valor esperado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk23" class="ihc-check"><label for="chk23"><strong>Indicação por Mais de um Recurso:</strong> Os erros são comunicados por texto ou ícone, sem utilizar somente a cor como identificação?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk24" class="ihc-check"><label for="chk24"><strong>Associação entre Erro e Campo:</strong> As mensagens de erro estão associadas programaticamente aos respectivos campos (leitores de tela)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk25" class="ihc-check"><label for="chk25"><strong>Preservação de Dados:</strong> Após um erro de validação, as informações já preenchidas corretamente permanecem salvas?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk26" class="ihc-check"><label for="chk26"><strong>Resumo de Erros:</strong> Em formulários extensos, a interface apresenta um resumo dos erros e permite navegação direta até eles?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk27" class="ihc-check"><label for="chk27"><strong>Revisão antes da Confirmação:</strong> Em ações críticas (jurídicas/financeiras), o usuário pode revisar ou corrigir dados antes do envio definitivo?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk28" class="ihc-check"><label for="chk28"><strong>Confirmação de Envio:</strong> Após envio bem-sucedido, a interface apresenta uma mensagem clara com protocolo/próximos passos?</label></div>
  </div>

  <div class="ihc-block">
    <h4>Robustez e Compatibilidade com Tecnologias Assistivas</h4>
    <div class="checklist-item"><input type="checkbox" id="chk29" class="ihc-check"><label for="chk29"><strong>Nome, Função, Valor e Estado:</strong> Componentes personalizados comunicam corretamente às tecnologias assistivas seu nome e estado atual?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk30" class="ihc-check"><label for="chk30"><strong>Mensagens Dinâmicas:</strong> Alertas e confirmações dinâmicos são anunciados aos leitores de tela (ex: regiões aria-live)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk31" class="ihc-check"><label for="chk31"><strong>Estados de Componentes:</strong> Menus e abas informam corretamente estados como aberto, fechado, selecionado ou desabilitado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk32" class="ihc-check"><label for="chk32"><strong>Dependência Visual:</strong> As instruções não dependem exclusivamente de posição, formato, tamanho ou cor (ex: "botão vermelho à direita")?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk33" class="ihc-check"><label for="chk33"><strong>Validação Prática:</strong> O formulário foi testado com navegação por teclado e leitor de tela para verificar a ordem de anúncios?</label></div>
  </div>

  <div class="auditoria-nota" style="background-color: #ecfdf5; border-left-color: #10b981; color: #047857;">
    <strong>Bloco B: Gerenciamento Perceptivo de Mídias e Foco</strong>
  </div>

  <div class="ihc-block">
    <h4>Critérios de Interface (UI/UX - Foco Visual e Mídia)</h4>
    <div class="checklist-item"><input type="checkbox" id="chk34" class="ihc-check"><label for="chk34"><strong>Foco Visual Explícito:</strong> Elementos interativos (links, botões, campos) possuem indicadores de foco altamente visíveis via teclado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk35" class="ihc-check"><label for="chk35"><strong>Controle de Mídia:</strong> Elementos com movimento contínuo (carrosséis) possuem botões explícitos para Pausar, Parar ou Ocultar?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk36" class="ihc-check"><label for="chk36"><strong>Textos Alternativos (alt):</strong> Imagens informativas têm atributo alt descritivo, e imagens puramente decorativas têm alt="" vazio?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk37" class="ihc-check"><label for="chk37"><strong>Redimensionamento e Zoom:</strong> A interface permite o aumento do texto em até 200% sem perda de conteúdo ou de funcionalidade?</label></div>
  </div>

  <div class="ihc-block" style="border-bottom: none;">
    <h4>Critérios de Desenvolvimento (Código e Teclado)</h4>
    <div class="checklist-item"><input type="checkbox" id="chk38" class="ihc-check"><label for="chk38"><strong>Acessibilidade Total por Teclado:</strong> Toda a funcionalidade da página está disponível apenas via teclado (Tab, Enter, Espaço, Setas)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk39" class="ihc-check"><label for="chk39"><strong>Prevenção de Armadilha (Keyboard Trap):</strong> O usuário consegue mover o foco para dentro e para fora de modais usando apenas teclado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk40" class="ihc-check"><label for="chk40"><strong>Ordem Lógica de Tabulação:</strong> A navegação via Tab segue a leitura visual lógica? O código evita usar tabindex positivo?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk41" class="ihc-check"><label for="chk41"><strong>Ocultação Semântica:</strong> Elementos visualmente ocultos estão devidamente marcados com aria-hidden="true" ou display:none?</label></div>
  </div>

  <div class="progress-section">
    <div class="progress-bar-container">
      <div class="progress-bar" id="progress-bar">0%</div>
    </div>
    <span id="score-text" style="color: #ef4444;">Risco Crítico de Exclusão - 0 de 41 critérios (0%)</span>
  </div>
</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
    const checkboxes = document.querySelectorAll('.ihc-check');
    const progressBar = document.getElementById('progress-bar');
    const scoreText = document.getElementById('score-text');
    const total = 41; // Novo total de regras oficiais

    function updateScore() {
        let checkedCount = 0;
        checkboxes.forEach(box => {
            if (box.checked) checkedCount++;
        });

        const percentage = Math.round((checkedCount / total) * 100);
        
        progressBar.style.width = percentage + '%';
        progressBar.innerText = percentage + '%';

        if (percentage <= 50) {
            progressBar.style.backgroundColor = '#ef4444'; // Vermelho
            scoreText.style.color = '#ef4444';
            scoreText.innerText = `Risco Crítico de Exclusão - ${checkedCount} de ${total} critérios (${percentage}%)`;
        } else if (percentage < 100) {
            progressBar.style.backgroundColor = '#f59e0b'; // Amarelo
            scoreText.style.color = '#f59e0b';
            scoreText.innerText = `Conformidade Parcial - ${checkedCount} de ${total} critérios (${percentage}%)`;
        } else {
            progressBar.style.backgroundColor = '#10b981'; // Verde
            scoreText.style.color = '#10b981';
            scoreText.innerText = `🎉 Conformidade Regular Alcançada! - ${checkedCount}/${total} (${percentage}%)`;
        }
    }

    checkboxes.forEach(box => {
        box.addEventListener('change', updateScore);
    });

    updateScore();
});
</script>