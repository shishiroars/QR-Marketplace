<template>
  <div class="home">
    <h1>{{ msg }}</h1>
    <ul>
      <li v-on:click="goToProductsPage('product1')">Product 1</li>
      <li>Product 2</li>
      <li>Product 3</li>
      <li>Product 4</li>
      <li>Product 5</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data () {
    return {
      msg: 'QR Code App'
    }
  },
  methods: {
    goToProductsPage: function (message) {
      this.$router.push({ name: 'ProdctDetails', params: { productId: message } })
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }
  ul {
    list-style-type: none;
    padding: 0;
  }
  li {
    display: inline-block;
    margin: 0 10px;
  }
  a {
    color: #42b983;
  }
</style>
