<template>
  <div class="home">
    <ul class="navbar__menu-mobile" :class="{ 'navbar__menu-mobile_active': isActive }">
      <li class="navbar__item-mobile" v-for="(item, index) in menu" :key="index">
        <a href="" class="navbar__item-link link">{{ item.name }}</a>
      </li>
    </ul>
    <HvNavbar @setActive="setActive" :menu="menu" />
    <header class="header">
      <div class="container">
        <div class="header__content">
          <h1>Жилой комплекс в историческом центре</h1>
          <div class="header__mouse-ico">
            <HvMouse />
          </div>
          <div class="header__contacts">
            <a href="#" class="header__contacts-item">
              <span class="icon-map"></span>
              <span class="">Наб. реки Фонтанки 10-15</span>
            </a>
            <a href="tel:+88121234567" class="header__contacts-item">
              <span class="icon-phone-call"></span>
              <span class="">8 (812) 123-45-67</span>
            </a>
          </div>
        </div>
      </div>
    </header>
    <section class="testimonials">
      <ul class="testimonials-items">
        <li class="testimonials-item" v-for="(item, index) in testimonials" :key="index">
          <i class="testimonials-item__ico" :class="item.ico"></i>
          <p class="testimonials-item__description">{{ item.description }}</p>
        </li>
      </ul>
    </section>
    <section class="appartments">
      <div class="container">
        <h2 class="appartments__title">Наши квартиры</h2>
        <div class="appartments__gallery">
          <div class="appartments__gallery-item" v-for="(item, index) in appartments" :key="index" :style="{
            'background-image':
              'url(' + require('@/assets/img/' + item.img) + ')',
          }">
            <p class="appartments__gallery-description">
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
    </section>
    <section class="feedback">
      <div class="container">
        <div class="feedback__content">
          <h2 class="feedback__title">Хотите посмотреть?</h2>
          <div class="feedback__group">
            <p class="feedback__description">
              Lorem Ipsum - это текст-"рыба", часто использемый в печати и
              вэб-дизайне. Lorem Ipsum является стандартной "рыбой" для текстов
              на латинице с начала XVI века. В то время некий безымянный
              печатник создал большую коллекцию размеров и форм шрифтов,
              используя Lorem Ipsum для распечатки образцов.
            </p>
            <div class="feedback__form">
              <div class="form__input-group">
                <input type="text" class="form__name" placeholder="Ваше имя" />
                <input type="text" class="form__phone" placeholder="Ваш телефон" />
              </div>
              <div class="form__submit-group">
                <p class="form__info">
                  *Мы никому не передаем ваши данные. И не сохраняем ваш номер в
                  базу.
                </p>
                <button class="form__btn btn">Посмотреть район</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="video">
      <div class="container">
        <div class="video__wrapper">
          <iframe class="video__item" width="1193" height="671" src="https://www.youtube.com/embed/N_UHTgGFTX8"
            title="Is This the Best Modern House in the World? (House Tour)" frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen></iframe>
        </div>
      </div>
    </section>
    <section class="map">
      <div class="container">
        <h2 class="map__title">Район на карте</h2>
        <div class="map__wrapper">
          <iframe class="map__item"
            src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d17965.197520935868!2d37.51450525604626!3d55.747215399999995!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46b54bdd017303b9%3A0xd1f63f945a2450c2!2z0JzQvtGB0LrQstCwINCh0LjRgtC4!5e0!3m2!1sru!2sru!4v1662205988739!5m2!1sru!2sru"
            width="600" height="450" style="border: 0" allowfullscreen="" loading="lazy"
            referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
      </div>
    </section>
    <section class="qa">
      <div class="container">
        <div class="qa__title">Есть вопросы?</div>
        <div class="qa__form">
          <input type="text" class="form__name" placeholder="Ваше имя" />
          <input type="text" class="form__phone" placeholder="Ваш телефон" />
          <p class="form__info">
            *Мы никому не передаем ваши данные. И не сохраняем ваш номер в базу.
          </p>
          <button class="form__btn btn">Посмотреть район</button>
        </div>
      </div>
    </section>
    <HvFooter />
    <div class="container num__wrapper">
      <div class="num__inner">
        <div class="num-2">II</div>
        <div class="num-3">III</div>
        <div class="num-4">IV</div>
        <div class="num-5">V</div>
      </div>
    </div>
  </div>
</template>

<script>
import HvNavbar from "@/components/hvNavbar.vue";
import HvMouse from "@/components/hvMouse.vue";
import HvFooter from "@/components/hvFooter.vue";
export default {
  components: { HvNavbar, HvMouse, HvFooter },
  data() {
    return {
      testimonials: [
        { ico: "icon-bench", description: "Рядом исторические парки и скверы" },
        { ico: "icon-building", description: "Полность обустроенный" },
        { ico: "icon-fountain", description: "10 фонтано на территории" },
        { ico: "icon-bicycle", description: "6 км велодорожек" },
      ],
      appartments: [
        { img: "photo1.png", description: "Лофт — 3 этажа" },
        { img: "photo2.png", description: "Лофт — 2 этажа" },
        { img: "photo1.png", description: "Лофт — 3 этажа" },
        { img: "photo2.png", description: "Лофт — 2 этажа" },
      ],
      menu: [
        { name: "О комплексе" },
        { name: "Район" },
        { name: "Каталог квартире" },
        { name: "Ипотека" },
        { name: "Контакты" },
      ],
      isActive: false
    };
  },
  methods: {
    setActive(isActive) {
      this.isActive = isActive;
    }
  }
};
</script>

<style lang="scss">
.home {
  max-width: 100%;
  position: relative;
  margin: 0 auto;
}

.header {
  position: relative;
  width: 100%;
  min-height: 840px;
  background-image: url("./assets/img/header.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  background-attachment: fixed;
  display: flex;
  align-items: flex-end;
}

.header:before {
  content: "";
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  position: absolute;
  background: linear-gradient(180deg,
      #242b33 11.98%,
      rgba(45, 52, 60, 0.38) 51.04%,
      #242b33 92.19%);
}

.header__content {
  position: relative;
  z-index: 2;
  max-width: 582px;
  margin: 0 auto;
  text-align: center;
}

.header__mouse-ico {
  position: absolute;

  top: 210px;
  left: 0;
  right: 0;
  margin: 0 auto;
}

.header__contacts {
  padding-bottom: 74px;
  margin-top: 340px;
  display: flex;
  justify-content: space-between;
}

.header__contacts-item {
  display: flex;
  align-items: center;
  font-size: 18px;
  line-height: 21px;
  text-align: center;
  color: #ffffff;
  text-decoration: none;
  transition: all 0.2s ease-in;
}

.header__contacts-item:hover {
  color: #d4c17f;
}

.header__contacts-item [class*="icon-"]::before {
  color: #ffffff;
  margin-right: 14px;
}

.header__contacts-item:hover [class*="icon-"]::before {
  color: #d4c17f;
}

.header__contacts-item .icon-map {
  font-size: 21px;
}

.header__contacts-item .icon-phone-call {
  font-size: 21px;
}

.testimonials {
  margin-top: 120px;
  display: flex;
  justify-content: center;
}

.testimonials-items {
  max-width: 794px;
  display: flex;
  justify-content: space-between;
}

.testimonials-item {
  text-align: center;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.testimonials-item__ico {
  font-size: 80px;
}

.testimonials-item__description {
  margin-top: 53px;
  font-family: "Roboto";
  font-style: normal;
  font-weight: 300;
  font-size: 20px;
  line-height: 27px;
  color: #ffffff;
}

.appartments {
  margin-top: 120px;
}

.appartments__title {
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 48px;
  color: #d4c17f;
}

.appartments__gallery {
  margin-top: 100px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 30px;
}

.appartments__gallery-item {
  background-repeat: no-repeat;
  background-size: cover;
  width: 535px;
  height: 320px;
  margin-bottom: 30px;
  position: relative;
  overflow: hidden;
}

.appartments__gallery-item:hover::before {
  bottom: 100%;
}

.appartments__gallery-item::before {
  transition: all 0.2s ease-in;
  position: absolute;
  bottom: 0;
  left: 0;
  content: "";
  width: 100%;
  height: 100%;
  background: linear-gradient(180deg, rgba(36, 43, 51, 0) 0%, #242b33 100%);
}

.appartments__gallery-img {
  background-size: contain;
}

.appartments__gallery-description {
  position: absolute;
  bottom: 50px;
  left: 50px;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 28px;
  color: #ffffff;
}

.feedback {
  position: relative;
  padding-top: 180px;
  background-image: url("./assets/img/view_sec.jpg");
}

.feedback::before {
  content: "";
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0;
  left: 0;
  background: linear-gradient(180deg,
      #242b33 10.42%,
      rgba(36, 43, 51, 0) 50.52%,
      #242b33 90.1%),
    linear-gradient(0deg, rgba(36, 43, 51, 0.9), rgba(36, 43, 51, 0.9));
}

.feedback__content {
  position: relative;
  z-index: 2;
}

.feedback__title {
  margin-top: 21px;
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 48px;
  color: #d4c17f;
}

.feedback__group {
  margin-top: 29px;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}

.feedback__description {
  max-width: 535px;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #ffffff;
}

.feedback__form {
  width: 540px;
}

.form__input-group {
  display: flex;
  justify-content: space-between;
}

.form__name,
.form__phone {
  width: 255px;
  height: 50px;
  background: #dfdfdf2d;
  border: none;
  text-align: center;
  color: #ffffff;
  border: none;
}

.form__submit-group {
  margin-top: 47px;
  display: flex;
  justify-content: space-between;
}

.form__info {
  max-width: 255px;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 400;
  font-size: 13px;
  line-height: 16px;
  text-align: center;
  color: #e7e7e7;
}

.form__btn {
  width: 255px;
  height: 50px;
  background: #d4c17f;
  font-family: "Raleway";
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 27px;
  color: #ffffff;
  border: none;
}

.video {
  margin-top: 180px;
}

.video__wrapper {
  padding-top: 56.25%;
  position: relative;
}

.video__item {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #626262;
}

.map {
  margin-top: 180px;
}

.map__title {
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 48px;
  color: #d4c17f;
}

.map__wrapper {
  margin-top: 100px;
  min-height: 358px;
  background: #626262;
  position: relative;
}

.map__item {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.qa {
  margin-top: 180px;
}

.qa__title {
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 48px;
  color: #d4c17f;
}

.qa__form {
  margin-top: 50px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  align-items: center;
}

.num__wrapper {
  position: absolute;
  z-index: -1;
  top: 0;
  right: 0;
  left: 0;
  margin: 0 auto;
}

.num__inner {
  position: relative;
}

.num-2,
.num-3,
.num-4,
.num-5 {
  font-family: "Playfair Display";
  font-style: normal;
  font-weight: 700;
  font-size: 400px;
  line-height: 533px;
  color: #ffffff;
  opacity: 0.02;
}

.num-2 {
  position: absolute;
  right: calc(-301px / 2);
  top: 812px;
}

.num-3 {
  position: absolute;
  left: calc(-452px / 2);
  top: 1222px;
}

.num-4 {
  position: absolute;
  right: calc(-418px / 2);
  top: 2697px;
}

.num-5 {
  position: absolute;
  left: calc(-268px / 2);
  top: 3419px;
}

/* lg-размер (<=1199px) */
@media screen and (max-width: 1199px) {

  /* CSS для ширины от 992px до 1199px */


  .appartmen .container {
    max-width: 1199px;
  }

  .appartments__gallery {
    justify-content: center;
    gap: 30px;
  }

  .appartments__gallery-item {
    width: 400px;
  }

  .feedback__title {
    text-align: center;
  }

  .feedback__group {
    justify-content: center;
  }

  .feedback__form {
    margin-top: 20px;
    margin: 0 auto;
    max-width: 540px;
  }

  .form__input-group {
    margin-top: 20px;
  }

  .qa__title {
    text-align: center;
  }

  .qa__form {
    padding-top: 50px;
    max-width: 600px;
    margin: 0 auto;
    gap: 30px;
  }
}

/* md-размер (<=991px) */
@media screen and (max-width: 991px) {

  /* CSS для ширины от 768px до 991px */
  .num__inner {
    display: none;
  }

  .appartments__gallery {
    justify-content: center;
    gap: 30px;
  }

  .appartments__gallery-item {
    width: 300px;
    height: 160px;
  }

  .header {
    min-height: 700px;
  }

  .header__contacts {
    margin-top: 250px;
  }

  .qa__form {
    padding-top: 50px;
    max-width: 600px;
    margin: 0 auto;
    gap: 30px;
  }
}

/* sm-размер (<=768px) */
@media screen and (max-width: 767px) {

  /* CSS для ширины от 576px до 767px */

  .num__inner {
    display: none;
  }

  .navbar {
    position: fixed;
    z-index: 999;
    padding: 10px 0;
    width: 100%;
    background-color: #2d343c;
    -webkit-box-shadow: 0px -5px 5px -5px rgba(45, 52, 60, 0.6) inset;
    -moz-box-shadow: 0px -5px 5px -5px rgba(45, 52, 60, 0.6) inset;
    box-shadow: 0px -5px 5px -5px rgba(45, 52, 60, 0.6) inset;
  }



  .navbar__menu {
    display: none;
  }

  .navbar__toggle {
    display: block;
    border: none;
    background: none;
    position: relative;
    width: 30px;
    height: 20px;
  }

  .navbar__toggle i {
    display: block;
    position: absolute;
    display: block;
    right: 0;
    width: 100%;
    height: 2px;
    background-color: #fff;
    transition: all 0.1s ease-in;
  }

  .navbar__toggle i:nth-child(1) {
    top: 0;
  }

  .navbar__toggle i:nth-child(2) {
    top: 50%;
    transform: translateY(-50%);
  }

  .navbar__toggle i:nth-child(3) {
    bottom: 0;
  }

  .navbar__toggle_active i:nth-child(1) {
    top: 50%;

    transform: rotate(45deg);
  }

  .navbar__toggle_active i:nth-child(2) {
    display: none;
  }

  .navbar__toggle_active i:nth-child(3) {
    top: 50%;
    transform: rotate(-45deg);
  }



  .navbar__menu-mobile {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    min-height: 80%;
    position: fixed;
    z-index: 3;
    top: -75%;
    left: 0;
    background-color: #2d343c;
    width: 100%;
    text-align: center;
    transition: all 0.7s cubic-bezier(0.075, 0.82, 0.165, 1);

  }

  .navbar__menu-mobile_active {
    top: 85px;
  }

  .navbar__menu-mobile {
    padding: 0;
  }

  .footer__inner {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
  }

  .appartments__gallery-item {
    width: 80%;
    height: 320px;
  }

  .testimonials,
  .appartments,
  .video,
  .map,
  .qa,
  .footer {
    margin-top: 50px;
  }

  .feedback {
    padding-top: 50px;
  }

  .qa__form {
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;
    max-width: 400px;
    margin: 0 auto;
  }
}

/* xs-размер (<=575px) */
@media screen and (max-width: 575px) {

  /* CSS для ширины до 575px (включительно) */
  .num__inner {
    display: none;
  }

  .appartments__title {
    text-align: center;
  }

  .form__input-group,
  .form__submit-group {
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;
  }

  .qa__form {
    justify-content: center;
    flex-wrap: wrap;
    gap: 30px;
  }

  .testimonials-items {
    flex-wrap: wrap;
    gap: 30px;
  }

  .header__mouse-ico {
    top: 150px;
  }

  .header__content h1 {
    font-size: 24px;
  }

  .header__contacts {
    margin-top: 100px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;
  }

  .header {
    min-height: 500px;
  }
}
</style>
