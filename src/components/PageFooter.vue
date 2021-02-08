<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__wrap">
        <div class="footer__column">
          <p class="footer__title">
            Готовы пообщаться?
            <base-form  class="footer__form"/>
          </p>
        </div>
        <div class="footer__column">
          <p class="footer__title title-margin">Мы <span>всегда</span> на связи</p>
          <a href="tel:++380639999999" class="footer__contacts">
            +38 (063) 999 99 99
          </a>
          <a href="mailto:soft.boost@gmail.com" class="footer__contacts">
            soft.boost@gmail.com
          </a>
        </div>
      </div>
      <div class="footer__links">
        <a href="#" class="footer__link">Политика конфеденциальности</a>
        <a href="#" class="footer__link">© "Soft Boost". Все права защищены</a>
      </div>
    </div>
  </footer>
</template>

<script>
import baseForm from "./regular/baseForm";
export default {
  components: { baseForm },
};
</script>

<style lang="scss">
.footer {
	padding: 60px 80px;
  background-color: $blue;

	&__wrap{
		display: flex;
		justify-content: space-between;
	}
	&__form{
		margin-top: 60px;
	}
  &__column {
  }

  &__title {
    color: #fff;
    font-weight: 600;
    font-size: 24px;
    line-height: 29px;
    span {
      color: $yellow;
    }
  }

  &__contacts {
		color: #fff;
		font-size: 40px;
		line-height: 49px;
		margin-bottom: 10px;
		font-weight: 300;
		display: block;
  }

  &__links {
		display: flex;
		justify-content: space-between;
		margin-top: 140px;
  }

  &__link {
    color: #fff;
    font-weight: 300;
    font-size: 16px;
    line-height: 20px;

    letter-spacing: 0.015em;
  }
}
.title-margin{
	margin-bottom: 60px;
}
</style>
