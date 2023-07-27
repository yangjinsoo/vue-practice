<template>

  <div v-if="모달창열렸나==true" class="black-bg">
    <div class="white-bg">
      <h4>{{products[product_num].title}}</h4>
      <p>{{products[product_num].content}}</p>
      <button @click="모달창열렸나=false" class="modal-btn">닫기</button>
    </div>
  </div>

  <div class="menu">
    <a href="#">Home</a>
    <a href="#">Products</a>
    <a href="#">About</a>
  </div>
  <div v-for="(product, i) in products" :key="i">
    <img class="room-img" :src="product.image" alt="매물사진">
    <h4 id="product-name" @click="openModal(i)">{{product.title}}</h4>
    <p>{{product.price}} 원</p>
  </div>
  
</template>

<script>
import data_products from "./data_product.js";

export default {
  name: 'App',
  data() {
    return {
      product_num : 0,
      products : data_products,
      모달창열렸나 : false,
    }
  },
  methods: {
    openModal(i) {
      this.product_num = i;
      this.모달창열렸나 = true;
    }
  },
  components: {

  }
}
</script>

<style>
.body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.5);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
  border-radius: 8px;
  padding: 20px;
}

.room-img {
  width: 100%;
  margin-top: 40px;
}

.modal-btn {
  float: right;
  cursor: pointer;
  margin-bottom: 10px;
}

#product-name {
  cursor: pointer;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
