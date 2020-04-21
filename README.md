# Asincronismo y pedidos HTTP - Buscador gatites

## Consignas

1. Hacer funcionar las tabs, para eso, al hacer click en una tab, debería:
  - sacarle la clase a `is-active` a todos los `li` de las tabs
  - agregarsela al `li` del tab que fue clickead (TIP: usar `parentElement` para acceder al `li`)
  - agregar la clase `is-hidden` a todos los elementos con clase `tab-section`
  - sacarle la clase `is-hidden` al elemento *cuyo id corresponda con la propiedad href del elemento clickeado*
  
2. Hacer funcionar la sección `Random`, para eso:
  - al cargar la página y al hacer click en el botón, debería cargar una nueva imagen de un gato
  - usar el siguiente endpoint: https://api.thecatapi.com/v1/images/search/
  - **EXTRA:** agregarle al botón la clase `is-loading` antes de hacer el pedido y sacársela cuando se obtiene la respuesta
  
3. Hacer la sección `Búsqueda de razas`, para eso:
  - al hacer click en el botón de búsqueda, obtener el `value` del input de búsqueda
  - con ese dato, hacer una consulta a https://api.thecatapi.com/v1/breeds/search?q=busqueda, reemplazando `busqueda` por el `value` del input
  - con la respuesta, actualizar la tabla para mostrar los nombres de las razas
  - **EXTRA:** agregarle al botón y al input la clase `is-loading` antes de hacer el pedido y sacársela cuando se obtiene la respuesta
  - **EXTRA:** hacer que funcione cuando se da enter al escribir la búsqueda  
  
4. Hacer funcionar la sección `Razas`, para eso
  - al cargar la página, cargar la lista de razas con el endpoint: https://api.thecatapi.com/v1/breeds
  - actualizar el select con los nombres de las razas, el option debería tener como value el id de la raza, por ejemplo
    ```html
    <option value="beng">Bengal</option>
    ```
  - Agregarle al primer `option` el atributo `selected`  
  - cuando se selecciona una raza, actualizar la información con imagen, descripción y temperamento
  - para reaccionar a la selección de una opción en un `select`, tenemos el evento `change`. El `value` de un `select` es el `value` del `option` seleccionado
  - para actualizar la info de una raza, usar el endpoint: https://api.thecatapi.com/v1/breeds/:id, donde `:id` es el id del value del select, por ejemplo https://api.thecatapi.com/v1/breeds/beng
  - la imagen la obtenemos de https://api.thecatapi.com/v1/images/search?breed_ids=raza_id, donde `raza_id` es el id de la raza
  - al cargar la página, actualizar la info de la raza con la primera raza de la consulta


Si necesitan modificar el HTML pueden hacerlo
