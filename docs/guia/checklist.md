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
    background-color: #3b82f6;
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
  }
  .auditoria-nota {
    background-color: #fef3c7;
    border-left: 4px solid #f59e0b;
    padding: 10px;
    font-size: 13px;
    color: #92400e;
    margin-bottom: 20px;
    border-radius: 4px;
  }
</style>

<div class="checklist-container">
  <h2 style="text-align: center; margin-bottom: 10px;">Ferramenta de Auditoria NBR 17225:2025</h2>
  <div class="auditoria-nota">
    <strong>Nota de Auditoria:</strong> Ferramentas automáticas (Lighthouse, ASES) capturam apenas 30% a 40% dos problemas. A inspeção manual da árvore de elementos por um analista WCAG é indispensável.
  </div>
  
  <div class="ihc-block">
    <h4>Bloco 1: Estrutura Global e Semântica da Aplicação</h4>
    <div class="checklist-item"><input type="checkbox" id="chk1" class="ihc-check" onclick="updateScore()"><label for="chk1"><strong>Idioma Principal (lang):</strong> A tag mestre &lt;html&gt; possui o atributo lang="pt-BR" para evitar sotaques estrangeiros em leitores de tela?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk2" class="ihc-check" onclick="updateScore()"><label for="chk2"><strong>Links de Salto (Skip Links):</strong> Existem links internos ocultos no início do código (ex: "Ir para o conteúdo") visíveis ao primeiro Tab?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk3" class="ihc-check" onclick="updateScore()"><label for="chk3"><strong>Marcos Semânticos (Landmarks):</strong> O código utiliza tags HTML5 puras (&lt;header&gt;, &lt;nav&gt;, &lt;main&gt;, &lt;footer&gt;) no lugar de &lt;div&gt; genéricas?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk4" class="ihc-check" onclick="updateScore()"><label for="chk4"><strong>Hierarquia de Títulos:</strong> Existe um único &lt;h1&gt;? Os subtítulos seguem ordem estrita sem pular níveis lógicos (ex: de h2 para h5)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk5" class="ihc-check" onclick="updateScore()"><label for="chk5"><strong>Validação de Sintaxe:</strong> A árvore DOM está livre de IDs duplicados (id="...") que confundem tecnologias assistivas?</label></div>
  </div>

  <div class="ihc-block">
    <h4>Bloco 2: Conteúdo, Compreensão e Formulários (Backstage)</h4>
    <div class="checklist-item"><input type="checkbox" id="chk6" class="ihc-check" onclick="updateScore()"><label for="chk6"><strong>Linguagem Simples e Siglas:</strong> Textos diretos sem jargões excessivos? Siglas explicadas na primeira aparição?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk7" class="ihc-check" onclick="updateScore()"><label for="chk7"><strong>Links Descritivos:</strong> Links informam claramente o destino (evitando "clique aqui" ou "saiba mais")?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk8" class="ihc-check" onclick="updateScore()"><label for="chk8"><strong>Previsibilidade:</strong> O foco em um componente evita mudanças inesperadas (abertura de abas ou envio automático)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk9" class="ihc-check" onclick="updateScore()"><label for="chk9"><strong>Rótulos de Formulário:</strong> Inputs possuem &lt;label&gt; associada explicitamente por atributos 'for' e 'id'?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk10" class="ihc-check" onclick="updateScore()"><label for="chk10"><strong>Instruções e Formatos:</strong> Instruções próximas aos campos estão associadas via 'aria-describedby'? O formato esperado é avisado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk11" class="ihc-check" onclick="updateScore()"><label for="chk11"><strong>Agrupamento e Autocomplete:</strong> Opções relacionadas usam &lt;fieldset&gt; e &lt;legend&gt;? O atributo 'autocomplete' é usado em dados pessoais?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk12" class="ihc-check" onclick="updateScore()"><label for="chk12"><strong>Semântica de Ação:</strong> Ações na página usam &lt;button&gt;, enquanto navegações para URLs usam &lt;a&gt;?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk13" class="ihc-check" onclick="updateScore()"><label for="chk13"><strong>Gestão de Erros (Prevenção):</strong> Erros são claros, sugerem correção, não dependem só de cor e não apagam dados já preenchidos?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk14" class="ihc-check" onclick="updateScore()"><label for="chk14"><strong>Consequências e Revisão:</strong> Ações críticas (jurídicas/financeiras) permitem revisão antes do envio definitivo?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk15" class="ihc-check" onclick="updateScore()"><label for="chk15"><strong>Robustez ARIA:</strong> Componentes dinâmicos informam estado (aberto/fechado)? Avisos na tela usam regiões 'aria-live'?</label></div>
  </div>

  <div class="ihc-block">
    <h4>Bloco 3: Gerenciamento Perceptivo, Mídias e Teclado (UI/UX)</h4>
    <div class="checklist-item"><input type="checkbox" id="chk16" class="ihc-check" onclick="updateScore()"><label for="chk16"><strong>Foco Visual Explícito:</strong> Elementos interativos possuem indicadores de foco altamente visíveis via teclado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk17" class="ihc-check" onclick="updateScore()"><label for="chk17"><strong>Controle de Mídia:</strong> Animações contínuas (carrosséis) possuem botões explícitos de Pausar, Parar ou Ocultar?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk18" class="ihc-check" onclick="updateScore()"><label for="chk18"><strong>Textos Alternativos (alt):</strong> Imagens informativas têm 'alt' descritivo e as decorativas usam alt="" vazio?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk19" class="ihc-check" onclick="updateScore()"><label for="chk19"><strong>Redimensionamento (Zoom):</strong> A interface permite aumento de texto em até 200% sem quebrar o layout (Reflow)?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk20" class="ihc-check" onclick="updateScore()"><label for="chk20"><strong>Acessibilidade Total por Teclado:</strong> Toda funcionalidade é operável via Tab/Enter/Espaço/Setas sem tempo limite?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk21" class="ihc-check" onclick="updateScore()"><label for="chk21"><strong>Armadilha de Teclado (Keyboard Trap):</strong> O usuário consegue entrar e sair de modais usando apenas o teclado?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk22" class="ihc-check" onclick="updateScore()"><label for="chk22"><strong>Ordem Lógica (tabindex):</strong> A ordem de tabulação segue a leitura visual sem o uso de tabindex positivo (ex: tabindex="1")?</label></div>
    <div class="checklist-item"><input type="checkbox" id="chk23" class="ihc-check" onclick="updateScore()"><label for="chk23"><strong>Ocultação Semântica:</strong> Elementos invisíveis na tela estão marcados com 'aria-hidden="true"' ou 'display: none'?</label></div>
  </div>

  <div class="progress-section">
    <div class="progress-bar-container">
      <div class="progress-bar" id="progress-bar">0%</div>
    </div>
    <span id="score-text" style="color: #dc3545;">Nível de Conformidade (0 / 23)</span>
  </div>
</div>

<script>
  function updateScore() {
    const checkboxes = document.querySelectorAll('.ihc-check');
    const total = checkboxes.length;
    let checkedCount = 0;

    checkboxes.forEach(box => {
      if (box.checked) checkedCount++;
    });

    const percentage = Math.round((checkedCount / total) * 100);
    const progressBar = document.getElementById('progress-bar');
    const scoreText = document.getElementById('score-text');

    progressBar.style.width = percentage + '%';
    progressBar.innerText = percentage + '%';

    if (percentage < 50) {
      progressBar.style.backgroundColor = '#ef4444'; // Vermelho
      scoreText.style.color = '#ef4444';
      scoreText.innerText = `Risco Crítico de Exclusão - ${checkedCount} de ${total} critérios (${percentage}%)`;
    } else if (percentage < 99) {
      progressBar.style.backgroundColor = '#f59e0b'; // Amarelo
      scoreText.style.color = '#f59e0b';
      scoreText.innerText = `Conformidade Parcial - ${checkedCount} de ${total} critérios (${percentage}%)`;
    } else {
      progressBar.style.backgroundColor = '#10b981'; // Verde
      scoreText.style.color = '#10b981';
      scoreText.innerText = `🎉 Conformidade Regular Alcançada! - ${checkedCount}/${total} (${percentage}%)`;
    }
  }
</script>