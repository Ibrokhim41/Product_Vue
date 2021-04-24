<template>
  <div id="app">
    <div class="container">
      <Product />
    </div>
  </div>
</template>

<script>
import Product from './views/Product'

export default {
  name: 'App',
  components: {
    Product
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300;0,400;0,500;0,700;1,400&display=swap');
#app {
  font-family: 'Rubik', sans-serif;
}
.container {
  width: 1024px;
  margin: 0 auto;
}
</style>
