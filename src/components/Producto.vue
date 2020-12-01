<template>
    <div class="card my-5">
        <div class="card-body">
            <h5 class="text-center card-title">{{ producto.titulo }}</h5>
            <img :src="producto.imagen" width="310" height="150">
            <p class="text-muted card-text">$ {{ Number(producto.precio).toFixed() }}</p>
            <button @click="agregarCarrito(producto)" class="btn btn-primary form-control" :disabled="estaEnCarrito">
                {{estaEnCarrito ? 'Agregado' : 'Agregar al carrito'}}
            </button>
        </div>
    </div>
</template>


<script>
export default {
    name: 'Producto',
    props: ['producto', 'estaEnCarrito'],
    methods:{
        agregarCarrito(producto){
            this.$emit('agregar-carrito', producto)
        }
    }
}
</script>


<style>

</style>