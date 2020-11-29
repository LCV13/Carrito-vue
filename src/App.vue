<template>
  <div id="app">
    <div class="row">
      <div class="col-md-7">
        <div class="row">
          <div class="col-md-6">
            <producto/>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Producto from './components/Producto.vue'


export default {
  name: 'App',
  components: {
     Producto 
  }
}
</script>

<style>

</style>
