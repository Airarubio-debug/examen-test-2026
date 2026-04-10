
<style>
  body { font-family: sans-serif; }
  .pregunta { display: none; margin-bottom: 20px; }
  .pregunta.activa { display: block; animation: fadein 0.5s; }
  @keyframes fadein { from { opacity: 0; } to { opacity: 1; } }
  .opcion { display: block; width: 100%; text-align: left; padding: 15px; margin: 10px 0; font-size: 16px; border: 1px solid #d0d7de; border-radius: 8px; background: #ffffff; cursor: pointer; transition: 0.2s; }
  .opcion:hover:not(:disabled) { background: #f3f4f6; }
  .correcta { background: #dafbe1 !important; border-color: #4ac26b !important; color: #1a7f37; font-weight: bold; }
  .incorrecta { background: #ffebe9 !important; border-color: #ff8182 !important; color: #cf222e; font-weight: bold; }
  #btn-siguiente { display: none; margin-top: 20px; padding: 12px 24px; font-size: 16px; background-color: #0969da; color: white; border: none; border-radius: 6px; cursor: pointer; float: right; font-weight: bold; }
  #btn-siguiente:hover { background-color: #0550ae; }
  #resultados { display: none; text-align: center; padding: 40px 20px; }
  #btn-repetir { margin-top: 20px; padding: 12px 24px; font-size: 16px; background-color: #2da44e; color: white; border: none; border-radius: 6px; cursor: pointer; font-weight: bold; }
</style>

<div id="contenedor-test">

  <div class="pregunta">
    <p><strong>1. ¿Cuál de los siguientes no es un tipo de estructura de control en Python?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) if</button>
    <button class="opcion" onclick="verificar(this, false)">b) for</button>
    <button class="opcion" onclick="verificar(this, true)">c) select</button>
    <button class="opcion" onclick="verificar(this, false)">d) while</button>
  </div>

  <div class="pregunta">
    <p><strong>2. ¿Qué palabra se utiliza para terminar un bucle antes de que finalice normalmente?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) stop</button>
    <button class="opcion" onclick="verificar(this, true)">b) break</button>
    <button class="opcion" onclick="verificar(this, false)">c) exit</button>
    <button class="opcion" onclick="verificar(this, false)">d) return</button>
  </div>

  <div class="pregunta">
    <p><strong>3. ¿Qué función se utiliza para mostrar texto en la consola?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) input()</button>
    <button class="opcion" onclick="verificar(this, false)">b) scan()</button>
    <button class="opcion" onclick="verificar(this, true)">c) print()</button>
    <button class="opcion" onclick="verificar(this, false)">d) echo()</button>
  </div>

  <div class="pregunta">
    <p><strong>4. ¿Cuál de las siguientes estructuras permite almacenar pares clave-valor?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) list</button>
    <button class="opcion" onclick="verificar(this, false)">b) set</button>
    <button class="opcion" onclick="verificar(this, true)">c) dict</button>
    <button class="opcion" onclick="verificar(this, false)">d) tuple</button>
  </div>

  <div class="pregunta">
    <p><strong>5. ¿Qué estructura de control se usa para repetir un bloque de código mientras se cumple una condición?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) while</button>
    <button class="opcion" onclick="verificar(this, false)">b) if</button>
    <button class="opcion" onclick="verificar(this, false)">c) for</button>
    <button class="opcion" onclick="verificar(this, false)">d) switch</button>
  </div>

  <div class="pregunta">
    <p><strong>6. ¿Cuál es la extensión típica de los archivos en Python?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) .txt</button>
    <button class="opcion" onclick="verificar(this, true)">b) .py</button>
    <button class="opcion" onclick="verificar(this, false)">c) .exe</button>
    <button class="opcion" onclick="verificar(this, false)">d) .docx</button>
  </div>

  <div class="pregunta">
    <p><strong>7. ¿Qué tipo de estructura permite almacenar múltiples valores en una sola variable y es inmutable?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) list</button>
    <button class="opcion" onclick="verificar(this, true)">b) tuple</button>
    <button class="opcion" onclick="verificar(this, false)">c) dict</button>
    <button class="opcion" onclick="verificar(this, false)">d) set</button>
  </div>

  <div class="pregunta">
    <p><strong>8. ¿Qué estructura permite recorrer los elementos de una lista uno por uno?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) if</button>
    <button class="opcion" onclick="verificar(this, false)">b) while</button>
    <button class="opcion" onclick="verificar(this, true)">c) for</button>
    <button class="opcion" onclick="verificar(this, false)">d) switch</button>
  </div>

  <div class="pregunta">
    <p><strong>9. ¿Qué símbolo se usa para comentarios en Python?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) #</button>
    <button class="opcion" onclick="verificar(this, false)">b) //</button>
    <button class="opcion" onclick="verificar(this, false)">c) &lt;!--</button>
    <button class="opcion" onclick="verificar(this, false)">d) %</button>
  </div>

  <div class="pregunta">
    <p><strong>10. ¿Cuál es el resultado de 3 // 2 en Python?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 1.5</button>
    <button class="opcion" onclick="verificar(this, false)">b) 2</button>
    <button class="opcion" onclick="verificar(this, true)">c) 1</button>
    <button class="opcion" onclick="verificar(this, false)">d) 0</button>
  </div>

  <div class="pregunta">
    <p><strong>11. ¿Cuál es la salida de print(len("Python"))?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 5</button>
    <button class="opcion" onclick="verificar(this, true)">b) 6</button>
    <button class="opcion" onclick="verificar(this, false)">c) 7</button>
    <button class="opcion" onclick="verificar(this, false)">d) Error</button>
  </div>

  <div class="pregunta">
    <p><strong>12. Si lista = [1, 2, 3, 4], ¿qué devuelve lista[-1]?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 0</button>
    <button class="opcion" onclick="verificar(this, false)">b) 1</button>
    <button class="opcion" onclick="verificar(this, true)">c) 4</button>
    <button class="opcion" onclick="verificar(this, false)">d) Error.</button>
  </div>

  <div class="pregunta">
    <p><strong>13. ¿Qué se necesita para evitar un bucle infinito en un while?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que la condición sea siempre verdadera.</button>
    <button class="opcion" onclick="verificar(this, false)">b) No usar break.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Que la condición cambie dentro del bucle.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Incluir un else.</button>
  </div>

  <div class="pregunta">
    <p><strong>14. ¿Cuál es el operador de asignación en Python?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) ==</button>
    <button class="opcion" onclick="verificar(this, true)">b) =</button>
    <button class="opcion" onclick="verificar(this, false)">c) :=</button>
    <button class="opcion" onclick="verificar(this, false)">d) =&gt;</button>
  </div>

  <div class="pregunta">
    <p><strong>15. ¿Qué método agrega un elemento al final de una lista?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) insert()</button>
    <button class="opcion" onclick="verificar(this, true)">b) append()</button>
    <button class="opcion" onclick="verificar(this, false)">c) add()</button>
    <button class="opcion" onclick="verificar(this, false)">d) push()</button>
  </div>

</div> <button id="btn-siguiente" onclick="siguientePregunta()">Siguiente pregunta ➡️</button>

<div id="resultados">
  <h2>¡Test completado! 🎉</h2>
  <p style="font-size: 18px;">Has acertado <strong id="aciertos">0</strong> de <strong id="total">0</strong> preguntas.</p>
  
  <div id="repaso-errores" style="display: none; margin-top: 30px; text-align: left;">
    <h3 style="color: #cf222e; border-bottom: 2px solid #cf222e; padding-bottom: 5px;">Repaso de preguntas falladas:</h3>
    <div id="lista-errores"></div>
  </div>

  <button id="btn-repetir" onclick="location.reload()" style="margin-top: 20px;">↻ Repetir test</button>
</div>

<script>
  let indexActual = 0;
  let aciertos = 0;
  let arrayErrores = []; // Memoria para guardar los fallos

  const contenedorTest = document.getElementById('contenedor-test');
  const btnSiguiente = document.getElementById('btn-siguiente');
  const divResultados = document.getElementById('resultados');

  let preguntasArray = Array.from(document.querySelectorAll('.pregunta'));

  // Borrar números
  preguntasArray.forEach(pregunta => {
    let textoPregunta = pregunta.querySelector('p strong');
    if (textoPregunta) {
      textoPregunta.innerHTML = textoPregunta.innerHTML.replace(/^\d+\.\s*/, '');
    }
  });

  // Crear contador
  const progresoDiv = document.createElement('div');
  progresoDiv.style.cssText = 'text-align: center; font-weight: bold; font-size: 16px; color: #57606a; margin-bottom: 20px; background: #f6f8fa; padding: 10px; border-radius: 8px; border: 1px solid #d0d7de;';
  contenedorTest.parentNode.insertBefore(progresoDiv, contenedorTest);

  // Barajar
  function mezclarPreguntas(array) {
    for (let i = array.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [array[i], array[j]] = [array[j], array[i]];
    }
  }
  mezclarPreguntas(preguntasArray);

  // Reordenar
  preguntasArray.forEach(pregunta => {
    pregunta.classList.remove('activa');
    contenedorTest.appendChild(pregunta); 
  });
  preguntasArray[0].classList.add('activa');

  const preguntas = preguntasArray;

  function actualizarProgreso() {
    progresoDiv.innerText = `Pregunta ${indexActual + 1} de ${preguntas.length}`;
  }
  actualizarProgreso();

  function verificar(boton, esCorrecto) {
    let contenedor = boton.parentElement;
    let botones = contenedor.querySelectorAll('button.opcion');
    
    // Buscar cuál era el botón correcto
    let botonCorrecto = Array.from(botones).find(b => b.getAttribute("onclick").includes("true"));
    
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
      botonCorrecto.classList.add('correcta');
      
      // GUARDAR EL FALLO EN LA MEMORIA
      let textoPregunta = contenedor.querySelector('p strong').innerText;
      let textoCorrecto = botonCorrecto.innerText;
      arrayErrores.push({ pregunta: textoPregunta, respuesta: textoCorrecto });
    }
    
    btnSiguiente.style.display = 'block';
  }

  function siguientePregunta() {
    preguntas[indexActual].classList.remove('activa');
    btnSiguiente.style.display = 'none';
    
    indexActual++;

    if (indexActual < preguntas.length) {
      preguntas[indexActual].classList.add('activa');
      actualizarProgreso();
    } else {
      // FINAL DEL TEST
      progresoDiv.style.display = 'none';
      contenedorTest.style.display = 'none';
      divResultados.style.display = 'block';
      document.getElementById('aciertos').innerText = aciertos;
      document.getElementById('total').innerText = preguntas.length;

      // MOSTRAR ERRORES SI LOS HAY
      if (arrayErrores.length > 0) {
        document.getElementById('repaso-errores').style.display = 'block';
        let listaHTML = '';
        arrayErrores.forEach((error, index) => {
          listaHTML += `
            <div style="background: #fff3f3; border-left: 5px solid #ff8182; padding: 12px; margin-bottom: 12px; border-radius: 4px;">
              <p style="margin: 0 0 8px 0; color: #24292f;"><strong>${index + 1}. ${error.pregunta}</strong></p>
              <p style="margin: 0; color: #1a7f37; font-weight: bold;">✔️ Respuesta: ${error.respuesta}</p>
            </div>
          `;
        });
        document.getElementById('lista-errores').innerHTML = listaHTML;
      }
    }
  }
</script>
