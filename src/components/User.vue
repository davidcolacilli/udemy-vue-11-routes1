<template>
    <div>
        <h3>Datos del usuario: {{$route.params.id}}</h3>
        <pre>{{$route.params}}</pre>
    </div>
</template>
<script>
export default {
    name: 'User'
}
</script>