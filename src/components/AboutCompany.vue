<script>
import { onMounted, ref } from "vue";
import gsap from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

export default {
    name: 'AboutCompany',
    setup() {
        const scrollSection = ref(null);
        const scrollContent = ref(null);

        onMounted(() => {
            gsap.to(scrollContent.value, {
                x: () => -(scrollContent.value.scrollWidth - scrollSection.value.clientWidth),
                ease: "none",
                scrollTrigger: {
                    trigger: scrollSection.value,
                    start: "top-=100 top",
                    end: () => "+=" + scrollContent.value.scrollWidth,
                    scrub: true,
                    pin: true,
                    pinSpacing: true,
                },
            });
        });

        return {
            scrollSection,
            scrollContent,
        };
    },
};
</script>

<template>
    <section class="about-company">
        <div class="container">
            <section ref="scrollSection" class="scroll-section">
                <div ref="scrollContent" class="scroll-content">
                    <div class="about-company__content">
                        <div class="text">
                            <h3>О компании</h3>
                            <p>
                                RG brands – лидирующая компания по производству напитков.
                                <br><br>
                                Мы создаем  бренды - каждый из которых призван сделать жизнь людей лучше.
                            </p>
                            <div class="text-card">
                                <h2>
                                    30
                                    <span>лет</span>
                                </h2>
                                <h4>На рынке Центральной Азии</h4>
                                <router-link to="/">
                                    <span>Статья</span>
                                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M3.29289 14.2929C2.90237 14.6834 2.90237 15.3166 3.29289 15.7071C3.68342 16.0976 4.31658 16.0976 4.70711 15.7071L3.29289 14.2929ZM16 4C16 3.44771 15.5523 3 15 3L6 3C5.44772 3 5 3.44771 5 4C5 4.55228 5.44772 5 6 5L14 5L14 13C14 13.5523 14.4477 14 15 14C15.5523 14 16 13.5523 16 13L16 4ZM4 15L4.70711 15.7071L15.7071 4.70711L15 4L14.2929 3.29289L3.29289 14.2929L4 15Z" fill="#2F2B2B" />
                                    </svg>
                                </router-link>
                            </div>
                        </div>
                        <img :src="$getImage('brand-logo.png')" alt="" class="brand-logo">
                        <ul class="card-wrap">
                            <li>
                                <h3>
                                    20
                                    <span>предприятий</span>
                                </h3>
                                <router-link to="/">
                                    <span>Контакты</span>
                                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M3.29289 14.2929C2.90237 14.6834 2.90237 15.3166 3.29289 15.7071C3.68342 16.0976 4.31658 16.0976 4.70711 15.7071L3.29289 14.2929ZM16 4C16 3.44771 15.5523 3 15 3L6 3C5.44772 3 5 3.44771 5 4C5 4.55228 5.44772 5 6 5L14 5L14 13C14 13.5523 14.4477 14 15 14C15.5523 14 16 13.5523 16 13L16 4ZM4 15L4.70711 15.7071L15.7071 4.70711L15 4L14.2929 3.29289L3.29289 14.2929L4 15Z" fill="white" />
                                    </svg>
                                </router-link>
                                <img :src="$getImage('map-card-1.png')" alt="" class="map-card">
                                <p>Мы работаем на территорие Казахстана, России, Кыргызстана </p>
                            </li>
                            <li class="card">
                                <h3>Миссия компании</h3>
                                <p>
                                    Улучшать качество жизни массового потребителя через опережающие инновации в маркетинге <br>
                                    и дистрибуции напитков и продуктов питания. 
                                </p>
                                <img :src="$getImage('company-card-icon-1.svg')" alt="" class="icon">
                            </li>
                            <li class="card">
                                <h3>Наша цель</h3>
                                <p>Улучшать качество жизни людей через инновации в производстве напитков, маркетинге и дистрибуции. Вместе мы делаем мир лучше! </p>
                                <img :src="$getImage('company-card-icon-2.svg')" alt="" class="icon">
                            </li>
                            <li class="card">
                                <h3>История успеха <br>RG Brands </h3>
                                <p>
                                    История RG Brands зародилась в 1994 году, когда компания начала свою деятельность в качестве дистрибутора импортируемых потребительских товаров известных международных марок, заложив в основу своего развития широкую дистрибуционную сеть. 
                                </p>
                                <img :src="$getImage('company-card-icon-3.svg')" alt="" class="icon">
                            </li>
                            <li class="card">
                                <h3>Карьера</h3>
                                <router-link class="more-link" to="/">
                                    <span>Подробнее о Карьере</span>
                                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M3.29289 14.2929C2.90237 14.6834 2.90237 15.3166 3.29289 15.7071C3.68342 16.0976 4.31658 16.0976 4.70711 15.7071L3.29289 14.2929ZM16 4C16 3.44771 15.5523 3 15 3L6 3C5.44772 3 5 3.44771 5 4C5 4.55228 5.44772 5 6 5L14 5L14 13C14 13.5523 14.4477 14 15 14C15.5523 14 16 13.5523 16 13L16 4ZM4 15L4.70711 15.7071L15.7071 4.70711L15 4L14.2929 3.29289L3.29289 14.2929L4 15Z" fill="#2F2B2B" />
                                    </svg>
                                </router-link>
                                <p>
                                    Новые возможности
                                    <br><br>
                                    Наши сотрудники, как и вся компания, работают на улучшение качества жизни потребителей.
                                    Чтобы создавать продукты, удовлетворяющие разнообразные потребности людей, нам нужно работать быстро и эффективно. Карьера в RG Brands открывает новые возможности для тех, кто любит соревноваться и побеждать.
                                </p>
                                <img :src="$getImage('company-card-icon-4.svg')" alt="" class="icon">
                            </li>
                            <li>
                                <router-link class="more-link" to="/">
                                    <span>Подробнее о бренде</span>
                                    <svg width="20" height="20" viewBox="0 0 20 20" fill="none" xmlns="http://www.w3.org/2000/svg">
                                        <path d="M3.29289 14.2929C2.90237 14.6834 2.90237 15.3166 3.29289 15.7071C3.68342 16.0976 4.31658 16.0976 4.70711 15.7071L3.29289 14.2929ZM16 4C16 3.44771 15.5523 3 15 3L6 3C5.44772 3 5 3.44771 5 4C5 4.55228 5.44772 5 6 5L14 5L14 13C14 13.5523 14.4477 14 15 14C15.5523 14 16 13.5523 16 13L16 4ZM4 15L4.70711 15.7071L15.7071 4.70711L15 4L14.2929 3.29289L3.29289 14.2929L4 15Z" fill="#2F2B2B" />
                                    </svg>
                                </router-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </section>
        </div>
    </section>
</template>
