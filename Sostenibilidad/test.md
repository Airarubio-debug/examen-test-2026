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
