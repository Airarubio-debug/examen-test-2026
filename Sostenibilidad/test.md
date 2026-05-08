<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
</head>
<body>

<style>
  :root {
    --primary: #0969da;
    --success: #1a7f37;
    --error: #cf222e;
    --bg: #f6f8fa;
    --text: #24292f;
    --border: #d0d7de;
  }

  #quiz-wrapper {
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
    color: var(--text);
    max-width: 650px;
    margin: 40px auto;
    padding: 20px;
    background: #ffffff;
    border: 1px solid var(--border);
    border-radius: 12px;
    box-shadow: 0 8px 24px rgba(149, 157, 165, 0.2);
  }

  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
    padding-bottom: 10px;
    border-bottom: 1px solid var(--border);
  }

  .progress-bar {
    height: 8px;
    background: var(--bg);
    border-radius: 4px;
    margin-bottom: 25px;
    overflow: hidden;
  }

  #progress-fill {
    height: 100%;
    background: var(--primary);
    width: 0%;
    transition: width 0.4s ease;
  }

  .pregunta-box {
    display: none;
    animation: fadeIn 0.4s ease-out;
  }

  .pregunta-box.active { display: block; }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(10px); }
    to { opacity: 1; transform: translateY(0); }
  }

  h2 { font-size: 20px; margin-bottom: 20px; line-height: 1.4; }

  .opcion-btn {
    display: block;
    width: 100%;
    padding: 15px 20px;
    margin-bottom: 12px;
    text-align: left;
    background: #fff;
    border: 1px solid var(--border);
    border-radius: 8px;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.2s ease;
  }

  .opcion-btn:hover:not(:disabled) {
    background: var(--bg);
    border-color: var(--primary);
  }

  .opcion-btn.correct {
    background: #dafbe1;
    border-color: #4ac26b;
    color: var(--success);
    font-weight: 600;
  }

  .opcion-btn.wrong {
    background: #ffebe9;
    border-color: #ff8182;
    color: var(--error);
    font-weight: 600;
  }

  .footer {
    margin-top: 30px;
    height: 50px;
  }

  #next-btn {
    float: right;
    padding: 12px 24px;
    background: var(--primary);
    color: white;
    border: none;
    border-radius: 6px;
    font-weight: 600;
    cursor: pointer;
    display: none;
    align-items: center;
    gap: 8px;
  }

  #next-btn:hover { background: #0550ae; }

  /* Pantalla Final */
  #results-screen { display: none; text-align: center; }
  .score { font-size: 48px; font-weight: 800; color: var(--primary); margin: 20px 0; }
  .review-item {
    text-align: left;
    background: #fff8f8;
    border-left: 4px solid var(--error);
    padding: 15px;
    margin-bottom: 10px;
    border-radius: 4px;
  }
</style>

<div id="quiz-wrapper">
  <div id="quiz-screen">
    <div class="header">
      <span id="category-tag" style="font-size: 12px; font-weight: bold; color: var(--primary); text-transform: uppercase;">Sostenibilidad ASIR</span>
      <span id="counter" style="font-size: 14px; color: #57606a;">Pregunta 1/10</span>
    </div>
    
    <div class="progress-bar"><div id="progress-fill"></div></div>

    <div id="questions-container">
      </div>

    <div class="footer">
      <button id="next-btn" onclick="nextQuestion()">Siguiente →</button>
    </div>
  </div>

  <div id="results-screen">
    <h2 style="margin-bottom: 10px;">¡Test Finalizado!</h2>
    <div class="score"><span id="correct-count">0</span> / <span id="total-count">0</span></div>
    <p id="feedback-msg"></p>
    
    <div id="error-review" style="margin-top: 30px; display: none;">
      <h3 style="text-align: left; font-size: 16px; color: var(--error);">Preguntas para reforzar:</h3>
      <div id="error-list"></div>
    </div>

    <button onclick="location.reload()" style="margin-top: 30px; background: none; border: 1px solid var(--border); padding: 10px 20px; border-radius: 6px; cursor: pointer;">Reintentar test</button>
  </div>
</div>

<script>
  // Datos extraídos y verificados con el PDF oficial
  const quizData = [
    { q: "¿Cuáles son los tres pilares del desarrollo sostenible?", o: ["Tecnología, rentabilidad y ecología", "Medioambiental, económico y social", "Humano, tecnológico y regulatorio", "Ambiental, digital y financiero"], a: 1 },
    { q: "El sistema biológico formado por una comunidad de seres vivos que habita un medio físico se denomina:", o: ["Sistema humano", "Ecosistema", "Sociedad", "Equilibrio"], a: 1 },
    { q: "Para que los ecosistemas sean sostenibles, nuestra huella ecológica debe ser:", o: ["Igual que la biocapacidad", "Mayor que la biocapacidad", "Menor que la biocapacidad", "Independiente del desarrollo sostenible"], a: 2 },
    { q: "Lo más recomendable para una empresa que quiere integrar los ODS es implicarse en el logro de:", o: ["Un ODS concreto", "Una meta concreta", "Un indicador de desempeño concreto", "Todos los ODS al mismo tiempo"], a: 1 },
    { q: "Las iniciativas que la UE ha puesto en marcha para el logro de los ODS suponen ventajas para las empresas, como:", o: ["Mayor posibilidad de recibir sanciones", "Reducción de impuestos", "Normas medioambientales estrictas", "Ayudas para mejorar la resiliencia"], a: 3 },
    { q: "Sobre los grupos de interés, señala la afirmación falsa:", o: ["Son colectivos humanos", "Influyen en las decisiones", "Las decisiones los influyen", "Siempre son externos a la empresa"], a: 3 },
    { q: "Para una empresa agrícola, la mayor frecuencia de sequías es un asunto:", o: ["Con materialidad de impacto", "Con doble materialidad", "Sin materialidad", "Con materialidad financiera"], a: 3 },
    { q: "Una marca de moda implementa blockchain para rastrear condiciones laborales. ¿Qué aspecto ASG se ve más afectado?", o: ["Financiero", "Ambiental", "Gobernanza", "Social"], a: 2 },
    { q: "Indica cuál de los siguientes estándares de información no financiera es más antiguo:", o: ["Global Reporting Initiative (GRI)", "Ley de Información no Financiera", "Directiva CSRD 2022", "Normas NEIS"], a: 0 },
    { q: "La declaración de impacto ambiental es redactada por:", o: ["La empresa promotora", "La autoridad medioambiental", "La constructora", "La oficina de prensa"], a: 1 }
  ];

  let currentIdx = 0;
  let score = 0;
  let errors = [];

  function initQuiz() {
    const container = document.getElementById('questions-container');
    quizData.forEach((data, index) => {
      const div = document.createElement('div');
      div.className = `pregunta-box ${index === 0 ? 'active' : ''}`;
      div.id = `q-${index}`;
      div.innerHTML = `
        <h2>${data.q}</h2>
        ${data.o.map((opt, i) => `
          <button class="opcion-btn" onclick="checkAnswer(${index}, ${i}, this)">${opt}</button>
        `).join('')}
      `;
      container.appendChild(div);
    });
    updateProgress();
  }

  function checkAnswer(qIdx, choiceIdx, btn) {
    const correctIdx = quizData[qIdx].a;
    const buttons = document.querySelectorAll(`#q-${qIdx} .opcion-btn`);
    
    buttons.forEach(b => b.disabled = true);
    
    if (choiceIdx === correctIdx) {
      btn.classList.add('correct');
      score++;
    } else {
      btn.classList.add('wrong');
      buttons[correctIdx].classList.add('correct');
      errors.push({ q: quizData[qIdx].q, a: quizData[qIdx].o[correctIdx] });
    }
    
    document.getElementById('next-btn').style.display = 'block';
  }

  function nextQuestion() {
    document.getElementById(`q-${currentIdx}`).classList.remove('active');
    currentIdx++;
    
    if (currentIdx < quizData.length) {
      document.getElementById(`q-${currentIdx}`).classList.add('active');
      document.getElementById('next-btn').style.display = 'none';
      updateProgress();
    } else {
      showResults();
    }
  }

  function updateProgress() {
    const progress = ((currentIdx + 1) / quizData.length) * 100;
    document.getElementById('progress-fill').style.width = `${progress}%`;
    document.getElementById('counter').innerText = `Pregunta ${currentIdx + 1}/${quizData.length}`;
  }

  function showResults() {
    document.getElementById('quiz-screen').style.display = 'none';
    const screen = document.getElementById('results-screen');
    screen.style.display = 'block';
    
    document.getElementById('correct-count').innerText = score;
    document.getElementById('total-count').innerText = quizData.length;
    
    if (errors.length > 0) {
      document.getElementById('error-review').style.display = 'block';
      const list = document.getElementById('error-list');
      errors.forEach(err => {
        list.innerHTML += `<div class="review-item"><strong>P:</strong> ${err.q}<br><span style="color:var(--success)"><strong>Correcta:</strong> ${err.a}</span></div>`;
      });
    }
  }

  initQuiz();
</script>
</body>
</html>
