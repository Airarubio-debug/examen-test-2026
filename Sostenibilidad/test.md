<style>
  body { font-family: sans-serif; }
  /* Ocultamos todas las preguntas por defecto */
  .pregunta { display: none; margin-bottom: 20px; }
  /* Solo mostramos la que tenga la clase 'activa' */
  .pregunta.activa { display: block; animation: fadein 0.5s; }
  
  @keyframes fadein { from { opacity: 0; } to { opacity: 1; } }

  .opcion {
    display: block; width: 100%; text-align: left; padding: 15px; margin: 10px 0;
    font-size: 16px; border: 1px solid #d0d7de; border-radius: 8px; 
    background: #ffffff; cursor: pointer; transition: 0.2s;
  }
  .opcion:hover:not(:disabled) { background: #f3f4f6; }
  .correcta { background: #dafbe1 !important; border-color: #4ac26b !important; color: #1a7f37; font-weight: bold; }
  .incorrecta { background: #ffebe9 !important; border-color: #ff8182 !important; color: #cf222e; font-weight: bold; }
  
  #btn-siguiente {
    display: none; margin-top: 20px; padding: 12px 24px; font-size: 16px; 
    background-color: #0969da; color: white; border: none; border-radius: 6px; 
    cursor: pointer; float: right; font-weight: bold;
  }
  #btn-siguiente:hover { background-color: #0550ae; }
  
  #resultados { display: none; text-align: center; padding: 40px 20px; }
  #btn-repetir {
    margin-top: 20px; padding: 12px 24px; font-size: 16px; background-color: #2da44e; 
    color: white; border: none; border-radius: 6px; cursor: pointer; font-weight: bold;
  }
</style>

<div id="contenedor-test">
  <div class="pregunta activa">
    <p><strong>1. El sistema biológico formado por una comunidad de seres vivos que habita un medio físico se denomina:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Sistema humano.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Ecosistema.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Sociedad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Equilibrio.</button>
  </div>

  <div class="pregunta">
    <p><strong>2. Los recursos naturales:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Proporcionan materiales a los sistemas económicos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Son materiales que se extraen de la naturaleza y se utilizan en la producción.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Son materiales que proceden de la actividad humana y resultan inservibles si no se transforman.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Son dinero, fundamentalmente.</button>
  </div>

  <div class="pregunta">
    <p><strong>3. No es una dimensión del desarrollo sostenible:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La económica.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La social.</button>
    <button class="opcion" onclick="verificar(this, true)">c) La estética.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La ecológica.</button>
  </div>

  <div class="pregunta">
    <p><strong>4. Para que los ecosistemas sean sostenibles, nuestra huella ecológica debe ser:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Inferior a la biocapacidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Superior a la biocapacidad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Basta con que sea reducida.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es independiente de la biocapacidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>5. El cambio climático actual tiene su principal origen en:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La actividad económica.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La capa de ozono.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La actividad del Sol.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La contaminación del suelo.</button>
  </div>

  <div class="pregunta">
    <p><strong>6. El mayor efecto medioambiental de la contaminación atmosférica es:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) El efecto invernadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Las formas de producir que despilfarran recursos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La pérdida de biodiversidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La contaminación del suelo.</button>
  </div>

  <div class="pregunta">
    <p><strong>7. El cambio climático supone para las empresas:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Menor demanda de energía en los hogares.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una mayor productividad de su plantilla.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El aumento de las primas de sus seguros.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un aumento en sus ingresos.</button>
  </div>

  <div class="pregunta">
    <p><strong>8. Plantar bosques es una medida de:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Descarbonización.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Desmaterialización.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Desertización.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Adaptación.</button>
  </div>

  <div class="pregunta">
    <p><strong>9. Las medidas de mitigación buscan:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Adaptar la empresa a la nueva situación climática.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Frenar o atenuar el cambio climático.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Atender a las personas con problemas de salud causados por el cambio climático.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Reducir la actividad económica, en todo caso.</button>
  </div>

  <div class="pregunta">
    <p><strong>10. La Agenda 2030:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es única, y su objetivo es guiar las acciones de las Naciones Unidas.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Es adaptada por muchas administraciones públicas para guiar sus propias estrategias de desarrollo sostenible.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se creó como iniciativa del Gobierno de España.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Busca que la Unión Europea se vuelva neutral en emisiones de carbono para 2030.</button>
  </div>
</div>

<button id="btn-siguiente" onclick="siguientePregunta()">Siguiente pregunta ➡️</button>

<div id="resultados">
  <h2>¡Test completado! 🎉</h2>
  <p style="font-size: 18px;">Has acertado <strong id="aciertos">0</strong> de <strong id="total">0</strong> preguntas.</p>
  <button id="btn-repetir" onclick="location.reload()">↻ Repetir test</button>
</div>

<script>
  let indexActual = 0;
  let aciertos = 0;
  const preguntas = document.querySelectorAll('.pregunta');
  const btnSiguiente = document.getElementById('btn-siguiente');
  const contenedorTest = document.getElementById('contenedor-test');
  const divResultados = document.getElementById('resultados');

  function verificar(boton, esCorrecto) {
    let contenedor = boton.parentElement;
    let botones = contenedor.querySelectorAll('button.opcion');
    
    // Deshabilita botones de esta pregunta para no poder pulsar dos veces
    botones.forEach(b => {
      b.disabled = true;
      b.style.cursor = 'default';
    });

    if (esCorrecto) {
      boton.classList.add('correcta');
      boton.innerHTML += " ✅";
      aciertos++;
    } else {
      boton.classList.add('incorrecta');
      boton.innerHTML += " ❌";
      // Te muestra la correcta en verde
      botones.forEach(b => {
        if(b.getAttribute("onclick").includes("true")) {
          b.classList.add('correcta');
        }
      });
    }
    
    // Muestra el botón de siguiente
    btnSiguiente.style.display = 'block';
  }

  function siguientePregunta() {
    // Oculta la pregunta actual
    preguntas[indexActual].classList.remove('activa');
    btnSiguiente.style.display = 'none';
    
    indexActual++;

    if (indexActual < preguntas.length) {
      // Muestra la siguiente
      preguntas[indexActual].classList.add('activa');
    } else {
      // Si ya no hay más, muestra los resultados
      contenedorTest.style.display = 'none';
      divResultados.style.display = 'block';
      document.getElementById('aciertos').innerText = aciertos;
      document.getElementById('total').innerText = preguntas.length;
    }
  }
</script>
