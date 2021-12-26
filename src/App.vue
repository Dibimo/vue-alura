<template>
  <div>
    <h1>{{ nomeApp }}</h1>
    <ul>
      <li v-for="foto in fotos" :key="foto.titulo">
        <img :src="foto.url" :alt="foto.titulo" :key="foto.titulo">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return{
      nomeApp: "Alurapic",
      fotos:[
        {
          url: "https://www.petlove.com.br/dicas/wp-content/uploads/2021/08/Gato-filhote-7.jpg",
          titulo:"gatinho fofo"
        },
        {
          url: "https://i.pinimg.com/236x/45/24/de/4524de2715890053f73b997f80688118.jpg",
          titulo:"outro gatinho fofo"
        }
      ]
    }
  }
};
</script>

<style></style>
