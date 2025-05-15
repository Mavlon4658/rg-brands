<script>
export default {
    name: "Header",
}
</script>

<template>
    <header class="header">
        <div class="container header-container">
            <router-link class="header-logo">
                <img :src="$getImage('logo.png')" alt="">
            </router-link>
            <ul class="header-navs">
                <li>
                    <router-link class="header-navs__link" to="/">Home</router-link>
                </li>
                <li>
                    <router-link class="header-navs__link" to="/about">About</router-link>
                </li>
            </ul>
        </div>
    </header>
</template>