<template>
    <div>
        <section>
            <h2>{{name}}</h2>
            <pre>
                {{this.$route.params}}
            </pre>
        </section>
    </div>
</template>
<script>
export default {
    name: 'Product',
    data() {
        return {
            name: this.$route.params.name
        }
    }
}
</script>
<style scoped>
</style>