<template>
  <div>
    <Navbar/>
    <div class="container mt-6">
      <div class="columns">
        <div class="column is-12 column--align-center">
          <router-view></router-view>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Navbar from './components/core/Navbar'
import CartList from "./components/cart/Cart_List";
import CartListItem from "./components/cart/Cart_List_Item";

export default {
  name: 'App',
  components: {
    Navbar,
    CartList,
    CartListItem
  }
}
</script>
<style>
html,
body {
  height: 100%;
  background: #f2f6fa;
}
</style>