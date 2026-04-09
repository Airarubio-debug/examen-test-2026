
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
    <button class="opcion" onclick="verificar(this, false)">d) Documentar reglas de negocio en lenguaje natural.</button>
  </div>

  <div class="pregunta">
    <p><strong>18. En el contexto de AMFE, la identificación de componentes críticos puede incluir:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solo los algoritmos de análisis, ignorando el resto del sistema.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Sistemas de almacenamiento, hardware/software y procesos de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Únicamente las decisiones del comité de dirección.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo las herramientas de visualización de cuadros de mando.</button>
  </div>

  <div class="pregunta">
    <p><strong>19. Una de las recomendaciones al elaborar un plan de acción tras el Ishikawa es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Plantear muchas acciones sin necesidad de seguimiento posterior.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Asignar siempre la misma persona responsable a todas las acciones.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Que cada acción ataque una causa raíz concreta, no solo un síntoma.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Evitar poner fechas límite para no presionar al equipo.</button>
  </div>

  <div class="pregunta">
    <p><strong>20. ¿Qué problema típico se asocia a la categoría 'Métodos' en un diagrama de Ishikawa?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Falta de sensores de temperatura en el CPD.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Formulario sin validación de campos críticos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Picos de tráfico en septiembre.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Usuarios novatos sin guía inicial.</button>
  </div>

  <div class="pregunta">
    <p><strong>21. ¿Cuál de las siguientes opciones corresponde a un ejemplo de 'proceso' en el ámbito de la digitalización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Validar el DNI en un formulario online.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Implantar matrícula online 2025.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Portal de pagos.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Matricular online a alumnos.</button>
  </div>

  <div class="pregunta">
    <p><strong>22. Cuando un modo de fallo obtiene un RPN muy alto, la recomendación es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Posponer su análisis para fases posteriores del proyecto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Tratarlo como riesgo residual aceptable.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Priorizar la implementación de medidas correctivas y preventivas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Centrarse solo en documentarlo sin tomar acciones.</button>
  </div>

  <div class="pregunta">
    <p><strong>23. AMFE son las siglas de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Análisis de Modelos Funcionales y Eficiencia.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Análisis Modal de Fallos y Efectos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aplicación Metódica de Fallos Estructurales.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Análisis de Métricas de Fiabilidad y Errores.</button>
  </div>

  <div class="pregunta">
    <p><strong>24. ¿Qué elemento NO es una categoría típica de causa en un diagrama de Ishikawa de las 6M adaptadas a digitalización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Materiales/Datos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Medición.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Marketing/Ventas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Maquinaria/Tecnología/Equipo.</button>
  </div>

  <div class="pregunta">
    <p><strong>25. En la guía inicial de AMFE, el 'modo de fallo' se define como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El impacto económico global del proyecto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La consecuencia visible en el cliente.</button>
    <button class="opcion" onclick="verificar(this, true)">c) La forma en que se manifiesta el fallo en el componente o proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La probabilidad de que el fallo ocurra en un periodo dado.</button>
  </div>

  <div class="pregunta">
    <p><strong>26. En la fase de lluvia de ideas de un diagrama de Ishikawa, es recomendable:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Buscar una única causa raíz desde el principio.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Escribir causas en varias categorías si están relacionadas con más de un ámbito.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evitar la participación de distintos perfiles del proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Plantear directamente soluciones en lugar de causas.</button>
  </div>

  <div class="pregunta">
    <p><strong>27. ¿Qué se evalúa con la 'severidad' en AMFE?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La facilidad para detectar el fallo antes de que suceda.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El impacto del fallo en términos de servicio, seguridad o coste.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El número de componentes afectados en el sistema.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La duración del proyecto de digitalización.</button>
  </div>

  <div class="pregunta">
    <p><strong>28. ¿Cuál es el nivel de modelado de BPMN que muestra el proceso completo con sus principales actividades y eventos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Nivel de actividades.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Diagrama de proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Nivel de implementación técnica.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Diagrama de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>29. En la categoría 'Materiales/Datos' del diagrama de Ishikawa se analizan principalmente:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Roles, turnos y carga de trabajo.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Calidad de datos, formatos e integridad de la información.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Normativa aplicable y calendario académico.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Alertas, paneles y registros de auditoría.</button>
  </div>

  <div class="pregunta">
    <p><strong>30. En BPMN, una 'tarea de usuario' se caracteriza porque:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La ejecuta automáticamente un sistema sin intervención humana.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La realiza una persona dentro del proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Representa un evento externo que dispara el proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sirve únicamente para agrupar otros subprocesos.</button>
  </div>

  <div class="pregunta">
    <p><strong>31. Entre las herramientas de software mencionadas para trabajar con BPMN se encuentra:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Wireshark.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Bizagi.</button>
    <button class="opcion" onclick="verificar(this, false)">c) MySQL Workbench.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Visual Studio Code.</button>
  </div>

  <div class="pregunta">
    <p><strong>32. ¿Cuál de las siguientes afirmaciones es correcta respecto al uso del diagrama de Ishikawa en digitalización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Su finalidad es automatizar directamente el proceso sin cambios previos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Permite evitar digitalizar errores existentes al identificar ineficiencias.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo es útil para procesos industriales físicos, no para procesos digitales.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sustituye completamente la necesidad de medir el rendimiento con KPIs.</button>
  </div>

  <div class="pregunta">
    <p><strong>33. Entre las mejores prácticas de modelado en BPMN se encuentra:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Usar nombres genéricos como 'hacer cosas' para las tareas.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Mantener la simplicidad y utilizar nombres descriptivos para los elementos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evitar las anotaciones explicativas para no recargar el diagrama.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Introducir todos los detalles técnicos posibles en un único diagrama.</button>
  </div>

  <div class="pregunta">
    <p><strong>34. ¿Cuál de las siguientes afirmaciones sobre las tareas en BPMN es correcta?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Todas las tareas deben ser automáticas para poder representarse.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una tarea representa una unidad de trabajo dentro del proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una tarea y un evento son equivalentes en la notación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las tareas solo se utilizan en procesos interdepartamentales.</button>
  </div>

  <div class="pregunta">
    <p><strong>35. ¿Cuál es el objetivo principal de un diagrama de Ishikawa en el contexto de la digitalización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Representar visualmente la secuencia temporal de un proyecto.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Identificar y agrupar posibles causas de un problema dentro de un proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Documentar los requisitos funcionales de un sistema de información.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Definir la arquitectura técnica de una solución en la nube.</button>
  </div>

  <div class="pregunta">
    <p><strong>36. En un análisis AMFE, el 'efecto' de un fallo hace referencia a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La causa técnica que lo provoca.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La consecuencia que se produce si el fallo ocurre.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La dificultad para detectarlo antes de que suceda.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El número de pasos del proceso afectados.</button>
  </div>

  <div class="pregunta">
    <p><strong>37. La categoría 'Medición' en un diagrama de Ishikawa se relaciona principalmente con:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) KPIs, logs, paneles y definición de qué se considera 'hecho'.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La experiencia previa del equipo de proyecto.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La ubicación física de los servidores.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los proveedores externos que intervienen en el proceso.</button>
  </div>

  <div class="pregunta">
    <p><strong>38. Una característica clave del diagrama de Ishikawa es que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se construye siempre de arriba hacia abajo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Solo puede ser elaborado por personal directivo.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Muestra categorías de causas conectadas a un efecto central.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se basa exclusivamente en datos cuantitativos históricos.</button>
  </div>

  <div class="pregunta">
    <p><strong>39. ¿Cuál de las siguientes afirmaciones sobre 'Mano de obra/Personas' es correcta?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se centra en la capacidad de los sistemas para procesar grandes volúmenes de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Incluye aspectos como competencias, comunicación y sobrecarga de trabajo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo analiza el número total de usuarios del sistema.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Hace referencia exclusiva a la formación en ciberseguridad.</button>
  </div>

  <div class="pregunta">
    <p><strong>40. BPMN se utiliza principalmente para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Modelar redes físicas de ordenadores.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Representar y documentar procesos de negocio de forma gráfica.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Diseñar bases de datos relacionales.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Estimar presupuestos de proyectos de TI.</button>
  </div>

  <div class="pregunta">
    <p><strong>41. ¿Cuál de los siguientes NO es un elemento básico de BPMN?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tareas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Eventos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Gateways (compuertas).</button>
    <button class="opcion" onclick="verificar(this, true)">d) Tablas de decisión SQL.</button>
  </div>

  <div class="pregunta">
    <p><strong>42. En la categoría 'Maquinaria/Tecnología/Equipo' se incluiría como causa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No hay checklist común de alta de usuarios.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Portal de matrícula se cae en momentos de pico de uso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Soporte solo disponible en horario de mañana.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Falta de ejemplos de documentos válidos.</button>
  </div>

  <div class="pregunta">
    <p><strong>43. ¿Cuál de las siguientes afirmaciones describe mejor el objetivo global de BPMN en la organización?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Servir de puente entre quienes analizan/mejoran el proceso y quienes lo implementan tecnológicamente.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Sustituir todos los demás lenguajes gráficos utilizados en ingeniería.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Representar únicamente diagramas de red y arquitectura técnica.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Imponer una forma única de trabajar sin posibilidad de adaptación.</button>
  </div>

  <div class="pregunta">
    <p><strong>44. Al usar Ishikawa, es recomendable formular las causas con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Etiquetas vagas como 'falta de interés' o 'desastre de proceso'.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Verbos de proceso como 'no se verifica' o 'no se calibra'.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Referencias personales a quién comete el error.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Descripciones emocionales para implicar al equipo.</button>
  </div>

  <div class="pregunta">
    <p><strong>45. ¿En qué momento del ciclo de mejora continua suele ser más útil un diagrama de Ishikawa?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Al definir los indicadores KPI.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Cuando ya se han implantado las soluciones definitivas.</button>
    <button class="opcion" onclick="verificar(this, true)">c) En la fase de análisis de causas de un problema detectado.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo al inicio del año académico.</button>
  </div>

  <div class="pregunta">
    <p><strong>46. En la aplicación de AMFE a sistemas de digitalización, un componente crítico puede ser:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El horario de apertura del centro educativo.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El sistema de almacenamiento de datos en la nube.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La política de marketing de la organización.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La decoración de la sala de servidores.</button>
  </div>

  <div class="pregunta">
    <p><strong>47. ¿Cuál de estas opciones corresponde a un síntoma y no a una causa raíz?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Los pedidos llegan tarde al cliente.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El proveedor entrega fuera de plazo por cambios de última hora.</button>
    <button class="opcion" onclick="verificar(this, false)">c) No existe un paso de aprobación antes de enviar el pedido.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No hay procedimiento estandarizado para registrar los pedidos.</button>
  </div>

  <div class="pregunta">
    <p><strong>48. Las flechas que conectan elementos en un diagrama BPMN representan:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La secuencia de ejecución del proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Los flujos de datos entre distintas bases de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La prioridad de cada tarea frente a las demás.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los permisos de acceso de los usuarios.</button>
  </div>

  <div class="pregunta">
    <p><strong>49. ¿Qué NO proporciona el diagrama de Ishikawa por sí solo?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Una lista estructurada de posibles causas por categorías.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un criterio numérico para priorizar qué causas atacar primero.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un mapa visual de relación causa–efecto.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un soporte para lluvia de ideas por categorías.</button>
  </div>

  <div class="pregunta">
    <p><strong>50. ¿Cuál es la fórmula del Índice de Prioridad de Riesgos (IPR o RPN) en AMFE?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) IPR = Severidad + Ocurrencia + Detección.</button>
    <button class="opcion" onclick="verificar(this, false)">b) IPR = (Severidad × Ocurrencia) + Detección.</button>
    <button class="opcion" onclick="verificar(this, true)">c) IPR = Severidad × Ocurrencia × Detección.</button>
    <button class="opcion" onclick="verificar(this, false)">d) IPR = Severidad ÷ (Ocurrencia × Detección).</button>
  </div>

  <div class="pregunta">
    <p><strong>51. La 'ocurrencia' en AMFE está relacionada con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La rapidez con la que se corrige un incidente.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La probabilidad o frecuencia con la que puede darse un modo de fallo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La importancia estratégica del cliente afectado.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La cantidad de datos almacenados en el sistema.</button>
  </div>

  <div class="pregunta">
    <p><strong>52. ¿Qué práctica es clave al aplicar la técnica de los '¿Por qué?' en un Ishikawa?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Formular las causas como juicios personales sobre las personas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Detenerse siempre en el segundo nivel de '¿por qué?'.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Acompañar cada '¿por qué?' con evidencias o ejemplos del proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Usar términos genéricos como 'mala calidad' o 'desastre' para resumir.</button>
  </div>

  <div class="pregunta">
    <p><strong>53. ¿Qué tres dimensiones se combinan en el cálculo del IPR (RPN) en AMFE?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Severidad, coste y tiempo.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Severidad, ocurrencia y detección.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Ocurrencia, detección y número de usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Probabilidad, impacto mediático y complejidad técnica.</button>
  </div>

  <div class="pregunta">
    <p><strong>54. Una “severidad” alta en AMFE indica que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El fallo se produce con mucha frecuencia.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El fallo es casi imposible de detectar.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Las consecuencias del fallo son muy graves para el cliente o el sistema.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El tiempo para corregir el fallo es muy corto.</button>
  </div>

  <div class="pregunta">
    <p><strong>55. En la escala de frecuencia de ocurrencia de AMFE, un valor alto indica que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El modo de fallo apenas se ha observado en procesos similares.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Existe gran probabilidad de que el fallo se produzca con frecuencia.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El fallo tiene un impacto poco relevante en el cliente.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El fallo es casi imposible de detectar antes de que ocurra.</button>
  </div>

  <div class="pregunta">
    <p><strong>56. En el proceso de modelado con BPMN, un primer paso recomendado es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Elegir la herramienta de automatización antes de conocer el proceso.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Identificar a los actores implicados, como empleados, sistemas o clientes.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Calcular directamente los costes de implementación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Definir la arquitectura de red de la organización.</button>
  </div>

  <div class="pregunta">
    <p><strong>57. ¿Cuál de los siguientes aspectos se menciona como ventaja del uso sistemático de BPMN?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Incrementa la ambigüedad sobre quién es responsable de cada tarea.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Dificulta el cumplimiento normativo al ocultar reglas de decisión.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Ayuda a detectar cuellos de botella, retrabajos y esperas en el proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Impide la integración con otras metodologías como Lean o AMFE.</button>
  </div>

  <div class="pregunta">
    <p><strong>58. En un diagrama de Ishikawa, el 'proceso' se entiende como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Una única tarea aislada realizada por un usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El conjunto de herramientas utilizadas para realizar un trabajo.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El conjunto de actividades relacionadas que transforman entradas en salidas con valor para un cliente.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un proyecto temporal con inicio y fin únicos para implantar un cambio.</button>
  </div>

  <div class="pregunta">
    <p><strong>59. En un proyecto de mejora continua, BPMN ayuda especialmente a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Definir el hardware exacto que hay que comprar.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Cerrar el ciclo entre análisis de causas, priorización de riesgos y ejecución del trabajo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Sustituir cualquier necesidad de indicadores KPI.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Asegurar que no haya intervención humana en los procesos.</button>
  </div>

  <div class="pregunta">
    <p><strong>60. ¿Qué enunciado describe mejor la categoría 'Medio ambiente/Entorno'?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Incluye políticas de copias de seguridad y restauración.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se centra en scripts de automatización y APIs.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Considera factores como calendario, picos de demanda y conectividad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Agrupa únicamente los riesgos legales del proyecto.</button>
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
