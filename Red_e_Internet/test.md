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
    <p><strong>1. Un dominio tiene un nombre, y todos sus miembros comparten el mismo.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>2. Señala la afirmación correcta sobre un FQDN (Nombre de Dominio Completo):</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El nombre de dominio completo puede tener un máximo de 63 caracteres.</button>
    <button class="opcion" onclick="verificar(this, false)">b) No se puede utilizar la letra ñ en ningún dominio actual.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Después del nombre de equipo, podemos tener el nombre del dominio de primer nivel, separado por un punto.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Siempre termina en un punto, que va implícito, que hace referencia al dominio raíz.</button>
    <button class="opcion" onclick="verificar(this, false)">e) Cada nodo puede tener una longitud de 255 caracteres.</button>
  </div>

  <div class="pregunta">
    <p><strong>3. El elemento más a la izquierda del nombre de dominio completo representa siempre el nombre del equipo o un alias.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>4. Los dominios y sus subdominios se separan exclusivamente con guiones.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>5. La jerarquía de dominios es descendente, del nivel superior hacia los inferiores, pero el nombre de domino completo se lee al revés, de izquierda a derecha.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>6. Podemos tener dos nombres de dominio completos que se llamen igual.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>7. Podemos crear alias de nombres sobre los equipos de máquinas.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>8. Si tenemos un servidor que resuelve en el dominio mheducation.com, la dirección IP de ese servidor se encuentra almacenada...</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Solo en el servidor de mheducation.com.</button>
    <button class="opcion" onclick="verificar(this, false)">b) En el servidor de mheducation.com y en los servidores de primer nivel del dominio .com.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Solo en los servidores de primer nivel para el dominio .com.</button>
    <button class="opcion" onclick="verificar(this, false)">d) En los servidores de primer nivel del domino .com y en los servidores raíz.</button>
  </div>

  <div class="pregunta">
    <p><strong>9. El dominio de primer nivel .net es un dominio de tipo sTLD.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>10. Los clientes DNS realizan sus consultas a través del resolutor (resolver).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>11. En un proceso de resolución del nombre DNS de www.mheducation.com, un servidor del dominio .com le envía a un servidor raíz la IP de www.mheducation.com.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) No existe este tipo de resolución.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se está realizando una resolución iterativa.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se está realizando una resolución recursiva.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se está realizando una resolución inversa.</button>
  </div>

  <div class="pregunta">
    <p><strong>12. En un proceso de resolución del nombre DNS de www.mheducation.com, un servidor del dominio .com le envía a nuestro servidor DNS directamente la IP de www.mheducation.com.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) No existe este tipo de resolución.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Se está realizando una resolución iterativa.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se está realizando una resolución recursiva.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se está realizando una resolución inversa.</button>
  </div>

  <div class="pregunta">
    <p><strong>13. El puerto 53 es donde están escuchando los servidores las peticiones DNS de los clientes.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>14. En la resolución directa, se busca por cierta IP para averiguar su nombre DNS.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>15. Existen cuatro tipos diferentes de servidores DNS: primario, secundario, caché y reenviador.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>16. Podemos realizar modificaciones en una zona secundaria.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>17. Una zona primaria contiene una copia del contenido de una zona secundaria.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>18. Una zona secundaria se puede usar para resolver nombres.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>19. Las zonas sirven para resoluciones directas, pero también para resoluciones inversas.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>20. Una zona slave es una zona secundaria.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>21. Un servidor DNS es autoritario sobre zonas primarias, pero no sobre las secundarias.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>22. ¿Qué podemos hacer si tenemos un servidor DNS con la zona correspondiente a un dominio dividido en subdominios?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que el servidor use zona del servidor de nivel superior.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que el servidor delegue en otras zonas la resolución de los nombres de los miembros de los subdominios.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Que el servidor tenga una sola zona para resolver nombres en todo el dominio.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que el servidor delegue la gestión de sus subdominios en servidores de terceros.</button>
  </div>

  <div class="pregunta">
    <p><strong>23. En los registros de recursos, el campo de marca de tiempo de vida (TTL) es un campo obligatorio.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>24. El tipo de registro PTR de la clase IN sirve para las búsquedas inversas.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>25. Para instalar el servidor DNS en GNU/Linux ejecutaremos $ sudo apt install named.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>26. Los archivos de configuración del servidor DNS BIND en GNU/Linux están en /etc/bind.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>27. Respecto a los archivos de configuración de BIND (Señala la correcta general):</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El archivo named.conf.default-zones contiene la información de las zonas por defecto del espacio de nombres.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El archivo named.conf.local contiene la información de las zonas creadas por defecto al instalar BIND.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El archivo named.conf.options contiene la información de las opciones globales del servidor.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El archivo named.conf incluye en su configuración el contenido de los tres anteriores.</button>
  </div>

  <div class="pregunta">
    <p><strong>28. En BIND podemos definir tantas acl de listas de direcciones IP como necesitemos.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>29. En BIND podemos utilizar cinco tipos de zonas: master, slave, hint, forward y view.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>30. El servicio DDNS surge por la escasez de IPv4.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>31. Solo podremos montarnos un servidor web en nuestro equipo con DDNS.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>32. ¿Qué servicio DDNS permite ser reutilizado por otros servicios DDNS?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) www.DynDNS.org.</button>
    <button class="opcion" onclick="verificar(this, false)">b) www.DtDNS.com.</button>
    <button class="opcion" onclick="verificar(this, true)">c) www.dnsomatic.com.</button>
    <button class="opcion" onclick="verificar(this, false)">d) www-no-ip.com.</button>
  </div>

  <div class="pregunta">
    <p><strong>33. El servicio DDNS también se utiliza para sincronizar el servicio DNS y el servicio DHCP entre ellos.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>34. El servicio DuckDNS funciona mediante una API HTTP, en modo seguro, con un certificado SSL firmado de 128 bits válido.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
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
