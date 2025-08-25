<script>
  import Interior from './Interior.svelte';
  export let nombre;
</script>

<Interior nombre="svelte" />

<h1 class="title">Hola {nombre}</h1>

<p class="texto">Bienvenido/a a mi proyecto Svelte</p>

<p class="texto">{new Date()}</p>

<style>
  .title {
    color: purple;
    font-size: 3rem;
    text-align: center;
  }

  .texto {
    color: black;
    font-size: 1.5rem;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
</style>

