<div id="quiz-container">
  <p>Cargando preguntas...</p>
</div>

<script>
// Este código busca el archivo preguntas.json en la misma carpeta
fetch('preguntas.json')
  .then(response => response.json())
  .then(data => {
    renderQuiz(data);
  });

function renderQuiz(preguntas) {
  const container = document.getElementById('quiz-container');
  container.innerHTML = `<h1>Test Interactivo</h1>`;
  
  preguntas.forEach((p, index) => {
    const div = document.createElement('div');
    div.innerHTML = `
      <p><strong>${index + 1}. ${p.question}</strong></p>
      ${p.answerOptions.map((opt, i) => `
        <button onclick="check(${opt.isCorrect}, this)">
          ${opt.text}
        </button>
      `).join('<br>')}
      <hr>
    `;
    container.appendChild(div);
  });
}

function check(isCorrect, btn) {
  btn.style.backgroundColor = isCorrect ? '#dafbe1' : '#ffebe9';
  alert(isCorrect ? "¡Correcto! 🎉" : "Incorrecto ❌");
}
</script>

<style>
  button { 
    display: block; width: 100%; padding: 10px; margin: 5px 0; 
    text-align: left; cursor: pointer; border: 1px solid #ccc; border-radius: 5px;
  }
</style>
