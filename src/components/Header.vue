<script>
export default {
    name: "Header",
    data () {
        return {
            navs: [
                {name: 'О компании', to: '/'},
                {name: 'Наши бренды', to: '/'},
                {name: 'медиа', to: '/'},
                {name: 'карьера', to: '/'},
                {name: 'Контакты', to: '/'},
            ],
            navsActive: 0,
            menuOpen: false,
        }
    },
    mounted () {
        let header = this.$refs.header;
        window.addEventListener('scroll', () => {
            if (scrollY > 100) {
                header.classList.add('active');
            } else {
                header.classList.remove('active');
            }
        })
    }
}
</script>

<template>
    <header class="header" ref="header">
        <div class="container header-container">
            <router-link class="header-logo" to="/">
                <img :src="$getImage('logo-light.svg')" alt="">
                <img :src="$getImage('logo.svg')" alt="">
            </router-link>
            <ul class="header-navs">
                <li v-for="(nav, i) in navs" :key="i">
                    <router-link 
                        class="header-navs__link " 
                        :class="{
                            'active': navsActive == i
                        }"
                        :to="nav.to"
                    >{{ nav.name }}</router-link>
                </li>
            </ul>
            <div class="header-right">
                <button>
                    <svg width="21" height="20" viewBox="0 0 21 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M8.03469 14C4.45057 14 1.53467 11.0841 1.53467 7.50002C1.53467 3.9159 4.45057 1 8.03469 1C11.6188 1 14.5347 3.9159 14.5347 7.50002C14.5347 11.0841 11.6188 14 8.03469 14ZM8.03469 2.3C5.16753 2.3 2.83467 4.63286 2.83467 7.50002C2.83467 10.3672 5.16753 12.7 8.03469 12.7C10.9018 12.7 13.2347 10.3672 13.2347 7.50002C13.2347 4.63286 10.9025 2.3 8.03469 2.3Z" fill="white" />
                        <path d="M17.8118 18C17.717 18.0001 17.623 17.9815 17.5354 17.9452C17.4478 17.9088 17.3683 17.8556 17.3013 17.7884L11.7461 12.2325C11.6791 12.1655 11.6259 12.0859 11.5896 11.9983C11.5534 11.9107 11.5347 11.8168 11.5347 11.722C11.5347 11.6272 11.5534 11.5333 11.5896 11.4457C11.6259 11.3581 11.6791 11.2785 11.7461 11.2115C11.8132 11.1445 11.8927 11.0912 11.9803 11.055C12.0679 11.0187 12.1618 11 12.2566 11C12.3514 11 12.4452 11.0187 12.5328 11.055C12.6204 11.0912 12.7 11.1445 12.7671 11.2115L18.3223 16.7674C18.4236 16.8682 18.4926 16.9969 18.5206 17.1371C18.5487 17.2772 18.5345 17.4226 18.4798 17.5547C18.4251 17.6867 18.3324 17.7996 18.2134 17.8789C18.0945 17.9582 17.9547 18.0003 17.8118 18Z" fill="white" />
                    </svg>
                </button>
                <a href="#">RU</a>
                <button @click="menuOpen = true" class="bars">
                    <svg width="24" height="16" viewBox="0 0 24 16" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path d="M23.5347 8C23.5347 7.73478 23.4501 7.48043 23.2997 7.29289C23.1492 7.10536 22.9451 7 22.7323 7H1.33699C1.1242 7 0.920129 7.10536 0.769664 7.29289C0.619198 7.48043 0.534668 7.73478 0.534668 8C0.534668 8.26522 0.619198 8.51957 0.769664 8.70711C0.920129 8.89464 1.1242 9 1.33699 9H22.7323C22.9451 9 23.1492 8.89464 23.2997 8.70711C23.4501 8.51957 23.5347 8.26522 23.5347 8Z" fill="white" />
                        <path d="M23.7778 15C23.7778 14.7348 23.6933 14.4804 23.5428 14.2929C23.3924 14.1054 23.1883 14 22.9755 14H1.58016C1.36737 14 1.16329 14.1054 1.01283 14.2929C0.862362 14.4804 0.777832 14.7348 0.777832 15C0.777832 15.2652 0.862362 15.5196 1.01283 15.7071C1.16329 15.8946 1.36737 16 1.58016 16H22.9755C23.1883 16 23.3924 15.8946 23.5428 15.7071C23.6933 15.5196 23.7778 15.2652 23.7778 15Z" fill="white" />
                        <path d="M24 1C24 0.734784 23.9155 0.48043 23.765 0.292894C23.6145 0.105357 23.4105 0 23.1977 0H1.80233C1.58954 0 1.38546 0.105357 1.235 0.292894C1.08453 0.48043 1 0.734784 1 1C1 1.26522 1.08453 1.51957 1.235 1.70711C1.38546 1.89464 1.58954 2 1.80233 2H23.1977C23.4105 2 23.6145 1.89464 23.765 1.70711C23.9155 1.51957 24 1.26522 24 1Z" fill="white" />
                    </svg>
                </button>
            </div>
        </div>
    </header>

    <!-- Menu -->
    <section :class="`menu ${menuOpen ? 'active' : ''}`">
        <div class="menu-top">
            <div class="menu-head">
                <router-link class="menu-logo" to="/">
                    <img :src="$getImage('logo-light.svg')" alt="">
                </router-link>
                <button @click="menuOpen = false" class="menu-close">
                    <img :src="$getImage('times.svg')" alt="">
                </button>
            </div>
            <ul class="menu-navs">
                <li v-for="(nav, i) in navs" :key="i">
                    <router-link class="menu-navs__link" :to="nav.to">{{ nav.name }}</router-link>
                </li>
            </ul>
        </div>
        <div class="menu-bottom">
            <p>© RG Brands</p>
            <img :src="$getImage('footer-logo-2.svg')" alt="">
        </div>
    </section>
    <!-- Menu end -->
</template>