<template>
    <ul>
        <li  v-for="product in products" :key="product.id">
            <router-link :to="{
                name:'product', 
                params:product
            }" 
            class="btn btn-link">{{product.name}}</router-link>
        </li>
    </ul>
</template>
<script>
export default {
    name: 'Products',
    data() {
        return {
            products: [
                {
                    name: 'Taza',
                    id: 'asdf'
                },
                {
                    name: 'Aeronave',
                    id: '32462'
                }
            ]
        }
    }
}
</script>
<style scoped>
ul {
    margin: 3rem 0
}
li {
    margin: 1rem
}
</style>