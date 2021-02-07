<template>
  <div class="container">
    <div class="choose">
      <div class="choose__column">
        <h2 class="choose__title title">
          Почему мы?
        </h2>
        <img src="@/assets/images/checkmark.svg" alt="" />
      </div>
      <div class="choose__column advantages">
        <div class="advantages__item">
          <img src="@/assets/images/date.svg" alt="Точно в срок" />
          <div class="advantages__info">
            <h4 class="advantages__title">Точно в срок</h4>
            <p class="advantages__text">
              Мы знаем, как умеют обещать "менеджеры", поэтому не перекладываем ответственность.
              <strong>Все процессы контроллируем лично, и несем за них ответственность.</strong>
            </p>
          </div>
        </div>
        <div class="advantages__item">
          <img src="@/assets/images/message.svg" alt="Всегда на связи" />
          <div class="advantages__info">
            <h4 class="advantages__title">Всегда на связи</h4>
            <p class="advantages__text">
              Это не просто слова, а реальные действия.
              <strong>Вы — наш приоритет</strong>, поэтому все планы
              подстраиваем так, чтобы удобно было Вам.
            </p>
          </div>
        </div>
        <div class="advantages__item">
          <img src="@/assets/images/happy.svg" alt="Сотрудничество" />
          <div class="advantages__info">
            <h4 class="advantages__title">Сотрудничество, которое порадует</h4>
            <p class="advantages__text">
              Ждете от сотрудничества такой отдачи, будто делаем проект для
              себя? С нами вы получите больше, ведь главное — результат на 100%
              и еще чуть чуть сверху.<strong> — результат на 100% и еще чуть чуть сверху.</strong>
            </p>
          </div>
        </div>
        <div class="advantages__item">
          <img src="@/assets/images/flag.svg" alt="Ваши достижения" />
          <div class="advantages__info">
            <h4 class="advantages__title">Ваши достижения — наша цель</h4>
            <p class="advantages__text">
              Наша цель — привести каждый проект к успеху, ведь
              <strong>вместе с вами растем и развиваемся и мы!</strong>
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">

.choose {
	display: flex;
		&__column {
			width: 50%;
		}

		&__title {
			margin-bottom: 40px;
		}
}

.advantages {

		&__item {
			display: flex;
			margin-bottom: 50px;
			align-items: flex-start;
			img{
				margin-top: -7px;
			}
		}

		&__info {
			margin-left: 35px;
		}

		&__title {
			font-weight: 700;
			font-size: 24px;
			line-height: 29px;
			margin-bottom: 10px;
		}

		&__text {
			letter-spacing: 0.015em;
			font-weight: 300;
		}
}

</style>
