<script>
  import { onMount } from 'svelte';
  import Card from './Card.svelte';

  let nombreCompleto;
  onMount(() => {

  })
</script>

<style>
  

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

<h1> Carnet de Biblioteca con IRINA</h1>

<div class="card">
  <h3>Card Component</h3>
  <Card nombreCompleto={nombreCompleto} />
</div>

