<template>
    <section class="container">
        <h2 class="my-4">About</h2>
        <h5>Blog about nothing special except some latin things, <nuxt-link class="d-inline" :to="'/'">check our articles</nuxt-link></h5>
    </section>
</template>
<script>
    export default {
        head: {
            title: 'About of blog',
            meta: [
                { charset: 'utf-8' },
                { name: 'viewport', content: 'width=device-width, initial-scale=1' },
                {
                hid: 'description',
                name: 'description',
                content: 'Learn about us on this page'
                }
            ],
            link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]
        }
    }
</script>
