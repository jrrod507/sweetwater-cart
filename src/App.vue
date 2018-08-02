<template>
  <div id="app">
    <h1>Sweetwater</h1>
    <h6>Products</h6>
    <ul>
      <li v-for="product in products">
        <div class="product-container">
          <div><span>Name: </span>{{ product.productName }}</div>
          <div><span>Price: </span>{{ product.price }}</div>
        </div>
      </li>
    </ul>
    
  </div>
</template>

<script>
export default {

  computed: {
    products() {
      return this.$store.state.products;
    }
  },
  
  data () {
    return {
     
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.product-container {
  border: 1px solid black;
  width: 600px;
  margin-bottom: 20px;
}

.product-container span {
  font-weight: bold;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
