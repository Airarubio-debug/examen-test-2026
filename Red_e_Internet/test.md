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

  <div class="pregunta">
    <p><strong>55. Completa la frase: El protocolo HTTP es un protocolo de transferencia de ___. Por defecto, establece el puerto ___ como puerto con el que se comunica el servidor con el ___. Para realizar una comunicación ___ entre un servidor y un cliente se necesita establecer previamente una conexión ___. En una comunicación HTTP, el cliente envía mensajes de ___, y el servidor envía mensajes de ___.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) TCP, 80, cliente, hipertexto, HTTP, respuesta, petición.</button>
    <button class="opcion" onclick="verificar(this, true)">b) hipertexto, TCP 80, cliente, HTTP, TCP, petición, respuesta.</button>
    <button class="opcion" onclick="verificar(this, false)">c) HTTP, 80, TCP, hipertexto, cliente, petición, respuesta.</button>
    <button class="opcion" onclick="verificar(this, false)">d) hipertexto, 80, cliente, TCP, HTTP, respuesta, petición.</button>
  </div>

  <div class="pregunta">
    <p><strong>56. ¿Cuál de los siguientes datos no forma parte de una línea de petición de un mensaje HTTP?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Versión de protocolo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Método.</button>
    <button class="opcion" onclick="verificar(this, false)">c) URI.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Descripción de estado.</button>
  </div>

  <div class="pregunta">
    <p><strong>57. ¿Cuál de los siguientes datos forma parte de una línea de respuesta de un mensaje HTTP?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Versión de protocolo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Método.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cuerpo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Servidor.</button>
  </div>

  <div class="pregunta">
    <p><strong>58. En principio, MIME se desarrolló para permitir la transmisión de multitud de tipos de archivos mediante:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El protocolo HTTP.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El protocolo FTP.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El correo electrónico.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El protocolo DNS.</button>
  </div>

  <div class="pregunta">
    <p><strong>59. El elemento de un documento web que sirve para enlazar con otro documento web se llama:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Hipertexto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Hipermedio.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Hipervínculo.</button>
    <button class="opcion" onclick="verificar(this, false)">d) HTML.</button>
  </div>

  <div class="pregunta">
    <p><strong>60. Una vez que se ha instalado el servidor web Apache, ¿qué carpeta es tomada como carpeta raíz del sitio web?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) /var/www/html</button>
    <button class="opcion" onclick="verificar(this, false)">b) /var/lib/apache2</button>
    <button class="opcion" onclick="verificar(this, false)">c) /etc/apache2</button>
    <button class="opcion" onclick="verificar(this, false)">d) /etc/init.d/apache2</button>
  </div>

  <div class="pregunta">
    <p><strong>61. Tras instalar el servidor Apache en un sistema Ubuntu, el archivo principal de configuración es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) /etc/apache/httpd.conf</button>
    <button class="opcion" onclick="verificar(this, true)">b) /etc/apache2/apache2.conf</button>
    <button class="opcion" onclick="verificar(this, false)">c) /etc/apache/apache2.conf</button>
    <button class="opcion" onclick="verificar(this, false)">d) /var/www</button>
  </div>

  <div class="pregunta">
    <p><strong>62. Indica cuál de los siguientes archivos se utiliza para la resolución del servidor web el equipo local.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) /etc/apache/httpd.conf</button>
    <button class="opcion" onclick="verificar(this, false)">b) /etc/apache2/apache2.conf</button>
    <button class="opcion" onclick="verificar(this, true)">c) /etc/hosts</button>
    <button class="opcion" onclick="verificar(this, false)">d) /etc/apache/apache2.conf</button>
  </div>

  <div class="pregunta">
    <p><strong>63. Indica cuál de los siguientes comandos volvería a arrancar el servicio Apache.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) $ sudo systemctl apache2 restart</button>
    <button class="opcion" onclick="verificar(this, true)">b) $ sudo systemctl restart apache2</button>
    <button class="opcion" onclick="verificar(this, false)">c) $ sudo service restart apache2</button>
    <button class="opcion" onclick="verificar(this, false)">d) $ sudo /etc/init.d/apache restart</button>
  </div>

  <div class="pregunta">
    <p><strong>64. De los siguientes servidores web, indica cuál de ellos tiene una mayor implantación a nivel global.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Apache.</button>
    <button class="opcion" onclick="verificar(this, false)">b) IIS.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Google.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Nginx.</button>
  </div>

  <div class="pregunta">
    <p><strong>65. Indica en cuál de los siguientes directorios se encuentran los archivos de carga de todos los módulos instalados para Apache.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) /usr/lib/apache2/modules</button>
    <button class="opcion" onclick="verificar(this, false)">b) /etc/apache2/modules</button>
    <button class="opcion" onclick="verificar(this, false)">c) /etc/apache2/mods-enabled</button>
    <button class="opcion" onclick="verificar(this, true)">d) /etc/apache2/mods-available</button>
  </div>

  <div class="pregunta">
    <p><strong>66. En la configuración de un servidor virtual, la directiva DocumentRoot debe escribirse en el archivo de configuración del servidor virtual...</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Dentro de la directiva VirtualHost.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Antes del comienzo de la directiva VirtualHost.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Después de finalizar la directiva VirtualHost.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Antes de comenzar la directiva NameVirtualHost.</button>
  </div>

  <div class="pregunta">
    <p><strong>67. La directiva de configuración de Apache ServerRoot /apache indica que...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los archivos de configuración del servidor están en /apache.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La carpeta raíz del sitio web es /apache.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las páginas web del sitio se almacenan bajo el directorio /apache.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El servidor está instalado en el directorio /apache.</button>
  </div>

  <div class="pregunta">
    <p><strong>68. De las siguientes afirmaciones, indica la opción verdadera.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El registro de Apache2 es similar al registro de Windows: almacena configuraciones del sistema.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La instalación de Apache2 deja, por defecto, activados sus mecanismos de registro de actividad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El registro de Apache2 no almacena registro de actividad del servidor web.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El registro de Apache2 no almacena información sobre los accesos al servidor web.</button>
  </div>

  <div class="pregunta">
    <p><strong>69. En relación con el módulo mod_userdir, indica cuál estas opciones es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cualquier usuario puede tener en su home su espacio web.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El usuario especificado es el dueño de su home.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Todos los usuarios, por defecto, pueden tener web propia.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El usuario especificado es el dueño del dominio.</button>
  </div>

  <div class="pregunta">
    <p><strong>70. Respecto a la directiva Satisfy, indica cuál es la opción correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Selecciona los usuarios autenticados que pueden acceder a un recurso.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Dispone de los parámetros allow y deny.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Puede requerir autenticación HTTP y por IP.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las opciones a y b.</button>
  </div>

  <div class="pregunta">
    <p><strong>71. Indica cuál de las siguientes afirmaciones es falsa.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La autenticación se lleva a cabo mediante el módulo mod_auth.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La autorización se controla mediante la sección Directory.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Hay, básicamente, dos tipos de autenticación: básica y digest.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La autenticación por IP equivale al control de acceso.</button>
  </div>

  <div class="pregunta">
    <p><strong>72. La autenticación es un...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Mecanismo para verificar la existencia del usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Mecanismo para la comprobación de permisos de los usuarios.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Mecanismo de comprobación de credenciales.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Mecanismo sustitutivo de los certificados digitales.</button>
  </div>

  <div class="pregunta">
    <p><strong>73. La utilización del control de acceso o autenticación por IP...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Requiere la utilización de las directivas Order y Require.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Utiliza Satisfy para combinarse con la autenticación HTTP.</button>
    <button class="opcion" onclick="verificar(this, false)">c) No permite la autenticación desde dominios.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Devuelve el error 403 de prohibición y da opción a volver a intentarlo.</button>
  </div>

  <div class="pregunta">
    <p><strong>74. Indica cuál de las siguientes afirmaciones es cierta.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) La autenticación por IP equivale al control de acceso.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La autenticación genérica se lleva a cabo mediante el módulo mod_auth.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La sección Location no permite control de acceso.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La autorización se controla mediante la sección VirtualHost.</button>
  </div>

  <div class="pregunta">
    <p><strong>75. Cuando se ejecuta en Ubuntu el comando para obtener un certificado autofirmado, ¿qué archivos se deben indicar dentro del comando?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El archivo del certificado y el de petición de firma del certificado.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El archivo de clave y el de petición de firma del certificado.</button>
    <button class="opcion" onclick="verificar(this, true)">c) El archivo de certificado y el de clave.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El archivo de certificado, el de petición de firma del certificado y el de clave.</button>
  </div>

  <div class="pregunta">
    <p><strong>76. En el certificado digital aparece la identidad de la autoridad de certificación.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>77. Verificar la validez de un certificado requiere comprobar la firma de la autoridad de certificación (CA) usando la clave pública de la CA.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>78. El objetivo de una CA es acreditar la correspondencia entre una clave y su propietario real.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>79. Una autoridad certificadora puede tener un certificado digital emitido por otra autoridad.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>80. La autoridad certificadora (CA) se encarga de firmar digitalmente...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los certificados de las autoridades de registro.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La clave pública de los usuarios junto con otra información de la identidad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las claves privadas de los usuarios de dicha CA.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las claves simétricas de los usuarios.</button>
  </div>

  <div class="pregunta">
    <p><strong>81. En relación con la firma digital, indica cuál de las siguientes afirmaciones es la correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Al adjuntar una firma digital a un mensaje se asegura su confidencialidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El receptor verifica la validez de la firma con su clave pública.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las opciones a y b.</button>
    <button class="opcion" onclick="verificar(this, true)">d) La firma digital de un mensaje no requiere cifrar todo el mensaje con la clave privada del remitente.</button>
  </div>

  <div class="pregunta">
    <p><strong>82. El módulo ssl requiere la desactivación del puerto 80.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>83. La directiva SSLEngine no requiere ningún parámetro.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>84. El módulo ssl requiere la utilización del archivo httpd-ssl.conf.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>85. La directiva SSLRequireSSL se debe poner a On para trabajar con soporte SSL.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>86. Respecto a SHA-1, indica cuál de las siguientes afirmaciones es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es un algoritmo para obtener un hash o resumen digital. Se utiliza en relación con la trazabilidad de la evidencia digital.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Es un algoritmo para cifrar una evidencia digital. Se utiliza en relación con la trazabilidad de la evidencia digital.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Es un algoritmo para cifrar una evidencia digital. Se utiliza en relación con la integridad de la evidencia digital.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Es un algoritmo para obtener un hash o resumen digital. Se utiliza en relación con la integridad de la evidencia digital.</button>
  </div>

  <div class="pregunta">
    <p><strong>87. En relación al proceso de análisis forense, indica cuál de las siguientes secuencias de fase es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Evaluar, analizar, adquirir e informar.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Informar, evaluar, adquirir y analizar.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Evaluar, adquirir, analizar e informar.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Adquirir, analizar, evaluar e informar.</button>
  </div>

  <div class="pregunta">
    <p><strong>88. La normativa ISO/IEC 27042 se aplica a...</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Analizar e interpretar evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Evaluar, adquirir y analizar las evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Evaluar y adquirir las evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Evaluar, adquirir las evidencias e informar.</button>
  </div>

  <div class="pregunta">
    <p><strong>89. Indica cuál de las siguientes no es una fase del análisis forense.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Identificación del incidente.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Análisis de la nube.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Captura de las evidencias.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Preservación de las evidencias.</button>
  </div>

  <div class="pregunta">
    <p><strong>90. Indica cuál es la regla de oro del análisis forense.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Proteger los metadatos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Proteger el original de la evidencia.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Proteger las cookies de navegación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Proteger los procesos en ejecución.</button>
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
