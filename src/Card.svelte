<script>
    import { onMount } from 'svelte'
    export let nombreCompleto;
  
    //$: firstName = nombreCompleto.split(" ").at(0);
    //$: lastName = nombreCompleto.split(" ").slice(1).join(" ") || '???';
  //Ojo con esto, que no se me olvide, en js no existe el metodo at() para los arrays y nos daría un error, asi que usamos []
    
  // $: {
    //   const names = nombreCompleto.split(' ');

    //   firstName = names[0] || '';
    //names[0]: names es un array que contiene los nombres divididos. names[0] accede al primer elemento del array, que sería el primer nombre.

// '': El operador lógico || se conoce como "or" (o). En esta expresión, si el primer nombre (names[0]) es un valor falsy (un valor que se considera falso en una evaluación booleana),
// entonces se asigna una cadena vacía ('') a firstName.

    //   lastName = names.slice(1).join(' ') || '???';
    //names.slice(1): names es un array que contiene los nombres divididos. slice(1) se utiliza para crear un nuevo array que contiene todos los elementos de names, excepto el primer elemento.
    //.join(' '): Después de obtener los apellidos, .join(' ') se utiliza para unir los elementos del array en una cadena, utilizando un espacio como separador. Esto significa que todos los apellidos se concatenarán en una sola cadena.
    //
    // }
    let name = "";
    let firstName = '';
    let lastName = '';

  onMount(() => {
    if (nombreCompleto) {
      const names = nombreCompleto.split(' ');
      firstName = names[0] || '';
      lastName = names.slice(1).join(' ') || '???';
    } else {
      fetch('https://random-data-api.com/api/v2/users')
        .then(response => response.json())
        .then(({ first_name, last_name }) => {
          firstName = first_name || '';
          lastName = last_name || '???';
        })
        .catch(error => {
          console.error('Error fetching data:', error);
        });
    }
  });

onMount(() => {
  fetch('https://random-data-api.com/api/v2/users')
    .then(response => response.json())
    .then(({first_name, last_name}) => name = `${first_name} ${last_name}`)
})

  </script>
  
  <p>nom: {firstName}</p>
  <p>cognoms: {lastName}</p>
  
  