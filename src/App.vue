<template>
  <div class="corpo">
    <h1 class="centralizado">{{ nomeApp }}</h1>
    <ul class="lista-fotos">
      <li class="lista-fotos-item" v-for="foto in fotos" :key="foto.titulo">
        <img :src="foto.url" :alt="foto.titulo" :key="foto.titulo">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return {
      nomeApp: "Alurapic",
      fotos:[]
    }
  },
  
  created(){
    this.$http.get("http://localhost:3000/v1/fotos")
      .then(res => res.json()) //resposta que veio do servidor converdita para json
      .then(fotos => this.fotos = fotos); //informação de fato que será utilizada pela aplicação
  }
};
</script>

<style>
  .corpo{
    font-family: Helvetica;
    width:96%;
    margin:0 auto;
  }

  .centralizado{
    text-align: center;
  }

  .lista-fotos{
    list-style: none;
  }

  .lista-fotos .lista-fotos-item{
    display: inline-block;
  }
</style>
