
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
    <p><strong>1. ¿Qué tipos de aplicación de gestión usan tecnología propietaria de IBM?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Las aplicaciones web.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Las aplicaciones de consola (terminales clásicos AS/400).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las aplicaciones de usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las aplicaciones de escritorio.</button>
  </div>

  <div class="pregunta">
    <p><strong>2. ¿Qué diferencia a la Web3 del resto de etapas de la Web?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es dinámica.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es estática.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Es distribuida (descentralizada / basada en blockchain).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es social.</button>
  </div>

  <div class="pregunta">
    <p><strong>3. ¿A partir de qué etapa de la Web existe comunicación fluida entre cliente y servidor?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Web 1.5.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Web 1.0.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Web 2.0 (aparición de AJAX y redes sociales).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Web3.</button>
  </div>

  <div class="pregunta">
    <p><strong>4. ¿Qué aplicaciones web funcionan con la tecnología de blockchain?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Web 1.5.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Web 2.0.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Web3.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Web 1.0.</button>
  </div>

  <div class="pregunta">
    <p><strong>5. ¿De qué partes se compone una aplicación web actual?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) De dos: del frontal y el dashboard.</button>
    <button class="opcion" onclick="verificar(this, false)">b) De una: la aplicación web.</button>
    <button class="opcion" onclick="verificar(this, false)">c) De cuatro: una web cliente, un dashboard al servidor, un SBGDR y criptomonedas.</button>
    <button class="opcion" onclick="verificar(this, true)">d) De tres: el front-end, el back-end y la base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>6. ¿Qué tecnologías y aspectos del diseño de interfaces se han de desarrollar en la parte cliente?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Todas las opciones son correctas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El código en JavaScript.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El HTML5 y el CSS3.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La UX/UI.</button>
  </div>

  <div class="pregunta">
    <p><strong>7. ¿Qué lenguaje de servidor podemos utilizar en nuestros desarrollos web?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) PHP.</button>
    <button class="opcion" onclick="verificar(this, false)">b) C.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Java EE.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas las opciones son correctas.</button>
  </div>

  <div class="pregunta">
    <p><strong>8. ¿Qué SGBDR instalamos con el metapaquete lamp-server^ en Ubuntu?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Cualquiera de los fork de MySQL (como MariaDB).</button>
    <button class="opcion" onclick="verificar(this, false)">b) IBM DB2.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Microsoft SQL Server.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Oracle Database.</button>
  </div>

  <div class="pregunta">
    <p><strong>9. ¿Qué servicio debemos contratar si queremos tener un espacio público web?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Hosting.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Una web.</button>
    <button class="opcion" onclick="verificar(this, false)">c) SaaS.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un espacio web.</button>
  </div>

  <div class="pregunta">
    <p><strong>10. ¿Dónde se sitúan las aplicaciones web como el servicio de e-mail web (ej. Gmail)?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) SaaS (Software as a Service).</button>
    <button class="opcion" onclick="verificar(this, false)">b) IaaS.</button>
    <button class="opcion" onclick="verificar(this, false)">c) PaaaS.</button>
    <button class="opcion" onclick="verificar(this, false)">d) In-house.</button>
  </div>

  <div class="pregunta">
    <p><strong>11. Si en una web de WordPress se ha creado un post, es lo mismo decir que se ha creado:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Una categoría.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Un widget.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una página.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Una entrada.</button>
  </div>

  <div class="pregunta">
    <p><strong>12. En el apartado 'extracto' de una entrada de WordPress se escribirá:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Un resumen del contenido de la entrada que, según el tema, se mostrará en una determinada ubicación.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El nombre del autor a modo de copyright y se mostrará siempre al pie de la entrada.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El nombre del autor a modo de copyright que, según el tema, se mostrará en una determinada ubicación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un resumen del contenido de la entrada que siempre se mostrará al final de la misma.</button>
  </div>

  <div class="pregunta">
    <p><strong>13. ¿Qué tipo de archivo se genera al exportar el contenido de las entradas de un sitio web realizado con WordPress?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) XLSX.</button>
    <button class="opcion" onclick="verificar(this, false)">b) CSV.</button>
    <button class="opcion" onclick="verificar(this, false)">c) DOCX.</button>
    <button class="opcion" onclick="verificar(this, true)">d) XML.</button>
  </div>

  <div class="pregunta">
    <p><strong>14. Para incluir un icono en un sitio web que se muestre en las pestañas del navegador (favicon), se debe hacer desde:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Menú de administración > Apariencia > Personalizar (Identidad del sitio).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Menú de administración > Apariencia > Menús.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Menú de administración > Apariencia > Temas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Menú de administración > Apariencia > Editor de temas.</button>
  </div>

  <div class="pregunta">
    <p><strong>15. De los siguientes roles de usuario de WordPress, ¿cuál tiene menos privilegios?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Editor.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Suscriptor.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Administrador.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Autor.</button>
  </div>

  <div class="pregunta">
    <p><strong>16. De los siguientes roles de usuario de WordPress, ¿cuál tiene más privilegios?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Autor.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Administrador.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Suscriptor.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Editor.</button>
  </div>

  <div class="pregunta">
    <p><strong>17. La carpeta 'plugins' de WordPress:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Está dentro de wp-content y contiene los plugins del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Está dentro de wp-admin y contiene los plugins del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Está dentro de wp-admin y contiene los recursos del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Está dentro de wp-content y contiene los recursos del sitio web.</button>
  </div>

  <div class="pregunta">
    <p><strong>18. La carpeta 'themes' de WordPress:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Está dentro de wp-content y contiene los temas del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Está dentro de wp-admin y contiene los temas del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Está dentro de wp-admin y contiene los plugins del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Está dentro de wp-content y contiene los plugins del sitio web.</button>
  </div>

  <div class="pregunta">
    <p><strong>19. La carpeta 'uploads' de WordPress:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Está dentro de wp-admin y contiene los recursos del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Está dentro de wp-admin y contiene los plugins del sitio web.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Está dentro de wp-content y contiene los recursos (archivos subidos) del sitio web.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Está dentro de wp-content y contiene los plugins del sitio web.</button>
  </div>

  <div class="pregunta">
    <p><strong>20. El plugin Akismet de WordPress:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es de pago y viene con la instalación de WordPress, pero desactivado.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es gratuito, pero hay que instalarlo y activarlo a propósito.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Es gratuito (para uso personal) y viene con la instalación de WordPress, pero desactivado.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es de pago, pero hay que instalarlo y activarlo a propósito.</button>
  </div>

  <div class="pregunta">
    <p><strong>21. La edición de hojas de cálculo con Nextcloud:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solamente se puede realizar si la hoja de cálculo ha sido creada previamente desde Google Drive.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Se puede realizar instalando alguna aplicación adicional, como por ejemplo ONLYOFFICE Docs o Collabora.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se puede realizar sin necesidad de instalar ninguna aplicación adicional, ya que esa función viene integrada en la propia instalación de Nextcloud.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solamente se puede realizar si la hoja de cálculo ha sido creada previamente desde Microsoft Office.</button>
  </div>

  <div class="pregunta">
    <p><strong>22. El idioma de la interfaz de Nextcloud:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No se puede cambiar, ya que la herramienta está predefinida en idioma inglés para todos los usuarios.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Lo puede cambiar cualquier usuario desde la opción de Configuración personal.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solamente lo puede cambiar el usuario administrador de la herramienta y se cambiará para todos los usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solamente se puede cambiar en la versión de pago de la herramienta.</button>
  </div>

  <div class="pregunta">
    <p><strong>23. Respecto a los usuarios de Nextcloud:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Se permite crear varios grupos y varios usuarios en cada uno de esos grupos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Solamente se permite tener un usuario administrador y otro usuario adicional que tendrá solamente permisos de lectura sobre los archivos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solamente se permite tener un usuario administrador.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se permite crear varios usuarios pero no grupos.</button>
  </div>

  <div class="pregunta">
    <p><strong>24. El registro de actividad de Nextcloud:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Sirve para configurar qué actividades se notifican a los usuarios y el administrador las configura, de forma individual, para cada grupo de usuarios de la herramienta.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Sirve para configurar qué actividades se notifican a los usuarios y el administrador las configura para que sean las mismas para todos los usuarios de la herramienta.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Sirve para configurar qué actividades se notifican a los usuarios y cada usuario configura las suyas propias.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sirve para configurar qué actividades se notifican a los usuarios y el administrador las configura, de forma individual, para cada usuario de la herramienta.</button>
  </div>

  <div class="pregunta">
    <p><strong>25. En Nextcloud, a la hora de compartir un archivo con otro usuario…</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Hemos de hacer clic en el icono Compartir y luego buscar el usuario, pero solamente lo encontraremos si indicamos su nombre exacto con el que está registrado en la herramienta.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Hemos de hacer clic en el icono Compartir y luego buscar el usuario, al que podemos encontrar tanto por su nombre como por su e-mail.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Hemos de hacer clic en el icono Compartir y luego buscar el usuario, pero solamente lo encontraremos por su e-mail.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No se puede, porque la función de compartir solamente está disponible para carpetas.</button>
  </div>

  <div class="pregunta">
    <p><strong>26. Los archivos que otros usuarios han compartido con nosotros en Nextcloud…</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No los podemos compartir con nadie más.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los podemos eliminar sin que le desaparezcan al usuario que los compartió con nosotros (solamente "abandonamos" la compartición).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los podemos eliminar, pero desaparecerán también del espacio del usuario que los compartió con nosotros.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aparecerán siempre en nuestro espacio y no hay forma de eliminarlos.</button>
  </div>

  <div class="pregunta">
    <p><strong>27. Para poder compartir por medio de enlaces en Nextcloud:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solamente el usuario administrador lo puede hacer con los documentos y carpetas que ha creado o subido él mismo a la herramienta.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Solamente se puede hacer si, previamente, el administrador ha habilitado la opción de compartir mediante enlaces desde la configuración de la herramienta.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solamente lo podrán hacer los usuarios concretos a los que el administrador les haya habilitado esta característica, el resto deberá solicitarlo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Nadie lo puede hacer, Nextcloud no ofrece esta característica actualmente.</button>
  </div>

  <div class="pregunta">
    <p><strong>28. En el caso de compartir una carpeta mediante enlaces en Nextcloud, se puede elegir entre las siguientes opciones:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solo lectura o subida/edición de archivos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Solo lectura, subida/edición de archivos o solo subir archivos (File drop).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo lectura o solo subir archivos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Subida/edición de archivos o solo subir archivos.</button>
  </div>

  <div class="pregunta">
    <p><strong>29. Después de instalar Nextcloud podemos consultar avisos de seguridad y configuración desde:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El menú Configuración > Aplicaciones.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El archivo de configuración de Nextcloud.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El menú Configuración > Administración > Vista General.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El archivo de configuración de Apache.</button>
  </div>

  <div class="pregunta">
    <p><strong>30. Marca la opción correcta sobre la vista de archivos en Nextcloud:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los archivos que han compartido con nosotros no los podemos descargar, solamente visualizarlos desde dentro de la herramienta.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Los archivos que han compartido con nosotros aparecen siempre completamente separados de los que hemos subido nosotros.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solamente podemos subir un archivo si previamente lo hemos subido a Google Drive.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Podemos ver una miniatura y actividad del archivo desde los tres puntos junto al archivo entrando en la opción de detalles.</button>
  </div>

  <div class="pregunta">
    <p><strong>31. Un programa realizado en PHP se debe ejecutar en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se ejecuta en el servidor o el cliente, el que esté menos ocupado.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El ordenador del cliente.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El servidor.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Parte en el servidor y parte en el cliente.</button>
  </div>

  <div class="pregunta">
    <p><strong>32. Para insertar código PHP dentro de código HTML se utilizan las etiquetas:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) &lt;? y ?&gt;</button>
    <button class="opcion" onclick="verificar(this, true)">b) &lt;?php y ?&gt;</button>
    <button class="opcion" onclick="verificar(this, false)">c) &lt;script language="php"&gt; y &lt;/script&gt;</button>
    <button class="opcion" onclick="verificar(this, false)">d) No es necesario indicar nada.</button>
  </div>

  <div class="pregunta">
    <p><strong>33. Indica la expresión correcta para comparar si la variable $a es igual a 0:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) $a == 0</button>
    <button class="opcion" onclick="verificar(this, false)">b) $a = 0</button>
    <button class="opcion" onclick="verificar(this, false)">c) $a != 0</button>
    <button class="opcion" onclick="verificar(this, false)">d) $a -&gt; 0</button>
  </div>

  <div class="pregunta">
    <p><strong>34. Para que el navegador muestre la palabra «Hola» en negrita desde PHP escribiremos:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) print_r Hola;</button>
    <button class="opcion" onclick="verificar(this, true)">b) echo '&lt;b&gt;Hola&lt;/b&gt;';</button>
    <button class="opcion" onclick="verificar(this, false)">c) print_r 'Hola';</button>
    <button class="opcion" onclick="verificar(this, false)">d) echo Hola;</button>
  </div>

  <div class="pregunta">
    <p><strong>35. Respecto a las variables y arrays en PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) En PHP solamente existen variables.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una variable escalar almacena un único dato y un array, un conjunto de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Son lo mismo, tanto las variables como los arrays sirven para almacenar un único dato.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Una variable almacena un conjunto de datos y un array un único dato.</button>
  </div>

  <div class="pregunta">
    <p><strong>36. La definición de array escalar (indexado) es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un sistema para convertir una variable de texto en un número.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Un conjunto de elementos que solo pueden ser enteros.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un conjunto de valores escalables que van incrementando de valor a medida que aumenta su posición.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Varios valores a los que se accede mediante un número entero llamado índice.</button>
  </div>

  <div class="pregunta">
    <p><strong>37. La función time() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Devuelve la fecha y hora actual (como un timestamp Unix).</button>
    <button class="opcion" onclick="verificar(this, false)">b) Devuelve solamente la fecha.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Da un error.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Devuelve solamente la hora.</button>
  </div>

  <div class="pregunta">
    <p><strong>38. Dado el siguiente código, la llamada correcta a la función es:<br><br>function suma($num1, $num2) {<br>  return $num1+$num2;<br>}<br><br>$a=5;<br>$b=6;</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) total = suma($a, $b);</button>
    <button class="opcion" onclick="verificar(this, true)">b) $total = suma($a, $b);</button>
    <button class="opcion" onclick="verificar(this, false)">c) $suma($a, $b);</button>
    <button class="opcion" onclick="verificar(this, false)">d) $total = $suma($num1, $num2);</button>
  </div>

  <div class="pregunta">
    <p><strong>39. Si se quiere definir una constante en PHP se deberá:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Utilizar la palabra def.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Utilizar la palabra con.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Utilizar la palabra const.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Utilizar la función define().</button>
  </div>

  <div class="pregunta">
    <p><strong>40. En el bucle foreach ($a as $b =&gt; $c) { … }</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) $b es el array, $a es la clave y $c es el valor.</button>
    <button class="opcion" onclick="verificar(this, true)">b) $a es el array, $b es la clave y $c es el valor.</button>
    <button class="opcion" onclick="verificar(this, false)">c) $c es el array, $b es la clave y $a es el valor.</button>
    <button class="opcion" onclick="verificar(this, false)">d) $a es el array, $c es la clave y $b es el valor.</button>
  </div>

  <div class="pregunta">
    <p><strong>41. La función mysqli_connect() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cierra una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Ejecuta una consulta sobre una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Devuelve el error obtenido al conectar a la base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Abre una conexión a una base de datos MySQL.</button>
  </div>

  <div class="pregunta">
    <p><strong>42. La función mysqli_close() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Devuelve el error obtenido al conectar a la base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Cierra una conexión con la base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Abre una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ejecuta una consulta sobre una base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>43. La función mysqli_connect_error() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Abre una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Devuelve la descripción del último error de conexión a la base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cierra una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ejecuta una consulta sobre una base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>44. La función mysqli_query() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Abre una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Cierra una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Ejecuta una consulta (query) sobre una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Devuelve el error obtenido al conectar a la base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>45. La función mysqli_fetch_assoc() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cierra una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Extrae una fila de un conjunto de resultados como un array asociativo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Abre una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ejecuta una consulta sobre una base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>46. La función mysqli_free_result() de PHP:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ejecuta una consulta sobre una base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Abre una conexión a una base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Libera la memoria asociada a un conjunto de resultados obtenidos de una consulta.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Extrae una fila del resultado obtenido de una consulta.</button>
  </div>

  <div class="pregunta">
    <p><strong>47. A través del lenguaje PHP, ¿qué tipos de consultas se pueden ejecutar sobre una base de datos MySQL?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) SELECT, INSERT y DELETE.</button>
    <button class="opcion" onclick="verificar(this, false)">b) SELECT y UPDATE.</button>
    <button class="opcion" onclick="verificar(this, true)">c) SELECT, INSERT, UPDATE y DELETE (Todas las sentencias CRUD).</button>
    <button class="opcion" onclick="verificar(this, false)">d) SELECT y DELETE.</button>
  </div>

  <div class="pregunta">
    <p><strong>48. Indica qué afirmación sobre PHP y MySQL es correcta:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) PHP y MySQL son incompatibles; por lo tanto, desde PHP no se puede acceder a MySQL de ninguna forma.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Desde PHP es fácil y nativo acceder a bases de datos como MySQL utilizando extensiones como mysqli o PDO.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Acceder a MySQL desde PHP es un proceso complejo que requiere de muchos pasos de configuración a través de phpMyAdmin.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Desde PHP es difícil acceder a MySQL, pero se puede hacer a través de aplicaciones que hacen de enlace como phpMyAdmin.</button>
  </div>

  <div class="pregunta">
    <p><strong>49. Indica la afirmación correcta sobre los plugins de WordPress:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se desactivan automáticamente si cambias de tema.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Se pueden programar a medida (desarrollo propio).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solamente se pueden instalar desde el repositorio oficial de WordPress.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solamente se pueden instalar desde sitios web de empresas desarrolladoras.</button>
  </div>

  <div class="pregunta">
    <p><strong>50. Un tema hijo (child theme) en WordPress:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tan solo se puede instalar desde el repositorio oficial de WordPress.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Puede funcionar perfectamente sin tener instalado el tema padre.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Necesita de un tema padre, ya que hereda su funcionalidad para poder realizar las modificaciones sin perderse en las actualizaciones.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Únicamente se puede instalar desde sitios web de empresas desarrolladoras.</button>
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
