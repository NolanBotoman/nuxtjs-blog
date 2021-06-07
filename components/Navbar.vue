<template>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container py-2 flex align-items-center">
            <nuxt-link class="navbar-brand h4" :to="'/'">NuxtJS Blog</nuxt-link>
            <ul class="navbar-nav flex align-items-center">
                <li class="nav-item">
                    <nuxt-link class="nav-link" :to="'/about'">About</nuxt-link>
                </li>
                <li class="nav-item">
                    <nuxt-link class="nav-link" :to="'/'">Articles</nuxt-link>
                </li>
            </ul>
        </div>
    </nav>
</template>