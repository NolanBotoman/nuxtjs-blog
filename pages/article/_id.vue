<template>
    <section class="container">
        <div class="card my-4">
            <img src="/" class="card-img-top" alt="">
            <div class="card-body">
                <h3 class="card-title">{{ title }}</h3>
                <p class="card-text">{{ body }}</p>
                <nuxt-link class="nav-link p-0" :to="'/'">Return back</nuxt-link>
            </div>
        </div>
    </section>
</template>
<script>
    import axios from 'axios'
    export default {
        validate ({ params }) {
            return !isNaN(+params.id)
        },
        async asyncData({params, error}){
            const {data} = await axios.get(`https://jsonplaceholder.typicode.com/posts/${+params.id}`)
            return data
        },
        head: {
            title: 'Articles of blog',
            meta: [
                { charset: 'utf-8' },
                { name: 'viewport', content: 'width=device-width, initial-scale=1' },
                {
                hid: 'description',
                name: 'description',
                content: 'Article of super blog'
                }
            ],
            link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]
        }
    }
</script>