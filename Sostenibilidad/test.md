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

<div class="pregunta">
    <p><strong>11. ¿Cuáles son los tres pilares del desarrollo sostenible?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tecnología, rentabilidad y ecología</button>
    <button class="opcion" onclick="verificar(this, true)">b) Medioambiental, económico y social</button>
    <button class="opcion" onclick="verificar(this, false)">c) Humano, tecnológico y regulatorio</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ambiental, digital y financiero</button>
  </div>

  <div class="pregunta">
    <p><strong>12. La huella ecológica debe ser:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Igual que la biocapacidad</button>
    <button class="opcion" onclick="verificar(this, false)">b) Mayor que la biocapacidad</button>
    <button class="opcion" onclick="verificar(this, true)">c) Menor que la biocapacidad</button>
    <button class="opcion" onclick="verificar(this, false)">d) No influye en el desarrollo sostenible</button>
  </div>

  <div class="pregunta">
    <p><strong>13. Los criterios ASG sirven para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aumentar beneficios exclusivamente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Evaluar prácticas empresariales y guiar decisiones sostenibles</button>
    <button class="opcion" onclick="verificar(this, false)">c) Sustituir la dirección de la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) Exigir auditoría interna anual</button>
  </div>

  <div class="pregunta">
    <p><strong>14. Dentro de las “A” de los ASG se incluye:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Derechos humanos</button>
    <button class="opcion" onclick="verificar(this, false)">b) Gobernanza corporativa</button>
    <button class="opcion" onclick="verificar(this, true)">c) Mitigación del cambio climático</button>
    <button class="opcion" onclick="verificar(this, false)">d) Rotación del personal</button>
  </div>

  <div class="pregunta">
    <p><strong>15. Un riesgo de no aplicar criterios sociales es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reducción del transporte</button>
    <button class="opcion" onclick="verificar(this, true)">b) Más absentismo y dificultades para atraer talento</button>
    <button class="opcion" onclick="verificar(this, false)">c) Más innovación tecnológica</button>
    <button class="opcion" onclick="verificar(this, false)">d) Exceso de stock</button>
  </div>

  <div class="pregunta">
    <p><strong>16. Una buena gestión ASG permite:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Disminuir la motivación de los empleados</button>
    <button class="opcion" onclick="verificar(this, false)">b) Perder acceso a financiación</button>
    <button class="opcion" onclick="verificar(this, true)">c) Mejorar la reputación y atraer talento</button>
    <button class="opcion" onclick="verificar(this, false)">d) Reducir la transparencia</button>
  </div>

  <div class="pregunta">
    <p><strong>17. Las empresas deben redactar un Informe No Financiero porque lo exige:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La OTAN</button>
    <button class="opcion" onclick="verificar(this, true)">b) La Unión Europea</button>
    <button class="opcion" onclick="verificar(this, false)">c) El Banco Mundial</button>
    <button class="opcion" onclick="verificar(this, false)">d) La OMS</button>
  </div>

  <div class="pregunta">
    <p><strong>18. La verificación externa de los informes de sostenibilidad por una auditoría:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es opcional</button>
    <button class="opcion" onclick="verificar(this, false)">b) Está prohibida</button>
    <button class="opcion" onclick="verificar(this, true)">c) Es obligatoria</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo aplica a ONG</button>
  </div>

  <div class="pregunta">
    <p><strong>19. Los grupos de interés son personas que influyen o son influidas por la empresa:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso</button>
  </div>

  <div class="pregunta">
    <p><strong>20. Los propietarios o accionistas aportan principalmente:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Mano de obra</button>
    <button class="opcion" onclick="verificar(this, true)">b) Capital</button>
    <button class="opcion" onclick="verificar(this, false)">c) Materias primas</button>
    <button class="opcion" onclick="verificar(this, false)">d) Trabajo</button>
  </div>

  <div class="pregunta">
    <p><strong>21. Un riesgo asociado a los empleados es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Incumplir leyes</button>
    <button class="opcion" onclick="verificar(this, true)">b) Desmotivación</button>
    <button class="opcion" onclick="verificar(this, false)">c) Competencia desleal</button>
    <button class="opcion" onclick="verificar(this, false)">d) Inflación</button>
  </div>

  <div class="pregunta">
    <p><strong>22. Las administraciones públicas aportan:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Financiación directa únicamente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Normas, bienes y servicios públicos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Mano de obra especializada</button>
    <button class="opcion" onclick="verificar(this, false)">d) Insumos productivos</button>
  </div>

  <div class="pregunta">
    <p><strong>23. La economía lineal se caracteriza por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Priorizar el reciclaje sobre la producción</button>
    <button class="opcion" onclick="verificar(this, true)">b) Modelo de extraer–fabricar–consumir-desechar</button>
    <button class="opcion" onclick="verificar(this, false)">c) Uso de energías renovables</button>
    <button class="opcion" onclick="verificar(this, false)">d) Minimización de residuos</button>
  </div>

  <div class="pregunta">
    <p><strong>24. “Renovar” en las 7R significa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Crear productos totalmente nuevos a partir de recursos naturales extraídos del planeta</button>
    <button class="opcion" onclick="verificar(this, true)">b) Dar un nuevo uso a productos existentes</button>
    <button class="opcion" onclick="verificar(this, false)">c) Consumir más recursos naturales</button>
    <button class="opcion" onclick="verificar(this, false)">d) Transformar desechos en nuevos productos</button>
  </div>

  <div class="pregunta">
    <p><strong>25. Un beneficio para la empresa que adopta economía verde:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Menores riesgos legales</button>
    <button class="opcion" onclick="verificar(this, false)">b) Mayor eficiencia energética</button>
    <button class="opcion" onclick="verificar(this, false)">c) Mayor fidelización de clientes</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas son correctas</button>
  </div>

  <div class="pregunta">
    <p><strong>26. El ciclo de vida comienza con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Distribución</button>
    <button class="opcion" onclick="verificar(this, false)">b) Consumo</button>
    <button class="opcion" onclick="verificar(this, true)">c) Aprovisionamiento</button>
    <button class="opcion" onclick="verificar(this, false)">d) Desecho</button>
  </div>

  <div class="pregunta">
    <p><strong>27. El ecodiseño según ISO 14006 se enfoca en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reducir el coste del marketing</button>
    <button class="opcion" onclick="verificar(this, true)">b) Minimizar impacto ambiental del ciclo de vida</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aumentar la rotación de productos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Vender productos premium</button>
  </div>

  <div class="pregunta">
    <p><strong>28. El principal límite estructural de la economía lineal se debe a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La saturación de los mercados globales</button>
    <button class="opcion" onclick="verificar(this, true)">b) El agotamiento de sumideros y fuentes naturales por encima de su capacidad</button>
    <button class="opcion" onclick="verificar(this, false)">c) El aumento del comercio internacional</button>
    <button class="opcion" onclick="verificar(this, false)">d) La reducción de emisiones en países desarrollados</button>
  </div>

  <div class="pregunta">
    <p><strong>29. Uno de los principios del ecodiseño es la “producción limpia”, que implica:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aumentar las emisiones para acelerar procesos</button>
    <button class="opcion" onclick="verificar(this, true)">b) Minimizar emisiones y descarbonizar procesos productivos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Duplicar el consumo de energía</button>
    <button class="opcion" onclick="verificar(this, false)">d) Limitar la innovación tecnológica</button>
  </div>

  <div class="pregunta">
    <p><strong>30. Un riesgo reputacional grave asociado a no cumplir los criterios sociales (S) es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aumento de la competencia externa</button>
    <button class="opcion" onclick="verificar(this, false)">b) Disminución del absentismo</button>
    <button class="opcion" onclick="verificar(this, true)">c) Dificultad de atraer talento y aumento de conflictos con inspecciones</button>
    <button class="opcion" onclick="verificar(this, false)">d) Pérdida de capacidad de innovación tecnológica</button>
  </div>

  <div class="pregunta">
    <p><strong>31. En el ámbito ASG, la gobernanza (G) adquiere relevancia estratégica porque:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reduce la responsabilidad de la junta directiva en materia de sostenibilidad</button>
    <button class="opcion" onclick="verificar(this, true)">b) Dicta medidas de control interno que generan confianza y previenen prácticas poco éticas</button>
    <button class="opcion" onclick="verificar(this, false)">c) Depende exclusivamente del comportamiento de los clientes</button>
    <button class="opcion" onclick="verificar(this, false)">d) Permite a las empresas evitar auditorías externas</button>
  </div>

  <div class="pregunta">
    <p><strong>32. Los criterios ASG se consideran una herramienta de gobernanza avanzada porque:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Eliminan la necesidad de emitir informes financieros</button>
    <button class="opcion" onclick="verificar(this, true)">b) Incorporan variables ambientales, sociales y éticas a la toma de decisiones estratégicas</button>
    <button class="opcion" onclick="verificar(this, false)">c) Garantizan la rentabilidad de corto plazo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sustituyen cualquier marco normativo europeo</button>
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
