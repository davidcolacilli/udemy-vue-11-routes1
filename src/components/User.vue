<template>
    <div>
        <h2>Datos del usuario: {{$route.params.id}}</h2>
        <pre>{{$route.params}}</pre>
    </div>
</template>
<script>
export default {
    name: 'User'
}
</script>