
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
    <p><strong>1. ¿Cuál de los siguientes es un portal de empleo público en España?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) LinkedIn</button>
    <button class="opcion" onclick="verificar(this, false)">b) InfoJobs</button>
    <button class="opcion" onclick="verificar(this, true)">c) SEPE (Servicio Público de Empleo Estatal)</button>
    <button class="opcion" onclick="verificar(this, false)">d) Indeed</button>
  </div>

  <div class="pregunta">
    <p><strong>2. El currículum cronológico inverso presenta la experiencia laboral:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Desde la más antigua a la más reciente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Desde la más reciente a la más antigua</button>
    <button class="opcion" onclick="verificar(this, false)">c) Por orden alfabético de empresas</button>
    <button class="opcion" onclick="verificar(this, false)">d) Agrupada por habilidades</button>
  </div>

  <div class="pregunta">
    <p><strong>3. ¿Qué es EURES?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Una plataforma española de empleo</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un portal europeo de movilidad laboral</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un sindicato europeo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un programa de becas universitarias</button>
  </div>

  <div class="pregunta">
    <p><strong>4. La huella digital activa se compone de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Datos recopilados automáticamente por las plataformas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Publicaciones, comentarios y contenido que el usuario genera voluntariamente</button>
    <button class="opcion" onclick="verificar(this, false)">c) El historial de navegación del usuario</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las cookies almacenadas en el dispositivo</button>
  </div>

  <div class="pregunta">
    <p><strong>5. La marca personal tiene como objetivo principal:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aumentar el número de seguidores en redes sociales</button>
    <button class="opcion" onclick="verificar(this, true)">b) Proyectar una imagen auténtica que genere oportunidades profesionales</button>
    <button class="opcion" onclick="verificar(this, false)">c) Vender productos propios en internet</button>
    <button class="opcion" onclick="verificar(this, false)">d) Obtener certificaciones académicas reconocidas</button>
  </div>

  <div class="pregunta">
    <p><strong>6. ¿Cuál es la principal diferencia entre una carta de presentación y una carta de motivación?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La carta de motivación es más formal que la de presentación</button>
    <button class="opcion" onclick="verificar(this, true)">b) La carta de presentación acompaña a una oferta concreta; la de motivación es más personal y académica</button>
    <button class="opcion" onclick="verificar(this, false)">c) La carta de motivación solo se usa en procesos de selección privados</button>
    <button class="opcion" onclick="verificar(this, false)">d) No existe diferencia, son documentos equivalentes</button>
  </div>

  <div class="pregunta">
    <p><strong>7. El networking profesional consiste en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Buscar empleo exclusivamente a través de internet</button>
    <button class="opcion" onclick="verificar(this, true)">b) Construir y mantener una red de contactos profesionales que generen oportunidades</button>
    <button class="opcion" onclick="verificar(this, false)">c) Publicar el currículum en múltiples portales de empleo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Acudir a todas las ofertas de trabajo disponibles</button>
  </div>

  <div class="pregunta">
    <p><strong>8. ¿Cuál de las siguientes afirmaciones sobre el currículum vitae es CORRECTA?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Debe incluir siempre una fotografía de cuerpo entero</button>
    <button class="opcion" onclick="verificar(this, true)">b) Su extensión recomendada es de 1 a 2 páginas adaptadas al puesto</button>
    <button class="opcion" onclick="verificar(this, false)">c) Debe enviarse en el mismo formato sin adaptar a cada oferta</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cuanta más información personal incluya, mejor valorado será</button>
  </div>

  <div class="pregunta">
    <p><strong>9. Una ETT (Empresa de Trabajo Temporal) se caracteriza por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Contratar trabajadores de forma indefinida</button>
    <button class="opcion" onclick="verificar(this, true)">b) Actuar como intermediaria cediendo trabajadores a otras empresas de forma temporal</button>
    <button class="opcion" onclick="verificar(this, false)">c) Gestionar únicamente ofertas de empleo público</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ofrecer solo contratos en prácticas</button>
  </div>

  <div class="pregunta">
    <p><strong>10. ¿Cuál de los siguientes es un ejemplo de soft skill?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Manejo de Excel avanzado</button>
    <button class="opcion" onclick="verificar(this, true)">b) Empatía y trabajo en equipo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Conocimiento de un lenguaje de programación</button>
    <button class="opcion" onclick="verificar(this, false)">d) Titulación universitaria</button>
  </div>

  <div class="pregunta">
    <p><strong>11. Las hard skills son:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Habilidades blandas relacionadas con la inteligencia emocional</button>
    <button class="opcion" onclick="verificar(this, true)">b) Habilidades técnicas adquiridas mediante formación y experiencia</button>
    <button class="opcion" onclick="verificar(this, false)">c) Competencias digitales exclusivamente</button>
    <button class="opcion" onclick="verificar(this, false)">d) Habilidades innatas que no pueden enseñarse</button>
  </div>

  <div class="pregunta">
    <p><strong>12. La inteligencia emocional incluye principalmente:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Habilidades matemáticas y lógicas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Reconocimiento y gestión de las propias emociones y las de los demás</button>
    <button class="opcion" onclick="verificar(this, false)">c) Capacidad de memorización rápida</button>
    <button class="opcion" onclick="verificar(this, false)">d) Dominio de idiomas extranjeros</button>
  </div>

  <div class="pregunta">
    <p><strong>13. La asertividad se define como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La capacidad de imponer las propias opiniones sin considerar a los demás</button>
    <button class="opcion" onclick="verificar(this, true)">b) La habilidad de expresar pensamientos y sentimientos de forma clara y respetuosa</button>
    <button class="opcion" onclick="verificar(this, false)">c) La tendencia a evitar conflictos cediendo siempre ante otros</button>
    <button class="opcion" onclick="verificar(this, false)">d) La capacidad de hablar en público sin preparación previa</button>
  </div>

  <div class="pregunta">
    <p><strong>14. ¿Cuál es la diferencia principal entre competencias personales y competencias sociales?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Las competencias personales son innatas; las sociales se aprenden únicamente en el trabajo</button>
    <button class="opcion" onclick="verificar(this, true)">b) Las personales incluyen habilidades como la autoestima y la autodisciplina; las sociales se centran en la comunicación y el trabajo en equipo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las sociales tienen mayor valor en el mercado laboral que las personales</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las competencias personales son equivalentes a las hard skills</button>
  </div>

  <div class="pregunta">
    <p><strong>15. El pensamiento crítico implica:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Rechazar toda información que no coincida con las propias creencias</button>
    <button class="opcion" onclick="verificar(this, true)">b) Evaluar información de manera objetiva para tomar decisiones informadas</button>
    <button class="opcion" onclick="verificar(this, false)">c) Memorizar grandes cantidades de datos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Resolver problemas de forma individual sin colaboración</button>
  </div>

  <div class="pregunta">
    <p><strong>16. La escucha activa consiste en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Esperar en silencio a que el interlocutor termine de hablar</button>
    <button class="opcion" onclick="verificar(this, true)">b) Prestar atención al contenido verbal y no verbal, hacer preguntas y parafrasear</button>
    <button class="opcion" onclick="verificar(this, false)">c) Tomar notas de todo lo que dice el emisor sin interrupciones</button>
    <button class="opcion" onclick="verificar(this, false)">d) Responder de forma inmediata para demostrar atención</button>
  </div>

  <div class="pregunta">
    <p><strong>17. La resiliencia en el ámbito laboral se refiere a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La capacidad de trabajar muchas horas sin descanso</button>
    <button class="opcion" onclick="verificar(this, true)">b) La habilidad de adaptarse y recuperarse ante situaciones adversas</button>
    <button class="opcion" onclick="verificar(this, false)">c) La tendencia a evitar riesgos en la toma de decisiones</button>
    <button class="opcion" onclick="verificar(this, false)">d) El nivel de productividad individual del trabajador</button>
  </div>

  <div class="pregunta">
    <p><strong>18. ¿Cuál de las siguientes herramientas digitales se menciona para la gestión de proyectos y el trabajo colaborativo?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Photoshop y Illustrator</button>
    <button class="opcion" onclick="verificar(this, true)">b) Trello, Asana o Google Calendar</button>
    <button class="opcion" onclick="verificar(this, false)">c) AutoCAD y Revit</button>
    <button class="opcion" onclick="verificar(this, false)">d) SAP y Oracle</button>
  </div>

  <div class="pregunta">
    <p><strong>19. Los elementos del proceso de comunicación son:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Emisor, receptor, mensaje, canal, código y retroalimentación</button>
    <button class="opcion" onclick="verificar(this, false)">b) Emisor, receptor y mensaje únicamente</button>
    <button class="opcion" onclick="verificar(this, false)">c) Canal, código y ruido</button>
    <button class="opcion" onclick="verificar(this, false)">d) Emisor, mensaje y audiencia</button>
  </div>

  <div class="pregunta">
    <p><strong>20. ¿Qué tipo de comunicación incluye gestos, postura y expresión facial?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Comunicación verbal</button>
    <button class="opcion" onclick="verificar(this, false)">b) Comunicación escrita</button>
    <button class="opcion" onclick="verificar(this, true)">c) Comunicación no verbal</button>
    <button class="opcion" onclick="verificar(this, false)">d) Comunicación digital</button>
  </div>

  <div class="pregunta">
    <p><strong>21. Una barrera semántica en la comunicación se produce cuando:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El ruido ambiental impide escuchar el mensaje</button>
    <button class="opcion" onclick="verificar(this, true)">b) El emisor y el receptor atribuyen significados distintos a las mismas palabras</button>
    <button class="opcion" onclick="verificar(this, false)">c) El canal de comunicación falla técnicamente</button>
    <button class="opcion" onclick="verificar(this, false)">d) El receptor no presta atención al mensaje</button>
  </div>

  <div class="pregunta">
    <p><strong>22. El feedback en la comunicación es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El canal por el que se transmite el mensaje</button>
    <button class="opcion" onclick="verificar(this, true)">b) La respuesta del receptor al emisor que confirma la recepción del mensaje</button>
    <button class="opcion" onclick="verificar(this, false)">c) El ruido que distorsiona el mensaje</button>
    <button class="opcion" onclick="verificar(this, false)">d) El código utilizado para cifrar la información</button>
  </div>

  <div class="pregunta">
    <p><strong>23. La comunicación asertiva se diferencia de la agresiva en que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La asertiva no expresa opiniones propias</button>
    <button class="opcion" onclick="verificar(this, true)">b) La asertiva expresa los propios derechos respetando los de los demás</button>
    <button class="opcion" onclick="verificar(this, false)">c) La agresiva es más efectiva en entornos profesionales</button>
    <button class="opcion" onclick="verificar(this, false)">d) No existe diferencia entre ambas</button>
  </div>

  <div class="pregunta">
    <p><strong>24. ¿Cuál de las siguientes técnicas mejora la comunicación oral?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Hablar rápido para transmitir más información</button>
    <button class="opcion" onclick="verificar(this, true)">b) Practicar la respiración y relajación para mejorar la proyección de la voz</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evitar el contacto visual para no intimidar al receptor</button>
    <button class="opcion" onclick="verificar(this, false)">d) Usar jerga técnica para demostrar dominio del tema</button>
  </div>

  <div class="pregunta">
    <p><strong>25. El lenguaje no verbal representa aproximadamente qué porcentaje del impacto de una comunicación:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El 20%</button>
    <button class="opcion" onclick="verificar(this, false)">b) El 40%</button>
    <button class="opcion" onclick="verificar(this, true)">c) Más del 50%</button>
    <button class="opcion" onclick="verificar(this, false)">d) El 10%</button>
  </div>

  <div class="pregunta">
    <p><strong>26. ¿Qué es la comunicación descendente en una organización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La comunicación entre empleados del mismo nivel jerárquico</button>
    <button class="opcion" onclick="verificar(this, true)">b) La que fluye de superiores hacia subordinados</button>
    <button class="opcion" onclick="verificar(this, false)">c) La comunicación con clientes externos</button>
    <button class="opcion" onclick="verificar(this, false)">d) La que proviene de los empleados hacia la dirección</button>
  </div>

  <div class="pregunta">
    <p><strong>27. Una de las técnicas para mejorar la comunicación escrita es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Usar frases largas y complejas para demostrar conocimiento</button>
    <button class="opcion" onclick="verificar(this, true)">b) Organizar el contenido de manera lógica y secuencial</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evitar la revisión gramatical para ahorrar tiempo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Usar lenguaje informal siempre para conectar con el lector</button>
  </div>

  <div class="pregunta">
    <p><strong>28. El análisis DAFO estudia:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Debilidades, Amenazas, Fortalezas y Oportunidades de una empresa</button>
    <button class="opcion" onclick="verificar(this, false)">b) Datos, Activos, Finanzas y Objetivos empresariales</button>
    <button class="opcion" onclick="verificar(this, false)">c) Demanda, Audiencia, Facturación y Organización</button>
    <button class="opcion" onclick="verificar(this, false)">d) Déficit, Activos, Fondos y Operaciones</button>
  </div>

  <div class="pregunta">
    <p><strong>29. En el modelo Canvas, la 'propuesta de valor' responde a la pregunta:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) ¿Quiénes son nuestros clientes?</button>
    <button class="opcion" onclick="verificar(this, true)">b) ¿Qué problema resolvemos y por qué nos elegirían?</button>
    <button class="opcion" onclick="verificar(this, false)">c) ¿Cómo generamos ingresos?</button>
    <button class="opcion" onclick="verificar(this, false)">d) ¿Qué recursos necesitamos?</button>
  </div>

  <div class="pregunta">
    <p><strong>30. La Responsabilidad Social Corporativa (RSC) implica:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Maximizar los beneficios económicos a cualquier coste</button>
    <button class="opcion" onclick="verificar(this, true)">b) Integrar criterios sociales, ambientales y éticos en la gestión empresarial</button>
    <button class="opcion" onclick="verificar(this, false)">c) Reducir los impuestos pagados por la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aumentar la productividad eliminando puestos de trabajo</button>
  </div>

  <div class="pregunta">
    <p><strong>31. En el modelo Canvas, ¿qué módulo describe las alianzas con proveedores y socios estratégicos externos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Actividades clave</button>
    <button class="opcion" onclick="verificar(this, false)">b) Recursos clave</button>
    <button class="opcion" onclick="verificar(this, true)">c) Asociaciones clave</button>
    <button class="opcion" onclick="verificar(this, false)">d) Canales</button>
  </div>

  <div class="pregunta">
    <p><strong>32. Las oportunidades en un DAFO hacen referencia a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Factores internos positivos de la empresa</button>
    <button class="opcion" onclick="verificar(this, true)">b) Factores externos del entorno que pueden beneficiar a la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los puntos débiles de la competencia</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las fortalezas que aún no se han desarrollado</button>
  </div>

  <div class="pregunta">
    <p><strong>33. ¿Cuál de los siguientes factores forma parte del macroentorno de una empresa según el análisis PESTEL?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La política de precios interna de la empresa</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los factores políticos, económicos, sociales, tecnológicos, ecológicos y legales del entorno</button>
    <button class="opcion" onclick="verificar(this, false)">c) La estructura del organigrama empresarial</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las relaciones con los proveedores habituales</button>
  </div>

  <div class="pregunta">
    <p><strong>34. En el Canvas, las 'fuentes de ingresos' incluyen:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los gastos fijos de la empresa</button>
    <button class="opcion" onclick="verificar(this, true)">b) Las formas en que la empresa genera dinero: ventas, suscripciones, publicidad, etc.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los recursos humanos de la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las alianzas estratégicas con proveedores</button>
  </div>

  <div class="pregunta">
    <p><strong>35. La estrategia del océano azul consiste en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Competir agresivamente en mercados ya existentes</button>
    <button class="opcion" onclick="verificar(this, true)">b) Crear un espacio de mercado nuevo donde no existe competencia directa</button>
    <button class="opcion" onclick="verificar(this, false)">c) Reducir precios por debajo de la competencia</button>
    <button class="opcion" onclick="verificar(this, false)">d) Copiar los modelos de éxito de otras empresas</button>
  </div>

  <div class="pregunta">
    <p><strong>36. Las 4P del marketing mix son:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Producto, Precio, Publicidad y Plaza</button>
    <button class="opcion" onclick="verificar(this, true)">b) Producto, Precio, Promoción y Distribución (Place)</button>
    <button class="opcion" onclick="verificar(this, false)">c) Producción, Personal, Precio y Posicionamiento</button>
    <button class="opcion" onclick="verificar(this, false)">d) Precio, Publicidad, Personal y Plaza</button>
  </div>

  <div class="pregunta">
    <p><strong>37. El estudio de mercado sirve para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Establecer los precios de los productos sin analizar la competencia</button>
    <button class="opcion" onclick="verificar(this, true)">b) Analizar el entorno competitivo y obtener información para tomar decisiones</button>
    <button class="opcion" onclick="verificar(this, false)">c) Diseñar el logotipo de la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) Gestionar los recursos humanos de la empresa</button>
  </div>

  <div class="pregunta">
    <p><strong>38. La segmentación de mercado consiste en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Vender el mismo producto a todos los consumidores por igual</button>
    <button class="opcion" onclick="verificar(this, true)">b) Dividir el mercado en grupos con características y necesidades comunes</button>
    <button class="opcion" onclick="verificar(this, false)">c) Reducir el número de productos ofrecidos por la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) Fijar precios distintos para el mismo producto</button>
  </div>

  <div class="pregunta">
    <p><strong>39. ¿Qué es el mapa de empatía?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un documento contable de la empresa</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una herramienta para comprender mejor las necesidades y motivaciones del cliente</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un organigrama del equipo de marketing</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un análisis de los canales de distribución</button>
  </div>

  <div class="pregunta">
    <p><strong>40. El SEO (Search Engine Optimization) tiene como objetivo:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Pagar anuncios en buscadores para aparecer en los primeros resultados</button>
    <button class="opcion" onclick="verificar(this, true)">b) Mejorar el posicionamiento orgánico de una web en los motores de búsqueda</button>
    <button class="opcion" onclick="verificar(this, false)">c) Gestionar las redes sociales de la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) Enviar correos masivos a clientes potenciales</button>
  </div>

  <div class="pregunta">
    <p><strong>41. La cuota de mercado se define como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El total de ventas de un sector en un periodo determinado</button>
    <button class="opcion" onclick="verificar(this, true)">b) El porcentaje de ventas de una empresa respecto al total del mercado</button>
    <button class="opcion" onclick="verificar(this, false)">c) El beneficio neto obtenido por la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) El número de clientes que tiene la empresa</button>
  </div>

  <div class="pregunta">
    <p><strong>42. El marketing digital incluye estrategias como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Publicidad en televisión y radio</button>
    <button class="opcion" onclick="verificar(this, true)">b) SEO, redes sociales, email marketing y publicidad online</button>
    <button class="opcion" onclick="verificar(this, false)">c) Venta directa puerta a puerta</button>
    <button class="opcion" onclick="verificar(this, false)">d) Distribución en tiendas físicas</button>
  </div>

  <div class="pregunta">
    <p><strong>43. En las 4P, 'distribución' o 'Place' se refiere a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El precio al que se vende el producto</button>
    <button class="opcion" onclick="verificar(this, false)">b) La publicidad realizada en medios digitales</button>
    <button class="opcion" onclick="verificar(this, true)">c) Los canales y métodos para hacer llegar el producto al cliente</button>
    <button class="opcion" onclick="verificar(this, false)">d) La imagen y marca del producto</button>
  </div>

  <div class="pregunta">
    <p><strong>44. ¿Cuál de los siguientes es un ejemplo de financiación propia?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Préstamo bancario</button>
    <button class="opcion" onclick="verificar(this, true)">b) Aportaciones de los socios y autofinanciación</button>
    <button class="opcion" onclick="verificar(this, false)">c) Línea de crédito</button>
    <button class="opcion" onclick="verificar(this, false)">d) Leasing</button>
  </div>

  <div class="pregunta">
    <p><strong>45. El crowdfunding consiste en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un préstamo bancario con garantía hipotecaria</button>
    <button class="opcion" onclick="verificar(this, true)">b) La financiación colectiva a través de pequeñas aportaciones de múltiples personas</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una subvención pública para emprendedores</button>
    <button class="opcion" onclick="verificar(this, false)">d) El intercambio de servicios entre empresas</button>
  </div>

  <div class="pregunta">
    <p><strong>46. ¿Cuál es la diferencia principal entre renting y leasing?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El renting es más caro que el leasing</button>
    <button class="opcion" onclick="verificar(this, true)">b) El leasing incluye opción de compra al final del contrato; el renting normalmente no</button>
    <button class="opcion" onclick="verificar(this, false)">c) El renting solo aplica a inmuebles y el leasing a vehículos</button>
    <button class="opcion" onclick="verificar(this, false)">d) No existe diferencia práctica entre ambos</button>
  </div>

  <div class="pregunta">
    <p><strong>47. Un business angel es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un inversor público que financia empresas a través de subvenciones</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un inversor privado que aporta capital a startups a cambio de participación</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un asesor bancario especializado en pymes</button>
    <button class="opcion" onclick="verificar(this, false)">d) Una entidad de capital riesgo de gran tamaño</button>
  </div>

  <div class="pregunta">
    <p><strong>48. Las subvenciones se caracterizan por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Deben devolverse con intereses al organismo concedente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Son ayudas económicas a fondo perdido sin obligación de devolución</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo pueden solicitarlas grandes empresas</button>
    <button class="opcion" onclick="verificar(this, false)">d) Siempre provienen de entidades privadas</button>
  </div>

  <div class="pregunta">
    <p><strong>49. ¿Qué diferencia hay entre un gasto y una inversión?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Son términos equivalentes en contabilidad</button>
    <button class="opcion" onclick="verificar(this, true)">b) El gasto se consume a corto plazo; la inversión genera beneficios a largo plazo</button>
    <button class="opcion" onclick="verificar(this, false)">c) La inversión siempre implica compra de maquinaria</button>
    <button class="opcion" onclick="verificar(this, false)">d) El gasto siempre es deducible fiscalmente</button>
  </div>

  <div class="pregunta">
    <p><strong>50. ¿Cuál de las siguientes opciones describe correctamente el funcionamiento de una incubadora de empresas?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ayuda a empresas ya consolidadas a expandirse internacionalmente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Apoya a nuevos emprendedores en la materialización de su idea mediante formación, asesoramiento y espacios de trabajo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Proporciona financiación exclusivamente a startups tecnológicas en fase de crecimiento</button>
    <button class="opcion" onclick="verificar(this, false)">d) Actúa como intermediaria entre inversores privados y empresas cotizadas en bolsa</button>
  </div>

  <div class="pregunta">
    <p><strong>51. El punto muerto o umbral de rentabilidad es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El momento en que los ingresos superan ampliamente a los costes</button>
    <button class="opcion" onclick="verificar(this, true)">b) El nivel de ventas en que los ingresos igualan exactamente a los costes totales</button>
    <button class="opcion" onclick="verificar(this, false)">c) El beneficio máximo que puede obtener una empresa</button>
    <button class="opcion" onclick="verificar(this, false)">d) El punto en que la empresa deja de necesitar financiación externa</button>
  </div>

  <div class="pregunta">
    <p><strong>52. El balance de situación muestra:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los ingresos y gastos de la empresa en un periodo</button>
    <button class="opcion" onclick="verificar(this, true)">b) El activo (lo que tiene), el pasivo (lo que debe) y el patrimonio neto de la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">c) El plan de financiación a largo plazo</button>
    <button class="opcion" onclick="verificar(this, false)">d) El presupuesto de tesorería mensual</button>
  </div>

  <div class="pregunta">
    <p><strong>53. La cuenta de pérdidas y ganancias refleja:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El patrimonio total de la empresa</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los ingresos y gastos durante un periodo, indicando si hay beneficio o pérdida</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las deudas pendientes con proveedores</button>
    <button class="opcion" onclick="verificar(this, false)">d) La evolución del precio de las acciones</button>
  </div>

  <div class="pregunta">
    <p><strong>54. El activo corriente de una empresa incluye:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los inmuebles y maquinaria de la empresa</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los elementos que se pueden convertir en dinero en menos de un año</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las deudas a largo plazo con entidades bancarias</button>
    <button class="opcion" onclick="verificar(this, false)">d) El capital social aportado por los socios</button>
  </div>

  <div class="pregunta">
    <p><strong>55. ¿Cuál de los siguientes indicadores mide la capacidad de la empresa para hacer frente a sus deudas a corto plazo con sus activos más líquidos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Rentabilidad económica (ROA)</button>
    <button class="opcion" onclick="verificar(this, true)">b) Ratio de liquidez o ratio corriente</button>
    <button class="opcion" onclick="verificar(this, false)">c) Fondo de maniobra negativo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Rentabilidad financiera (ROE)</button>
  </div>

  <div class="pregunta">
    <p><strong>56. ¿Cuál es el capital mínimo requerido para constituir una Sociedad Limitada (SL) en España?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 3.000 €</button>
    <button class="opcion" onclick="verificar(this, true)">b) 1 € (Ley Crea y Crece)</button>
    <button class="opcion" onclick="verificar(this, false)">c) 6.000 €</button>
    <button class="opcion" onclick="verificar(this, false)">d) 60.000 €</button>
  </div>

  <div class="pregunta">
    <p><strong>57. El autónomo tributa sus beneficios a través de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El Impuesto de Sociedades (IS)</button>
    <button class="opcion" onclick="verificar(this, true)">b) El IRPF (Impuesto sobre la Renta de las Personas Físicas)</button>
    <button class="opcion" onclick="verificar(this, false)">c) El IVA</button>
    <button class="opcion" onclick="verificar(this, false)">d) El Impuesto de Actividades Económicas (IAE)</button>
  </div>

  <div class="pregunta">
    <p><strong>58. Una comunidad de bienes se caracteriza por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tener personalidad jurídica propia independiente de sus socios</button>
    <button class="opcion" onclick="verificar(this, true)">b) No tener personalidad jurídica propia y tener responsabilidad ilimitada</button>
    <button class="opcion" onclick="verificar(this, false)">c) Requerir un capital mínimo de 3.000 €</button>
    <button class="opcion" onclick="verificar(this, false)">d) Estar sujeta al Impuesto de Sociedades obligatoriamente</button>
  </div>

  <div class="pregunta">
    <p><strong>59. La responsabilidad limitada en una Sociedad Limitada significa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los socios responden con todo su patrimonio personal ante deudas</button>
    <button class="opcion" onclick="verificar(this, true)">b) La responsabilidad de los socios se limita al capital aportado</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo el administrador responde ante las deudas</button>
    <button class="opcion" onclick="verificar(this, false)">d) La empresa no puede contraer deudas superiores al capital social</button>
  </div>

  <div class="pregunta">
    <p><strong>60. ¿Qué impuesto grava los beneficios de las sociedades mercantiles?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) IRPF</button>
    <button class="opcion" onclick="verificar(this, false)">b) IVA</button>
    <button class="opcion" onclick="verificar(this, true)">c) Impuesto de Sociedades (IS)</button>
    <button class="opcion" onclick="verificar(this, false)">d) IAE</button>
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

  // Borrar números fijos
  preguntasArray.forEach(pregunta => {
    let textoPregunta = pregunta.querySelector('p strong');
    if (textoPregunta) {
      textoPregunta.innerHTML = textoPregunta.innerHTML.replace(/^\d+\.\s*/, '');
    }
  });

  // Crear contador visual
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

  // Reordenar DOM
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
