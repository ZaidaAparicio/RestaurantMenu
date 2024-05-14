<template>
    <div class="min-h-screen flex items-center justify-center with-background-image">
      <div class="max-w-4xl mx-auto py-8 px-4">
        <!-- El contenido del menú dentro de MyHome -->
        <MyHome></MyHome>
      </div>
    </div>
  </template>

<script>
    import MyHome from './components/MyHome.vue';

    export default {
        name: 'App',
        components: {
            MyHome,
        }
    }
</script>
  