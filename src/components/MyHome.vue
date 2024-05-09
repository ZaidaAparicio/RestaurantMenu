<template>
    <div id="my-home">
        <h1>Componente Nuevo</h1>
        <h3>{{ menu }}</h3>
    </div>
</template> 

<script>
    export default {
        name: 'MyHome',
        data() {
            return {
                menu: 'prueba 1'
            }
        }
    }
</script>
