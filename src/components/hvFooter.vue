<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__inner">
        <a href="#" class="navbar__logo">
          <img src="@/assets/img/logo.svg" alt="" class="navbar__logo-img" />
        </a>
        <ul class="footer__items">
          <li class="footer__item">
            <a href="#" class="footer__item-link link">О комплексе</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Район</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Каталог квартир</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Ипотека</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Контакты</a>
          </li>
        </ul>
        <ul class="footer__items">
          <li class="footer__item">
            <a href="#" class="footer__item-link link">О комплексе</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Район</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Каталог квартир</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Ипотека</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Контакты</a>
          </li>
        </ul>
        <ul class="footer__items">
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Адрес: Наб. реки Фонтанки 10-15</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Телефон: 8 (812) 123-45-67</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">Отдел продаж: 10:00 - 20:00</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">E-mail: vip@housevip.ru</a>
          </li>
          <li class="footer__item">
            <a href="#" class="footer__item-link link">
              <span class="footer__ico icon-youtube"> </span>
            </a>
            <a href="#" class="footer__item-link link">
              <span class="footer__ico icon-vk"> </span>
            </a>
            <a href="#" class="footer__item-link link">
              <span class="footer__ico icon-facebook"> </span>
            </a>
            <a href="#" class="footer__item-link link">
              <span class="footer__ico icon-instagram"> </span>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss">
.footer {
  margin-top: 180px;
  padding: 60px 0 50px;
  background: #2d343c;
}

.footer__inner {
  display: flex;
  justify-content: space-between;
}


.footer__item {
  margin-bottom: 15px;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 16px;
  letter-spacing: 0.05em;
}

.footer__ico {
  margin-right: 20px;
}

.icon-youtube::before,
.icon-vk::before,
.icon-facebook::before,
.icon-instagram::before {
  font-size: 20px;
}

.footer__inner .navbar__logo {
  padding-bottom: 30px;
}
</style>
