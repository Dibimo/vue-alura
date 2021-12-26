<template>
  <div>
    <h1>{{ nomeApp }}</h1>
    <img
      :src="foto.url"
      :alt="foto.titulo"
    />
  </div>
</template>

<script>
export default {
  data(){
    return{
      nomeApp: "Alurapic",
      foto:{
        url: "https://www.petlove.com.br/dicas/wp-content/uploads/2021/08/Gato-filhote-7.jpg",
        titulo:"gatinho fofo"
      }
    }
  }
};
</script>

<style></style>
