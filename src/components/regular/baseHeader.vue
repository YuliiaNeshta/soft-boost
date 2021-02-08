<template>
  <header class="header">
    <div class="header-cnt">
      <div class="header__logo">
        <img src="@/assets/images/logo.png" alt="Soft Boost" />
      </div>
      <nav class="header__nav header-nav">
        <a class="header-nav__link" href="#">Главная</a>
        <a class="header-nav__link" href="#">О нас</a>
        <a class="header-nav__link" href="#">Почему мы?</a>
        <a class="header-nav__link" href="#">Как работаем?</a>
        <a class="header-nav__link" href="#">Контакты</a>
      </nav>
      <div class="header__switcher">
        <button class="header__lang">ru</button>
        <button class="header__lang">eng</button>
      </div>
      <base-button>Пообщаемся?</base-button>
    </div>
  </header>
</template>

<script>
import baseButton from "./baseButton";

export default {
  components: { baseButton },
};
</script>

<style lang="scss">
.header-cnt {
  max-width: 1340px;
  padding: 20px 10px;
  width: 100%;
  margin: 0 auto;
	    display: flex;
    align-items: center;
    justify-content: space-between;
}
.header {
  width: 100%;
  position: fixed;
  z-index: 8;
  background-color: #fff;
  display: flex;
  align-items: center;
  justify-content: space-between;
  &__logo {
    width: 110px;
    height: 64px;
  }

  &__nav {
    margin-left: auto;
    margin-right: 60px;
  }

  &__switcher {
    margin-right: 70px;
  }

  &__lang {
    background: #ffffff;
    border: 1px solid #cdcdcd;
    padding: 5px 10px;
    font-size: 16px;
    line-height: 19px;
    transition: all 0.3s ease 0s;
    &:hover {
      background-color: $yellow;
      border: 1px solid $yellow;
    }
  }
}

.header-nav {
  &__link {
    font-size: 16px;
    line-height: 19px;
    color: $blue;
    font-weight: 700;
    margin-left: 30px;
    position: relative;
    &:after {
      content: "";
      transition: all 0.5s ease 0s;
    }
    &:hover {
      &:after {
        position: absolute;
        bottom: -7px;
        right: 10px;
        height: 2px;
        background-color: $yellow;
        width: 100%;
      }
    }
  }
}
</style>
