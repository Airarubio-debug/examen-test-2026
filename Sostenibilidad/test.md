<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <title>Examen Test 2026</title>
</head>
<body>

<style>
  body { font-family: sans-serif; }
  .pregunta { display: none; margin-bottom: 20px; }
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
    <p><strong>14. Dentro de las "A" de los ASG se incluye:</strong></p>
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
    <p><strong>24. "Renovar" en las 7R significa:</strong></p>
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
    <p><strong>29. Uno de los principios del ecodiseño es la "producción limpia", que implica:</strong></p>
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

  <!-- PREGUNTA 42 CORREGIDA: opciones a) y d) eran confusas; la respuesta correcta es c) -->
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
    <button class="opcion" onclick="verificar(this, true)">a) Identificar las fases del ciclo de vida del producto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Identificar estrategias de mejora medioambiental del producto.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Desarrollar soluciones técnicas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Fijar objetivos o metas medioambientales.</button>
  </div>

  <div class="pregunta">
    <p><strong>63. Un dato o un conjunto de datos que permite medir el rendimiento de una actividad en relación con un objetivo o una meta es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un objetivo.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un indicador de desempeño.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una meta.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un sistema de gestión ambiental.</button>
  </div>

  <div class="pregunta">
    <p><strong>64. En la fijación de objetivos para la empresa, es importante tomar como punto de partida:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) El análisis de cada proceso.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Seleccionar objetivos relevantes.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Comprobar los medios disponibles para cumplirlos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Fijar un horizonte temporal.</button>
  </div>

  <div class="pregunta">
    <p><strong>65. El objetivo de la evaluación del desempeño medioambiental es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Implantar indicadores clave de desempeño en la empresa.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Establecer fórmulas que indiquen cómo calcular los indicadores.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Encontrar culpables de que los planes no se cumplan.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Lograr la mejora continua en los procesos y en la empresa.</button>
  </div>

  <div class="pregunta">
    <p><strong>66. ¿Qué tipo de certificados de sostenibilidad medioambiental reconocidos en normas ISO no requieren de entidades externas a la empresa que los utiliza?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los de tipo I (ecoetiquetas).</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los de tipo II (autodeclaraciones ambientales).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los de tipo III (declaraciones ambientales de producto).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los no cubiertos por normas ISO.</button>
  </div>

  <div class="pregunta">
    <p><strong>67. ¿Qué certificado está formado por la bandera europea y una hoja con diversas formas que representa la naturaleza y la sostenibilidad?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La Etiqueta Ecológica Europea (EEE).</button>
    <button class="opcion" onclick="verificar(this, true)">b) El logotipo de producción ecológica de la UE.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El certificado FSC de gestión forestal.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El certificado de pesca sostenible.</button>
  </div>

  <div class="pregunta">
    <p><strong>68. Sobre la Etiqueta Ecológica Europea (EEE), señala la afirmación falsa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es una etiqueta de tipo I.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Requiere que la empresa redacte un informe sobre sus actividades.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Es gestionado directamente por la UE.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es necesario pagar una tasa para gestionar su solicitud.</button>
  </div>

  <div class="pregunta">
    <p><strong>69. ¿Cuál de las afirmaciones siguientes no se refiere a la inversión financiera?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tiene relación con la inversión productiva.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Consiste en producir un bien o servicio para venderlo en el mercado.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se refleja en unos documentos llamados títulos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) En su análisis se tiene en cuenta la rentabilidad, el riesgo y la liquidez.</button>
  </div>

  <div class="pregunta">
    <p><strong>70. Selecciona la respuesta más completa. El análisis de inversiones socialmente responsables (ISR) valora:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La rentabilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El riesgo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los aspectos ASG.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todo lo anterior.</button>
  </div>

  <div class="pregunta">
    <p><strong>71. Los indicadores de inversión socialmente responsable (ISR) con integración de aspectos ASG:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Son listados que excluyen a empresas que se dedican a actividades abiertamente incompatibles con los ODS y la sostenibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Incluyen solo a empresas que se dedican a actividades especialmente vinculadas con la sostenibilidad.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Incluyen títulos de empresas que cumplen con los criterios ASG de acuerdo con los estándares fijados por las agencias que han creado y gestionan esos índices.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Consideran los aspectos ASG, solamente.</button>
  </div>

  <div class="pregunta">
    <p><strong>72. Las organizaciones normalizadoras:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Crean las leyes que rigen la actividad de las empresas y las personas, y toman decisiones de gobierno y gestión diaria.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Crean normas especializadas que regulan actividades y procesos concretos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Son empresas acreditadas para extender certificados de sostenibilidad, entre otros.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Califican inversiones y empresas en función del grado de cumplimiento de los aspectos ASG.</button>
  </div>

  <div class="pregunta">
    <p><strong>73. Indica cuál de los siguientes estándares de información no financiera es más antiguo:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Global Reporting Initiative (GRI).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Directiva 2022/2464 de Informes de Sostenibilidad Empresarial (CSRD).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Normas Europeas de Información sobre Sostenibilidad (NEIS).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ley de Información no Financiera y Diversidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>74. En relación con el estándar GRI, señala la afirmación falsa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Su primera versión es del año 2000.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Fue creado por la Unión Europea.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La mayoría de las grandes empresas lo utiliza.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es en realidad una familia de estándares.</button>
  </div>

  <div class="pregunta">
    <p><strong>75. El plan de sostenibilidad:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es un documento obligatorio para las empresas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es un documento de planificación a corto plazo (un año o menos).</button>
    <button class="opcion" onclick="verificar(this, true)">c) Sirve para guiar las acciones de la organización en materia de sostenibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Da cuenta de las actuaciones realizadas el año anterior en materia de sostenibilidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>76. El plan de sostenibilidad es (señala la respuesta más completa):</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Una herramienta de planificación.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una herramienta de comunicación.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Una herramienta de planificación y comunicación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Una herramienta de planificación y evaluación.</button>
  </div>

  <div class="pregunta">
    <p><strong>77. El primer apartado de un plan de sostenibilidad debe ser:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La identificación de impactos y dependencias.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La identificación de los ODS clave.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El diseño de objetivos y acciones concretas.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El análisis del contexto de la organización.</button>
  </div>

  <div class="pregunta">
    <p><strong>78. Para una empresa agrícola, la mayor frecuencia de sequías es un asunto:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Con materialidad de impacto.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Con materialidad financiera.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Con doble materialidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sin materialidad para la empresa.</button>
  </div>

  <div class="pregunta">
    <p><strong>79. Para que un asunto tenga prioridad de primer nivel en la matriz de materialidad y relevancia, debe tener:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Doble materialidad.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Elevada relevancia para los grupos de interés internos y externos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Elevada relevancia y elevada factibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Elevada relevancia para la dirección de la organización, solamente.</button>
  </div>

  <div class="pregunta">
    <p><strong>80. A diferencia del estado de sostenibilidad, el informe o memoria de sostenibilidad:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Informa sobre el desempeño de la organización en materia de sostenibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se refiere a un periodo de tiempo definido (un año).</button>
    <button class="opcion" onclick="verificar(this, true)">c) Tiene gran utilidad como herramienta de comunicación de las políticas de sostenibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Habla solamente de los logros de la organización en materia de sostenibilidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>81. En el procedimiento administrativo de evaluación de impacto ambiental no interviene:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La entidad que promueve una obra, proyecto o acción de cierta importancia.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La autoridad medioambiental.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El documento llamado estudio de impacto ambiental.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El documento llamado informe medioambiental.</button>
  </div>

  <div class="pregunta">
    <p><strong>82. La declaración de impacto ambiental es redactada por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La empresa promotora del proyecto.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La autoridad medioambiental.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La empresa que construye efectivamente el proyecto.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La oficina de prensa de la empresa.</button>
  </div>

  <div class="pregunta">
    <p><strong>83. ¿Cuál de las siguientes acciones contribuye directamente a la descarbonización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reducir la eficiencia energética para disminuir costes</button>
    <button class="opcion" onclick="verificar(this, true)">b) Reemplazar sistemas de energía fósil por fuentes renovables como solar o eólica</button>
    <button class="opcion" onclick="verificar(this, false)">c) Incrementar el uso de carbón en procesos industriales</button>
    <button class="opcion" onclick="verificar(this, false)">d) Utilizar únicamente materias primas vírgenes</button>
  </div>

  <div class="pregunta">
    <p><strong>84. ¿Qué describe mejor el concepto de ecosistema?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un conjunto de especies que compiten entre sí por recursos limitados</button>
    <button class="opcion" onclick="verificar(this, false)">b) Un lugar donde solo existen plantas y microorganismos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un espacio geográfico sin influencia de factores abióticos</button>
    <button class="opcion" onclick="verificar(this, true)">d) La interacción entre organismos vivos y los factores físicos del entorno en un área determinada</button>
  </div>

  <div class="pregunta">
    <p><strong>85. ¿Qué impacto puede tener el cambio climático en los costes de las empresas?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Incrementa porque suben los impuestos</button>
    <button class="opcion" onclick="verificar(this, false)">b) Reducción de costes energéticos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Ninguna es correcta</button>
    <button class="opcion" onclick="verificar(this, true)">d) Incremento por adaptación y seguros</button>
  </div>

  <div class="pregunta">
    <p><strong>86. ¿Cómo puede afectar la desmaterialización a la sostenibilidad de una empresa?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aumentando obligatoriamente la huella de carbono</button>
    <button class="opcion" onclick="verificar(this, false)">b) Incrementando el uso de recursos físicos y logísticos</button>
    <button class="opcion" onclick="verificar(this, true)">c) Reduciendo el consumo de materiales y la generación de residuos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Dependiendo exclusivamente de proveedores externos de papel</button>
  </div>

  <div class="pregunta">
    <p><strong>87. ¿Qué práctica se asocia directamente con la desmaterialización dentro de una empresa o administración pública?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Almacenar todas las facturas en archivadores tradicionales</button>
    <button class="opcion" onclick="verificar(this, false)">b) Requerir que todos los informes se entreguen impresos y firmados en papel</button>
    <button class="opcion" onclick="verificar(this, true)">c) Migrar servicios y comunicaciones a plataformas digitales para minimizar recursos físicos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aumentar el número de envíos postales para mejorar la comunicación interna</button>
  </div>

  <div class="pregunta">
    <p><strong>88. ¿Qué objetivo persigue la descarbonización en el contexto corporativo y público?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Mantener las emisiones en niveles actuales para evitar costes adicionales</button>
    <button class="opcion" onclick="verificar(this, false)">b) Establecer un sistema de compensaciones que permita seguir emitiendo sin cambios operativos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Lograr un aumento gradual del uso de carbón y gas para asegurar el suministro</button>
    <button class="opcion" onclick="verificar(this, true)">d) Reducir o eliminar las emisiones de gases de efecto invernadero mediante cambios estructurales, tecnológicos y de consumo energético</button>
  </div>

  <div class="pregunta">
    <p><strong>89. ¿Cuál es el principal instrumento adoptado por la ONU para impulsar el desarrollo sostenible a escala global?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El Protocolo de Montreal</button>
    <button class="opcion" onclick="verificar(this, false)">b) El Acuerdo de Basilea</button>
    <button class="opcion" onclick="verificar(this, false)">c) La Declaración de Estocolmo</button>
    <button class="opcion" onclick="verificar(this, true)">d) La Agenda 2030 y sus Objetivos de Desarrollo Sostenible (ODS)</button>
  </div>

  <div class="pregunta">
    <p><strong>90. ¿Qué papel desempeña la ONU en materia de sostenibilidad?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Coordinar esfuerzos internacionales, establecer marcos globales y promover metas comunes para el desarrollo sostenible</button>
    <button class="opcion" onclick="verificar(this, false)">b) Sustituir a los gobiernos nacionales en la toma de decisiones ambientales</button>
    <button class="opcion" onclick="verificar(this, false)">c) Elaborar leyes obligatorias para todos los países sin excepción</button>
    <button class="opcion" onclick="verificar(this, false)">d) Controlar directamente los recursos naturales de los países miembros</button>
  </div>

  <div class="pregunta">
    <p><strong>91. ¿Cuál de las siguientes áreas forma parte de las iniciativas clave del Pacto Verde Europeo?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reducir la inversión en innovación tecnológica ambiental</button>
    <button class="opcion" onclick="verificar(this, true)">b) Transformar sectores como energía, transporte, agricultura e industria hacia modelos más sostenibles</button>
    <button class="opcion" onclick="verificar(this, false)">c) Incentivar el uso de carbón para reducir costes energéticos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Eliminar gradualmente las energías renovables del mercado europeo</button>
  </div>

  <div class="pregunta">
    <p><strong>92. No es una dimensión como tal de los ODS:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La ecológica</button>
    <button class="opcion" onclick="verificar(this, false)">b) La social</button>
    <button class="opcion" onclick="verificar(this, false)">c) La económica</button>
    <button class="opcion" onclick="verificar(this, true)">d) La cultural</button>
  </div>

  <div class="pregunta">
    <p><strong>93. ¿Cuál es el propósito general de los 17 ODS establecidos por la ONU?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Promover únicamente el crecimiento económico mundial</button>
    <button class="opcion" onclick="verificar(this, false)">b) Reemplazar las leyes nacionales de desarrollo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Establecer metas solo para países en desarrollo</button>
    <button class="opcion" onclick="verificar(this, true)">d) Crear un marco global para abordar desafíos sociales, ambientales y económicos antes de 2030</button>
  </div>

  <div class="pregunta">
    <p><strong>94. ¿Qué enfoque adoptan los ODS para enfrentar los desafíos globales?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se centran exclusivamente en la cooperación internacional</button>
    <button class="opcion" onclick="verificar(this, true)">b) Plantean un enfoque integrado que combina lo social, lo ambiental y lo económico</button>
    <button class="opcion" onclick="verificar(this, false)">c) Abordan un único ámbito (económico) para simplificar su implementación</button>
    <button class="opcion" onclick="verificar(this, false)">d) Proponen acciones compartimentadas sin conexión entre sí</button>
  </div>

  <div class="pregunta">
    <p><strong>95. ¿Cuántos ODS hay?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 30</button>
    <button class="opcion" onclick="verificar(this, true)">b) 17</button>
    <button class="opcion" onclick="verificar(this, false)">c) 50</button>
    <button class="opcion" onclick="verificar(this, false)">d) Depende del país</button>
  </div>

  <div class="pregunta">
    <p><strong>96. ¿Por qué son esenciales los indicadores de desempeño para implementar los ODS?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Porque ayudan a comparar avances, identificar brechas y orientar decisiones de políticas públicas y estrategias privadas</button>
    <button class="opcion" onclick="verificar(this, false)">b) Porque hacen que los ODS sean obligatorios para todos los países al convertir sus metas en exigencias de carácter normativo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Porque eliminan la necesidad de establecer metas concretas</button>
    <button class="opcion" onclick="verificar(this, false)">d) Porque permiten aplicar los ODS sin necesidad de recopilar datos ni realizar análisis continuos</button>
  </div>

  <div class="pregunta">
    <p><strong>97. La integración de aspectos ASG en la empresa suele implicar para ella:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Una mejora de la reputación corporativa y de la percepción de la marca</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una mayor dificultad para atraer y retener talento</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un acceso más limitado a financiación sostenible y a inversores responsables</button>
    <button class="opcion" onclick="verificar(this, false)">d) Una reducción del rendimiento y competitividad a largo plazo</button>
  </div>

  <div class="pregunta">
    <p><strong>98. La huella ecológica debe ser:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un factor irrelevante que no tiene impacto en el desarrollo sostenible</button>
    <button class="opcion" onclick="verificar(this, false)">b) Superior a la biocapacidad disponible, incluso si eso implica sobreexplotación de recursos</button>
    <button class="opcion" onclick="verificar(this, true)">c) Inferior a la biocapacidad, garantizando que los ecosistemas puedan regenerar los recursos utilizados</button>
    <button class="opcion" onclick="verificar(this, false)">d) Exactamente igual a la biocapacidad del planeta o territorio, sin margen de variación</button>
  </div>

  <div class="pregunta">
    <p><strong>99. Una marca de moda implementa un sistema blockchain para rastrear materiales, fábricas y condiciones laborales en toda su cadena de valor. ¿Qué aspecto ASG se ve más afectado?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Financiero</button>
    <button class="opcion" onclick="verificar(this, false)">b) Ambiental</button>
    <button class="opcion" onclick="verificar(this, true)">c) Gobernanza</button>
    <button class="opcion" onclick="verificar(this, false)">d) Social</button>
  </div>

  <div class="pregunta">
    <p><strong>100. Una empresa de transporte anuncia que sustituirá su flota diésel por vehículos eléctricos y utilizará energía 100% renovable en sus centros. ¿Qué aspecto ASG mejora principalmente?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Financiero</button>
    <button class="opcion" onclick="verificar(this, false)">b) Gobernanza</button>
    <button class="opcion" onclick="verificar(this, true)">c) Ambiental</button>
    <button class="opcion" onclick="verificar(this, false)">d) Social</button>
  </div>

  <div class="pregunta">
    <p><strong>101. Una empresa de transporte anuncia que implementará un programa integral para mejorar la seguridad y el bienestar de sus conductores, incluyendo formación especializada, reducción de horas de trabajo excesivas y apoyo psicológico. ¿Qué aspecto ASG mejora principalmente?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Gobernanza</button>
    <button class="opcion" onclick="verificar(this, false)">b) Ambiental</button>
    <button class="opcion" onclick="verificar(this, true)">c) Social</button>
    <button class="opcion" onclick="verificar(this, false)">d) Financiero</button>
  </div>

  <div class="pregunta">
    <p><strong>102. Los criterios ASG sirven para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Exigir automáticamente una auditoría interna anual, independientemente del desempeño real de la empresa</button>
    <button class="opcion" onclick="verificar(this, false)">b) Reemplazar por completo las funciones de la dirección y la alta gerencia</button>
    <button class="opcion" onclick="verificar(this, false)">c) Incrementar los beneficios de la empresa como único objetivo, sin considerar otros impactos</button>
    <button class="opcion" onclick="verificar(this, true)">d) Evaluar de manera integral las prácticas empresariales y orientar decisiones sostenibles en materia ambiental, social y de gobernanza</button>
  </div>

  <div class="pregunta">
    <p><strong>103. ¿Qué riesgo puede asumir una empresa que ignora los criterios ASG en su gestión?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Enfrentar sanciones, pérdida de confianza y menor acceso a financiación sostenible</button>
    <button class="opcion" onclick="verificar(this, false)">b) Mejorar automáticamente su competitividad internacional</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aumentar su capacidad de anticipar riesgos regulatorios</button>
    <button class="opcion" onclick="verificar(this, false)">d) Incrementar su resiliencia frente a cambios sociales y ambientales</button>
  </div>

  <div class="pregunta">
    <p><strong>104. Señala la afirmación falsa acerca de los grupos de interés:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Las decisiones que toma la empresa pueden afectarles directa o indirectamente</button>
    <button class="opcion" onclick="verificar(this, false)">b) Son colectivos humanos con algún grado de relación o impacto con la organización</button>
    <button class="opcion" onclick="verificar(this, true)">c) Siempre son externos a la empresa, sin formar parte de ella en ningún caso</button>
    <button class="opcion" onclick="verificar(this, false)">d) Son capaces de influir en las decisiones y estrategias de la empresa</button>
  </div>

  <div class="pregunta">
    <p><strong>105. ¿Cuál es una ventaja clave de la economía circular respecto al modelo lineal tradicional?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Genera más residuos para mantener la actividad económica</button>
    <button class="opcion" onclick="verificar(this, false)">b) Obliga a producir a mayor velocidad sin controles ambientales</button>
    <button class="opcion" onclick="verificar(this, false)">c) Incrementa la dependencia de combustibles fósiles</button>
    <button class="opcion" onclick="verificar(this, true)">d) Reduce la necesidad de materias primas vírgenes al fomentar la reutilización y el reciclaje</button>
  </div>

  <div class="pregunta">
    <p><strong>106. ¿Cuál es un beneficio ambiental directo de adoptar una economía circular?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un incremento de la contaminación del agua y del suelo como consecuencia de procesos productivos lineales.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La disminución de la generación de residuos al mantener los materiales en uso durante más tiempo, aprovechando estrategias como la reutilización, reparación, refabricación y reciclaje eficiente.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una mayor producción de residuos y vertidos debido a procesos que continúan desechando materiales después de un solo uso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La extracción continua e intensiva de recursos naturales sin límites, lo que incrementa la degradación ambiental.</button>
  </div>

  <div class="pregunta">
    <p><strong>107. La economía circular busca:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Limitar la colaboración con proveedores</button>
    <button class="opcion" onclick="verificar(this, true)">b) Mantener el valor de los recursos el mayor tiempo posible</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aumentar el uso de productos desechables</button>
    <button class="opcion" onclick="verificar(this, false)">d) Acortar el ciclo de vida del producto</button>
  </div>

  <div class="pregunta">
    <p><strong>108. Un principio del ecodiseño es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Fomentar una producción con mayor cantidad de emisiones</button>
    <button class="opcion" onclick="verificar(this, true)">b) Facilitar la reparabilidad</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aumentar el consumo energético</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aumentar la cantidad de residuos para así poder reciclarlos</button>
  </div>

  <div class="pregunta">
    <p><strong>109. Un producto puede considerarse mal diseñado desde la perspectiva del ecodiseño cuando:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tiene un envase compostable</button>
    <button class="opcion" onclick="verificar(this, false)">b) Reduce el consumo energético</button>
    <button class="opcion" onclick="verificar(this, true)">c) Emplea materiales difíciles de separar o no reciclables</button>
    <button class="opcion" onclick="verificar(this, false)">d) Presenta elevada durabilidad y reparabilidad</button>
  </div>

  <!-- PREGUNTA 110 COMPLETADA (estaba cortada en el original) -->
  <div class="pregunta">
    <p><strong>110. ¿Cuál es el objetivo principal de la evaluación del desempeño ambiental?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Analizar de forma sistemática el impacto ambiental de la organización para identificar áreas de mejora continua.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Obtener la certificación ISO 14001 de forma obligatoria.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Reducir exclusivamente las emisiones de CO₂.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cumplir con la normativa fiscal medioambiental.</button>
  </div>

</div><!-- FIN #contenedor-test -->

<button id="btn-siguiente" onclick="siguientePregunta()">Siguiente pregunta ➡️</button>

<div id="resultados">
  <h2>¡Test completado! 🎉</h2>
  <p style="font-size: 18px;">Has acertado <strong id="aciertos">0</strong> de <strong id="total">0</strong> preguntas.</p>

  <div id="repaso-errores" style="display: none; margin-top: 30px; text-align: left;">
    <h3 style="color: #cf222e; border-bottom: 2px solid #cf222e; padding-bottom: 5px;">Repaso de preguntas falladas:</h3>
    <div id="lista-errores"></div>
  </div>

  <button id="btn-repetir" onclick="location.reload()">↻ Repetir test</button>
</div>

<script>
  let indexActual = 0;
  let aciertos = 0;
  let arrayErrores = [];

  const contenedorTest = document.getElementById('contenedor-test');
  const btnSiguiente = document.getElementById('btn-siguiente');
  const divResultados = document.getElementById('resultados');

  let preguntasArray = Array.from(document.querySelectorAll('.pregunta'));

  // Eliminar numeración del enunciado
  preguntasArray.forEach(pregunta => {
    let textoPregunta = pregunta.querySelector('p strong');
    if (textoPregunta) {
      textoPregunta.innerHTML = textoPregunta.innerHTML.replace(/^\d+\.\s*/, '');
    }
  });

  // Crear contador de progreso
  const progresoDiv = document.createElement('div');
  progresoDiv.style.cssText = 'text-align: center; font-weight: bold; font-size: 16px; color: #57606a; margin-bottom: 20px; background: #f6f8fa; padding: 10px; border-radius: 8px; border: 1px solid #d0d7de;';
  contenedorTest.parentNode.insertBefore(progresoDiv, contenedorTest);

  // Barajar preguntas
  function mezclarPreguntas(array) {
    for (let i = array.length - 1; i > 0; i--) {
      const j = Math.floor(Math.random() * (i + 1));
      [array[i], array[j]] = [array[j], array[i]];
    }
  }
  mezclarPreguntas(preguntasArray);

  // Reordenar en el DOM y activar la primera
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
    let botonCorrecto = Array.from(botones).find(b => b.getAttribute('onclick').includes('true'));

    botones.forEach(b => { b.disabled = true; b.style.cursor = 'default'; });

    if (esCorrecto) {
      boton.classList.add('correcta');
      boton.innerHTML += ' ✅';
      aciertos++;
    } else {
      boton.classList.add('incorrecta');
      boton.innerHTML += ' ❌';
      botonCorrecto.classList.add('correcta');

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
      progresoDiv.style.display = 'none';
      contenedorTest.style.display = 'none';
      divResultados.style.display = 'block';
      document.getElementById('aciertos').innerText = aciertos;
      document.getElementById('total').innerText = preguntas.length;

      if (arrayErrores.length > 0) {
        document.getElementById('repaso-errores').style.display = 'block';
        let listaHTML = '';
        arrayErrores.forEach((error, index) => {
          listaHTML += `
            <div style="background: #fff3f3; border-left: 5px solid #ff8182; padding: 12px; margin-bottom: 12px; border-radius: 4px;">
              <p style="margin: 0 0 8px 0; color: #24292f;"><strong>${index + 1}. ${error.pregunta}</strong></p>
              <p style="margin: 0; color: #1a7f37; font-weight: bold;">✔️ Respuesta: ${error.respuesta}</p>
            </div>`;
        });
        document.getElementById('lista-errores').innerHTML = listaHTML;
      }
    }
  }
</script>

</body>
</html>
