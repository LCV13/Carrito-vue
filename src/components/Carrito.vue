<template>
    <div>
        <ul class="list-group">
            <li class="list-group-item" v-for="item in items" :key="item.id">
                {{item.titulo}} - ${{item.precio}}
                 <button class="btn badge badge-danger float-right" @click="removerItem(item)">Eliminar</button>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Carrito',
    props: ['items'],
    methods:{
        removerItem(item){
            this.$emit('remover-item', item)
        }
    }
}
</script>