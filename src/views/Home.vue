<script>
export default {
  name: 'Home',
}
</script>

<template>
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