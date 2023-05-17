<script>
  export let nombreCompleto;
  let firstName = '';
  let lastName = '';

  $: {
    const names = nombreCompleto.split(' ');
    firstName = names[0] || '';
    lastName = names.slice(1).join(' ') || '???';
  }
</script>

<style>
  .card {
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
  }
</style>

<div class="card">
  <h3>Card Component</h3>
  <p>nom: {firstName}</p>
  <p>cognoms: {lastName}</p>
</div>
