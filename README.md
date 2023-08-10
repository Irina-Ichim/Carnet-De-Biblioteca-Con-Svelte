# Carnet de Biblioteca - Svelte

Este es un proyecto de ejemplo que utiliza Svelte para crear un "Carnet de Biblioteca" virtual. Permite mostrar el nombre completo de una persona y generar nombres aleatorios si no se proporciona uno.

## Características

- Muestra el nombre random de una persona en un diseño de "carnet de biblioteca".
- Si no se proporciona un nombre, obtiene nombres aleatorios de la API `random-data-api.com`.

## Instrucciones de Uso

1. Clona este repositorio en tu computadora:

   ```sh
   git clone https://github.com/Irina-Ichim/Carnet-De-Biblioteca-Con-Svelte.git
   ```

2. Navega a la carpeta del proyecto:

   ```sh
   cd tu-repositorio
   ```

3. Instala las dependencias utilizando npm:

   ```sh
   npm install
   ```

4. Ejecuta el servidor de desarrollo utilizando npm:

   ```sh
   npm run dev
   ```

5. Abre tu navegador web y visita la dirección [http://localhost:8080](http://localhost:8080).

## Descripción del Proyecto

Este proyecto utiliza Svelte, una biblioteca de JavaScript que se centra en la construcción de interfaces de usuario interactivas y reactivas. La aplicación consta de un componente de "Carnet de Biblioteca" que muestra el nombre random completo de una persona y genera nombres aleatorios utilizando la API `random-data-api.com` si no se proporciona un nombre. A continuación, se describen algunas partes clave del proyecto:

- La página principal utiliza estilos CSS para centrar el contenido y darle formato visual.
- El componente `Card.svelte` es un componente reutilizable que muestra el nombre completo en un formato de "carnet de biblioteca".
- La variable `nombreCompleto` se pasa al componente `Card` desde el componente principal.
- Se utiliza el hook `onMount` para realizar acciones una vez que el componente ha sido montado en el DOM.
- Si se proporciona un `nombreCompleto`, se divide en nombre y apellidos utilizando el método `.split` y se muestra en el componente.
- Si no se proporciona un `nombreCompleto`, se realiza una solicitud a la API `random-data-api.com` para obtener nombres aleatorios y se muestran en el componente.
- El componente principal también muestra los nombres separados y unidos utilizando las variables `firstName` y `lastName`.

## Capturas de Pantalla

A continuación, se muestra cómo se ve la aplicación:

![Captura de Pantalla](/src/lib/Captura%20de%20pantalla%20(124).png)

## ¡Diviértete explorando tu proyecto! 😊📚