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
    <p><strong>1. Una *instancia* de SGBD describe:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cualquier base de datos concreta dentro del sistema</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una ejecución concreta del motor con su configuración y ficheros asociados</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un usuario con permisos de administrador</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un clúster completo de bases de datos distribuidas</button>
  </div>

  <div class="pregunta">
    <p><strong>2. Un sistema optimizado para OLTP se asocia más con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Consultas analíticas largas y agregaciones masivas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Transacciones cortas y muchas operaciones pequeñas</button>
    <button class="opcion" onclick="verificar(this, false)">c) Procesos por lotes sin usuarios concurrentes</button>
    <button class="opcion" onclick="verificar(this, false)">d) Procesamiento exclusivamente en columnas</button>
  </div>

  <div class="pregunta">
    <p><strong>3. Según la arquitectura ANSI/X3/SPARC, el NIVEL INTERNO describe:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Vistas particulares para cada usuario</button>
    <button class="opcion" onclick="verificar(this, false)">b) El modelo conceptual de negocio</button>
    <button class="opcion" onclick="verificar(this, true)">c) La organización física en dispositivos y estructuras de almacenamiento</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los informes que genera la aplicación</button>
  </div>

  <div class="pregunta">
    <p><strong>4. Un *esquema* (schema) en una BD relacional es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un backup completo</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un contenedor lógico que agrupa tablas y objetos relacionados</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una tabla temporal generada automáticamente</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un listado de usuarios y roles</button>
  </div>

  <div class="pregunta">
    <p><strong>5. La independencia *lógica* de los datos permite:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Cambiar el esquema conceptual sin tocar las vistas externas</button>
    <button class="opcion" onclick="verificar(this, false)">b) Cambiar los ficheros físicos sin modificar el esquema interno</button>
    <button class="opcion" onclick="verificar(this, false)">c) Modificar los programas cliente sin cambiar el SGBD</button>
    <button class="opcion" onclick="verificar(this, false)">d) Alterar una tabla sin afectar a sus restricciones</button>
  </div>

  <div class="pregunta">
    <p><strong>6. Los logs del SGBD se utilizan, entre otras cosas, para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Almacenar solo estadísticas gráficas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Reconstruir el estado ante fallos y auditar acciones</button>
    <button class="opcion" onclick="verificar(this, false)">c) Reemplazar las copias de seguridad</button>
    <button class="opcion" onclick="verificar(this, false)">d) Guardar configuraciones del sistema operativo</button>
  </div>

  <div class="pregunta">
    <p><strong>7. En un sistema de información, el *contenido* está formado por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los programas de red</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los datos con significado</button>
    <button class="opcion" onclick="verificar(this, false)">c) El sistema operativo</button>
    <button class="opcion" onclick="verificar(this, false)">d) El hardware del servidor</button>
  </div>

  <div class="pregunta">
    <p><strong>8. La *coherencia* de la información implica que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No existan datos duplicados en ningún caso</button>
    <button class="opcion" onclick="verificar(this, false)">b) Los datos sean físicamente accesibles en disco</button>
    <button class="opcion" onclick="verificar(this, true)">c) La información no sea contradictoria dentro del propio sistema</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo el administrador pueda modificarlos</button>
  </div>

  <div class="pregunta">
    <p><strong>9. Conceder o revocar permisos a un usuario es propio de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DDL</button>
    <button class="opcion" onclick="verificar(this, false)">b) DML</button>
    <button class="opcion" onclick="verificar(this, true)">c) DCL</button>
    <button class="opcion" onclick="verificar(this, false)">d) TCL</button>
  </div>

  <div class="pregunta">
    <p><strong>10. Guardar físicamente los registros en ficheros de disco corresponde a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) BD (datos)</button>
    <button class="opcion" onclick="verificar(this, false)">b) Cliente</button>
    <button class="opcion" onclick="verificar(this, true)">c) SGBD</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sistema operativo exclusivamente</button>
  </div>

  <div class="pregunta">
    <p><strong>11. El motor de almacenamiento se ocupa principalmente de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Dibujar diagramas ER automáticamente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Cómo se guardan físicamente los datos y qué capacidades (bloqueos, transacciones…) ofrece</button>
    <button class="opcion" onclick="verificar(this, false)">c) Gestionar la interfaz del cliente gráfico</button>
    <button class="opcion" onclick="verificar(this, false)">d) Traducir SQL a HTML</button>
  </div>

  <div class="pregunta">
    <p><strong>12. La *autenticación* responde a la pregunta:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) ¿Qué puedes hacer?</button>
    <button class="opcion" onclick="verificar(this, true)">b) ¿Quién eres?</button>
    <button class="opcion" onclick="verificar(this, false)">c) ¿Dónde se guardan los datos?</button>
    <button class="opcion" onclick="verificar(this, false)">d) ¿Cuánto espacio queda en disco?</button>
  </div>

  <div class="pregunta">
    <p><strong>13. Que los datos estén completos para cumplir su función se asocia a la cualidad de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Significado</button>
    <button class="opcion" onclick="verificar(this, false)">b) Coherencia</button>
    <button class="opcion" onclick="verificar(this, true)">c) Compleción</button>
    <button class="opcion" onclick="verificar(this, false)">d) Precisión</button>
  </div>

  <div class="pregunta">
    <p><strong>14. La *oportunidad* de la información se relaciona principalmente con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El porcentaje de datos correctos</button>
    <button class="opcion" onclick="verificar(this, true)">b) El tiempo que tarda en estar disponible para el usuario</button>
    <button class="opcion" onclick="verificar(this, false)">c) El número de usuarios que la consultan</button>
    <button class="opcion" onclick="verificar(this, false)">d) El tamaño del fichero donde se almacena</button>
  </div>

  <div class="pregunta">
    <p><strong>15. ¿Cuál de estas NO es una función esencial del SGBD?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Definir y manipular datos</button>
    <button class="opcion" onclick="verificar(this, false)">b) Proporcionar acceso concurrente seguro</button>
    <button class="opcion" onclick="verificar(this, true)">c) Renderizar la interfaz gráfica de usuario</button>
    <button class="opcion" onclick="verificar(this, false)">d) Gestionar seguridad e integridad</button>
  </div>

  <div class="pregunta">
    <p><strong>16. ¿Cuál de estos componentes NO forma parte del soporte lógico de un sistema de información?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Sistema Gestor de Bases de Datos</button>
    <button class="opcion" onclick="verificar(this, false)">b) Sistema Operativo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Software de redes</button>
    <button class="opcion" onclick="verificar(this, true)">d) Fuente de alimentación redundante</button>
  </div>

  <div class="pregunta">
    <p><strong>17. La integridad de entidad garantiza que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No existan columnas sin índice</button>
    <button class="opcion" onclick="verificar(this, true)">b) Cada fila esté identificada de forma única</button>
    <button class="opcion" onclick="verificar(this, false)">c) Ninguna tabla esté vacía</button>
    <button class="opcion" onclick="verificar(this, false)">d) Todas las columnas acepten valores nulos</button>
  </div>

  <div class="pregunta">
    <p><strong>18. La integridad referencial evita:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Valores fuera de rango</button>
    <button class="opcion" onclick="verificar(this, false)">b) Claves primarias duplicadas</button>
    <button class="opcion" onclick="verificar(this, true)">c) Referencias a filas inexistentes en tablas relacionadas</button>
    <button class="opcion" onclick="verificar(this, false)">d) La creación de índices innecesarios</button>
  </div>

  <div class="pregunta">
    <p><strong>19. El diccionario de datos almacena principalmente:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Copias de seguridad completas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Metadatos sobre tablas, columnas, claves, vistas, permisos…</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los registros de negocio de cada tabla</button>
    <button class="opcion" onclick="verificar(this, false)">d) Logs de errores del sistema operativo</button>
  </div>

  <div class="pregunta">
    <p><strong>20. ¿Quién es responsable del control técnico global del sistema de BD?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Usuario final</button>
    <button class="opcion" onclick="verificar(this, false)">b) Programador de aplicaciones</button>
    <button class="opcion" onclick="verificar(this, true)">c) Administrador de la base de datos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Responsable de marketing</button>
  </div>

  <div class="pregunta">
    <p><strong>21. Un sistema OLAP típico prioriza:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Latencia mínima en cada operación de escritura</button>
    <button class="opcion" onclick="verificar(this, true)">b) Análisis sobre grandes volúmenes de datos, aunque las consultas tarden más</button>
    <button class="opcion" onclick="verificar(this, false)">c) Bloquear el acceso concurrente</button>
    <button class="opcion" onclick="verificar(this, false)">d) Evitar cualquier tipo de agregación</button>
  </div>

  <div class="pregunta">
    <p><strong>22. Los sistemas DSS/EIS se asocian sobre todo al nivel:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Operacional</button>
    <button class="opcion" onclick="verificar(this, true)">b) Táctico y estratégico</button>
    <button class="opcion" onclick="verificar(this, false)">c) Físico</button>
    <button class="opcion" onclick="verificar(this, false)">d) Interno de la BD</button>
  </div>

  <div class="pregunta">
    <p><strong>23. Un motor monousuario embebido suele ser adecuado para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Grandes sistemas con cientos de usuarios concurrentes</button>
    <button class="opcion" onclick="verificar(this, true)">b) Aplicaciones de escritorio donde solo trabaja una persona</button>
    <button class="opcion" onclick="verificar(this, false)">c) Clústeres distribuidos entre varios CPD</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sistemas OLAP masivos</button>
  </div>

  <div class="pregunta">
    <p><strong>24. ¿Cuál de estos criterios NO es clave habitual al elegir un SGBD?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Funcionalidad y seguridad</button>
    <button class="opcion" onclick="verificar(this, false)">b) Rendimiento y escalabilidad</button>
    <button class="opcion" onclick="verificar(this, false)">c) Integración con otros sistemas</button>
    <button class="opcion" onclick="verificar(this, true)">d) Color del icono de la aplicación</button>
  </div>

  <div class="pregunta">
    <p><strong>25. La propiedad de transacciones que garantiza que los cambios confirmados sobreviven a un corte de luz es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Atomicidad</button>
    <button class="opcion" onclick="verificar(this, false)">b) Consistencia</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aislamiento</button>
    <button class="opcion" onclick="verificar(this, true)">d) Durabilidad</button>
  </div>

  <div class="pregunta">
    <p><strong>26. Una transacción que agrupa varias operaciones debe cumplir que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Se ejecuten siempre en orden alfabético</button>
    <button class="opcion" onclick="verificar(this, true)">b) Si algo falla, el sistema pueda deshacer el conjunto completo</button>
    <button class="opcion" onclick="verificar(this, false)">c) Nunca genere registros en los logs</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo pueda incluir operaciones de lectura</button>
  </div>

  <div class="pregunta">
    <p><strong>27. Establecer restricciones de seguridad, integridad y confidencialidad recae principalmente en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El navegador web</button>
    <button class="opcion" onclick="verificar(this, true)">b) El SGBD y el administrador de la BD</button>
    <button class="opcion" onclick="verificar(this, false)">c) El antivirus del servidor</button>
    <button class="opcion" onclick="verificar(this, false)">d) La aplicación cliente</button>
  </div>

  <div class="pregunta">
    <p><strong>28. Consultar qué columnas y restricciones tiene una tabla implica trabajar sobre:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DML</button>
    <button class="opcion" onclick="verificar(this, false)">b) DCL</button>
    <button class="opcion" onclick="verificar(this, true)">c) Diccionario de datos</button>
    <button class="opcion" onclick="verificar(this, false)">d) TCL</button>
  </div>

  <div class="pregunta">
    <p><strong>29. Controlar la redundancia significa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Impedir cualquier copia de seguridad</button>
    <button class="opcion" onclick="verificar(this, true)">b) Evitar duplicidades no planificadas que generan inconsistencias</button>
    <button class="opcion" onclick="verificar(this, false)">c) No tener índices en el sistema</button>
    <button class="opcion" onclick="verificar(this, false)">d) Trabajar siempre con ficheros de texto plano</button>
  </div>

  <div class="pregunta">
    <p><strong>30. La integridad de dominio se asegura principalmente mediante:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Tipos de datos, rangos y formatos adecuados por columna</button>
    <button class="opcion" onclick="verificar(this, false)">b) Copias de seguridad diarias</button>
    <button class="opcion" onclick="verificar(this, false)">c) Roles y permisos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Índices agrupados</button>
  </div>

  <div class="pregunta">
    <p><strong>31. La independencia *física* de los datos permite:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Cambiar el esquema interno sin cambiar el conceptual ni las vistas</button>
    <button class="opcion" onclick="verificar(this, false)">b) Modificar las vistas sin cambiar las aplicaciones</button>
    <button class="opcion" onclick="verificar(this, false)">c) Eliminar índices sin impacto en el rendimiento</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cambiar el modelo relacional por uno jerárquico automáticamente</button>
  </div>

  <div class="pregunta">
    <p><strong>32. Un error de integridad referencial suele indicar que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Falta un índice en la tabla</button>
    <button class="opcion" onclick="verificar(this, true)">b) Se intenta insertar o mantener una referencia a un registro inexistente en otra tabla</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se ha superado el tamaño máximo del fichero</button>
    <button class="opcion" onclick="verificar(this, false)">d) Hay demasiadas columnas en una tabla</button>
  </div>

  <div class="pregunta">
    <p><strong>33. Un *backup* es:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Una optimización de consultas complejas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una copia de seguridad destinada a poder recuperar la BD</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un índice especial para búsquedas</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un log recortado de errores</button>
  </div>

  <div class="pregunta">
    <p><strong>34. La “independencia de los datos” busca principalmente:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que el usuario final edite la estructura interna</button>
    <button class="opcion" onclick="verificar(this, true)">b) Separar cómo se almacenan físicamente de cómo se ven y usan</button>
    <button class="opcion" onclick="verificar(this, false)">c) Quitar al SGBD de la ecuación</button>
    <button class="opcion" onclick="verificar(this, false)">d) Forzar a que cada aplicación tenga su propio fichero</button>
  </div>

  <div class="pregunta">
    <p><strong>35. Insertar filas nuevas en una tabla pertenece a:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) DML</button>
    <button class="opcion" onclick="verificar(this, false)">b) DDL</button>
    <button class="opcion" onclick="verificar(this, false)">c) DCL</button>
    <button class="opcion" onclick="verificar(this, false)">d) TCL</button>
  </div>

  <div class="pregunta">
    <p><strong>36. Una información muy precisa pero nada oportuna suele:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Mantener intacto su valor informativo</button>
    <button class="opcion" onclick="verificar(this, true)">b) Perder valor para la toma de decisiones</button>
    <button class="opcion" onclick="verificar(this, false)">c) Mejorar la coherencia del sistema</button>
    <button class="opcion" onclick="verificar(this, false)">d) Aumentar la seguridad de acceso</button>
  </div>

  <div class="pregunta">
    <p><strong>37. El NIVEL CONCEPTUAL de la arquitectura de 3 niveles se centra en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Direcciones de bloques en disco</button>
    <button class="opcion" onclick="verificar(this, true)">b) Necesidades de información y relaciones entre datos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Campos que muestra cada formulario de la aplicación</button>
    <button class="opcion" onclick="verificar(this, false)">d) Permisos de usuarios del sistema operativo</button>
  </div>

  <div class="pregunta">
    <p><strong>38. El *servicio* del SGBD se refiere a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La interfaz gráfica del cliente</button>
    <button class="opcion" onclick="verificar(this, true)">b) El proceso en ejecución que atiende peticiones, normalmente por red</button>
    <button class="opcion" onclick="verificar(this, false)">c) El conjunto de tablas activas</button>
    <button class="opcion" onclick="verificar(this, false)">d) El departamento de soporte al usuario final</button>
  </div>

  <div class="pregunta">
    <p><strong>39. Que la BD sea “no redundante” significa que:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) No puede tener índices</button>
    <button class="opcion" onclick="verificar(this, false)">b) Nunca habrá copias de seguridad</button>
    <button class="opcion" onclick="verificar(this, true)">c) Se evita la duplicación innecesaria de la misma información</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo existe una tabla por base de datos</button>
  </div>

  <div class="pregunta">
    <p><strong>40. Confirmar de forma explícita los cambios agrupados en una transacción es tarea de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DML</button>
    <button class="opcion" onclick="verificar(this, false)">b) DCL</button>
    <button class="opcion" onclick="verificar(this, true)">c) TCL</button>
    <button class="opcion" onclick="verificar(this, false)">d) Diccionario de datos</button>
  </div>

  <div class="pregunta">
    <p><strong>41. Crear una tabla con sus columnas y tipos se considera una operación de:</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) DDL</button>
    <button class="opcion" onclick="verificar(this, false)">b) DML</button>
    <button class="opcion" onclick="verificar(this, false)">c) DCL</button>
    <button class="opcion" onclick="verificar(this, false)">d) TCL</button>
  </div>

  <div class="pregunta">
    <p><strong>42. La clave primaria de una tabla debe, como mínimo:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aceptar valores nulos</button>
    <button class="opcion" onclick="verificar(this, true)">b) No admitir duplicados y poder identificar cada fila</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cambiar en cada consulta</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ser de tipo texto obligatoriamente</button>
  </div>

  <div class="pregunta">
    <p><strong>43. En el nivel operacional de una organización se trabaja típicamente con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Información muy agregada para directivos</button>
    <button class="opcion" onclick="verificar(this, true)">b) Microdatos y tareas rutinarias</button>
    <button class="opcion" onclick="verificar(this, false)">c) Informes estratégicos a largo plazo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Exclusivamente indicadores financieros</button>
  </div>

  <div class="pregunta">
    <p><strong>44. En una arquitectura con *partición* de datos:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cada nodo tiene exactamente la misma información</button>
    <button class="opcion" onclick="verificar(this, true)">b) Cada nodo almacena un subconjunto distinto de los datos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Siempre hay un único punto de fallo</button>
    <button class="opcion" onclick="verificar(this, false)">d) No es posible escalar añadiendo nodos</button>
  </div>

  <div class="pregunta">
    <p><strong>45. Garantizar que varios usuarios trabajen sin “pisarse” cambios es una función relacionada con:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Integridad</button>
    <button class="opcion" onclick="verificar(this, true)">b) Acceso concurrente y control de transacciones</button>
    <button class="opcion" onclick="verificar(this, false)">c) Compleción</button>
    <button class="opcion" onclick="verificar(this, false)">d) Nivel externo</button>
  </div>

  <div class="pregunta">
    <p><strong>46. ¿Cuál de estos riesgos se relaciona más directamente con la pérdida de *seguridad*?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un informe con datos desactualizados</button>
    <button class="opcion" onclick="verificar(this, false)">b) Registros incompletos en un informe de ventas</button>
    <button class="opcion" onclick="verificar(this, true)">c) Accesos no autorizados a datos confidenciales</button>
    <button class="opcion" onclick="verificar(this, false)">d) Tablas sin clave primaria definida</button>
  </div>

  <div class="pregunta">
    <p><strong>47. Validar que una columna NOT NULL no reciba valores vacíos corresponde a:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Exclusivamente a la aplicación cliente</button>
    <button class="opcion" onclick="verificar(this, true)">b) Al SGBD mediante sus reglas de integridad</button>
    <button class="opcion" onclick="verificar(this, false)">c) Al sistema de archivos</button>
    <button class="opcion" onclick="verificar(this, false)">d) Al driver de red</button>
  </div>

  <div class="pregunta">
    <p><strong>48. ¿Qué componente se ejecuta típicamente como servicio escuchando en un puerto?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La base de datos como contenido</button>
    <button class="opcion" onclick="verificar(this, true)">b) El SGBD/motor</button>
    <button class="opcion" onclick="verificar(this, false)">c) El cliente SQL</button>
    <button class="opcion" onclick="verificar(this, false)">d) El diccionario de datos</button>
  </div>

  <div class="pregunta">
    <p><strong>49. Un ejemplo de tarea del nivel operacional sería:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Decidir la apertura de una nueva sucursal</button>
    <button class="opcion" onclick="verificar(this, false)">b) Diseñar el plan estratégico a cinco años</button>
    <button class="opcion" onclick="verificar(this, true)">c) Registrar la entrada diaria de mercancía en almacén</button>
    <button class="opcion" onclick="verificar(this, false)">d) Definir la política de backups corporativos</button>
  </div>

  <div class="pregunta">
    <p><strong>50. Un *índice* en una tabla sirve sobre todo para:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reducir el tamaño de la BD</button>
    <button class="opcion" onclick="verificar(this, true)">b) Acelerar búsquedas y ordenaciones a costa de algo de espacio</button>
    <button class="opcion" onclick="verificar(this, false)">c) Almacenar copias de los logs</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cifrar la información sensible</button>
  </div>

  <div class="pregunta">
    <p><strong>51. Definir el esquema conceptual es función típica de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Usuario final</button>
    <button class="opcion" onclick="verificar(this, true)">b) Administrador de la BD</button>
    <button class="opcion" onclick="verificar(this, false)">c) Sistema operativo</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cliente gráfico</button>
  </div>

  <div class="pregunta">
    <p><strong>52. En un sistema distribuido con *replicación*:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cada nodo guarda una porción distinta de los datos</button>
    <button class="opcion" onclick="verificar(this, true)">b) Todos los nodos contienen copias sincronizadas de las mismas tablas</button>
    <button class="opcion" onclick="verificar(this, false)">c) No existe copia redundante de la información</button>
    <button class="opcion" onclick="verificar(this, false)">d) No se permite el acceso concurrente</button>
  </div>

  <div class="pregunta">
    <p><strong>53. Un motor documental NoSQL se caracteriza típicamente por:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Requerir siempre esquema fijo tipo tablas</button>
    <button class="opcion" onclick="verificar(this, true)">b) Guardar documentos semiestructurados</button>
    <button class="opcion" onclick="verificar(this, false)">c) No permitir consultas</button>
    <button class="opcion" onclick="verificar(this, false)">d) No soportar escalabilidad horizontal</button>
  </div>

  <div class="pregunta">
    <p><strong>54. Mostrar en pantalla el resultado de una consulta es función típica de:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) BD</button>
    <button class="opcion" onclick="verificar(this, false)">b) SGBD</button>
    <button class="opcion" onclick="verificar(this, true)">c) Cliente</button>
    <button class="opcion" onclick="verificar(this, false)">d) Diccionario de datos</button>
  </div>

  <div class="pregunta">
    <p><strong>55. El NIVEL EXTERNO representa:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El conjunto de backups históricos</button>
    <button class="opcion" onclick="verificar(this, false)">b) La visión del administrador sobre el hardware</button>
    <button class="opcion" onclick="verificar(this, true)">c) Vistas específicas de la BD adaptadas a usuarios o aplicaciones</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sólo la representación gráfica de los datos</button>
  </div>

  <div class="pregunta">
    <p><strong>56. Cuando varias personas actualizan a la vez la misma fila y el sistema usa bloqueos para coordinarles, está actuando sobre:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Seguridad</button>
    <button class="opcion" onclick="verificar(this, true)">b) Concurrencia y aislamiento</button>
    <button class="opcion" onclick="verificar(this, false)">c) Significado</button>
    <button class="opcion" onclick="verificar(this, false)">d) Compleción</button>
  </div>

  <div class="pregunta">
    <p><strong>57. Un SGBD relacional organiza los datos principalmente en:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Árboles de ficheros</button>
    <button class="opcion" onclick="verificar(this, true)">b) Tablas y relaciones bien definidas</button>
    <button class="opcion" onclick="verificar(this, false)">c) Documentos sin estructura</button>
    <button class="opcion" onclick="verificar(this, false)">d) Arrays de bytes sin esquema</button>
  </div>

  <div class="pregunta">
    <p><strong>58. El principio de *mínimos privilegios* persigue:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reducir el tamaño de la BD</button>
    <button class="opcion" onclick="verificar(this, true)">b) Dar a cada usuario solo los permisos necesarios</button>
    <button class="opcion" onclick="verificar(this, false)">c) Aumentar el número de roles en el sistema</button>
    <button class="opcion" onclick="verificar(this, false)">d) Forzar a todos a ser administradores</button>
  </div>

  <div class="pregunta">
    <p><strong>59. Una base de datos se caracteriza, entre otras cosas, por ser:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un conjunto aleatorio de archivos de texto</button>
    <button class="opcion" onclick="verificar(this, true)">b) Una colección organizada y relacionada de datos</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un programa que ejecuta consultas SQL</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un único fichero plano con muchos campos</button>
  </div>

  <div class="pregunta">
    <p><strong>60. El SGBD se sitúa entre:</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La red y el sistema operativo</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los usuarios/aplicaciones y los datos almacenados</button>
    <button class="opcion" onclick="verificar(this, false)">c) El hardware y la red eléctrica</button>
    <button class="opcion" onclick="verificar(this, false)">d) El navegador y el sistema de archivos del cliente</button>
  </div>

  <div class="pregunta">
    <p><strong>61. ¿Qué categoría del lenguaje SQL se utiliza para definir y modificar la estructura de la base de datos (tablas, columnas, claves)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DML (Data Manipulation Language).</button>
    <button class="opcion" onclick="verificar(this, false)">b) DCL (Data Control Language).</button>
    <button class="opcion" onclick="verificar(this, true)">c) DDL (Data Definition Language).</button>
    <button class="opcion" onclick="verificar(this, false)">d) TCL (Transaction Control Language).</button>
  </div>

  <div class="pregunta">
    <p><strong>62. ¿Cuál de las siguientes instrucciones es un ejemplo de DML?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) CREATE TABLE.</button>
    <button class="opcion" onclick="verificar(this, false)">b) ALTER TABLE.</button>
    <button class="opcion" onclick="verificar(this, true)">c) UPDATE.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DROP INDEX.</button>
  </div>

  <div class="pregunta">
    <p><strong>63. ¿Qué es el "Diccionario de Datos" en un SGBD?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un libro de texto para aprender SQL.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un conjunto de metadatos que describen la estructura, relaciones y restricciones de la base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una tabla donde se guardan las contraseñas de los usuarios en texto plano.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El manual de instalación del servidor.</button>
  </div>

  <div class="pregunta">
    <p><strong>64. ¿Qué tipo de regla de integridad asegura que un campo no pueda quedar vacío?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Integridad Referencial.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Restricción UNIQUE.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Restricción NOT NULL.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Clave Primaria.</button>
  </div>

  <div class="pregunta">
    <p><strong>65. ¿Qué garantiza la "Integridad Referencial"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que todos los números sean enteros.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que los valores de una clave ajena (FK) coincidan con los de la clave primaria (PK) de la tabla relacionada.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que la base de datos sea accesible desde Internet.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que no existan dos registros iguales en la misma tabla.</button>
  </div>

  <div class="pregunta">
    <p><strong>66. ¿Qué objeto de la base de datos permite guardar una consulta compleja para usarla como si fuera una tabla virtual?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Índice.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Secuencia.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Vista (View).</button>
    <button class="opcion" onclick="verificar(this, false)">d) Disparador (Trigger).</button>
  </div>

  <div class="pregunta">
    <p><strong>67. ¿Cuál es la función principal de un "Índice" en una base de datos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ocupar menos espacio en el disco duro.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Acelerar la velocidad de las consultas de búsqueda.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Impedir que se borren datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Generar números automáticos para las facturas.</button>
  </div>

  <div class="pregunta">
    <p><strong>68. ¿Qué objeto se utiliza para generar automáticamente valores numéricos únicos, como números de pedido?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Vista.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Secuencia.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Metadatos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DDL.</button>
  </div>

  <div class="pregunta">
    <p><strong>69. En el contexto de transacciones, ¿qué significa la propiedad de "Atomicidad"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que los datos se guardan en átomos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que la transacción se realiza por completo o no se realiza nada.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que varios usuarios pueden escribir a la vez.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que los datos son visibles antes de terminar el proceso.</button>
  </div>

  <div class="pregunta">
    <p><strong>70. ¿Qué comando SQL se utiliza para confirmar y guardar permanentemente todos los cambios de una transacción?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) ROLLBACK.</button>
    <button class="opcion" onclick="verificar(this, false)">b) SAVEPOINT.</button>
    <button class="opcion" onclick="verificar(this, true)">c) COMMIT.</button>
    <button class="opcion" onclick="verificar(this, false)">d) END.</button>
  </div>

  <div class="pregunta">
    <p><strong>71. ¿Para qué sirve el comando ROLLBACK?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Para borrar la base de datos completa.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Para deshacer los cambios de una transacción que no ha finalizado correctamente.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Para hacer una copia de seguridad en la nube.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Para reiniciar el servidor.</button>
  </div>

  <div class="pregunta">
    <p><strong>72. ¿Qué propiedad de las transacciones asegura que los datos sean válidos y respeten todas las reglas de integridad al finalizar?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Aislamiento.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Durabilidad.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Consistencia.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Atomicidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>73. ¿Cuál es la unidad básica de almacenamiento de datos en una base de datos relacional?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La Vista.</button>
    <button class="opcion" onclick="verificar(this, false)">b) El Índice.</button>
    <button class="opcion" onclick="verificar(this, true)">c) La Tabla.</button>
    <button class="opcion" onclick="verificar(this, false)">d) El Log.</button>
  </div>

  <div class="pregunta">
    <p><strong>74. ¿Qué tipo de carga se caracteriza por procesar miles de transacciones pequeñas y rápidas en tiempo real (ej. un cajero automático)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) OLAP (Online Analytical Processing).</button>
    <button class="opcion" onclick="verificar(this, true)">b) OLTP (Online Transaction Processing).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Data Warehouse.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Carga en frío.</button>
  </div>

  <div class="pregunta">
    <p><strong>75. ¿Cuál es el objetivo principal de los sistemas OLAP?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Realizar ventas rápidas en una web.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Análisis de grandes volúmenes de datos históricos para la toma de decisiones.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Registrar el inicio de sesión de los usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Formatear el disco duro del servidor.</button>
  </div>

  <div class="pregunta">
    <p><strong>76. ¿Qué técnica se utiliza en OLAP para pre-calcular resultados de consultas lentas y acelerar el análisis?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Vistas materializadas.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Índices primarios.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Transacciones atómicas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Claves ajenas.</button>
  </div>

  <div class="pregunta">
    <p><strong>77. ¿Qué arquitectura de base de datos divide los datos entre varios nodos para mejorar el rendimiento con grandes volúmenes?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Centralizada.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Replicada.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Particionada.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Virtualizada.</button>
  </div>

  <div class="pregunta">
    <p><strong>78. ¿Qué caracteriza a una arquitectura de base de datos "Replicada"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Los datos se guardan en un único servidor central.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Varios nodos mantienen copias sincronizadas de los mismos datos para mejorar la disponibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los datos se borran cada vez que se leen.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Solo permite consultas de lectura, nunca de escritura.</button>
  </div>

  <div class="pregunta">
    <p><strong>79. ¿Cuál es el propósito del comando ALTER TABLE?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Insertar un nuevo registro.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Modificar la estructura de una tabla ya existente (añadir columnas, cambiar tipos, etc.).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Consultar los datos de una tabla.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Eliminar permanentemente una tabla.</button>
  </div>

  <div class="pregunta">
    <p><strong>80. ¿Qué motor de base de datos optimizado se menciona como ejemplo para acelerar el análisis en arquitecturas OLAP?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Motores orientados a filas.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Motores optimizados por columnas (ej. BigQuery, ClickHouse).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Motores de búsqueda de texto plano.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Sistemas de archivos FAT32.</button>
  </div>

  <div class="pregunta">
    <p><strong>81. ¿Qué tres pilares forman la "Tríada CIA" en la seguridad de bases de datos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Control, Informática y Almacenamiento.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Confidencialidad, Integridad y Disponibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Conectividad, Inteligencia y Autenticación.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Cifrado, Interconexión y Auditoría.</button>
  </div>

  <div class="pregunta">
    <p><strong>82. ¿Cuál de los pilares de la seguridad garantiza que solo las personas autorizadas puedan ver los datos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Disponibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Integridad.</button>
    <button class="opcion" onclick="verificar(this, true)">c) Confidencialidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Escalabilidad.</button>
  </div>

  <div class="pregunta">
    <p><strong>83. ¿Qué pilar de la seguridad se ve afectado si un hacker modifica las coordenadas de aterrizaje de un cohete sin permiso?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Integridad.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Disponibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Confidencialidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Rendimiento.</button>
  </div>

  <div class="pregunta">
    <p><strong>84. ¿Qué concepto de seguridad se define como "la suma de todos los puntos donde un atacante puede intentar entrar o extraer datos"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Perímetro de red.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Superficie de ataque.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Defensa en profundidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Triángulo de confianza.</button>
  </div>

  <div class="pregunta">
    <p><strong>85. ¿Qué principio de seguridad dicta que "un usuario debe tener solo los permisos mínimos necesarios para realizar su trabajo"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Principio de Confidencialidad total.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Principio de Mínimo Privilegio.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Principio de Disponibilidad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Principio de Root único.</button>
  </div>

  <div class="pregunta">
    <p><strong>86. ¿Por qué es peligroso utilizar la cuenta de "root" o "superuser" para las tareas diarias de una aplicación?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Porque la cuenta root es más lenta que las demás.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Porque si la cuenta es comprometida, el atacante tiene control total sobre todo el servidor de base de datos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Porque root no puede realizar consultas SELECT.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Porque root solo funciona en servidores locales.</button>
  </div>

  <div class="pregunta">
    <p><strong>87. ¿Qué es la "Defensa en Profundidad" en el contexto de un SGBD?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Poner una contraseña muy larga.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Implementar múltiples capas de seguridad (red, sistema operativo, base de datos) para que, si una falla, las otras protejan el dato.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Guardar los servidores en el sótano del edificio.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Hacer copias de seguridad cada hora.</button>
  </div>

  <div class="pregunta">
    <p><strong>88. ¿Qué significan las siglas RBAC?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Remote Backup Access Control.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Role-Based Access Control (Control de Acceso Basado en Roles).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Relational Binary Access Code.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Root Backup and Control.</button>
  </div>

  <div class="pregunta">
    <p><strong>89. En el modelo RBAC, ¿a qué se le asignan los permisos de acceso (SELECT, INSERT, etc.)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Directamente a cada persona por su nombre.</button>
    <button class="opcion" onclick="verificar(this, true)">b) A los Roles (cargos), que luego se asignan a los usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Únicamente al administrador del sistema.</button>
    <button class="opcion" onclick="verificar(this, false)">d) A las direcciones IP de los ordenadores.</button>
  </div>

  <div class="pregunta">
    <p><strong>90. ¿Cuál es una ventaja principal de utilizar Roles en lugar de permisos individuales?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La base de datos ocupa menos espacio.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Facilita la administración; si un empleado cambia de puesto, solo hay que cambiarle el rol en lugar de reasignar cientos de permisos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Los roles eliminan la necesidad de usar contraseñas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Los roles solo se pueden usar en bases de datos de la NASA.</button>
  </div>

  <div class="pregunta">
    <p><strong>91. ¿Qué instrucción SQL de la categoría DCL se utiliza para dar un permiso o un rol a un usuario?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) GIVE.</button>
    <button class="opcion" onclick="verificar(this, false)">b) ALLOW.</button>
    <button class="opcion" onclick="verificar(this, true)">c) GRANT.</button>
    <button class="opcion" onclick="verificar(this, false)">d) PERMIT.</button>
  </div>

  <div class="pregunta">
    <p><strong>92. ¿Qué instrucción SQL se utiliza para quitar un permiso previamente otorgado?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DELETE.</button>
    <button class="opcion" onclick="verificar(this, true)">b) REVOKE.</button>
    <button class="opcion" onclick="verificar(this, false)">c) REMOVE.</button>
    <button class="opcion" onclick="verificar(this, false)">d) DENY.</button>
  </div>

  <div class="pregunta">
    <p><strong>93. Según el documento, ¿qué es la "Seguridad desde el Diseño" (DDL)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Usar colores bonitos en la interfaz.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Aplicar restricciones (como NOT NULL o Check) a nivel de tabla para que la estructura misma impida datos erróneos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Crear tablas solo para los administradores.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No usar claves primarias.</button>
  </div>

  <div class="pregunta">
    <p><strong>94. ¿Qué restricción DDL impide que se introduzcan valores negativos en una columna de "Edad"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) PRIMARY KEY.</button>
    <button class="opcion" onclick="verificar(this, false)">b) DEFAULT.</button>
    <button class="opcion" onclick="verificar(this, true)">c) CHECK.</button>
    <button class="opcion" onclick="verificar(this, false)">d) UNIQUE.</button>
  </div>

  <div class="pregunta">
    <p><strong>95. ¿Cómo ayuda una restricción UNIQUE a la seguridad/integridad de los datos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Cifra el contenido de la columna.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Evita la duplicidad de registros críticos, como el DNI o el correo electrónico.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Permite que cualquier usuario vea los datos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Borra los datos antiguos automáticamente.</button>
  </div>

  <div class="pregunta">
    <p><strong>96. En la gestión de usuarios, ¿qué significa la restricción por dirección IP (ej: 'usuario'@'192.168.1.10')?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que el usuario puede conectarse desde cualquier parte del mundo.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que el acceso solo se permite si el usuario se conecta desde esa máquina específica.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que el usuario no necesita contraseña si está en esa IP.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que la base de datos es pública.</button>
  </div>

  <div class="pregunta">
    <p><strong>97. En el ejercicio práctico del documento, ¿qué paso es crítico después de asignar un rol a un usuario para que este pueda usar sus permisos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reiniciar el servidor de base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Activar el rol (SET ROLE o configuración de rol por defecto).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cambiar la contraseña del usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Borrar la tabla root.</button>
  </div>

  <div class="pregunta">
    <p><strong>98. Si un usuario tiene asignado el rol "r_patrullero", pero inicia sesión y el sistema le dice que no tiene permisos, ¿cuál es la causa más probable según el texto?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que el usuario ha olvidado su nombre.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que el rol no está activo automáticamente al iniciar sesión (entró "sin su placa").</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que el rol ha caducado.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que la base de datos está llena.</button>
  </div>

  <div class="pregunta">
    <p><strong>99. ¿Cuál es la "superficie de ataque" de un usuario que puede conectarse desde cualquier IP (%) comparado con uno limitado a una IP local?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Es menor, porque es más flexible.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Es mayor, porque permite intentos de conexión desde cualquier lugar de Internet.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Es igual en ambos casos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) No tiene relación con la seguridad.</button>
  </div>

  <div class="pregunta">
    <p><strong>100. ¿A qué se refiere el documento con "gestión de privilegios a nivel de columna"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) A que el usuario solo puede ver ciertas tablas.</button>
    <button class="opcion" onclick="verificar(this, true)">b) A la capacidad de permitir que un usuario vea una tabla pero solo algunas de sus columnas (ocultando datos sensibles).</button>
    <button class="opcion" onclick="verificar(this, false)">c) A que todas las columnas deben ser de tipo texto.</button>
    <button class="opcion" onclick="verificar(this, false)">d) A eliminar todas las columnas de una base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>101. ¿Cuál es la diferencia fundamental entre Autenticación y Autorización?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La autenticación da permisos y la autorización pide la contraseña.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La autenticación verifica quién eres y la autorización determina qué puedes hacer.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Son procesos idénticos que ocurren en la capa física.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La autorización siempre ocurre antes que la autenticación.</button>
  </div>

  <div class="pregunta">
    <p><strong>102. ¿Qué analogía utiliza el texto para explicar la Estrategia del Mínimo Privilegio?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La llave de un hotel.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La llave del aparcacoches (Valet Parking).</button>
    <button class="opcion" onclick="verificar(this, false)">c) El carnet de conducir.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Una caja fuerte de un banco.</button>
  </div>

  <div class="pregunta">
    <p><strong>103. ¿Por qué es una mala práctica de administración utilizar el comando GRANT ALL habitualmente?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Porque ralentiza la base de datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Porque viola el principio de mínimo privilegio, otorgando permisos peligrosos innecesarios.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Porque el comando GRANT ALL ha sido eliminado en SQL moderno.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Porque solo funciona para el usuario root.</button>
  </div>

  <div class="pregunta">
    <p><strong>104. En la sintaxis de la orden GRANT, ¿qué parte indica sobre qué objeto recae el permiso?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) La cláusula TO.</button>
    <button class="opcion" onclick="verificar(this, true)">b) La cláusula ON.</button>
    <button class="opcion" onclick="verificar(this, false)">c) La cláusula IDENTIFIED BY.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La cláusula WITH ADMIN.</button>
  </div>

  <div class="pregunta">
    <p><strong>105. ¿Cuál es el riesgo de seguridad de permitir que una aplicación web use el permiso DROP?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ninguno, es necesario para actualizar datos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un error o un ataque de inyección SQL podría borrar tablas enteras o la base de datos completa.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que el usuario no pueda cerrar la sesión.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que la base de datos se duplique por error.</button>
  </div>

  <div class="pregunta">
    <p><strong>106. ¿A qué se refiere el documento con "Jerarquía de Privilegios"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) A que el jefe siempre tiene más permisos que el empleado.</button>
    <button class="opcion" onclick="verificar(this, true)">b) A que los permisos se pueden asignar a nivel Global, de Base de Datos, de Tabla o de Columna.</button>
    <button class="opcion" onclick="verificar(this, false)">c) A que el servidor más caro tiene más permisos.</button>
    <button class="opcion" onclick="verificar(this, false)">d) A la velocidad de escritura de los discos duros.</button>
  </div>

  <div class="pregunta">
    <p><strong>107. ¿Qué tipo de permiso es GRANT SELECT ON *.* TO...?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Permiso a nivel de Tabla.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Permiso a nivel Global (toda la instancia).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Permiso a nivel de Columna.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Permiso de sistema operativo.</button>
  </div>

  <div class="pregunta">
    <p><strong>108. ¿Para qué sirve la "Sintaxis Quirúrgica" o permisos a nivel de columna?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Para que el usuario solo pueda usar el ratón y no el teclado.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Para permitir, por ejemplo, que un usuario actualice el 'teléfono' pero no el 'sueldo' en una misma tabla.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Para borrar columnas que no se usan.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Para cambiar el nombre de las columnas automáticamente.</button>
  </div>

  <div class="pregunta">
    <p><strong>109. ¿Qué sucede si intentas otorgar permisos de SELECT a nivel de columna en algunos motores como MySQL?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Funciona perfectamente igual que el UPDATE.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Es más complejo o requiere el uso de Vistas para ocultar las columnas que no se deben ver.</button>
    <button class="opcion" onclick="verificar(this, false)">c) El sistema se bloquea por seguridad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se borran los datos de la columna automáticamente.</button>
  </div>

  <div class="pregunta">
    <p><strong>110. ¿Cómo se denomina el acto de intentar realizar una operación sin tener permiso para verificar que la seguridad funciona?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Error de sistema.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Momento Hacker (Verificación de privilegios).</button>
    <button class="opcion" onclick="verificar(this, false)">c) Transacción fallida.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Auditoría de hardware.</button>
  </div>

  <div class="pregunta">
    <p><strong>111. ¿Cuál es la función del comando SHOW GRANTS FOR 'usuario'@'host';?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Dar nuevos permisos al usuario.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Consultar qué permisos tiene asignados un usuario específico.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cambiar la contraseña del usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Borrar al usuario del sistema.</button>
  </div>

  <div class="pregunta">
    <p><strong>112. En el documento, ¿qué comando se usa para quitar el permiso de borrar (DELETE) a un usuario?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) DELETE PERMISSION.</button>
    <button class="opcion" onclick="verificar(this, false)">b) REMOVE DELETE.</button>
    <button class="opcion" onclick="verificar(this, true)">c) REVOKE DELETE ON...</button>
    <button class="opcion" onclick="verificar(this, false)">d) DENY DELETE.</button>
  </div>

  <div class="pregunta">
    <p><strong>113. Si un usuario tiene el permiso UPDATE solo en la columna 'coordenadas', ¿qué pasa si intenta hacer un UPDATE en la columna 'id_mision'?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) El SGBD denegará la operación con un error de "command denied".</button>
    <button class="opcion" onclick="verificar(this, false)">b) El sistema lo permite pero lo guarda en un log.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Se actualiza la columna 'coordenadas' en su lugar.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se cierra la conexión del usuario.</button>
  </div>

  <div class="pregunta">
    <p><strong>114. ¿Qué es un "Escenario de Desastre" según el texto respecto a los permisos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Perder la conexión a Internet.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que un usuario junior ejecute un DELETE sin WHERE teniendo permisos globales.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que el disco duro se llene.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que el administrador olvide su contraseña.</button>
  </div>

  <div class="pregunta">
    <p><strong>115. Según la "Teoría de la Cebolla" de la seguridad, ¿cuál es la capa más interna y granular?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Infraestructura (Hosts).</button>
    <button class="opcion" onclick="verificar(this, false)">b) RBAC (Roles).</button>
    <button class="opcion" onclick="verificar(this, true)">c) Privilegios Granulares y Vistas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Copias de seguridad.</button>
  </div>

  <div class="pregunta">
    <p><strong>116. ¿Qué comando se utiliza para desbloquear una cuenta de usuario que ha sido bloqueada previamente?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) UNLOCK ACCOUNT.</button>
    <button class="opcion" onclick="verificar(this, true)">b) ALTER USER ... ACCOUNT UNLOCK.</button>
    <button class="opcion" onclick="verificar(this, false)">c) GRANT ACCESS.</button>
    <button class="opcion" onclick="verificar(this, false)">d) OPEN USER.</button>
  </div>

  <div class="pregunta">
    <p><strong>117. ¿Qué comando asegura que un rol se active automáticamente cuando el usuario inicia sesión?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) ACTIVATE ROLE.</button>
    <button class="opcion" onclick="verificar(this, true)">b) SET DEFAULT ROLE.</button>
    <button class="opcion" onclick="verificar(this, false)">c) ENABLE ROLE ALWAYS.</button>
    <button class="opcion" onclick="verificar(this, false)">d) GRANT DEFAULT.</button>
  </div>

  <div class="pregunta">
    <p><strong>118. ¿Qué significa el host '%' en la creación de un usuario (ej: 'unidad_movil'@'%')?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que el usuario solo puede usar el 1% de la CPU.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que el usuario puede conectarse desde cualquier dirección IP.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que el usuario es un administrador.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que la contraseña es opcional.</button>
  </div>

  <div class="pregunta">
    <p><strong>119. ¿Cuál es el objetivo de usar la opción IDENTIFIED BY en un comando de gestión de usuarios?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Ponerle un nombre real al usuario.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Establecer o cambiar la contraseña del usuario.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Indicar el departamento al que pertenece.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Definir el tipo de datos que puede manejar.</button>
  </div>

  <div class="pregunta">
    <p><strong>120. ¿Qué se consigue al combinar un usuario limitado a una IP con un Rol específico?</strong></p>
    <button class="opcion" onclick="verificar(this, true)">a) Reducir drásticamente la superficie de ataque.</button>
    <button class="opcion" onclick="verificar(this, false)">b) Que la base de datos sea más rápida.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que no haga falta hacer copias de seguridad.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Que el usuario pueda usar cualquier base de datos del servidor.</button>
  </div>

  <div class="pregunta">
    <p><strong>121. ¿Cuál es el nombre del archivo de configuración principal en sistemas Linux para MySQL/MariaDB?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) config.sys</button>
    <button class="opcion" onclick="verificar(this, true)">b) my.cnf</button>
    <button class="opcion" onclick="verificar(this, false)">c) mysql.ini</button>
    <button class="opcion" onclick="verificar(this, false)">d) settings.conf</button>
  </div>

  <div class="pregunta">
    <p><strong>122. ¿Qué analogía utiliza el documento para explicar la configuración de un SGBD?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El motor de un coche de carreras que necesita puesta a punto.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Los ajustes de un videojuego o un móvil nuevo.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Una receta de cocina.</button>
    <button class="opcion" onclick="verificar(this, false)">d) La construcción de una casa.</button>
  </div>

  <div class="pregunta">
    <p><strong>123. ¿Por qué no es recomendable copiar un archivo de configuración de un servidor de Internet directamente a tu servidor local?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Porque el archivo puede tener virus.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Porque cada servidor tiene un hardware diferente (RAM, CPU) y una carga de trabajo distinta.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Porque los archivos de Internet están en inglés.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Porque el formato del archivo cambia cada día.</button>
  </div>

  <div class="pregunta">
    <p><strong>124. ¿Cuál es la "Regla de Oro" antes de modificar cualquier archivo de configuración?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Reiniciar el servidor.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Hacer una copia de seguridad (backup) del archivo original.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Cambiar la contraseña de root.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Borrar los logs antiguos.</button>
  </div>

  <div class="pregunta">
    <p><strong>125. ¿Qué sucede si cometes un error de sintaxis en el archivo my.cnf y reinicias el servicio?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) El servidor ignora el error y arranca normalmente.</button>
    <button class="opcion" onclick="verificar(this, true)">b) El motor de la base de datos no arrancará (Fallo de inicio).</button>
    <button class="opcion" onclick="verificar(this, false)">c) La base de datos se vuelve más lenta.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Se borran todas las tablas automáticamente.</button>
  </div>

  <div class="pregunta">
    <p><strong>126. ¿Qué variable controla cuánta memoria RAM reserva MySQL para cachear datos e índices de las tablas?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) max_connections</button>
    <button class="opcion" onclick="verificar(this, true)">b) innodb_buffer_pool_size</button>
    <button class="opcion" onclick="verificar(this, false)">c) tmp_table_size</button>
    <button class="opcion" onclick="verificar(this, false)">d) wait_timeout</button>
  </div>

  <div class="pregunta">
    <p><strong>127. ¿Qué porcentaje de la RAM total se recomienda asignar a innodb_buffer_pool_size en un servidor dedicado solo a base de datos?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) 10%</button>
    <button class="opcion" onclick="verificar(this, true)">b) 50% - 80%</button>
    <button class="opcion" onclick="verificar(this, false)">c) 100%</button>
    <button class="opcion" onclick="verificar(this, false)">d) 5%</button>
  </div>

  <div class="pregunta">
    <p><strong>128. ¿Para qué sirve la variable max_connections?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Para limitar la velocidad de descarga.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Para definir el número máximo de usuarios o aplicaciones que pueden estar conectados a la vez.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Para establecer el número de tablas permitidas.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Para limitar el tamaño de los archivos de log.</button>
  </div>

  <div class="pregunta">
    <p><strong>129. ¿Qué variable de seguridad impide que el servidor de base de datos escuche peticiones desde fuera de la máquina local (localhost)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) secure_file_priv</button>
    <button class="opcion" onclick="verificar(this, true)">b) bind-address = 127.0.0.1</button>
    <button class="opcion" onclick="verificar(this, false)">c) local_infile</button>
    <button class="opcion" onclick="verificar(this, false)">d) server_id</button>
  </div>

  <div class="pregunta">
    <p><strong>130. ¿Cuál es la función del "Slow Query Log" (Log de consultas lentas)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Borrar las consultas que tardan mucho.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Registrar las consultas SQL que superan un tiempo determinado para poder optimizarlas.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Acelerar el disco duro.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Contar cuántas personas entran en la base de datos.</button>
  </div>

  <div class="pregunta">
    <p><strong>131. Si quieres registrar absolutamente todas las acciones que ocurren en el servidor, ¿qué log debes activar?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Error Log.</button>
    <button class="opcion" onclick="verificar(this, true)">b) General Query Log.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Slow Query Log.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Binary Log.</button>
  </div>

  <div class="pregunta">
    <p><strong>132. ¿Qué variable define el tiempo (en segundos) a partir del cual una consulta se considera "lenta"?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) wait_timeout</button>
    <button class="opcion" onclick="verificar(this, true)">b) long_query_time</button>
    <button class="opcion" onclick="verificar(this, false)">c) innodb_log_file_size</button>
    <button class="opcion" onclick="verificar(this, false)">d) slow_launch_time</button>
  </div>

  <div class="pregunta">
    <p><strong>133. ¿Qué herramienta o comando se suele usar en Linux para reiniciar el servicio de base de datos tras un cambio de configuración?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) reboot now</button>
    <button class="opcion" onclick="verificar(this, true)">b) systemctl restart mysql</button>
    <button class="opcion" onclick="verificar(this, false)">c) fdisk -l</button>
    <button class="opcion" onclick="verificar(this, false)">d) chmod 777 my.cnf</button>
  </div>

  <div class="pregunta">
    <p><strong>134. ¿Qué es el "Binary Log" (binlog)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Un log que guarda solo ceros y unos.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Un registro de todos los cambios en los datos, fundamental para la replicación y recuperación ante desastres.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Un log que guarda los nombres de los usuarios.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Un archivo temporal que se borra al apagar el PC.</button>
  </div>

  <div class="pregunta">
    <p><strong>135. ¿Qué variable de configuración es crítica para identificar de forma única a un servidor en un entorno de replicación?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) character-set-server</button>
    <button class="opcion" onclick="verificar(this, true)">b) server_id</button>
    <button class="opcion" onclick="verificar(this, false)">c) port</button>
    <button class="opcion" onclick="verificar(this, false)">d) user</button>
  </div>

  <div class="pregunta">
    <p><strong>136. ¿Para qué sirve ajustar wait_timeout e interactive_timeout?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Para que el servidor nunca se apague.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Para cerrar conexiones inactivas y liberar recursos del servidor.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Para aumentar el tiempo de espera del usuario al escribir.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Para cambiar la zona horaria del sistema.</button>
  </div>

  <div class="pregunta">
    <p><strong>137. ¿Qué variable controla dónde puede el SGBD leer o escribir archivos externos (como un CSV)?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) local_infile</button>
    <button class="opcion" onclick="verificar(this, true)">b) secure_file_priv</button>
    <button class="opcion" onclick="verificar(this, false)">c) datadir</button>
    <button class="opcion" onclick="verificar(this, false)">d) log_error</button>
  </div>

  <div class="pregunta">
    <p><strong>138. ¿Cuál es el riesgo de tener un max_connections demasiado alto si no tenemos suficiente RAM?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Que la pantalla se vea borrosa.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Que el servidor sufra un error de "Out of Memory" y colapse al intentar atender a todos.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Que las contraseñas dejen de funcionar.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Ninguno, cuantas más conexiones mejor.</button>
  </div>

  <div class="pregunta">
    <p><strong>139. ¿Qué comando SQL permite ver el valor actual de una variable de configuración sin abrir el archivo físico?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) SELECT * FROM config;</button>
    <button class="opcion" onclick="verificar(this, true)">b) SHOW VARIABLES LIKE 'nombre_variable';</button>
    <button class="opcion" onclick="verificar(this, false)">c) DESCRIBE system;</button>
    <button class="opcion" onclick="verificar(this, false)">d) GET SETTINGS;</button>
  </div>

  <div class="pregunta">
    <p><strong>140. Según el documento, ¿cuál es el consejo final para un DBA sobre la configuración?</strong></p>
    <button class="opcion" onclick="verificar(this, false)">a) Tocar todas las variables a la vez para acabar rápido.</button>
    <button class="opcion" onclick="verificar(this, true)">b) Ser minimalista: tocar solo lo necesario y entender qué hace cada variable antes de cambiarla.</button>
    <button class="opcion" onclick="verificar(this, false)">c) Dejar siempre la configuración por defecto de fábrica.</button>
    <button class="opcion" onclick="verificar(this, false)">d) Usar siempre la configuración más alta posible para todo.</button>
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
