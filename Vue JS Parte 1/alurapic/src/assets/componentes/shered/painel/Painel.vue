
<template>
  <div class="corpo">
    <h1 class="centralizado">{{ titulo }}</h1>
    <ul class="lista-fotos">
      <li class="lista-fotos-item" v-for="foto in fotos">
        <meu-painel :titulo="foto.titulo">
          <img class="imagem-responsiva" :src="foto.url" :alt="foto.titulo" />
        </meu-painel>
      </li>
    </ul>
  </div>
</template>




<script>
export default {
  props: ["titulo"],
};





</script>


<style>
.painel {
  padding: 0 auto;
  border: solid 2px grey;
  display: inline-block;
  margin: 5px;
  box-shadow: 5px 5px 10px grey;
  width: 200px;
  height: 100%;
  vertical-align: top;
  text-align: center;
}

.painel .painel-titulo {
  text-align: center;
  border: solid 2px;
  background: lightblue;
  margin: 0 0 15px 0;
  padding: 10px;
  text-transform: uppercase;
}


*{
  box-shadow: 5px 5px 5px;
}
</style>
