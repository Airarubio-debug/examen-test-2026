
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
    <p><strong>1. De los siguientes, indicar cuál es el activo más importante de una empresa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los ordenadores.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Las salas con equipamiento.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Los datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los usuarios.</button>
  </div>

  <div class="pregunta">
    <p><strong>2. Indicar cuál de las siguientes afirmaciones es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La seguridad informática se engloba dentro de la seguridad de la información.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La seguridad de la información se engloba dentro de la seguridad informática.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La ciberseguridad se engloba dentro de la seguridad informática.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La seguridad de la información se engloba dentro de la ciberseguridad.</button>
  </div>

  <div class="pregunta">
    <p><strong>3. En relación al ciclo de Deming (PDCA), indicar la afirmación correcta:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Consiste en planificar, verificar y actuar.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Consiste en verificar, planificar, hacer y actuar.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Consiste en planificar, verificar y hacer.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Consiste en planificar, hacer, verificar y actuar.</button>
  </div>

  <div class="pregunta">
    <p><strong>4. Respecto a las bases de la seguridad informática, indicar cuál de las siguientes afirmaciones es correcta:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La fiabilidad no influye en la seguridad informática.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La confidencialidad protege de la divulgación indiscriminada de la información.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La disponibilidad afecta a las modificaciones no autorizadas de la información.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La integridad afecta a la propiedad de la información.</button>
  </div>

  <div class="pregunta">
    <p><strong>5. Indicar cuál de los siguientes no es un mecanismo principal de autenticación del usuario:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Lo que el usuario hace (comportamiento puro no suele ser un factor principal, a diferencia de biometría de acción).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Lo que el usuario tiene (token/móvil).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Lo que el usuario es (biometría).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Lo que el usuario sabe (contraseña).</button>
  </div>

  <div class="pregunta">
    <p><strong>6. La posibilidad de que se materialice o no una amenaza explotando una vulnerabilidad es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La definición de impacto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La definición de vulnerabilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La definición de ataque.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Una definición de riesgo.</button>
  </div>

  <div class="pregunta">
    <p><strong>7. Un análisis de las vulnerabilidades del sistema:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Valora los activos de un sistema para descubrir sus debilidades frente a amenazas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) No tiene sentido si el sistema no es vulnerable.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Es la valoración que el impacto de un ataque causaría.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solamente se hace si se ha producido un ataque sobre el sistema.</button>
  </div>

  <div class="pregunta">
    <p><strong>8. En un análisis de las vulnerabilidades del sistema:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se valoran los daños de un ataque (eso es impacto).</button>
    <button class="opcion" onclick="verificar(this, true)">b) Se valoran las posibles amenazas (para ver qué debilidades pueden explotar).</button>
    <button class="opcion" onclick="verificar(this, false)">c) No es necesario identificar los activos del sistema.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No se especifican las medidas de protección posibles.</button>
  </div>

  <div class="pregunta">
    <p><strong>9. En relación a un sistema informático (SI) y los incidentes:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Si en el SI no existe una vulnerabilidad no está amenazado por ella.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Aunque no haya vulnerabilidades conocidas, sigue habiendo amenazas (la amenaza existe independientemente del sistema).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Si se materializa una amenaza, el sistema está comprometido (no siempre, los controles pueden frenarlo).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un ataque se produce cuando se materializa una amenaza (el ataque es la intención, el incidente es cuando se materializa).</button>
  </div>

  <div class="pregunta">
    <p><strong>10. Señala la afirmación FALSA sobre los conceptos de seguridad:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Riesgo para un sistema informático es lo mismo que amenaza.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El punto más débil de cualquier sistema informático son las personas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El objetivo de la confidencialidad es prevenir la divulgación no autorizada de la información.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La autenticación consiste en la verificación de la identidad del usuario.</button>
  </div>

  <div class="pregunta">
    <p><strong>11. Si alguien descubre la contraseña de acceso al sistema de un usuario, constituye una amenaza:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) De interrupción.</button>
    <button class="opcion" onclick="verificar(this, true)">b) De interceptación (rompe la confidencialidad).</button>
    <button class="opcion" onclick="verificar(this, false)">c) De modificación, porque pueden cambiar la contraseña por otra que el usuario no conozca.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No constituye ninguna amenaza.</button>
  </div>

  <div class="pregunta">
    <p><strong>12. Indicar, de las siguientes consecuencias, cuál tiene más probabilidad de ser la materialización de una amenaza física.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El equipo se reinicia continuamente (suele ser malware/drivers).</button>
    <button class="opcion" onclick="verificar(this, false)">b) El equipo se ralentiza mucho (suele ser recursos lógicos/malware).</button>
    <button class="opcion" onclick="verificar(this, false)">c) El usuario no puede acceder al sistema con su usuario y contraseña.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El equipo no arranca (por ejemplo, por fallo eléctrico, fuego o rotura de hardware).</button>
  </div>

  <div class="pregunta">
    <p><strong>13. Las redes sociales generan un gran número de vulnerabilidades de seguridad (ingeniería social, suplantación) principalmente porque:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Almacenan y exponen mucha información personal de cada usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Comunican a un gran número de personas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Darse de alta es muy sencillo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Son muy sensibles a la infección por troyanos.</button>
  </div>

  <div class="pregunta">
    <p><strong>14. Las amenazas, según su tipo de ataque a la información, pueden ser de interrupción, y además:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) De interrelación, modificación y fabricación.</button>
    <button class="opcion" onclick="verificar(this, true)">b) De interceptación, modificación y fabricación.</button>
    <button class="opcion" onclick="verificar(this, false)">c) De modificación, interrelación, identificación y fabricación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Físicas y de modificación.</button>
  </div>

  <div class="pregunta">
    <p><strong>15. Indica cuál es la opción falsa de las siguientes afirmaciones relacionadas con posibles ataques realizados a personas:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) El basureo (dumpster diving) se basa en obtener información dejada encima de la mesa.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La ingeniería social puede conducir a actos tipificados como delito por la ley.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El shoulder surfing consiste en "espiar" físicamente a los usuarios mirando por encima del hombro.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El masquerading se basa en suplantar la identidad de un usuario autorizado.</button>
  </div>

  <div class="pregunta">
    <p><strong>16. El acceso a un CPD (Centro de Proceso de Datos) de una persona no autorizada es:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Una amenaza física.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una amenaza lógica.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una amenaza de modificación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Una amenaza de interrelación.</button>
  </div>

  <div class="pregunta">
    <p><strong>17. La diferencia entre un SAI (Sistema de Alimentación Ininterrumpida) y un grupo electrógeno es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El SAI es capaz de generar energía eléctrica de la nada.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El grupo electrógeno suministra electricidad de forma instantánea sin corte previo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El SAI utiliza energía mecánica para generar electricidad.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El grupo electrógeno es capaz de generar electricidad a partir de energía mecánica (combustible) y el SAI no (usa baterías acumuladas).</button>
  </div>

  <div class="pregunta">
    <p><strong>18. De las siguientes medidas, indicar cuál es de seguridad pasiva (actúa después del incidente para minimizar daños):</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Medidas de carácter activo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Medidas de carácter preventivo.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Medidas de carácter reparativo (por ejemplo, las copias de seguridad).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Todas son de seguridad pasiva.</button>
  </div>

  <div class="pregunta">
    <p><strong>19. ¿En qué tipo de SAI no hay un tiempo de conmutación y las baterías están constantemente trabajando (alimentando a los equipos)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) In line interactivo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Off line pasivo.</button>
    <button class="opcion" onclick="verificar(this, true)">c) On line (doble conversión).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna es válida.</button>
  </div>

  <div class="pregunta">
    <p><strong>20. Indicar, de las siguientes, cuál es una función del SAI.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Protege el dispositivo electrónico de picos de tensión.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Protege el dispositivo electrónico de caídas de tensión.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Protege el dispositivo electrónico de cortes de tensión.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas son válidas (actúa como filtro y batería).</button>
  </div>

  <div class="pregunta">
    <p><strong>21. La determinación del nivel aceptable de seguridad corresponde a una política de:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Aceptar el riesgo (asumimos que existe un riesgo residual y decidimos no invertir más en mitigarlo).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Evitar el riesgo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Olvidar el riesgo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna de las anteriores.</button>
  </div>

  <div class="pregunta">
    <p><strong>22. La política de seguridad de la organización:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Debe describir qué se intenta proteger y por qué se debe hacer, sin entrar en detalles técnicos acerca del cómo (eso son los procedimientos).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Debe describir qué se intenta proteger, por qué se debe hacer y cómo se debe implementar paso a paso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Debe describir qué se intenta proteger, por qué se debe hacer, cómo se debe implementar y cuándo hay que implementar los mecanismos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Debe describir qué se intenta proteger, cómo se debe aplicar y cuándo hay que implementar los mecanismos.</button>
  </div>

  <div class="pregunta">
    <p><strong>23. En relación con las políticas de seguridad, indicar qué norma o procedimiento NO debe establecer una política de seguridad TIC:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Temas salariales.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Seguridad física y ambiental.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Plan de contingencia.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Prevención y detección de malware.</button>
  </div>

  <div class="pregunta">
    <p><strong>24. Respecto al nivel de riesgo de los datos o su clasificación, indicar cuál de los siguientes NO suele ser una etiqueta de clasificación estándar:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Confidencial.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Uso restringido.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Uso interno.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Uso particular (no es una clasificación empresarial típica).</button>
  </div>

</div> <button id="btn-siguiente" onclick="siguientePregunta()">Siguiente pregunta ➡️</button>

<div id="resultados">
  <h2>¡Test completado! 🎉</h2>
  <p style="font-size: 18px;">Has acertado <strong id="aciertos">0</strong> de <strong id="total">0</strong> preguntas.</p>
  <button id="btn-repetir" onclick="location.reload()">↻ Repetir test</button>
</div>

<script>
  let indexActual = 0;
  let aciertos = 0;
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
      botones.forEach(b => {
        if(b.getAttribute("onclick").includes("true")) {
          b.classList.add('correcta');
        }
      });
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
      progresoDiv.style.display = 'none';
      contenedorTest.style.display = 'none';
      divResultados.style.display = 'block';
      document.getElementById('aciertos').innerText = aciertos;
      document.getElementById('total').innerText = preguntas.length;
    }
  }
</script>
