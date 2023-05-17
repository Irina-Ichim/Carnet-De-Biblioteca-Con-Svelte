<script>
  import { onMount } from 'svelte';
  import Card from './Card.svelte';

  let nombreCompleto;
  onMount(() => {

  })
</script>

<style>
  /*body {
    background-color: black;
    color: white;
    padding: 20px;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
  }*/

  h1 {
    font-size: 32px;
    text-align: center;
    margin-bottom: 20px;
    color: #FF6B6B;
  }

  .card {
    border: 1px solid white;
    padding: 20px;
    background: linear-gradient(to bottom, #FF6B6B, #FF8E53);
    color: white;
  }
</style>

<h1>IRINA</h1>

<div class="card">
  <h3>Card Component</h3>
  <Card nombreCompleto={nombreCompleto} />
</div>

