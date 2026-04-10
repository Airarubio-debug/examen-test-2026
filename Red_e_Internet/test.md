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

  <div class="pregunta">
    <p><strong>91. El servicio FTP se creó después del servicio WWW.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>92. Los objetivos del servicio FTP son ser útil, distribuido, multiplataforma y eficaz o eficiente.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>93. ¿Cuál de los siguientes NO es un tipo de usuario real del servicio FTP?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Usuario local, que existe en el sistema y se conecta con su propia cuenta.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Usuario genérico (anónimo), que se conecta sin usuario y sin clave.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Usuario virtual, que se autentica en una base de datos específica.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Usuario FTP, que tiene una clave maestra para conectarse a cualquier servidor sin autenticarse.</button>
  </div>

  <div class="pregunta">
    <p><strong>94. Tanto el modo activo como el pasivo transmiten los datos por el puerto 20.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>95. En el modo aislado (standalone), es el servidor quien gestiona los puertos del servicio FTP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>96. El servidor vsftpd crea, al instalarse, el usuario FTP con el home en /srv/ftp.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>97. El servidor FileZilla Server puede trabajar con los protocolos FTP, FTPS o SFTP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>98. Indica cuál de las siguientes afirmaciones sobre el funcionamiento de los protocolos FTP, FTPS o SFTP es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) En los tres casos se utilizan credenciales para establecer un canal seguro cifrado.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Solo FTP envía los datos en texto claro.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El servicio SFTP encripta la comunicación utilizando TLS/SSL.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El servicio FTPES no requiere ningún tipo de certificado.</button>
  </div>

  <div class="pregunta">
    <p><strong>99. Cuando instalamos el servicio open-sftp-server, realmente instalamos el servidor sshd.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>100. Al arrancar el equipo, para que no se active un servicio ejecutamos $ systemctl enable &lt;servicio&gt;.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>101. Existe un único modo para conectarse al servidor FTP: mediante un cliente GUI.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>102. Podemos conectarnos a un servidor FTP desde el gestor de archivos conectando a unidad de red.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>103. Indica cuál de las siguientes afirmaciones relativas al cliente FileZilla es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tiene diez zonas diferenciadas de trabajo.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Disponemos de una ventana de solo archivos para el equipo local y para el remoto.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Existen tres familias de protocolos: FTP (FTP, FTPS y FTPES), SFTP y otra para la nube.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Podemos transferir archivos solo arrastrándolos.</button>
  </div>

  <div class="pregunta">
    <p><strong>104. FileZilla Client posibilita continuar descargas interrumpidas si el servidor lo permite.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>105. Desde la terminal de cualquier sistema operativo, aunque no tengamos ningún programa cliente de FTP, podemos conectarnos a cualquier servidor FTP y transferir archivos.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>106. En el archivo de configuración de vsftpd solo podemos tener comentarios o directivas.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>107. Los grupos de ámbito global pueden contener usuarios y grupos locales y universales de otros dominios.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>108. El nombre de inicio de sesión de las cuentas de usuario (pre-Windows 2000) no debe sobrepasar los 20 caracteres.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>109. El cambio del nombre del equipo es una práctica obligatoria. Sin el cambio del nombre, el equipo no se podrá integrar en el dominio.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>110. Cuando un usuario anónimo se conecta al servidor FTP, entra al directorio home del usuario ftp (/srv/ftp) y este es su directorio raíz por la utilización del ambiente o «jaula chroot».</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>111. Indica cuál de estas afirmaciones respecto a las opciones del servidor vsftpd para usuarios anónimos es correcta.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La carga de archivos está desactivada por defecto, pero podemos activarla.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La directiva anon_other_write_enable=YES permite que modifiquen los archivos que pertenecen a usuarios anónimos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La directiva anon_mkdir_write_enable=YES permite que puedan crear directorios.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas las anteriores son correctas.</button>
  </div>

  <div class="pregunta">
    <p><strong>112. El servidor de FileZilla guarda su configuración en archivos XML.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>113. El servidor de FileZilla nos permite configurar el nivel de registro que queremos aplicar al servidor en cinco niveles.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>114. Los clientes de correo también se denominan...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) SMTP.</button>
    <button class="opcion" onclick="verificar(this, true)">b) MUA.</button>
    <button class="opcion" onclick="verificar(this, false)">c) MTA.</button>
    <button class="opcion" onclick="verificar(this, false)">d) MDA.</button>
  </div>

  <div class="pregunta">
    <p><strong>115. Los protocolos que se utilizan para descargar los correos desde un MDA son...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) MTA y MDA.</button>
    <button class="opcion" onclick="verificar(this, true)">b) POP3 e IMAP4.</button>
    <button class="opcion" onclick="verificar(this, false)">c) POP3 y SMTP.</button>
    <button class="opcion" onclick="verificar(this, false)">d) IMAP4 y SMTP.</button>
  </div>

  <div class="pregunta">
    <p><strong>116. Los correos electrónicos permiten enviar...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Solo texto.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Solo contenido multimedia.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Texto y contenido multimedia.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo mensajes cortos de menos de 255 caracteres.</button>
  </div>

  <div class="pregunta">
    <p><strong>117. Cuando un servidor MTA delega en otro MTA el envío de todo el correo, al segundo MTA se le llama...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Smartphone.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Middleware.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Middle host.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Relay host.</button>
  </div>

  <div class="pregunta">
    <p><strong>118. ¿Qué comando sirve para averiguar cuál es el MTA del dominio «example.com»?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) dig example.com A</button>
    <button class="opcion" onclick="verificar(this, false)">b) mta-find example.com</button>
    <button class="opcion" onclick="verificar(this, true)">c) dig example.com MX</button>
    <button class="opcion" onclick="verificar(this, false)">d) host example.com</button>
  </div>

  <div class="pregunta">
    <p><strong>119. El tipo de registro DNS que identifica al MTA de un dominio es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) A.</button>
    <button class="opcion" onclick="verificar(this, true)">b) MX.</button>
    <button class="opcion" onclick="verificar(this, false)">c) TX.</button>
    <button class="opcion" onclick="verificar(this, false)">d) PTR.</button>
  </div>

  <div class="pregunta">
    <p><strong>120. El comando SMTP para indicar el destinatario del mensaje es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) HELO.</button>
    <button class="opcion" onclick="verificar(this, false)">b) MAIL FROM.</button>
    <button class="opcion" onclick="verificar(this, true)">c) RCPT TO.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DATA.</button>
  </div>

  <div class="pregunta">
    <p><strong>121. Es posible recibir correos externos dirigidos a nuestro dominio sin haber configurado explícitamente el registro MX para ese dominio (debido a que los servidores intentarán resolver el registro A como alternativa).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>122. Cuando hay varios registros MX, ¿cuál se usa primero?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El primero que aparece en el archivo de configuración de la zona.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El que tiene menor prioridad (el número más bajo).</button>
    <button class="opcion" onclick="verificar(this, false)">c) El que aparece el último en la zona.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Es ilegal tener más de un MX.</button>
  </div>

  <div class="pregunta">
    <p><strong>123. ¿Qué MUA podemos utilizar para leer el correo desde la terminal de Linux en modo texto?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Thunderbird.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Gmail.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Hotmail.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Alpine.</button>
  </div>

  <div class="pregunta">
    <p><strong>124. En el protocolo POP3, ¿qué puerto se utiliza por defecto para el tráfico en texto plano y cuál para el tráfico cifrado SSL/TLS, respectivamente?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) 110 y 995.</button>
    <button class="opcion" onclick="verificar(this, false)">b) 252 y 8080.</button>
    <button class="opcion" onclick="verificar(this, false)">c) 230 y 500.</button>
    <button class="opcion" onclick="verificar(this, false)">d) 995 y 110.</button>
  </div>

  <div class="pregunta">
    <p><strong>125. ¿Cómo se denomina al servidor encargado de entregar correo al MUA?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) POP3.</button>
    <button class="opcion" onclick="verificar(this, false)">b) MTA.</button>
    <button class="opcion" onclick="verificar(this, true)">c) MDA.</button>
    <button class="opcion" onclick="verificar(this, false)">d) MUA.</button>
  </div>

  <div class="pregunta">
    <p><strong>126. Un MUA utiliza el protocolo ___ o ___ para descargar el correo desde el MDA.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) SMTP o IMAP4.</button>
    <button class="opcion" onclick="verificar(this, true)">b) POP3 o IMAP4.</button>
    <button class="opcion" onclick="verificar(this, false)">c) POP2 o FTP.</button>
    <button class="opcion" onclick="verificar(this, false)">d) IMAF o SSH.</button>
  </div>

  <div class="pregunta">
    <p><strong>127. El protocolo IMAP4 usa los puertos ___ y ___ por defecto (para texto plano y cifrado, respectivamente).</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 110 y 25.</button>
    <button class="opcion" onclick="verificar(this, true)">b) 143 y 993.</button>
    <button class="opcion" onclick="verificar(this, false)">c) 112 y 800.</button>
    <button class="opcion" onclick="verificar(this, false)">d) 25 y 995.</button>
  </div>

  <div class="pregunta">
    <p><strong>128. El tráfico POP3 en texto plano está obsoleto, y se recomienda cifrar las comunicaciones mediante...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) TLS 1.1.</button>
    <button class="opcion" onclick="verificar(this, false)">b) SSL 2.0 o superior.</button>
    <button class="opcion" onclick="verificar(this, false)">c) SSL 3.0.</button>
    <button class="opcion" onclick="verificar(this, true)">d) TLS 1.2 o superior.</button>
  </div>

  <div class="pregunta">
    <p><strong>129. El puerto submission (587) se utiliza para recibir correo de los MUA, y el puerto relay (25) para recibir el de los MTA.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>130. Para minimizar el riesgo de que nuestros correos acaben en la bandeja de spam, se recomiendan tres técnicas de autenticación:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) SFP, DMIK y MARC.</button>
    <button class="opcion" onclick="verificar(this, true)">b) SPF, DKIM y DMARC.</button>
    <button class="opcion" onclick="verificar(this, false)">c) SSH, MARC y DCRAC.</button>
    <button class="opcion" onclick="verificar(this, false)">d) SPF, DKIM y MARC.</button>
  </div>

  <div class="pregunta">
    <p><strong>131. Si cerramos el puerto 25 para evitar ataques DOS/DDOS, seguiremos recibiendo todos los correos externos sin problemas.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (El puerto 25 es necesario para la comunicación entre MTAs, si se cierra, no entrará correo de otros dominios).</button>
  </div>

  <div class="pregunta">
    <p><strong>132. En el caso de que nuestra organización tuviera un volumen moderado o reducido, sería más recomendable contratar un servicio de correo externo (en la nube) que montar uno propio.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>133. ¿Qué garantía es opcional en TLS?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Confidencialidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Autenticación del servidor.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Integridad.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Autenticación del cliente.</button>
  </div>

  <div class="pregunta">
    <p><strong>134. Las listas de correo únicamente son privadas y el usuario decide suscribirse a ellas.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>135. El usuario decide suscribirse a una lista de correo pública pulsando en algún enlace, por ejemplo.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>136. ¿Qué aplicación permite el envío de mensajería instantánea por la red local sin necesidad de servidor?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) IP Messenger.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Slack.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Discord.</button>
    <button class="opcion" onclick="verificar(this, false)">d) MS Teams.</button>
  </div>

  <div class="pregunta">
    <p><strong>137. Los correos enviados a la lista se almacenan en el servidor por un tiempo determinado, con lo que permiten su consulta vía web.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>138. Para que los mensajes de las listas de distribución públicas no se envíen a la bandeja de spam, estas deberían...</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Confirmar la suscripción mediante correo electrónico y mostrar indicaciones claras para darse de baja mediante un enlace.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Meter las direcciones sin confirmar.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Únicamente confirmar la suscripción.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo mostrar indicaciones para darse de baja.</button>
  </div>

  <div class="pregunta">
    <p><strong>139. Cuanto mayor es la amplitud de la señal del sonido, mayor volumen perciben nuestros oídos.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>140. La ......................, expresada en hercios, mide la separación horizontal entre picos de la señal.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Latencia.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Sonoridad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Amplitud de onda.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Frecuencia.</button>
  </div>

  <div class="pregunta">
    <p><strong>141. Las frecuencias bajas equivalen a tonos agudos y picos más juntos.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Las bajas equivalen a tonos graves).</button>
  </div>

  <div class="pregunta">
    <p><strong>142. Cuando la señal pasa de analógico a digital, se produce pérdida de información.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>143. Ajustando la ganancia de los micrófonos al rango de entrada del ADC durante la adquisición, se evita el clipping.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>144. Los formatos con compresión que aplican técnicas para reducir su tamaño siempre tienen pérdidas de calidad.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Existen formatos de compresión sin pérdida, como FLAC).</button>
  </div>

  <div class="pregunta">
    <p><strong>145. Podemos guardar audio utilizando el códec Opus o PCM en un formato contenedor M4A.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (M4A se usa típicamente para ALAC o AAC).</button>
  </div>

  <div class="pregunta">
    <p><strong>146. La extensión del archivo es indicadora del códec utilizado para comprimir el audio.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (La extensión indica el formato contenedor, no el códec).</button>
  </div>

  <div class="pregunta">
    <p><strong>147. Los códecs de audio pueden empezar a reproducir un bloque antes de haberlo recibido y decodificado en su totalidad.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>148. Al mecanismo de almacenar varios bloques antes de empezar a reproducir para evitar cortes se le llama...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aprovisionamiento.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Buffering.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Descarga.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Acumulación.</button>
  </div>

  <div class="pregunta">
    <p><strong>149. Al número de columnas y filas de la imagen se le llama...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Píxeles.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Relación de aspecto.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Resolución.</button>
    <button class="opcion" onclick="verificar(this, false)">d) ADC.</button>
  </div>

  <div class="pregunta">
    <p><strong>150. Existen resoluciones estandarizadas que reciben nombres comerciales.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>151. En un sistema entrelazado, cada fotograma se envía entero.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Se envían las líneas pares y luego las impares).</button>
  </div>

  <div class="pregunta">
    <p><strong>152. Si vamos a montar un vídeo a partir de distintas fuentes, es importante que todas se graben con la misma cantidad de fotogramas por segundo (fps).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>153. Actualmente, el reproductor más utilizado es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Winamp.</button>
    <button class="opcion" onclick="verificar(this, true)">b) VLC Media Player.</button>
    <button class="opcion" onclick="verificar(this, false)">c) SM Player.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Media Monkey.</button>
  </div>

  <div class="pregunta">
    <p><strong>154. Los algoritmos de compresión de imágenes funcionan aprovechando redundancias de información en la imagen.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>155. Todos los formatos de compresión de imágenes permiten tener o no tener pérdidas.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>156. Uno de los artefactos característicos de la compresión JPEG es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El efecto peine.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La aparición de bloques.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El color es más nítido.</button>
  </div>

  <div class="pregunta">
    <p><strong>157. Cuando un fotograma se codifica usando los cambios respecto al anterior, a este se le llama fotograma P.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>158. ¿Cuál de las opciones es una herramienta multiplataforma que ofrece un GUI sencillo para convertir entre archivos multimedia?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) FFmpeg.</button>
    <button class="opcion" onclick="verificar(this, false)">b) YouTube.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Handbrake.</button>
    <button class="opcion" onclick="verificar(this, false)">d) CRF.</button>
  </div>

  <div class="pregunta">
    <p><strong>159. El streaming requiere un ancho de banda proporcional a la cantidad de espectadores.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>160. ¿Cuál de los siguientes es un protocolo de streaming?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) SMTP.</button>
    <button class="opcion" onclick="verificar(this, false)">b) HTTP.</button>
    <button class="opcion" onclick="verificar(this, true)">c) RTSP.</button>
    <button class="opcion" onclick="verificar(this, false)">d) ASP.</button>
  </div>

  <div class="pregunta">
    <p><strong>161. ¿Cuál de estas plataformas pertenece al grupo de las más importantes para hospedar pódcast en la actualidad?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Anchor.fm.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Twitch.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Google Play Music.</button>
  </div>

  <div class="pregunta">
    <p><strong>162. Una de las aplicaciones más versátiles para generar contenido a partir de múltiples fuentes y grabarlo en un archivo local o enviarlo a servidores de streaming en tiempo real es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) OBK.</button>
    <button class="opcion" onclick="verificar(this, true)">b) OBS.</button>
    <button class="opcion" onclick="verificar(this, false)">c) HLS.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Content Generator.</button>
  </div>

  <div class="pregunta">
    <p><strong>163. ¿Cuál de estos formatos de streaming es incompatible con navegadores de Apple?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) RTSP.</button>
    <button class="opcion" onclick="verificar(this, false)">b) RTMP.</button>
    <button class="opcion" onclick="verificar(this, false)">c) HLS.</button>
    <button class="opcion" onclick="verificar(this, true)">d) DASH.</button>
  </div>

  <div class="pregunta">
    <p><strong>164. La principal desventaja de los paneles de administración es...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que son un quebradero de cabeza en el caso de migrar.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Que no son especialmente recomendables para empresas que revendan espacio de servidor.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que dificultan la actualización y explotación a largo plazo.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Que suponen una dependencia de un entorno de administración (lock-in).</button>
  </div>

  <div class="pregunta">
    <p><strong>165. A la hora de elegir un panel de administración...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Elegiremos un panel como Webmin o Virtualmin cuando necesitemos un panel comercial robusto con un gran soporte detrás.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Elegiremos un panel como CPanel o Plesk cuando solo nos haga falta un frontend de administración sobre el servidor.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El aislamiento de usuarios en servidor compartido no es un tema crítico.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Elegiremos un panel como CPanel o Plesk cuando necesitemos un panel comercial robusto con un gran soporte detrás.</button>
  </div>

  <div class="pregunta">
    <p><strong>166. HestiaCP es un panel de licencia libre, potente y centrado en la seguridad, pero muy limitado a unas pocas versiones de Linux (Debian/Ubuntu).</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>167. La filosofía y estructura de ficheros de configuración no estándar en HestiaCP es muy diferente a la de paneles como Cpanel o Plesk, y no es extrapolable.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (HestiaCP usa ficheros estándar del sistema en gran medida).</button>
  </div>

  <div class="pregunta">
    <p><strong>168. En los servicios web de HestiaCP, Apache escucha las peticiones directamente desde los puertos 80 y 443.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Nginx actúa como reverse proxy y escucha esos puertos, pasando la petición luego a Apache).</button>
  </div>

  <div class="pregunta">
    <p><strong>169. En los servicios de email, HestiaCP implementa soporte DKIM y SSL mediante certificado con Let’s Encrypt.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>170. Para cambiar opciones de los servicios web que no vienen en el panel, podremos cambiar los ficheros de configuración de HestiaCP manualmente.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>171. HestiaCP incorpora multiprocesamiento de páginas dinámicas en ASP, PHP y JSP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Soporta principalmente PHP, no incluye ASP ni JSP por defecto).</button>
  </div>

  <div class="pregunta">
    <p><strong>172. Indica cuál es la opción falsa sobre HestiaCP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ofrece chroot jail en los usuarios SSH/SFTP, para aislamiento.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Ofrece un gran soporte multiplataforma para Windows y Linux.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Centrado en la seguridad, ofrece certificados Let’s Encrypt para correo y web.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Arquitectura reverse proxy con Apache/Nginx y soporte multiPHP.</button>
  </div>

  <div class="pregunta">
    <p><strong>173. Indica la opción correcta respecto a HestiaCP y los servicios que ofrece.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ofrece un servicio web con arquitectura reverse proxy con Apache/Nginx.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Ofrece servicio de correo electrónico con Exim, Dovecot, SpamAssasin, ClamAV y RoundCube.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Ofrece servicio DNS mediante bind.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas son correctas.</button>
  </div>

  <div class="pregunta">
    <p><strong>174. Indica la opción correcta respecto a los servicios DNS y relacionados en la nube.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) En la nube no se utilizan los servicios DNS tradicionales.</button>
    <button class="opcion" onclick="verificar(this, false)">b) En lugar de servicios DNS, se utilizan balanceadores de carga, que enrutan las peticiones según latencia, ubicación geográfica, ponderación, etcétera.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El uso de monitorización y health checks ha sustituido la resolución de nombres.</button>
    <button class="opcion" onclick="verificar(this, true)">d) El desarrollo del cloud ha provisto a los servicios DNS de funcionalidades extendidas para funcionar correctamente a nivel global.</button>
  </div>

  <div class="pregunta">
    <p><strong>175. El enrutamiento de peticiones DNS como extensión de servicio en la nube se puede realizar...</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) De acuerdo con latencia, ubicación geográfica, ponderación y temperatura.</button>
    <button class="opcion" onclick="verificar(this, true)">b) De acuerdo con latencia, ubicación geográfica, ponderación, fallo o mezcla de varias.</button>
    <button class="opcion" onclick="verificar(this, false)">c) De acuerdo con fallo, latencia, ubicación geográfica y carga de cada nodo destino.</button>
    <button class="opcion" onclick="verificar(this, false)">d) De acuerdo con latencia, ubicación geográfica, fallo y VPC.</button>
  </div>

  <div class="pregunta">
    <p><strong>176. Normalmente no es posible lanzar nuestro propio servicio DHCP en la nube (salvo contadas excepciones en soluciones privadas). Por ejemplo, en AWS se implementa mediante conjuntos de opciones elegibles.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>177. Indica la opción correcta respecto a servicios de red Cloud.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El servicio de configuración automática en Azure se llama Traffic Manager.</button>
    <button class="opcion" onclick="verificar(this, false)">b) En la nube no se hace uso de DHCP; se ha sustituido por la infraestructura como código o IaC.</button>
    <button class="opcion" onclick="verificar(this, false)">c) NetBIOS para configuración de varias máquinas virtuales está incluido en la configuración DHCP de AWS y Azure.</button>
    <button class="opcion" onclick="verificar(this, true)">d) En Azure no existen configuraciones personalizadas de DHCP, pero se pueden especificar los DNS de cada VNet.</button>
  </div>

  <div class="pregunta">
    <p><strong>178. Indica la opción correcta referida a Infraestructura como Código.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La IaC o infraestructura como código permite crear, configurar y mantener estructuras en la nube mediante scripting.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Existen diferentes estándares de IaC para cada proveedor de la nube, pero hay un lenguaje unificado independiente, llamado Terraform.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Todas son correctas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) En AWS existe un editor gráfico de IaC y una galería de soluciones profesionales en scripting llamada AWS Quick Starts.</button>
  </div>

  <div class="pregunta">
    <p><strong>179. Servicios como AWS S3 ofrecen espacio de almacenamiento masivo que puede usarse para servir contenido web estático sin mantener servidores.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>180. El almacenamiento de contenido web estático en la nube es una buena opción, pero es mejor el uso de servidores Apache + PHP para ello.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Para contenido puramente estático, S3 o Blob Storage es infinitamente más barato y eficiente).</button>
  </div>

  <div class="pregunta">
    <p><strong>181. El almacenamiento de contenido web estático en la nube (S3/Blob) puede procesar peticiones PHP, ASP o JSP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>182. Servicios como AWS S3 o Azure Blob solo se pueden usar para el almacenamiento multimedia on-line, no para contenido HTML, JS o CSS.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>183. Una «red de distribución de contenidos», o CDN, es un servicio que permite servir copias de contenidos de una web (a modo de caché) desde ubicaciones que estén más cercanas geográficamente al visitante de esta.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>184. Un CDN ofrece protección frente a ataques de phishing y robo de identidad, dado que establece una verificación de las peticiones distribuido y robusto frente a estos ataques a través de DNS Anycast.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Los CDN protegen contra DDoS y sobrecargas, pero no evitan el phishing u otros robos de identidad a nivel aplicación).</button>
  </div>

  <div class="pregunta">
    <p><strong>185. Señala la opción incorrecta en el esquema de una aplicación moderna.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Peticiones dinámicas como PHP son atendidas por servidores clónicos en escalado horizontal, todos con el mismo código compartido de un repositorio común.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Siguen siendo necesarios servidores, que están detrás de un balanceador de carga, de forma que procesan las peticiones dinámicas, cada uno con su código fuente propio.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La multimedia de la web es servida por un almacenamiento estático masivo a escala global sin servidores concretos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La base de datos debe poder escalar desde un servidor a un complejo clúster, sin que se vean alterados sustancialmente los modos de acceso desde la aplicación.</button>
  </div>

  <div class="pregunta">
    <p><strong>186. Indica la opción incorrecta en una aplicación de una sola página o SPA.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un ejemplo de SPA puede ser Gmail.com, Google Maps o Airbnb.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Utiliza los formularios clásicos GET o POST para el envío de peticiones, recargando el sitio web entero.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Suele realizar una carga inicial pesada y luego utiliza peticiones asíncronas para las acciones, sin refrescar la página.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La carga inicial de datos se refiere a multimedia, HTML, librerías CSS o JS: datos web estáticos, en definitiva.</button>
  </div>

  <div class="pregunta">
    <p><strong>187. Señala la opción correcta sobre el esquema de una aplicación moderna llevada a AWS.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Las peticiones son recibidas por Route 53 y divididas por el CDN CloudFront en estáticas y dinámicas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La base de datos a la que llegan las peticiones de los servidores usualmente se implementa en servicio RDS.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las peticiones estáticas son servidas por S3, y las dinámicas, por un balanceador de carga gestiona un grupo de servidores.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas son correctas.</button>
  </div>

  <div class="pregunta">
    <p><strong>188. Señala la opción incorrecta respecto a servicios de AWS para implementar una aplicación moderna.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los servidores que gestionan las peticiones dinámicas suelen estar en un grupo de autoescalado, para crecer o disminuir en número.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El servicio CloudFlare, la CDN de AWS, tiene un coste muy reducido o incluso gratuito hasta dimensiones muy elevadas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los servidores que gestionan las peticiones dinámicas suelen compartir el código fuente desde un repositorio común EFS.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El servicio Route 53 de DNS sí interviene en este esquema de infraestructura.</button>
  </div>

  <div class="pregunta">
    <p><strong>189. Señala la respuesta correcta sobre la red telefónica conmutada o RTC.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se establecía una conmutación de paquetes, manualmente o mediante máquinas, entre emisor y receptor de la comunicación.</button>
    <button class="opcion" onclick="verificar(this, false)">b) La principal ventaja es que tiene una capacidad de uso prácticamente ilimitada.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Se establecía un circuito, manualmente o mediante máquinas, entre emisor y receptor de la comunicación, conmutando en diferentes centralitas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Hasta la segunda mitad del siglo XX, usaba conmutación de circuitos, y a partir de ahí conmutación de paquetes.</button>
  </div>

  <div class="pregunta">
    <p><strong>190. Señala la respuesta incorrecta respecto a la transición a telefonía IP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los teléfonos convencionales deben sustituirse por teléfonos IP.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los teléfonos convencionales deben sustituirse por softphones que conectan directamente con las troncales SIP.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Las centralitas privadas PBX deben sustituirse por centralitas PBX IP.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Las troncales convencionales se sustituyen por troncales SIP.</button>
  </div>

  <div class="pregunta">
    <p><strong>191. La telefonía IP surge de la idea de digitalizar y encapsular la voz como datos y transmitirlos como paquetes IP por red local e Internet, abandonando progresivamente la conmutación de circuitos en favor de conmutación de paquetes.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>192. Los gateway VoIP fueron un elemento esencial en la transición de la RTC convencional a la telefonía IP en las empresas, pero hoy en día es prácticamente imposible encontrar dispositivos que permitan usar teléfonos convencionales para VoIP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (Aún existen y se usan adaptadores ATA o Gateways para aprovechar teléfonos antiguos).</button>
  </div>

  <div class="pregunta">
    <p><strong>193. Las PBX IP son el reemplazo de las PBX convencionales para ubicaciones privadas con la transición a telefonía IP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>194. Las PBX IP son también conocidas como troncales SIP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Falso (La PBX es la centralita, la troncal SIP es la "línea" que la conecta al operador).</button>
  </div>

  <div class="pregunta">
    <p><strong>195. La gestión de números virtuales (DID) o los menús de respuesta interactiva de voz (IVR) son características deseables en las PBX IP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Verdadero.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Falso.</button>
  </div>

  <div class="pregunta">
    <p><strong>196. Indica la opción verdadera respecto a la transición a telefonía IP.</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) WebRTC surge como tecnología unificadora para suplir carencias de seguridad y compatibilidad, principalmente respecto a SIP.</button>
    <button class="opcion" onclick="verificar(this, false)">b) WebRTC fue un intento de realizar una red telefónica conmutada o RTC a través de navegadores de Internet.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La principal desventaja de WebRTC es que necesita de plugins para funcionar.</button>
    <button class="opcion" onclick="verificar(this, false)">d) WebRTC tiene la ventaja de funcionar bajo navegadores de forma universal, pero no está coordinada con organizaciones de estandarización como IETF o W3C.</button>
  </div>

  <div class="pregunta">
    <p><strong>197. Indica la opción correcta sobre protocolos de telefonía IP.</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El protocolo SIP hace uso del protocolo SDP y de los protocolos STUN/TURN bajo framework ICE.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El proyecto WebRTC hace uso del protocolo SDP y de los protocolos STUN/TURN bajo framework ICE.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El proyecto WebRTC hace uso de los protocolos SRTP y DTLS para dotar de más seguridad a la transmisión.</button>
    <button class="opcion" onclick="verificar(this, true)">d) Todas son ciertas.</button>
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
