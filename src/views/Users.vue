<template>
    <div>
        <h1>Usuario</h1>
        <!-- <router-link :to="item" v-for="(item, index) of userNames" :key="index"> -->
        <router-link :to="{ name:'Users', params:{id:item}}" v-for="(item, index) of userNames" :key="index">
            <a>{{item}}</a>
        </router-link>
        <user/>
    </div>
</template>
<script>
import User from "@/components/User.vue"

export default {
    name: 'Users',
    components: {
        User
    },
    data() {
        return {
            userNames: ["Juan", "Pedro", "Carlos"]
        }
    }
}
</script>
<style scoped>
a {
    display: inline-block;
    margin: 1rem .5rem;
}
</style>