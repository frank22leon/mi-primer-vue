<template>
  <table class="table">
    <thead>
      <tr>
        <th scope="col">#</th>
        <th scope="col">Nombre</th>
        <th scope="col">Apellido</th>
        <th scope="col">RUT</th>
        <th scope="col">Edad</th>
        <th scope="col">Fecha de Nacimiento</th>
      </tr>
    </thead>
    <tbody>
      <tr v-for="(persona, $index) of personas" :key="$index">
        <td>{{ $index }}</td>
        <td>{{ persona.nombre }}</td>
        <td>{{ persona.apellido }}</td>
        <td>{{ persona.rut }}</td>
        <td>{{ persona.edad }}</td>
        <td>{{ persona.fechaDeNacimiento }}</td>
      </tr>
    </tbody>
  </table>
</template>

<script>
export default {
  name: 'App',
  data: () => ({
    personas: [
      {
        nombre: 'Francisco',
        apellido: 'Leon',
        rut: '5.222.225-9',
        edad: 21,
        fechaDeNacimiento: '22-01-2000'
      },
      {
        nombre: 'Jose',
        apellido: 'Jimenez',
        rut: '4.555.555.8',
        edad: 21,
        fechaDeNacimiento: '28-01-2000'
      }
    ]
  })
}
</script>

<style></style>