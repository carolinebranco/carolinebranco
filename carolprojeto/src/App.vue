<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Item from './components/Item.vue'
import Footer from './components/Footer.vue'
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
    let target = "https://raw.githubusercontent.com/yurimarcon/link-services/main/src/Dados/Services.json";
    fetch(target)
      .then(res => res.json())
      .then(res => this.servicos = res)
      .catch(e => console.log(e))
  }
}
</script>

<template>
  <img alt="Profile" style="width:150px; border-radius:50%" src="https://avatars.githubusercontent.com/u/44410208?v=4" />
  
  <h1>Yuri Marcon</h1>
  
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
  color: #2c3e50;
  margin-top: 60px;
  margin-bottom: 100px;
}
html{
  background: url("https://cdn.pixabay.com/photo/2017/01/24/03/53/plant-2004483_960_720.jpg");
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