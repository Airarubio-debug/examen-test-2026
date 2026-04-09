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

<div class="pregunta">
    <p><strong>35. Un ordenador tiene la IP 170.10.30.5, y máscara 255.255.0.0. Su identificador de red es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 5.</button>
    <button class="opcion" onclick="verificar(this, false)">b) 34.5.</button>
    <button class="opcion" onclick="verificar(this, true)">c) 170.10.</button>
    <button class="opcion" onclick="verificar(this, false)">d) 170.10.30.</button>
  </div>

  <div class="pregunta">
    <p><strong>36. En la configuración manual o fija de los parámetros de red, indica cuál de los siguientes parámetros no se configura.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) IPv4.</button>
    <button class="opcion" onclick="verificar(this, false)">b) IPv6.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Servidor DNS.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Servidor DHCP.</button>
  </div>

  <div class="pregunta">
    <p><strong>37. Un adaptador de red tiene IP 170.10.30.1 y máscara 255.255.0.0. En esa IP, indica cuál es el identificador del host o del adaptador dentro de la red.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 170.10</button>
    <button class="opcion" onclick="verificar(this, false)">b) 170.10.30</button>
    <button class="opcion" onclick="verificar(this, false)">c) 1</button>
    <button class="opcion" onclick="verificar(this, true)">d) 30.1</button>
  </div>

  <div class="pregunta">
    <p><strong>38. «Es obligatorio que la puerta de enlace predeterminada y los servidores DNS que se establezcan en la configuración de red de un ordenador estén en la misma red que el ordenador para que este pueda conectarse y trabajar en Internet».</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>39. En la configuración de los adaptadores de red, si se quiere que la IP se asigne mediante DHCP, indica cuál debe ser el valor asignado al parámetro renderer (en Ubuntu/Netplan).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) renderer: networkd</button>
    <button class="opcion" onclick="verificar(this, false)">b) renderer: NetworkManager</button>
    <button class="opcion" onclick="verificar(this, false)">c) renderer: dhcp</button>
    <button class="opcion" onclick="verificar(this, false)">d) renderer: false</button>
  </div>

  <div class="pregunta">
    <p><strong>40. De los siguientes mensajes DHCP, indica cuál de ellos no es enviado de cliente a servidor DHCP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) DHCP_ACK.</button>
    <button class="opcion" onclick="verificar(this, false)">b) DHCP_RELEASE.</button>
    <button class="opcion" onclick="verificar(this, false)">c) DHCP_DISCOVER.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DHCP_REQUEST.</button>
  </div>

  <div class="pregunta">
    <p><strong>41. Cuando un cliente DHCP solicita la renovación de una concesión DHCP, el primer mensaje que envía es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DHCP_DISCOVER.</button>
    <button class="opcion" onclick="verificar(this, false)">b) DHCP_OFFER.</button>
    <button class="opcion" onclick="verificar(this, true)">c) DHCP_REQUEST.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DHCP_RELEASE.</button>
  </div>

  <div class="pregunta">
    <p><strong>42. En un proceso normal de solicitud y asignación de una IP en un cliente DHCP desde un servidor, se transmiten mensajes DHCP en este orden:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) DHCP_DISCOVER, DHCP_OFFER, DHCP_REQUEST, DHCP_ACK.</button>
    <button class="opcion" onclick="verificar(this, false)">b) DHCP_DISCOVER, DHCP_REQUEST, DHCP_OFFER, DHCP_ACK.</button>
    <button class="opcion" onclick="verificar(this, false)">c) DHCP_OFFER, DHCP_DISCOVER, DHCP_REQUEST, DHCP_ACCEPT.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DHCP_OFFER, DHCP_REQUEST, DHCP_DISCOVER, DHCP_ACCEPT.</button>
  </div>

  <div class="pregunta">
    <p><strong>43. Indica cuál de los siguientes parámetros no se considera obligatorio para ser entregado por un servidor DHCP a los clientes.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Direcciones IP de los servidores DNS.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Direcciones IP para los clientes.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Tiempo de concesión.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Tiempo de renovación de licencia.</button>
  </div>

  <div class="pregunta">
    <p><strong>44. Señala el método de asignación DHCP en el que un mismo adaptador de red no puede recibir desde un mismo servidor diferentes direcciones IP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Asignación manual.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Asignación automática.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Asignación dinámica.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguna de las anteriores.</button>
  </div>

  <div class="pregunta">
    <p><strong>45. Indica en qué directorio se encuentra el archivo de configuración dhcpd.conf en sistemas Ubuntu.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) /etc/</button>
    <button class="opcion" onclick="verificar(this, true)">b) /etc/dhcp/</button>
    <button class="opcion" onclick="verificar(this, false)">c) /etc/init.d/</button>
    <button class="opcion" onclick="verificar(this, false)">d) /var/lib/dhcp/</button>
  </div>

  <div class="pregunta">
    <p><strong>46. Indica en qué declaración del archivo de configuración dhcpd.conf se deben especificar los rangos de direcciones IP que se asignan dinámicamente.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) subnet.</button>
    <button class="opcion" onclick="verificar(this, false)">b) shared-network.</button>
    <button class="opcion" onclick="verificar(this, false)">c) host.</button>
    <button class="opcion" onclick="verificar(this, false)">d) group.</button>
  </div>

  <div class="pregunta">
    <p><strong>47. De los siguientes comandos, indica cuál no se debe usar en sistemas GNU/Linux Ubuntu relacionados con el funcionamiento de DHCP y la configuración de red (por estar obsoleto frente a Netplan/iproute2).</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) route.</button>
    <button class="opcion" onclick="verificar(this, false)">b) ip.</button>
    <button class="opcion" onclick="verificar(this, false)">c) dhclient.</button>
    <button class="opcion" onclick="verificar(this, true)">d) ifup.</button>
  </div>

  <div class="pregunta">
    <p><strong>48. De los siguientes comandos, indica cuál se utiliza para detener el servicio DHCP en sistemas GNU/Linux Ubuntu.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) sudo /etc/init.d/dhcp3-server start</button>
    <button class="opcion" onclick="verificar(this, false)">b) /etc/init.d/dhcp3-server</button>
    <button class="opcion" onclick="verificar(this, false)">c) sudo service dns-server start</button>
    <button class="opcion" onclick="verificar(this, true)">d) service dhcp3-server stop</button>
  </div>

  <div class="pregunta">
    <p><strong>49. El paquete para instalar el servidor DHCP de ISC en sistemas GNU/Linux Ubuntu se llama:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) dhcp.</button>
    <button class="opcion" onclick="verificar(this, true)">b) isc-dhcp-server.</button>
    <button class="opcion" onclick="verificar(this, false)">c) dhcpd.</button>
    <button class="opcion" onclick="verificar(this, false)">d) dhcpd-isc-server.</button>
  </div>

  <div class="pregunta">
    <p><strong>50. Si se recibe una configuración DHCP no permitida, se manda un mensaje DHCPNack denegando esa configuración. Indica cuál es, de los siguientes, el parámetro utilizado para ello.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) range.</button>
    <button class="opcion" onclick="verificar(this, false)">b) group.</button>
    <button class="opcion" onclick="verificar(this, true)">c) authoritative.</button>
    <button class="opcion" onclick="verificar(this, false)">d) param.</button>
  </div>

  <div class="pregunta">
    <p><strong>51. Indica cuál de las siguientes afirmaciones es verdadera.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) El servidor DHCP mantiene una base datos con las conexiones activas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El servidor DHCP puede detectar clientes no autorizados.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El servidor DHCP no puede ofrecer parámetros de red a varias subredes a la vez.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El servidor DHCP no permite la realización de auditorías.</button>
  </div>

  <div class="pregunta">
    <p><strong>52. Indica cuál de las siguientes situaciones no se podrá resolver mediante un servidor DHCP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Un equipo no autorizado con una IP válida puede acceder a la red.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Un equipo que se reubica en una subred diferente hay que configurarlo manualmente.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cuando se configuran los parámetros de los equipos de la red de forma manual, se pueden introducir errores.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La configuración manual de los parámetros de los equipos de la red es administrativamente tediosa.</button>
  </div>

  <div class="pregunta">
    <p><strong>53. Indica cuál de las siguientes afirmaciones es falsa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El DHCP snooping se configura en el switch.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El rogue DHCP tiene como objetivo posibilitar ataques man-in-the-middle.</button>
    <button class="opcion" onclick="verificar(this, false)">c) En el switch hay que indicar qué puertos son asignados a servidores DHCP autorizados.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El DHCP snooping bloquea mensajes tipo DISCOVER y REQUEST emitidos desde puertos no asignados a servidores DHCP autorizados.</button>
  </div>

  <div class="pregunta">
    <p><strong>54. Indica cuál es la verdadera de las siguientes afirmaciones referidas al mensaje DHCPNack utilizado por un servidor DHCP autoritativo.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reconocer la configuración asignada por otro servidor DHCP.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Rechazar la configuración autoasignada por un cliente.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aceptar la configuración autoasignada por un cliente.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Impedir que un cliente reciba los parámetros de configuración de red de otro servidor DHCP.</button>
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
