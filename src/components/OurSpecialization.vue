<template>
  <div class="special">
    <div class="container">
      <h2 class="special__title title">Что мы делаем?</h2>
    </div>
    <div class="special__bg">
      <div class="container">
        <div class="special__item">
          <p class="special__number"><span>01.</span> Сайты</p>
          <p class="special__text">
            Создание дизайна, фирменного стиля, всевозможных логотипов и,
            конечно, разработка. На Тильде или ВордПресс — выбор всегда остаётся
            за вами.
          </p>
        </div>
      </div>
    </div>
		<div class="special__bg">
      <div class="container">
        <div class="special__item">
          <p class="special__number"><span>02.</span> Мобильные приложения</p>
          <p class="special__text">
            Ищите решение для смартфонов? Приложение для фитнеса, или площадка для продажи в онлайне? Мы сможем найти точки соприкосновения в каждой нише.
          </p>
        </div>
      </div>
    </div>
		<div class="special__bg">
      <div class="container">
        <div class="special__item">
          <p class="special__number"><span>03.</span> Веб - приложения</p>
          <p class="special__text">
            Платформа для онлайн обучения? Или альтернативу тиндеру?<br>
						Мы создадим для вас то, что вам нужно, вкладывая туда свои знания и часть души.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.special {
  padding: 200px 0px;

  &__title {
    margin-bottom: 60px;
  }
  &__bg {
    transition: all 0.3s ease 0s;
    &:hover {
      background-color: $yellow;
    }
  }

  &__item {
    display: flex;
    padding: 40px 0px;
    border-bottom: 1px solid #dddddd;
    &:last-child {
      margin-bottom: 0px;
    }
  }

  &__number {
		max-width: 285px;
    font-weight: 700;
    font-size: 24px;
    line-height: 29px;
		display: flex;
    span {
      margin-right: 70px;
    }
  }

  &__text {
    margin-left: auto;
    max-width: 533px;
		letter-spacing: 0.015em;
    width: 100%;
  }
}
</style>
