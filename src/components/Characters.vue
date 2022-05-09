<template>
  <div class="list-characters">
      <img :src="imagen">
      <p>{{ nombre }}</p>
  </div>
</template>

<script>
export default {
props: ["nombre", "imagen"]
}
</script>

<style>
.list-characters {
    display: flex;
    margin: 20px;
    align-items: center; 
    }

img {
    border-radius: 50%;
    width: 10rem;
}
p {
    color: rgb(137, 207, 32);
    font-family: 'Courier New', Courier, monospace;
    font-size: 20px;
    margin: 20px;
}
</style>