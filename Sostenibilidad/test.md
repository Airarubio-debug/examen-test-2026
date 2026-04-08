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

  <div class="pregunta">
    <p><strong>33. No es una dimensión como tal de los ODS:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La económica.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La ecológica.</button>
    <button class="opcion" onclick="verificar(this, true)">c) La cultural.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La social.</button>
  </div>

  <div class="pregunta">
    <p><strong>34. Los ODS:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Son objetivos de obligado cumplimiento por las empresas de todos los países, y la ONU invita a las administraciones públicas a sumarse a ellos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Son objetivos de obligado cumplimiento por todas las personas, y la ONU invita a todas las administraciones públicas a sumarse a ellos.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Son objetivos de obligado cumplimiento por las administraciones públicas, y la ONU invita a todas las personas y empresas a sumarse a ellos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Son objetivos de obligado cumplimiento por las administraciones públicas, las empresas y las personas de todos los países.</button>
  </div>

  <div class="pregunta">
    <p><strong>35. ¿Cuál es la función de los indicadores de desempeño?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Guiar y coordinar las acciones de la humanidad para lograr el desarrollo sostenible.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Especificar situaciones de llegada concretas en relación con cada ODS.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Medir el grado de consecución de las metas del desarrollo sostenible.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Informar de la rentabilidad de una empresa.</button>
  </div>

  <div class="pregunta">
    <p><strong>36. No es un ámbito del consumo responsable:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El agua.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Los bienes de consumo duradero.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El transporte.</button>
    <button class="opcion" onclick="verificar(this, true)">d) La producción.</button>
  </div>

  <div class="pregunta">
    <p><strong>37. Desplazarse a pie ayuda especialmente a cumplir el ODS:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 8. Trabajo decente y crecimiento económico.</button>
    <button class="opcion" onclick="verificar(this, true)">b) 11. Ciudades y comunidades sostenibles.</button>
    <button class="opcion" onclick="verificar(this, false)">c) 12. Producción y consumo responsables.</button>
    <button class="opcion" onclick="verificar(this, false)">d) 15. Vida de ecosistemas terrestres.</button>
  </div>

  <div class="pregunta">
    <p><strong>38. Un empleado de una empresa sin responsabilidades directivas puede ayudar al logro de los ODS:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Procurando aplicar en el puesto de trabajo principios similares a los del consumo responsable.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Esperando a que la dirección realice cambios que nos acerquen a los ODS.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Basta con hacer lo mismo que nuestros compañeros.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sin responsabilidades de dirección no se puede trabajar por los ODS.</button>
  </div>

  <div class="pregunta">
    <p><strong>39. Lo más recomendable para una empresa que quiere integrar los ODS en las estrategias y los planes de la empresa es implicarse en el logro de:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Un ODS concreto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una meta concreta.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un indicador de desempeño concreto.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Todos los ODS al mismo tiempo.</button>
  </div>

  <div class="pregunta">
    <p><strong>40. ¿Qué iniciativa de la UE busca lograr la neutralidad de emisiones de carbono? Señala la respuesta más completa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El Pacto Verde Europeo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La Estrategia de Movilidad Sostenible.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La Nueva Estrategia Industrial para Europa.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas las anteriores.</button>
  </div>

  <div class="pregunta">
    <p><strong>41. No es una iniciativa surgida en la UE:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La Estrategia de Movilidad Sostenible.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El acuerdo de París.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El Pacto Verde Europeo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La Nueva Estrategia Industrial para Europa.</button>
  </div>

  <div class="pregunta">
    <p><strong>42. Las iniciativas que la UE ha puesto en marcha para el logro de los ODS suponen ventajas para las empresas, como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Normas medioambientales cada vez más estrictas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Mayor posibilidad de recibir sanciones.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Ayudas para mejorar la resiliencia.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Reducción de impuestos.</button>
  </div>

  <div class="pregunta">
    <p><strong>43. La mayor parte del empleo lo generan:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Las empresas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Las administraciones.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las entidades del tercer sector.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La banca.</button>
  </div>

  <div class="pregunta">
    <p><strong>44. Sobre los grupos de interés, señala la afirmación falsa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Son colectivos humanos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Son capaces de influir en las decisiones de la empresa.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las decisiones de la empresa los influyen a ellos.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Siempre son externos a la empresa.</button>
  </div>

  <div class="pregunta">
    <p><strong>45. Es un grupo de interés interno:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los proveedores.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La competencia.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los clientes.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Los propietarios.</button>
  </div>

  <div class="pregunta">
    <p><strong>46. El grupo de interés que persigue obtener de la empresa el mejor producto posible al menor precio posible son:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los propietarios.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Los directivos.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Los clientes.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los proveedores.</button>
  </div>

  <div class="pregunta">
    <p><strong>47. Los aspectos ASG relacionados con el trato a las personas internas y externas a la empresa son:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aspectos ambientales.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Aspectos sociales.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aspectos de gobernanza.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aspectos financieros.</button>
  </div>

  <div class="pregunta">
    <p><strong>48. Los aspectos ASG relacionados con la ética empresarial son:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aspectos ambientales.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Aspectos sociales.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Aspectos de gobernanza.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aspectos filosóficos.</button>
  </div>

  <div class="pregunta">
    <p><strong>49. No es un aspecto ASG ambiental:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La adaptación al cambio climático.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La biodiversidad y los ecosistemas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El uso de recursos y la economía circular.</button>
    <button class="opcion" onclick="verificar(this, true)">d) La relación con las comunidades.</button>
  </div>

  <div class="pregunta">
    <p><strong>50. Un estado no financiero organiza sus indicadores según:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los ODS.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Los grupos de interés.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las líneas de negocio.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Los aspectos ASG.</button>
  </div>

  <div class="pregunta">
    <p><strong>51. Las normas NEIS han sido creadas por:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La Unión Europea.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Las Naciones Unidas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El Gobierno de España.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La Consejería de Medio Ambiente.</button>
  </div>

  <div class="pregunta">
    <p><strong>52. La integración de aspectos ASG en la empresa supone para ella:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un peor acceso a financiación.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una mejor imagen de marca.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una peor retención del talento.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un menor beneficio a la larga.</button>
  </div>

  <div class="pregunta">
    <p><strong>53. La fase del ciclo de vida del producto en la que el producto es puesto al servicio del consumidor se conoce como:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Producción.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Distribución.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Consumo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Desecho.</button>
  </div>

  <div class="pregunta">
    <p><strong>54. En el modelo lineal de producción y consumo, cada fase del ciclo de vida del producto se relaciona directamente:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solo con la inmediata anterior.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Con todas las demás al mismo tiempo.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Con la inmediatamente anterior y la inmediatamente posterior.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Con todas las que tiene detrás.</button>
  </div>

  <div class="pregunta">
    <p><strong>55. Si utilizamos recursos no renovables para producir nuestro bien o servicio, nos exponemos al riesgo de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Contaminación.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Escasez de recursos y precios cada vez mayores.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Problemas de seguridad en el trabajo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Menores oportunidades de expansión a otros mercados.</button>
  </div>

  <div class="pregunta">
    <p><strong>56. Cuando aplicamos la regla de las 7 «R», el valor de los recursos y productos a lo largo de su ciclo de vida:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se reduce rápidamente.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Se mantiene por más tiempo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aumenta rápidamente.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No se ve afectado.</button>
  </div>

  <div class="pregunta">
    <p><strong>57. Dos procesos asociados a la economía circular son:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La deforestación y la desertización.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La deslocalización y la externalización.</button>
    <button class="opcion" onclick="verificar(this, true)">c) La desmaterialización y la descarbonización.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La descentralización y la concentración.</button>
  </div>

  <div class="pregunta">
    <p><strong>58. La fase de la evaluación de producción limpia en la que se diseña y ejecuta un plan de acción es la de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Recogida y análisis de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Generación de opciones.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Implementación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Evaluación y control.</button>
  </div>

  <div class="pregunta">
    <p><strong>59. No es una opción de implantación de la producción limpia:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los cambios en los materiales.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los cambios en la demanda.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los cambios en el producto.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La reutilización in situ.</button>
  </div>

  <div class="pregunta">
    <p><strong>60. El ecodiseño busca:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La integración de aspectos medioambientales en el diseño.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La implantación de procesos de producción más respetuosos con el medio ambiente.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La integración de aspectos medioambientales en las decisiones de los consumidores.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La integración de los aspectos económicos en el diseño.</button>
  </div>

  <div class="pregunta">
    <p><strong>61. Una forma de usar materiales de impacto reducido es:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Usar materiales de proveedores locales.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Añadir multifuncionalidad al producto.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Reducir el número de procesos en la producción.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Reducir las necesidades de mantenimiento.</button>
  </div>

  <div class="pregunta">
    <p><strong>62. Todo proceso de ecodiseño debe comenzar por:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Identificar la fases del ciclo de vida del producto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Identificar estrategias de mejora medioambiental del producto.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Desarrollar soluciones técnicas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Fijar objetivos o metas medioambientales.</button>
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
