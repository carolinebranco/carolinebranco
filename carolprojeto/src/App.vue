<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

</script>

<script>
// import Dados from './Dados/Services.json';
export default {
  data(){
    return{
      servicos: null
    }
  },
  mounted(){
    let target = "Design sem nome.png";
    fetch(target)
      .then(res => res.json())
      .then(res => this.servicos = res)
      .catch(e => console.log(e))
  }
}
</script>

<template>
  <img alt="Profile" style="width:150px; border-radius:50%" src="./assets/logo2.png" />
  <h1>carol</h1>
  
  <blockquote cite="Mahatma Gandhi">
    <p>
      "Seja a mudança que você quer ver no mundo"
      <small> - Mahatma Gandhi - </small>
    </p>
  </blockquote>
  
  <hr/>
  <div class="items">
    <Item 
    v-for="servico, index in servicos"
    :key="index"
    :item="servico"
    />

  </div>

  <Footer />
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #c3d3e4;
  margin-top: 60px;
  margin-bottom: 100px;
}
html{
  background: url("https://img.freepik.com/fotos-gratis/fundo-de-ficcao-cientifica-futurista-moderno_35913-2152.jpg?size=626&ext=jpg&ga=GA1.2.1685019074.1647624948");
  background-repeat: no-repeat;
  background-size: cover;
  min-height: 100%;
}
.items{
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  
}
</style>