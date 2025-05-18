<script>
import AboutCompany from '@/components/AboutCompany.vue';

export default {
  name: 'Home',
  components: {
    AboutCompany,
  },
  data () {
    return {
      newsHead: ['Все новости','Новости СМИ','Новости о Брендах','Новинки ','Прессрелизы ','Акции',],
      newsActive: 3,
    }
  }
}
</script>

<template>
  <!-- Home -->
  <section class="home">
    <div class="container home-container">
      <h1 class="home-title">Напитки на любой вкус <br>Для каждого случая</h1>
      <div class="home-card">
        <h2>Хотите стать партнерам?</h2>
        <p>Если вы хотите обсудить вопросы сотрудничества или спонсорства</p>
        <main-btn theme="green">ОСТАВИТЬ ЗАЯВКУ</main-btn>
      </div>
    </div>
  </section>
  <!-- Home end -->

  <!-- About company -->
  <AboutCompany />
  <!-- About company end -->

  <!-- Product -->
  <section class="product">
    <div class="container product-container">
      <div class="product-left">
        <h2>Наша продукция</h2>
        <p>Если вы хотите обсудить вопросы сотрудничества или спонсорства</p>
        <ul>
          <li v-for="i in 10" :key="i">
            <router-link to="/">
              <img :src="$getImage(`product-logo-${i}.svg`)" alt="">
            </router-link>
          </li>
        </ul>
      </div>
      <div class="main-card">
        <img :src="$getImage('product-card-bg.png')" alt="" class="bg-img">
        <img :src="$getImage('product-card-1.png')" alt="">
      </div>
      <div class="product-right">
        <div class="text">
          <h3>A’SU</h3>
          <p>Вода A’SU берет свое начало с ледяных горных вершин, благодаря чему она обогащена уникальным балансом горных минералов и может полностью усваиваться организмом.</p>
          <main-btn>ОСТАВИТЬ ЗАЯВКУ</main-btn>
          <ul>
            <li>
              <div class="main-img">
                <img :src="$getImage('product-card-bg.png')" alt="" class="bg-img">
                <img :src="$getImage('product-card-2.png')" alt="">
              </div>
              <h4>A’SU TERRA</h4>
            </li>
            <li>
              <div class="main-img">
                <img :src="$getImage('product-card-bg.png')" alt="" class="bg-img">
                <img :src="$getImage('product-card-3.png')" alt="">
              </div>
              <h4>A’SU</h4>
            </li>
            <li>
              <div class="main-img">
                <img :src="$getImage('product-card-bg.png')" alt="" class="bg-img">
                <img :src="$getImage('product-card-4.png')" alt="">
              </div>
              <h4>A’SU VO!</h4>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
  <!-- Product end -->

  <!-- News -->
  <section class="news">
    <div class="container">
      <select name="" id="" class="news-select">
        <option 
          v-for="(data, i) in newsHead"
          :key="i"
          value=""
        >{{ data }}</option>
      </select>
      <ul class="news-head">
        <li
          v-for="(data, i) in newsHead"
          :key="i"
          :class="{
            'active': i == newsActive
          }"
          @click="newsActive = i"
        >
          {{ data }}
        </li>
      </ul>
      <div class="news-content">
        <div class="news-content__left">
          <div class="main-img">
            <img :src="$getImage('news-card.png')" alt="">
          </div>
          <div class="text">
            <h2>Запуск продукции  "DaDa Экстра-Витамины"</h2>
            <p>«DaDa Экстра-Витамины» - это сочетание понятных, всем знакомых и популярных фруктов и ягод, а польза витаминов усилена с помощью экстрактов: ромашки, шиповника, малина.</p>
            <h4>01 ноября, 2019</h4>
          </div>
        </div>
        <div class="news-content__right">
          <ul class="news-card__wrap">
            <li class="news-card">
              <img :src="$getImage('news-card-1.png')" alt="" class="main-img">
              <div class="news-card__text">
                <h3>Запуск продукции <br> "DaDa Экстра-Витамины"</h3>
                <p>«DaDa Экстра-Витамины» - это сочетание понятных, всем знакомых и популярных фруктов и ягод, а польза витаминов усилена с помощью экстрактов: ромашки, шиповника, малина.</p>
                <h4>01 ноября, 2019</h4>
              </div>
            </li>
            <li class="news-card">
              <img :src="$getImage('news-card-2.png')" alt="" class="main-img">
              <div class="news-card__text">
                <h3>Запуск продукции <br> "DaDa Экстра-Витамины"</h3>
                <p>«DaDa Экстра-Витамины» - это сочетание понятных, всем знакомых и популярных фруктов и ягод, а польза витаминов усилена с помощью экстрактов: ромашки, шиповника, малина.</p>
                <h4>01 ноября, 2019</h4>
              </div>
            </li>
            <li class="news-card">
              <img :src="$getImage('news-card-3.png')" alt="" class="main-img">
              <div class="news-card__text">
                <h3>Запуск продукции <br> "DaDa Экстра-Витамины"</h3>
                <p>«DaDa Экстра-Витамины» - это сочетание понятных, всем знакомых и популярных фруктов и ягод, а польза витаминов усилена с помощью экстрактов: ромашки, шиповника, малина.</p>
                <h4>01 ноября, 2019</h4>
              </div>
            </li>
          </ul>
          <router-link class="more-link" to="/">
            <span>Смотреть все</span>
            <svg width="21" height="20" viewBox="0 0 21 20" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M3.79289 14.2929C3.40237 14.6834 3.40237 15.3166 3.79289 15.7071C4.18342 16.0976 4.81658 16.0976 5.20711 15.7071L3.79289 14.2929ZM16.5 4C16.5 3.44771 16.0523 3 15.5 3L6.5 3C5.94772 3 5.5 3.44771 5.5 4C5.5 4.55228 5.94772 5 6.5 5L14.5 5L14.5 13C14.5 13.5523 14.9477 14 15.5 14C16.0523 14 16.5 13.5523 16.5 13L16.5 4ZM4.5 15L5.20711 15.7071L16.2071 4.70711L15.5 4L14.7929 3.29289L3.79289 14.2929L4.5 15Z" fill="#2F2B2B" />
            </svg>
          </router-link>
        </div>
      </div>
    </div>
  </section>
  <!-- News end -->

  <!-- Vacancy -->
  <section class="vacancy">
    <div class="vacancy-left">
      <img :src="$getImage('vacancy-card.png')" alt="">
    </div>
    <div class="vacancy-right">
      <h3>Станьте ближе к работе мечты и узнайте больше о преимуществах работы в RG Brands</h3>
      <h2>
        50+
        <span>Открытых вакансий</span>
      </h2>
      <main-btn>СМОТРЕТЬ ВАКАНСИИ</main-btn>
    </div>
  </section>
  <!-- Vacancy end -->

  <!-- Contact -->
  <section class="contact">
    <div class="container contact-container">
      <div class="contact-left">
        <iframe src="https://yandex.ru/map-widget/v1/?um=constructor%3Aac59191707d6df18e87aba307510aaa5b58477e80ccf97680f39ac00504ed1e7&amp;source=constructor" width="1280" height="720" frameborder="0"></iframe>
        <ul>
          <li>
            <img :src="$getImage('circle-1.svg')" alt="">
            <span>Главный офис</span>
          </li>
          <li>
            <img :src="$getImage('circle-2.svg')" alt="">
            <span>Филиал</span>
          </li>
          <li>
            <img :src="$getImage('circle-3.svg')" alt="">
            <span>Производство</span>
          </li>
          <li>
            <img :src="$getImage('circle-4.svg')" alt="">
            <span>Дистрибьютор</span>
          </li>
        </ul>
      </div>
      <div class="contact-right">
        <h2>Контакты</h2>
        <p>Наши офисы находятся на территорие Казахстана России и Кыргызстана</p>
        <ul>
          <li>
            Головной офис: <a href="#">Казахстан, г. Алматы A05A5C7, пр. Райымбека, 212Б</a> <br>
            Телефон: <a href="tel:+7 (727) 331-55-55 (1000)">+7 (727) 331-55-55 (1000)</a>
          </li>
          <li>
            Пиар отдел- <a href="mailto:pr@brands.kz" target="_blank">pr@brands.kz</a>
          </li>
          <li>
            Телефон горячей линии в Кыргызстане: <a href="tel:3775">3775</a> <br>
            Телефон горячей линии в Узбекистане: <a href="tel:1309">1309</a> <br>
            Телефон горячей линии в России: <a href="tel:8 800 350 37 75">8 800 350 37 75</a>
          </li>
          <li>
            Горячая линия: <a href="tel:3775">3775</a> <br>
            E-mail: <a href="mailto:info@brands.kz" target="_blank">info@brands.kz</a>
          </li>
        </ul>
        <main-btn>ВСЕ контакты</main-btn>
      </div>
    </div>
  </section>
  <!-- Contact end -->

  <!-- Networks -->
  <section class="networks">
    <div class="container networks-container">
      <h2>Мы в соц.сетях</h2>
      <p>Следите за нашими новостями. Участвуйте во всех акциях от компании и побеждайте!</p>
      <ul>
        <li>
          <a href="#" class="link-whatsapp">
            <img :src="$getImage('network-icon-1.svg')" alt="">
            <span>WhatsApp</span>
          </a>
        </li>
        <li>
          <a href="#" class="link-tiktok">
            <img :src="$getImage('network-icon-2.svg')" alt="">
            <span>WhatsApp</span>
          </a>
        </li>
        <li>
          <a href="#" class="link-instagram">
            <img :src="$getImage('network-icon-3.svg')" alt="">
            <span>WhatsApp</span>
          </a>
        </li>
      </ul>
      <img :src="$getImage('networks-bg.png')" alt="" class="bg-img">
      <img :src="$getImage('networks-card.png')" alt="" class="networks-card">
    </div>
  </section>
  <!-- Networks end -->
</template>