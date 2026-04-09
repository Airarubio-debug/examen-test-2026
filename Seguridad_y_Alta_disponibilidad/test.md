
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

  <div class="pregunta">
    <p><strong>25. La estenografía permite:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Firmar una imagen.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Cifrar una imagen.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cifrar la imagen por píxel.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Transmitir información por canal subliminal (ocultando información dentro de otro archivo).</button>
  </div>

  <div class="pregunta">
    <p><strong>26. De las siguientes afirmaciones indicar cuál de ellas define la propiedad ‘difusión’ en el cifrado de bloque:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Un pequeño cambio en el texto en claro debería producir un cambio del 50% del texto cifrado resultante.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Un pequeño cambio en la clave debería producir un cambio del 50% del texto cifrado resultante.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Utiliza la técnica ‘divide y vencerás’.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cada bit del texto cifrado dependerá de cada bit de la clave.</button>
  </div>

  <div class="pregunta">
    <p><strong>27. La firma digital y el certificado digital se caracterizan porque:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La firma verifica la identidad del firmante.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El certificado digital tiene funciones similares a las de la firma autógrafa.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Son iguales.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El certificado digital contiene alguna firma digital (la de la CA que lo emite, pero la 'a' es su función principal de autenticación).</button>
  </div>

  <div class="pregunta">
    <p><strong>28. El certificado digital:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Contiene la clave privada del usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es lo mismo que la firma electrónica del usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Necesita del uso de la clave privada del usuario.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Es, sin más, un medio de identificación del usuario en la red.</button>
  </div>

  <div class="pregunta">
    <p><strong>29. De las siguientes afirmaciones selecciona la válida:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El criptoanálisis compromete la seguridad de un criptosistema.</button>
    <button class="opcion" onclick="verificar(this, false)">b) IDEA es un algoritmo de criptografía asimétrica muy conocido.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El cifrado en bloque se hace forma independiente.</button>
    <button class="opcion" onclick="verificar(this, true)">d) En general, en un criptosistema cuanto más grande es la clave más segura será.</button>
  </div>

  <div class="pregunta">
    <p><strong>30. En términos de identidad digital, indica la opción falsa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Existe normativa en España.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Incluye certificado digital y firma electrónica.</button>
    <button class="opcion" onclick="verificar(this, true)">c) No presenta problemas de seguridad física y lógica (Falso, sí que los presenta, como el robo de tokens o contraseñas).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Garantiza la confidencialidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>31. Selecciona la opción válida:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El cifrado en bloque se hace forma independiente.</button>
    <button class="opcion" onclick="verificar(this, false)">b) En cada mensaje la clave simétrica utilizada es diferente.</button>
    <button class="opcion" onclick="verificar(this, false)">c) IDEA es un algoritmo de criptografía asimétrica muy conocido.</button>
    <button class="opcion" onclick="verificar(this, true)">d) En general, en un criptosistema cuanto más grande es la clave más segura será.</button>
  </div>

  <div class="pregunta">
    <p><strong>32. En criptografía, la confusión consiste en:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Ocultar la relación entre el texto cifrado y la clave secreta.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Eliminar cualquier relación estadística entre el mensaje original y su texto cifrado.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Enviar al atacante falsos textos para confundirlo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Mezclar las letras entre sí para confundirlas.</button>
  </div>

  <div class="pregunta">
    <p><strong>33. La firma manuscrita de la persona se considera que pertenece a la llamada:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Biometría fisiológica.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Biometría posicional.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Biometría conductual.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Biometría analítica.</button>
  </div>

  <div class="pregunta">
    <p><strong>34. La función hash:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cifran todo el mensaje.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Su longitud depende del tamaño del mensaje.</button>
    <button class="opcion" onclick="verificar(this, false)">c) No se utiliza en la firma digital.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Genera un resumen o huella digital.</button>
  </div>

  <div class="pregunta">
    <p><strong>35. En una ACL los permisos por defecto sobre un directorio:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No se pueden establecer.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se establecen con la opción -r.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Afectan a los archivos de un directorio.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Afectan a los archivos que se creen en el directorio.</button>
  </div>

  <div class="pregunta">
    <p><strong>36. Las ACL se pueden utilizar:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Sobre cualquier sistema de archivos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Siempre, si el usuario sabe configurarlas.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Requieren soporte en el núcleo del sistema operativo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sobre cualquier sistema de archivos montado.</button>
  </div>

  <div class="pregunta">
    <p><strong>37. En relación con los objetivos de la seguridad lógica, indicar cuál de las siguientes afirmaciones es falsa.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Restringen el acceso a los programas y archivos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La información recibida es la misma que ha sido transmitida.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Existen sistemas alternativos secundarios de almacenamiento (Esto es seguridad física/disponibilidad).</button>
    <button class="opcion" onclick="verificar(this, false)">d) La información recibida proviene de un solo emisor.</button>
  </div>

  <div class="pregunta">
    <p><strong>38. En relación con la ACL extendida, indicar cuál de las siguientes afirmaciones es cierta.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Contiene una entrada mask.</button>
    <button class="opcion" onclick="verificar(this, false)">b) No contiene una entrada mask.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los permisos se heredan desde el directorio padre.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna de las anteriores es cierta.</button>
  </div>

  <div class="pregunta">
    <p><strong>39. En relación con la ACL por defecto, indicar cuál de las siguientes afirmaciones es cierta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Contiene una entrada mask.</button>
    <button class="opcion" onclick="verificar(this, false)">b) No contiene una entrada mask.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Los permisos se heredan desde el directorio padre.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna de las anteriores es cierta.</button>
  </div>

  <div class="pregunta">
    <p><strong>40. Ocultar los caracteres cuando se introduce una contraseña es una medida:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Innecesaria.</button>
    <button class="opcion" onclick="verificar(this, false)">b) De seguridad pasiva.</button>
    <button class="opcion" onclick="verificar(this, true)">c) De seguridad activa.</button>
    <button class="opcion" onclick="verificar(this, false)">d) De seguridad física.</button>
  </div>

  <div class="pregunta">
    <p><strong>41. En un ataque por 'fuerza bruta':</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La longitud de la clave sí importa.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La longitud de la clave no importa.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Conseguir la contraseña en general es rápido.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El algoritmo de cifrado es indiferente.</button>
  </div>

  <div class="pregunta">
    <p><strong>42. El ataque por diccionario:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Es más eficiente que un ataque por fuerza bruta.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es menos eficiente que un ataque por fuerza bruta.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Depende de la robustez de la contraseña.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna de las anteriores es correcta.</button>
  </div>

  <div class="pregunta">
    <p><strong>43. En relación con la autenticación con varios factores, indica cuál de las siguientes afirmaciones es verdadera:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es lo mismo que la autenticación Single Sign-On.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Mejora el control de acceso.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Requiere contraseñas de más de 10 caracteres.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No existe este mecanismo.</button>
  </div>

  <div class="pregunta">
    <p><strong>44. Indicar en GNU/Linux Ubuntu cómo o dónde se almacenan las contraseñas de los usuarios del sistema.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) En texto plano.</button>
    <button class="opcion" onclick="verificar(this, false)">b) En la nube.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cifradas en el archivo /etc/passwd.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Cifradas en el archivo /etc/shadow.</button>
  </div>

  <div class="pregunta">
    <p><strong>45. Si ciframos en forma local un documento con GPG obtenemos un texto cifrado. Si volvemos a cifrar el mismo documento con la misma clave, indicar si:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los dos criptogramas serán iguales.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los dos criptogramas serán distintos (porque se usan vectores de inicialización dinámicos).</button>
    <button class="opcion" onclick="verificar(this, false)">c) No se puede hacer porque no acepta cifrar con la misma clave.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No se puede cifrar un documento con GPG.</button>
  </div>

  <div class="pregunta">
    <p><strong>46. En los criptosistemas asimétricos, la confidencialidad y la autenticidad se logran:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Por separado (se cifra para confidencialidad, se firma para autenticidad).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Rara vez.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Conjuntamente.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es imposible.</button>
  </div>

  <div class="pregunta">
    <p><strong>47. Los criptosistemas se clasifican en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Simétricos y hash.</button>
    <button class="opcion" onclick="verificar(this, false)">b) De bloque, de flujo y hash.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Clave privada y de bloque.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Clave privada (simétrica) y asimétrico (clave pública).</button>
  </div>

  <div class="pregunta">
    <p><strong>48. Para firmar un mensaje usando criptografía de clave pública:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se cifra el mensaje usando la clave pública.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se cifra el mensaje usando una clave secreta cifrada a su vez con la clave pública.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Se cifra un resumen del mensaje (hash) usando la clave privada.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se cifra la firma manuscrita escaneada y se añade al mensaje.</button>
  </div>

  <div class="pregunta">
    <p><strong>49. El algoritmo Diffie-Hellman:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Se utiliza en criptosistemas de clave pública (para el intercambio de claves).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se utiliza en criptosistemas de clave secreta.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Es un algoritmo de aplicación de “fuerza bruta”.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es un sistema generador de funciones hash.</button>
  </div>

  <div class="pregunta">
    <p><strong>50. De las siguientes afirmaciones, indica cuál de ellas es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La firma electrónica requiere la firma digital.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La firma digital es un tipo o implementación de la firma electrónica.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El certificado digital contiene la clave privada del usuario o entidad que representa.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La autoridad de certificación certifica claves privadas.</button>
  </div>

  <div class="pregunta">
    <p><strong>51. En relación a la autoridad de certificación (CA):</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Su misión es certificar claves privadas en una conexión segura mediante el navegador.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Guarda una copia de la clave privada del certificado digital emitido.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Firma el certificado digital expedido con su clave pública.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Guarda la clave pública del certificado digital emitido.</button>
  </div>

  <div class="pregunta">
    <p><strong>52. El DNI electrónico:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Contiene una firma electrónica.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es una firma electrónica.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Es un certificado electrónico.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Encripta la información.</button>
  </div>

  <div class="pregunta">
    <p><strong>53. Indicar cuál de las siguientes posibilidades es el principal problema que intentan resolver los sistemas de clave pública (Public Key Infrastructure, PKI).</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La mala intención de los usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La publicidad de la red Internet.</button>
    <button class="opcion" onclick="verificar(this, true)">c) La suplantación de identidad entre usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La escasa seguridad en las comunicaciones LAN.</button>
  </div>

  <div class="pregunta">
    <p><strong>54. Firmar digitalmente un documento es:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Cifrar el documento (o su resumen hash) con la clave privada.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Cifrar el documento (o parte) con la clave pública.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cifrar el documento con las claves pública y privada.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Descifrar el documento con las claves pública y privada.</button>
  </div>

  <div class="pregunta">
    <p><strong>55. Indicar cuál de los siguientes no es un rasgo biométrico identificativo (fisiológico).</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reconocimiento de la voz.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Firma manuscrita (es de comportamiento/conductual).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Huella dactilar.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Patrón de venas de la mano.</button>
  </div>

  <div class="pregunta">
    <p><strong>56. De los siguientes, cuál crees que sería rechazado por los sistemas biométricos (falso negativo).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Una persona autorizada no puede entrar en una sala.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una persona autorizada es confundida con otra persona autorizada.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un intruso puede entrar en la sala.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un intruso suplanta a una persona autorizada.</button>
  </div>

  <div class="pregunta">
    <p><strong>57. De los siguientes elementos, cuál se puede afirmar que identifica de forma inequívoca a una persona.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El rostro.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La mano.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El pie.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El iris.</button>
  </div>

  <div class="pregunta">
    <p><strong>58. De las siguientes opciones, cuál representa la posibilidad de que un dispositivo biométrico no reconozca a la persona autorizada.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Falso negativo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso positivo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Falsa aceptación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna de las otras.</button>
  </div>

  <div class="pregunta">
    <p><strong>59. Indicar cuál de los siguientes no es un rasgo de comportamiento biométrico.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La forma de andar.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La geometría del rostro (es fisiológico).</button>
    <button class="opcion" onclick="verificar(this, false)">c) La contraseña.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La voz.</button>
  </div>

  <div class="pregunta">
    <p><strong>60. Respecto a SHA-1, indicar cuál de las siguientes afirmaciones es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es un algoritmo para obtener un hash o un resumen digital. Se utiliza en relación con la trazabilidad de la evidencia digital.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es un algoritmo para cifrar una evidencia digital. Se utiliza en relación con la trazabilidad de la evidencia digital.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Es un algoritmo para cifrar una evidencia digital. Se utiliza en relación con la integridad de la evidencia digital.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Es un algoritmo para obtener un hash o un resumen digital. Se utiliza en relación con la integridad de la evidencia digital.</button>
  </div>

  <div class="pregunta">
    <p><strong>61. En relación con el proceso de análisis forense, indicar cuál de las siguientes secuencias de fase es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Evaluar, analizar, adquirir e informar.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Informar, evaluar, adquirir y analizar.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evaluar, adquirir, analizar e informar.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Adquirir, analizar, evaluar e informar.</button>
  </div>

  <div class="pregunta">
    <p><strong>62. La normativa ISO/IEC 27042 se utiliza para:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Analizar e interpretar evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Evaluar, adquirir y analizar las evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evaluar y adquirir las evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Evaluar, adquirir las evidencias e informar.</button>
  </div>

  <div class="pregunta">
    <p><strong>63. Indicar cuál de las siguientes no es una fase del análisis forense.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Identificación del incidente.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Análisis de la nube.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Captura de las evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Preservación de las evidencias.</button>
  </div>

  <div class="pregunta">
    <p><strong>64. Indicar cuál es la regla de oro del análisis forense.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Proteger los metadatos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Proteger el original de la evidencia.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Proteger las cookies de navegación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Proteger los procesos en ejecución.</button>
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
