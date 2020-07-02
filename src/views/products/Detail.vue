<template>
    <div>
        <section>
            <h2><a @click="back" class="previous">&#8249;</a> {{name}}</h2>
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
/* .previous {
    text-decoration: none;
    display: inline-block;
    padding: 8px 16px;
    background-color: #f1f1f1;
    border-radius: 50%;
}
.previous:hover {
  background-color: #ddd;
} */
</style>