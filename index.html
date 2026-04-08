<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>English Verb Quiz</title>
  <style>
    * { box-sizing: border-box; }
    body {
      font-family: 'Segoe UI', Roboto, Arial, sans-serif;
      margin: 0;
      background: linear-gradient(135deg, #ffd6ec, #d6f0ff, #e6d6ff);
      color: #222;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }
    .container {
      max-width: 900px;
      margin: 20px auto;
      background: white;
      padding: 20px;
      border-radius: 20px;
      box-shadow: 0 10px 25px rgba(0,0,0,0.08);
    }
    h1 { text-align: center; color: #7b5cff; margin-top: 0; }
    .question { margin-bottom: 16px; padding: 14px; border-radius: 12px; background: #f9f9ff; }
    fieldset { border: none; padding: 0; margin: 0; }
    legend { font-weight: 600; margin-bottom: 8px; }
    label { display: block; margin: 6px 0; cursor: pointer; }
    input[type="radio"] { margin-right: 8px; }
    .controls { display:flex; gap:12px; margin-top:12px; }
    button {
      padding: 12px 16px; border: none; border-radius: 10px;
      background: linear-gradient(90deg,#ff9ad5,#9ad8ff,#c59aff);
      color: white; font-size: 16px; font-weight: bold; cursor: pointer;
      transition: transform .12s ease, opacity .12s ease; flex:1;
    }
    button.secondary { background:#f0f4ff; color:#333; font-weight:600; border:1px solid #e0e8ff; }
    button:disabled { opacity:.6; cursor:not-allowed; transform:none; }
    .result { margin-top: 20px; }
    .card { padding:12px; border-radius:12px; margin-bottom:12px; background:#f8faff; border-left:6px solid; }
    .correct-card { border-color:#4CAF50; }
    .wrong-card { border-color:#F44336; }
    .score-box { text-align:center; padding:14px; border-radius:12px; background:#f0f8ff; margin-bottom:16px; }
    .answer { font-weight:bold; }
    .explanation { margin-top:6px; color:#333; }
    @media (max-width:600px) { .container{margin:10px;padding:15px;} h1{font-size:22px;} .controls{flex-direction:column;} }

    /* Results screen (overlay / nova "tela") */
    #resultsScreen {
      position: fixed;
      inset: 0;
      background: rgba(10,10,20,0.6);
      display: none;
      align-items: center;
      justify-content: center;
      z-index: 9999;
      padding: 20px;
    }
    #resultsContent {
      width: 100%;
      max-width: 1000px;
      max-height: 90vh;
      overflow: auto;
      background: #fff;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 20px 50px rgba(0,0,0,0.3);
    }
    .results-header { display:flex; gap:12px; align-items:center; justify-content:space-between; margin-bottom:12px; }
    .results-actions { display:flex; gap:8px; }
    .small-btn { padding:8px 12px; border-radius:8px; border:none; cursor:pointer; font-weight:600; }
    .small-btn.primary { background: linear-gradient(90deg,#7b5cff,#9ad8ff); color:#fff; }
    .small-btn.ghost { background:#f0f4ff; color:#222; border:1px solid #e6ecff; }

    /* Styling for tense/grammar block */
    .tense { font-weight:700; margin-top:8px; color:#333; }
    .reason { margin-top:6px; color:#444; }
  </style>
</head>
<body>
  <main class="container" aria-labelledby="quizTitle">
    <h1 id="quizTitle">English Verb Quiz</h1>

    <form id="quizForm" aria-describedby="instructions">
      <p id="instructions">Escolha a opção correta para cada frase. Ao terminar, clique em <strong>Finish Quiz</strong>.</p>
      <!-- Perguntas serão injetadas aqui -->
    </form>

    <div class="controls" role="group" aria-label="Controles do quiz">
      <button id="finishBtn" type="button">Finish Quiz</button>
      <button id="resetBtn" type="button" class="secondary">Reset</button>
    </div>
  </main>

  <!-- Tela de resultados (nova "página" / overlay) -->
  <div id="resultsScreen" role="dialog" aria-modal="true" aria-hidden="true">
    <div id="resultsContent" tabindex="-1">
      <div class="results-header">
        <div>
          <h2 id="resultsTitle">Resultados</h2>
          <div id="scoreSummary" aria-live="polite"></div>
        </div>
        <div class="results-actions">
          <button id="exportPdfBtn" class="small-btn primary" type="button">Exportar PDF</button>
          <button id="closeResultsBtn" class="small-btn ghost" type="button">Voltar ao Quiz</button>
        </div>
      </div>

      <div id="resultsInner">
        <!-- Cards de resultado serão injetados aqui -->
      </div>
    </div>
  </div>

  <!-- Bibliotecas para gerar PDF a partir do HTML -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/html2canvas/1.4.1/html2canvas.min.js" integrity="sha512-BNa5m0kq3q3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6m3q2k6g==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js" integrity="sha512-+q3m6r1q2..." crossorigin="anonymous" referrerpolicy="no-referrer"></script>

  <script>
    // Perguntas com campo 'tense' e explicação detalhada (tempo verbal + motivo)
    const questions = [
      {
        q: "She ____ to work every day.",
        options: ["go","goes","going","gone"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'goes' porque o sujeito 'she' exige a forma com -s no presente simples; a frase descreve uma rotina habitual."
      },
      {
        q: "Yesterday, I ____ a movie.",
        options: ["watch","watched","watching","watches"],
        answer: 1,
        tense: "Past Simple (regular verb)",
        explanation: "Usamos 'watched' porque 'yesterday' indica passado; verbos regulares formam o passado com -ed."
      },
      {
        q: "He has ____ his homework.",
        options: ["do","did","done","doing"],
        answer: 2,
        tense: "Present Perfect (have/has + past participle)",
        explanation: "Usamos 'done' porque 'has' pede o particípio passado; present perfect conecta ação passada com relevância no presente."
      },
      {
        q: "They ____ playing soccer now.",
        options: ["is","are","was","be"],
        answer: 1,
        tense: "Present Continuous (be + -ing)",
        explanation: "Usamos 'are' como auxiliar para 'they' no present continuous ('are playing') para indicar ação em progresso agora."
      },
      {
        q: "She ____ a letter to her friend.",
        options: ["write","writes","writing","written"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'writes' porque 'she' exige -s no presente simples; é um verbo transitivo com objeto 'a letter'."
      },
      {
        q: "The baby ____ all night.",
        options: ["cry","cries","cried","crying"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'cries' para concordância com 'the baby' no presente simples; descreve um comportamento habitual ou estado."
      },
      {
        q: "We ____ dinner when he arrived.",
        options: ["eat","eating","were eating","ate"],
        answer: 2,
        tense: "Past Continuous (was/were + -ing)",
        explanation: "Usamos 'were eating' para indicar uma ação em progresso no passado que foi interrompida por outro evento ('he arrived')."
      },
      {
        q: "I ____ never been to Paris.",
        options: ["have","has","had","having"],
        answer: 0,
        tense: "Present Perfect (have/has + past participle)",
        explanation: "Usamos 'have' com 'I' no present perfect ('have been') para indicar experiência de vida até o presente."
      },
      {
        q: "She ____ quickly.",
        options: ["runs","run","running","ran"],
        answer: 0,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'runs' porque 'she' exige -s no presente simples; verbo intransitivo aqui (não precisa de objeto)."
      },
      {
        q: "He ____ the ball to me.",
        options: ["throw","throws","throwing","thrown"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'throws' para concordância com 'he'; é transitivo porque tem objeto 'the ball'."
      },
      {
        q: "They ____ finished the project.",
        options: ["has","have","had","having"],
        answer: 1,
        tense: "Present Perfect (have/has + past participle)",
        explanation: "Usamos 'have' com 'they' no present perfect ('have finished') para indicar conclusão com relevância atual."
      },
      {
        q: "I ____ my keys yesterday.",
        options: ["lose","lost","losing","loses"],
        answer: 1,
        tense: "Past Simple (irregular verb)",
        explanation: "Usamos 'lost' porque 'yesterday' indica passado e 'lose' é irregular: lose → lost."
      },
      {
        q: "She ____ already left.",
        options: ["has","have","had","having"],
        answer: 0,
        tense: "Present Perfect (have/has + past participle)",
        explanation: "Usamos 'has' com 'she' no present perfect ('has left') para indicar que a ação ocorreu antes do momento presente."
      },
      {
        q: "We ____ to the gym every week.",
        options: ["go","goes","went","gone"],
        answer: 0,
        tense: "Present Simple (plural subject)",
        explanation: "Usamos 'go' porque 'we' exige a forma base no presente simples; a frase descreve uma rotina."
      },
      {
        q: "He ____ a cake for the party.",
        options: ["make","makes","made","making"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'makes' para concordância com 'he' no presente simples; descreve uma ação habitual ou presente."
      },
      {
        q: "The sun ____ in the east.",
        options: ["rise","rises","rose","rising"],
        answer: 1,
        tense: "Present Simple (general truth)",
        explanation: "Usamos 'rises' no presente simples para enunciar uma verdade geral ou fato científico."
      },
      {
        q: "I ____ TV when you called.",
        options: ["watch","was watching","watched","watching"],
        answer: 1,
        tense: "Past Continuous (was/were + -ing)",
        explanation: "Usamos 'was watching' para indicar uma ação em progresso no passado que foi interrompida por outra ação ('you called')."
      },
      {
        q: "She ____ me a message.",
        options: ["send","sends","sent","sending"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'sends' porque 'she' exige -s no presente simples; verbo transitivo com objeto 'me a message'."
      },
      {
        q: "He ____ very fast.",
        options: ["run","runs","ran","running"],
        answer: 1,
        tense: "Present Simple (third person singular)",
        explanation: "Usamos 'runs' para concordância com 'he' no presente simples; descreve uma habilidade ou hábito."
      },
      {
        q: "They ____ already eaten.",
        options: ["has","have","had","having"],
        answer: 1,
        tense: "Present Perfect (have/has + past participle)",
        explanation: "Usamos 'have' com 'they' no present perfect ('have already eaten') para indicar que a ação foi concluída antes do momento presente."
      }
    ];

    const form = document.getElementById('quizForm');
    const finishBtn = document.getElementById('finishBtn');
    const resetBtn = document.getElementById('resetBtn');
    const resultsScreen = document.getElementById('resultsScreen');
    const resultsInner = document.getElementById('resultsInner');
    const scoreSummary = document.getElementById('scoreSummary');
    const exportPdfBtn = document.getElementById('exportPdfBtn');
    const closeResultsBtn = document.getElementById('closeResultsBtn');

    // Constrói o quiz
    function buildQuiz() {
      form.innerHTML = '';
      questions.forEach((item, index) => {
        const qDiv = document.createElement('div');
        qDiv.className = 'question';

        const fieldset = document.createElement('fieldset');
        fieldset.id = `q${index}-fieldset`;

        const legend = document.createElement('legend');
        legend.textContent = `${index + 1}. ${item.q}`;
        fieldset.appendChild(legend);

        item.options.forEach((opt, i) => {
          const label = document.createElement('label');
          label.htmlFor = `q${index}_opt${i}`;

          const radio = document.createElement('input');
          radio.type = 'radio';
          radio.name = `q${index}`;
          radio.id = `q${index}_opt${i}`;
          radio.value = i;
          radio.setAttribute('aria-label', opt);

          label.appendChild(radio);
          label.appendChild(document.createTextNode(opt));
          fieldset.appendChild(label);
        });

        qDiv.appendChild(fieldset);
        form.appendChild(qDiv);
      });
    }

    // Avalia e mostra resultados em nova tela
    function submitQuiz() {
      if (finishBtn.disabled) return;

      let score = 0;
      const total = questions.length;
      resultsInner.innerHTML = ''; // limpa

      questions.forEach((item, index) => {
        const selected = form.querySelector(`input[name="q${index}"]:checked`);
        const userIndex = selected ? parseInt(selected.value, 10) : null;
        const userAnswer = userIndex !== null ? item.options[userIndex] : 'No answer';
        const correctAnswer = item.options[item.answer];
        const isCorrect = userIndex === item.answer;
        if (isCorrect) score++;

        const card = document.createElement('div');
        card.className = 'card ' + (isCorrect ? 'correct-card' : 'wrong-card');

        const qPara = document.createElement('p');
        qPara.innerHTML = `<strong>Question ${index + 1}:</strong> ${item.q}`;
        card.appendChild(qPara);

        const yourPara = document.createElement('p');
        yourPara.innerHTML = `Your answer: <span class="answer">${escapeHtml(userAnswer)}</span>`;
        card.appendChild(yourPara);

        const correctPara = document.createElement('p');
        correctPara.innerHTML = `Correct answer: <span class="answer">${escapeHtml(correctAnswer)}</span>`;
        card.appendChild(correctPara);

        // Tense and reason block
        const tensePara = document.createElement('p');
        tensePara.className = 'tense';
        tensePara.innerHTML = `<strong>Tempo verbal correto:</strong> ${escapeHtml(item.tense)}`;
        card.appendChild(tensePara);

        const reasonPara = document.createElement('p');
        reasonPara.className = 'reason';
        reasonPara.textContent = `Por que: ${item.explanation}`;
        card.appendChild(reasonPara);

        resultsInner.appendChild(card);
      });

      const percentage = ((score / total) * 100).toFixed(1);
      scoreSummary.innerHTML = `<div class="score-box"><h3>Score: ${score}/${total}</h3><h4>Accuracy: ${percentage}%</h4></div>`;

      // Mostrar a tela de resultados (overlay)
      resultsScreen.style.display = 'flex';
      resultsScreen.setAttribute('aria-hidden', 'false');
      // Desabilitar botão finish para evitar reenvio
      finishBtn.disabled = true;
      resetBtn.disabled = false;

      // Focar no conteúdo de resultados para leitores de tela
      document.getElementById('resultsContent').focus();
    }

    // Fecha a tela de resultados e volta ao quiz
    function closeResults() {
      resultsScreen.style.display = 'none';
      resultsScreen.setAttribute('aria-hidden', 'true');
      // manter finish disabled até reset
      finishBtn.disabled = true;
      resetBtn.focus();
    }

    // Gera PDF do conteúdo de resultados usando html2canvas + jsPDF
    async function exportResultsToPDF() {
      exportPdfBtn.disabled = true;
      exportPdfBtn.textContent = 'Gerando PDF...';

      try {
        const element = document.getElementById('resultsContent');
        const scale = 2;
        const canvas = await html2canvas(element, {
          scale,
          useCORS: true,
          backgroundColor: '#ffffff'
        });

        const imgData = canvas.toDataURL('image/png');
        const { jsPDF } = window.jspdf;
        const pdf = new jsPDF({
          orientation: 'portrait',
          unit: 'pt',
          format: 'a4'
        });

        const pageWidth = pdf.internal.pageSize.getWidth();
        const pageHeight = pdf.internal.pageSize.getHeight();

        const imgWidth = canvas.width;
        const imgHeight = canvas.height;
        const ratio = Math.min(pageWidth / imgWidth, pageHeight / imgHeight);
        const renderWidth = imgWidth * ratio;
        const renderHeight = imgHeight * ratio;

        // Dividir em páginas se necessário
        const fullImg = new Image();
        fullImg.src = imgData;
        await new Promise((res) => { fullImg.onload = res; });

        const totalPages = Math.ceil((imgHeight * ratio) / pageHeight);
        const pageCanvas = document.createElement('canvas');
        const pageCtx = pageCanvas.getContext('2d');
        pageCanvas.width = Math.floor(pageWidth * scale);
        pageCanvas.height = Math.floor(pageHeight * scale);

        for (let i = 0; i < totalPages; i++) {
          pageCtx.fillStyle = '#ffffff';
          pageCtx.fillRect(0, 0, pageCanvas.width, pageCanvas.height);

          const sx = 0;
          const sy = Math.floor((i * pageHeight) / ratio);
          const sWidth = imgWidth;
          const sHeight = Math.floor(pageHeight / ratio);

          pageCtx.drawImage(fullImg, sx, sy, sWidth, sHeight, 0, 0, pageCanvas.width, pageCanvas.height);

          const pageData = pageCanvas.toDataURL('image/png');
          if (i > 0) pdf.addPage();
          pdf.addImage(pageData, 'PNG', 0, 0, pageWidth, pageHeight);
        }

        const fileName = `quiz-results-${new Date().toISOString().slice(0,19).replace(/[:T]/g,'-')}.pdf`;
        pdf.save(fileName);
      } catch (err) {
        console.error('Erro ao gerar PDF:', err);
        alert('Ocorreu um erro ao gerar o PDF. Tente novamente.');
      } finally {
        exportPdfBtn.disabled = false;
        exportPdfBtn.textContent = 'Exportar PDF';
      }
    }

    // Reset do quiz para tentar novamente
    function resetQuiz() {
      buildQuiz();
      resultsInner.innerHTML = '';
      scoreSummary.innerHTML = '';
      resultsScreen.style.display = 'none';
      resultsScreen.setAttribute('aria-hidden', 'true');
      finishBtn.disabled = false;
      resetBtn.disabled = true;
      const firstInput = form.querySelector('input[type="radio"]');
      if (firstInput) firstInput.focus();
    }

    // Helper para escapar texto
    function escapeHtml(text) {
      if (typeof text !== 'string') return text;
      return text.replace(/[&<>"']/g, function (m) {
        return ({ '&': '&amp;', '<': '&lt;', '>': '&gt;', '"': '&quot;', "'": '&#39;' })[m];
      });
    }

    // Listeners
    finishBtn.addEventListener('click', submitQuiz);
    resetBtn.addEventListener('click', resetQuiz);
    closeResultsBtn.addEventListener('click', closeResults);
    exportPdfBtn.addEventListener('click', exportResultsToPDF);

    // Inicializa
    buildQuiz();
    resetBtn.disabled = true;
  </script>
</body>
</html>
