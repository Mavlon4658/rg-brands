<script>
import Header from '@/components/Header.vue';
import Footer from '@/components/Footer.vue';

export default {
    name: "App",
    components: {
      Header,
      Footer,
    },
}
</script>

<template>
  <div class="wrapper">
    <Header />
    <main>
      <router-view/>
    </main>
    <Footer />
  </div>
</template>
