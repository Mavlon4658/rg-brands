<script>
export default {
    name: "Footer"
}
</script>

<template>
    <footer class="footer">
        <div class="container">
            <div class="footer-head">
                <router-link class="footer-logo" to="/">
                    <img :src="$getImage('logo-light.svg')" alt="">
                </router-link>
                <a href="mailto:info@brands.kz" target="_blank" class="mail-link">info@brands.kz</a>
                <ul>
                    <li>
                        <a href="#">
                            <img :src="$getImage('facebook-icon.svg')" alt="">
                        </a>
                    </li>
                    <li>
                        <a href="#">
                            <img :src="$getImage('instagram-icon.svg')" alt="">
                        </a>
                    </li>
                </ul>
            </div>
            <div class="footer-body">
                <div class="footer-body__item">
                    <h3>продукция</h3>
                    <div class="footer-navs__wrap">
                        <ul class="footer-navs">
                            <li>
                                <router-link class="footer-navs__link" to="/">Пиала Gold</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">Пиала Ice Tea</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">A'SU</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">Нектар Солнечный</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">DaDa</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">Gracio</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">Моё</router-link>
                            </li>
                        </ul>
                        <ul class="footer-navs">
                            <li>
                                <router-link class="footer-navs__link" to="/">Pepsi</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">Lipton Ice Tea</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">Mirinda</router-link>
                            </li>
                            <li>
                                <router-link class="footer-navs__link" to="/">7UP</router-link>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="footer-body__item">
                    <h3>О компании</h3>
                    <ul class="footer-navs">
                        <li>
                            <router-link class="footer-navs__link" to="/">История успеха</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Производство</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Руководство</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Награды и сертификаты</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Социальная ответственность</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Документы РФ</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Фото и видео</router-link>
                        </li>
                    </ul>
                </div>
                <div class="footer-body__item">
                    <h3>Медиа</h3>
                    <ul class="footer-navs">
                        <li>
                            <router-link class="footer-navs__link" to="/">Новинки</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Медиа</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Акции</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Новинки</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Пиар акции</router-link>
                        </li>
                    </ul>
                </div>
                <div class="footer-body__item">
                    <h3>Карьера</h3>
                    <ul class="footer-navs">
                        <li>
                            <router-link class="footer-navs__link" to="/">Жизнь компании</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Вакансии</router-link>
                        </li>
                    </ul>
                </div>
                <div class="footer-body__item">
                    <h3>Контакты</h3>
                    <ul class="footer-navs">
                        <li>
                            <router-link class="footer-navs__link" to="/">Все контакты</router-link>
                        </li>
                        <li>
                            <router-link class="footer-navs__link" to="/">Оставить заявку</router-link>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>