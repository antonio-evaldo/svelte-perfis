<script lang="ts">
	import Titulo from './components/Titulo.svelte';

  let valorInput = 'antonio';

  function aoSubmeter() {
    console.log(valorInput);
  }
</script>

<div class="app">
	<header>
		<Titulo />

    <div class="busca-usuario">
      <form on:submit|preventDefault={aoSubmeter}>
        <input type="text" class="input" bind:value={valorInput}>

        <div class="botao-container">
          <button type="submit" class="botao">Buscar</button>
        </div>
      </form>
    </div>
	</header>
</div>

<style>
	.app {
    max-height: 100vh;
  }
 
  header {    
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .busca-usuario {
    position: relative;
    width: 70%;
  }
 
  .input {
    padding: 15px 25px;
    width: calc(100% - 8.75rem);
    font-size: 1rem;
    border-radius: 8px;
    border: 1px solid #2e80fa;
    box-shadow: 0px 17px 52px rgba(222, 231, 247, 0.4);
    outline: 0;
  }
 
  .input::placeholder {
    font-family: "Roboto";
    font-style: italic;
    font-weight: 300;
    font-size: 19.5px;
    line-height: 26px;
    color: #6e8cba;
  }
 
  .botao-container {
    position: absolute;
    width: 9.625rem;
    right: 0;
    top: 0;
    bottom: 0;
    display: flex;
  }
 
  .botao {
    padding: 15px 24px;
    border-radius: 8px;
    border: none;
    background: #2e80fa;
    line-height: 26px;
    color: #fff;
    font-size: 22px;
    cursor: pointer;
 
    transition: background-color 0.2s;
 
    display: flex;
    align-items: center;
    gap: 13px;
  }
 
  .botao:hover {
    background: #4590ff;
  }

</style>