<template>
  <section class="container">
  <div>

<Navbar> </Navbar>
<Products ></Products>
<Cart> </Cart>
<Description> </Description>

    </div>
  </section>
</template>

<script>

import Products from '~/components/Products.vue'
import Cart from '~/components/Cart.vue'
import Description from '~/components/Description.vue'
import Navbar from '~/components/Navbar.vue'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
Vue.use(BootstrapVue)

export default {
  components: {
    Products,
    Description,
    Cart,
    Navbar
  }
}
</script>

<style>

/* .container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
} */

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

</style>

