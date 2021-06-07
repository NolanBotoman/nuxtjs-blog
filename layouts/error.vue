<template>
    <div class="container">
        <h2 class="my-4" v-if="error.statusCode === 404">Page not found</h2>
        <h2 class="my-4" v-else>An internal error occurred on our blog</h2>
        <h5><nuxt-link class="d-inline" :to="'/'">Try again</nuxt-link> or consider reporting this issue to us at blog@blog.com</h5>
    </div>
</template>

<script>
    export default {
        props: ['error'],
        layout: 'error'
    }
</script>
