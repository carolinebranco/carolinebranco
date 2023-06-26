<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>Mini Delivery de Ervas</title>
</head>
<body>
  <div id="app">
    <!-- Seu código Vue.js aqui -->
  </div>

  <script src="https://cdn.jsdelivr.net/npm/vue@2.6.14/dist/vue.js"></script>
  <script>
    // Seu código Vue.js aqui
  </script>
</body>
</html>
<template>
  <div class="store">
    <h1>Bem-vindo à Nossa Loja</h1>
    <div class="product-list">
      <div v-for="product in products" :key="product.id" class="product">
        <img :src="product.image" :alt="product.name" />
        <h3>{{ product.name }}</h3>
        <p>{{ product.price }}</p>
        <button @click="addToCart(product)">Adicionar ao Carrinho</button>
      </div>
    </div>
    <div class="cart">
      <h2>Carrinho de Compras</h2>
      <ul>
        <li v-for="item in cartItems" :key="item.id">
          {{ item.name }} - {{ item.quantity }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        { id: 1, name: 'Produto 1', price: 10.99, image: 'product1.jpg' },
        { id: 2, name: 'Produto 2', price: 19.99, image: 'product2.jpg' },
        { id: 3, name: 'Produto 3', price: 7.99, image: 'product3.jpg' },
      ],
      cartItems: [],
    };
  },
  methods: {
    addToCart(product) {
      const item = this.cartItems.find((item) => item.id === product.id);
      if (item) {
        item.quantity++;
      } else {
        this.cartItems.push({ ...product, quantity: 1 });
      }
    },
  },
};
</script>

<style>
.store {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 20px;
}

.product-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 20px;
  margin-top: 20px;
}

.product {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 200px;
}

.product img {
  width: 150px;
  height: 150px;
  object-fit: cover;
}

.cart {
  margin-top: 40px;
}

.cart h2 {
  margin-bottom: 10px;
}
</style>
