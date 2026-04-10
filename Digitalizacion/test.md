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
    <p><strong>1. La 'detección' en AMFE mide:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La capacidad de detectar el fallo antes de que tenga impacto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El tiempo que tarda el usuario en informar del fallo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El número de equipos implicados en el proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El coste de sustituir el componente defectuoso.</button>
  </div>

  <div class="pregunta">
    <p><strong>2. ¿Cuál es la relación entre AMFE y BPMN?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) BPMN sustituye completamente a AMFE en la gestión de riesgos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) AMFE modela el flujo y BPMN prioriza riesgos.</button>
    <button class="opcion" onclick="verificar(this, true)">c) BPMN sirve para plasmar en el proceso las mejoras y controles priorizados con AMFE.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No existe relación; se usan en contextos totalmente distintos.</button>
  </div>

  <div class="pregunta">
    <p><strong>3. Una ventaja de BPMN en relación con la automatización es que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No puede usarse nunca como base para motores de workflow.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Incluye un metamodelo y formato de intercambio que facilita su ejecución en algunas herramientas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo sirve para documentación impresa, no para herramientas software.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Debe traducirse siempre manualmente a código fuente sin soporte automático.</button>
  </div>

  <div class="pregunta">
    <p><strong>4. La siguiente opción de una App: 'Resetear contraseña’; se considera:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un proceso.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una tarea o actividad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un sistema o herramienta.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un proyecto.</button>
  </div>

  <div class="pregunta">
    <p><strong>5. En el diagrama de Ishikawa, la 'cabeza del pez' representa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La categoría de causas más importante.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La herramienta informática que soporta el proceso.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El problema o efecto que se quiere analizar.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El plan de acción para corregir el problema.</button>
  </div>

  <div class="pregunta">
    <p><strong>6. ¿Qué tipo de elementos permiten representar ciclos o repeticiones en un diagrama BPMN?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Data Objects.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Pools y lanes.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Bucles y secuencias configuradas en actividades.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Eventos de inicio múltiples.</button>
  </div>

  <div class="pregunta">
    <p><strong>7. En la tabla de plan de acción derivada del Ishikawa suele aparecer, entre otros, el siguiente campo:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Presupuesto total del proyecto de digitalización.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Cómo se comprobará la mejora obtenida.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Nombre comercial del proveedor de hardware.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Listado detallado de todos los usuarios finales.</button>
  </div>

  <div class="pregunta">
    <p><strong>8. En BPMN, las 'piscinas' (pools) y 'carriles' (lanes) sirven para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Indicar el nivel de prioridad de las tareas.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Agrupar elementos según roles, departamentos u organizaciones.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Mostrar únicamente los tiempos de espera entre actividades.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Definir la estructura de datos del sistema.</button>
  </div>

  <div class="pregunta">
    <p><strong>9. Un beneficio clave de BPMN es que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solo puede ser entendido por perfiles técnicos muy especializados.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Proporciona un lenguaje común entre negocio y TI para describir procesos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se limita a representar organigramas de la empresa.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No permite modelar decisiones ni eventos.</button>
  </div>

  <div class="pregunta">
    <p><strong>10. Una ventaja de aplicar AMFE de forma sistemática es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Permite eliminar completamente todos los riesgos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Facilita focalizar recursos en los riesgos que tienen mayor prioridad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Sustituye la necesidad de monitorizar el sistema en producción.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Evita tener que hablar con usuarios o responsables del proceso.</button>
  </div>

  <div class="pregunta">
    <p><strong>11. Las siglas BPMN significan:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Business Process Model and Notation.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Business Project Management Network.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Business Performance Metrics Notation.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Binary Process Modeling Notation.</button>
  </div>

  <div class="pregunta">
    <p><strong>12. ¿Cuál es la relación principal entre el diagrama de Ishikawa y la metodología AMFE?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El Ishikawa cuantifica riesgos y el AMFE los representa gráficamente.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El Ishikawa identifica posibles causas y el AMFE valora su riesgo y prioriza acciones.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El AMFE se utiliza solo antes de elaborar el diagrama de Ishikawa.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ambos se usan exclusivamente para documentar procesos sin tomar decisiones.</button>
  </div>

  <div class="pregunta">
    <p><strong>13. En un diagrama BPMN, los eventos de inicio:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Indican el momento en que un proceso o subproceso comienza.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Representan las decisiones internas de un responsable.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo se usan en procesos automáticos sin intervención humana.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Deben situarse siempre al final del diagrama.</button>
  </div>

  <div class="pregunta">
    <p><strong>14. Un 'Data Object' en BPMN representa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un servidor físico donde se almacenan los datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los datos utilizados o generados en el proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La base de datos corporativa completa.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un usuario que introduce información en el sistema.</button>
  </div>

  <div class="pregunta">
    <p><strong>15. Los subprocesos en BPMN se utilizan para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Resumir varios procesos independientes en un solo símbolo sin detalle.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Dividir un proceso en partes más manejables y detallarlas cuando sea necesario.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Representar decisiones complejas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Modelar exclusivamente interacciones con sistemas externos.</button>
  </div>

  <div class="pregunta">
    <p><strong>16. ¿Cuál de las siguientes afirmaciones sobre AMFE es correcta?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es una metodología puramente cuantitativa basada solo en datos históricos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Es más económico reducir la probabilidad de fallo que dedicar recursos a resolverlo después.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se aplica únicamente a productos físicos, no a procesos digitales.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sustituye completamente la necesidad de formación del personal.</button>
  </div>

  <div class="pregunta">
    <p><strong>17. En BPMN, los 'gateways' se utilizan para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Definir los datos de entrada y salida.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Representar puntos de decisión o división del flujo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Indicar el inicio o fin del proceso.</button>
