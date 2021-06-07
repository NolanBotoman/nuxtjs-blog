<template>
    <main>
        <Navbar />
        <nuxt />
    </main>
</template>
<script>
    import Navbar from '~/components/Navbar.vue'
    export default {
        components:{
            Navbar
        }
    }
</script>
<style>
    html {
        overflow: -moz-scrollbars-vertical; 
        overflow-y: scroll;
    }
</style>