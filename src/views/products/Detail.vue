<template>
    <div>
        <section>
            <h2><a href="#" @click="back" class="previous">&#8249;</a> {{name}}</h2>
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
    },
    methods: {
        back: function() {
            this.$router.go(-1);
        }
    }
}
</script>
<style scoped>
h2 {margin: 2rem 0;}
.previous {
    padding: 0 1rem;
    text-decoration: none;
}
</style>