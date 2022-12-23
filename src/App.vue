<template>
  <div id="app">
    <HelloWorld/>
    <div class="body_section">
      <SideNav class="side_nav"/>
      <ListofProducts class="product_items" />
    </div>
 
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import ListofProducts from './components/ListofProducts.vue';
import SideNav from './components/SideNav.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    SideNav,
    ListofProducts,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.body_section {
  height: 100vh-80px;
  margin-top: 30px;
  display: flex;
  flex-direction: row;
  /* justify-content: space-evenly; */
}

.side_nav {
  width: 1630px;
  height: auto;
  position: absolute;
}


</style>
