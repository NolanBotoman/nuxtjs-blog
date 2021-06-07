<template>
    <section class="container">
        <h2 class="my-4">Articles</h2>
        <div>
            <ul class="list-unstyled d-grid g-wrapper gap-4">
                <li v-for="article in articles":key="article.id" class="item" >
                    <div class="card">
                      <img src="/" class="card-img-top" alt="">
                        <div class="card-body">
                            <h5 class="card-title">{{ article.title }}</h5>
                            <p class="card-text">{{ article.body | truncate(50) }}</p>
                            <nuxt-link class="nav-link p-0" :to="'/article/' + article.id">See this article</nuxt-link>
                        </div>
                    </div>
                </li>
            </ul>
        </div>
    </section>
</template>
<script>
    import axios from 'axios';
    export default {
        async asyncData () {
            const {data} = await axios.get('https://jsonplaceholder.typicode.com/posts');
            return {articles:data};
        },
        filters: {
            truncate(string, value) {
                return (string || '').substring(0, value) + '...';
            }
        },
        head: {
            title: 'Articles of my blog',
            meta: [
                { charset: 'utf-8' },
                { name: 'viewport', content: 'width=device-width, initial-scale=1' },
                {
                hid: 'description',
                name: 'description',
                content: 'Blog description best articles in da world'
                }
            ],
            link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]
        }
    }
</script>
<style>
    .g-wrapper {
        grid-template-columns: repeat(3, 1fr);
    }
</style>
