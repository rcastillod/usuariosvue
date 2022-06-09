<template>
  <div id="app">
    <h1 class="text-center mb-4">{{title}}</h1>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <table class="table">
              <thead>
                  <tr>
                      <th scope="col">#</th>
                      <th scope="col">Nombre</th>
                      <th scope="col">Apellido</th>
                      <th scope="col">RUN</th>
                      <th scope="col">Fecha de Nacimiento</th>
                      <th scope="col">Edad</th>
                  </tr>
              </thead>
              <tbody>
                  <tr v-for="(usuario, index) in usuarios" :key="index">
                      <th scope="row">{{index+1}}</th>
                      <td>{{usuario.nombre}}</td>
                      <td>{{usuario.apellido}}</td>
                      <td>{{usuario.run}}</td>
                      <td>{{usuario.fechanac}}</td>
                      <td>{{usuario.edad}}</td>
                  </tr>
              </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'App',
  data: function() {
    return {
      title: 'Tabla usando Vue CLI',
      usuarios: [
          {
              nombre: 'Brad',
              apellido: 'Gibson',
              run: '2604847-8',
              fechanac: '20-01-1993-07',
              edad: '26',
          },
          {
              nombre: 'Lumi',
              apellido: 'Salminen',
              run: '8178471-k',
              fechanac: '20-04-2005',
              edad: '17',
          },
          {
              nombre: 'Kilian',
              apellido: 'Taubert',
              run: '8604884-1',
              fechanac: '17-12-2009',
              edad: '13',
          },
          {
              nombre: 'Albert',
              apellido: 'Mortensen',
              run: '2529403-3	',
              fechanac: '03-05-1967',
              edad: '55',
          },
          {
              nombre: 'Mohamed',
              apellido: 'Morales',
              run: '17635122-5',
              fechanac: '29-12-1986',
              edad: '36',
          },
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
