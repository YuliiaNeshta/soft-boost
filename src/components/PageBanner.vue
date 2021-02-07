<template>
  <div class="banner">
    <div class="container">
			<h3 class="banner__title">
          Сделаем крутой продукт <span>вместе</span>
      </h3>
      <div class="banner__wrap">
        <div class="banner__column">
          <base-form />
        </div>
        <div class="banner__column">
          <!-- <div class="banner__img">
            <img src="@/assets/images/logo-blue.svg" alt="Soft Boost" />
          </div> -->
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

  &__column {
    width: 50%;
  }
}
</style>
