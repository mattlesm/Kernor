<template>
  <v-main>
    <div class="wrapper">
      <h2 class="titre">{{ title }}</h2>
    </div>
  </v-main>
</template>

<style>
  .wrapper {
    position:absolute;
    object-fit:cover;
    height:100%;
    width:100%;
    background: url('@/assets/home.jpg');
  }
  .titre {
    font-size:400%;
    text-align: center;
    margin-top: 20%;
  }
</style >

<script>
  export default {
    name: 'Maps',
    data() {
        return {
            title: "Bienvenue à Kernor",
            path: "'require('@/assets/home.jpg')'"
        }
    }
  };
</script>