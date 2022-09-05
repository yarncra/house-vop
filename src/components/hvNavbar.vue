<template>
  <nav class="navbar">

    <div class="container navbar__inner">
      <a href="#" class="navbar__logo">
        <img src="@/assets/img/logo.svg" alt="" class="navbar__logo-img" />
      </a>
      <button class="navbar__toggle" :class="{ navbar__toggle_active: isActive }" @click="burgerToggle">
        <i></i>
        <i></i>
        <i></i>
      </button>
      <ul class="navbar__menu">
        <li class="navbar__item" v-for="(item, index) in menu" :key="index">
          <a href="" class="navbar__item-link link">{{ item.name }}</a>
        </li>
      </ul>

    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },

  props: {
    menu: {
      type: Array,
      require: true
    }
  },
  methods: {
    burgerToggle() {
      this.isActive = !this.isActive;
      this.$emit('setActive', this.isActive);
    }
  },
};
</script>

<style lang="scss">
.navbar {
  padding: 10px 0;
  position: fixed;
  z-index: 999;
  top: 0;
  left: 0;
  width: 100%;
  background: #2d343c;
  box-shadow: 0px -5px 5px -5px rgba(45, 52, 60, 0.6) inset;
}

.navbar__inner {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.navbar__menu {
  display: flex;
}

.navbar__item {
  margin-left: 40px;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 16px;
  letter-spacing: 0.05em;
}

.navbar__toggle {
  display: none;
}

.navbar__menu-mobile {
  display: none;
}
</style>
