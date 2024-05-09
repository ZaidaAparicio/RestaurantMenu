<template>
    <div id="app">
        <div id="main-container">
          <!--  -->
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

