<template>
  <div>
    <h1 class="title">Componentes Vue</h1>
    <Characters 
    v-for="(personaje, i) of personajes"
    :key="i"
    :nombre="personaje.nombre"
    :imagen="personaje.src"/>
  </div>
</template>

<script>
import Characters from "./components/Characters.vue";
export default {
  name: "App",
  components: {
    Characters,
  },
  data: () => ({
    personajes: [
      {
        nombre: "Rick Sanchez",
        src: "https://rickandmortyapi.com/api/character/avatar/1.jpeg",
      },
      {
        nombre: "Morty Smith",
        src: "https://rickandmortyapi.com/api/character/avatar/2.jpeg",
      },
      {
        nombre: "Summer Smith",
        src: "https://rickandmortyapi.com/api/character/avatar/3.jpeg",
      },
      {
        nombre: "Beth Smith",
        src: "https://rickandmortyapi.com/api/character/avatar/4.jpeg",
      },
      {
        nombre: "Jerry Smith",
        src: "https://rickandmortyapi.com/api/character/avatar/5.jpeg",
      },
    ],
  }),
};
</script>

<style>
body {
  background-image: url("../src/assets/img/background.png")
}
.title {
  color:rgb(137, 207, 32);
  font-family: 'Courier New', Courier, monospace;
}
</style>