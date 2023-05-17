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
  
  <p>nom: {firstName}</p>
  <p>cognoms: {lastName}</p>
  
  