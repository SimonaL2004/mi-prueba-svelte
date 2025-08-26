<script>
  import Interior from './Interior.svelte';
  export let nombre;
  let palabra;

  function alerta(e){
    const target = e.target;
    palabra = e.target.value;
  }
</script>


<Interior nombre="svelte" />

<h1 class="title">Hola {nombre}</h1>

<p class="texto">Bienvenido/a a mi proyecto Svelte</p>

<p class="texto">{new Date()}</p>

<p class="texto">¡Hola, {palabra}!</p>

<button  class = 'mi-boton' on:click={() => console.log("Me pulsaste")}> Haz click aqui </button>

<input type='text' placeholder="Saluda a ..."  
  class='palabra' on:keyup={alerta} />

<style>
  .title {
    color: purple;
    font-size: 3rem;
    text-align: center;
  }
  .palabra{
    padding: 0.5rem;
    font-size: 1rem;
    border: 2px solid palevioletred;
  }

  .texto {
    color: black;
    font-size: 1.5rem;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
    .mi-boton{
    background-color: plum;
    color: black;
    border: none;
    padding: 1rem 2rem;
    font-size: 1.2rem;
    border-radius: 8px;
    cursor: pointer;
    transition: background 0.3s;
    text-align: start;
  }

  .mi-boton:hover {
    background-color: purple;
  }
</style>

