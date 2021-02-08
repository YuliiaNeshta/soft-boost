<template>
  <div class="banner">
    <div class="container">
      <div class="banner__wrap">
        <div class="banner__column banner__form">
          <h3 class="banner__title">
            Сделаем крутой продукт <span>вместе</span>
          </h3>
          <base-form class="banner__form-wrap" />
        </div>
        <div class="banner__column banner__column--img">
          <div class="banner__img">
            <img src="@/assets/images/logo-blue.png" alt="Soft Boost" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import baseForm from "./regular/baseForm";
export default {
  components: { baseForm },
};
</script>

<style lang="scss">
.banner {
  background-color: $blue;
  margin-bottom: 200px;
  padding: 60px 0px;
  &__wrap {
    display: flex;
  }

  &__title {
    font-weight: 600;
    font-size: 40px;
    line-height: 49px;
    color: #fff;
    span {
      color: $yellow;
    }
  }
  &__form {
    flex: 0 0 auto;
    width: 58.3333333333%;
		&-wrap{
			margin-top: 70px;
		}
  }
  &__img {
		margin-top: -9px;
    position: relative;
  }

  &__column {
    &--img {
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
}
</style>
