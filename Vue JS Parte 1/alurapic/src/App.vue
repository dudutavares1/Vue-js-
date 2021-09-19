<template>
  <div class="corpo">
    <h1 class="centralizado">{{ titulo }}</h1>

    <ul class="lista-fotos">
      <li class="lista-fotos-itens" v-for="foto of fotos">
        <img :src="foto.url" :alt="foto.titulo" />
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: "Alurapic",

      fotos: {
        url: "https://www.doglife.com.br/site/assets/images/cao.png",
        titulo: "Golden",
      },
    };
  },
  created() {
    this.$http
      .get("http://localhost:3000/v1/fotos")
      .then((res) => res.json())
      .then((fotos) => (this.fotos = fotos));
  },
};
</script>

<style>
.corpo {
  font-family: Helvetica, sans-serif;
  widows: 96%;
  margin: 0 auto;

}

</style>
