<template>
    <div>
        <h2>Usuarios</h2>
        <!-- <router-link :to="item" v-for="(item, index) of userNames" :key="index"> -->
        <nav>
            <router-link :to="{ name:'Users', params:{id:item}}" v-for="(item, index) of userNames" :key="index">
                {{item}}
            </router-link>
        </nav>
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
nav {
    display: inline-block;
    background: #fafafa;
    border-radius: 3px;
    overflow: hidden;
}
a {
    display: inline-block;
    padding: 1rem 1.5rem;
}
a, a:hover {
    text-decoration: none;
}
.router-link-active {
    background: #f0f0f0;
}
</style>