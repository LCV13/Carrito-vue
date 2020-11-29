<template>
  <div id="app">

    <div class="row">
      <div class="col-md-7">
        <div class="row">
          <div class="col-md-6" v-for="prod in productos" :key="prod.id">
            <producto :producto="prod"></producto>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import productos from './productos.json'
import Producto from './components/Producto.vue'


export default {
  name: 'App',
  components: {
     Producto 
  }, 
  data(){
    return{
      productos
    }
  }
}
</script>

<style>

</style>
